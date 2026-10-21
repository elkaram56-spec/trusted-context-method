# TCM v1.5 — матрица соответствия шаблонов формальным схемам

**Статус:** аудит; рекомендации не изменяют утверждённую нормативную спецификацию.  
**Источник:** `docs/ru/method-reference.md`, раздел 6 (формальные схемы) и раздел 7 (Gates).  
**Область:** `templates/ru/*.md`, семь опубликованных шаблонов.

## Общие поля

Во всех шаблонах необходимо явно представить:
`artifact_id` (string), `version` (string), `question_id` (string), `created_at` (ISO datetime), `owner` (string), `status` (DRAFT/REVIEW/APPROVED), `source_refs` (array), `reviewer` (string|null), `approved_at` (date|null).

Текущая строка «Идентификатор и версия» недостаточна для однозначного машинного обмена.

## Матрица

| Артефакт | Отсутствующие/неоднозначные идентификаторы | Рекомендация |
| --- | --- | --- |
| VBQ | `as_of_date`, `scope_in`, `scope_out`, `acceptance_criteria` | Разделить дату, включения и исключения; указать массив критериев |
| MVTC | `relation_types`, `relations`, `constraints`, `rules`, `claims` | Разделить типы связей и экземпляры; явные массивы |
| TCBS | `approved_plan_id`, `write_log`, `readback_snapshot`, `comparison_result`, `diffs` | Явно связать план, фактическую запись, снимок и результат сверки |
| GCP | `source_id`, `source_version`, `evidence_id`, `locator`, `claim_id`, `warrant_id`, `validity`, `scope`, `gaps`, `conflicts` | Выделить адресуемые ID и условия применимости; warrant условно обязателен |
| TCAC | `connector`, `interface`, `resource_scope`, `permission_snapshot`, `request_log`, `retrieved_ids`, `access_result` | Фиксировать разрешения и фактическое чтение отдельно |
| VRP | `verified_claims`, `evidence_links`, `warrant_checks`, `assumptions`, `limitations`, `unknowns`, `conflicts`, `verification_result` | Разделить доказательства, допущения, пределы и итог |
| DSP | `decision_status`, `rationale`, `verification_ref`, `authority`, `next_action`, `constraints`, `revisit_trigger` | Разделить субъект полномочия, действие, ограничения и пересмотр |

## Gate-проверки

- G1: человек утвердил недвусмысленный вопрос, дату и scope.
- G2: модель достаточна, Evidence Needs и неизвестное представлены явно.
- G3: `READ → PLAN → APPROVE → WRITE → READ BACK → COMPARE`; `comparison_result=PASS` только при совпадении с согласованным планом и отсутствии побочных изменений.
- G4: каждый существенный Claim имеет точный Evidence/locator либо статус UNKNOWN.
- G5: `access_result=PASS` требует фактического чтения в допустимом scope; аутентификация недостаточна.
- G6: проверены evidence, warrant, время, противоречия и ограничения.
- G7: `ACT` допустим только при наличии достаточных оснований и полномочий.

## Принцип исправления

1. Сохранить текст утверждённой спецификации v1.5 без изменений.
2. Создать новые согласованные шаблоны с явными ID полей, типами и Gate.
3. Не объявлять автоматически пройденным Gate при одной лишь структурной корректности.
4. Устранить разночтение лицензий CC BY-SA / CC BY-NC-SA до финального выпуска.
5. Проверить шаблоны на одном сквозном примере, включая UNKNOWN и REQUEST EVIDENCE.

**Решение о принятии исправленных шаблонов:** ожидается.
