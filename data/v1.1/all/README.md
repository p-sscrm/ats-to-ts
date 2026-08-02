# Data Structure

The structure of the detailed mapping file is the following for this version:

## Field Descriptions

| Field | Type | Description |
|-------|------|-------------|
| `MITRE ATTACK Technique` | String | MITRE ATT&CK technique identifier |
| `P-SSCRM Task` | String | P-SSCRM task identifier |
| `Transitive (M1)` | Boolean | If found by strategy M1: Transitive |
| `LLM (M2)` | Boolean | If found by strategy M2: LLM |
| `Framework (M3)` | Boolean | If found by strategy M3: Framework |
| `Report (M4)` | Boolean | If found by strategy M4: Report |
| `Is Gap` | Boolean | If the task was a new task (gap tasks) |
| `Agreed Upon All Strategies` | Boolean | If all four strategies were agreed upon |
| `Manual v1.1 Mapping` | Boolean | If the mapping was added in the manual v1.1 mapping |

## Example

```json
{
  "MITRE ATTACK Technique": "T1001",    // MITRE ATT&CK Technique ID
  "P-SSCRM Task": "E.3.7",              // P-SSCRM Task identifier
  "Transitive (M1)": true,              // If found by strategy M1: Transitive
  "LLM (M2)": false,                    // If found by strategy M2: LLM
  "Framework (M3)": true,               // If found by strategy M3: Framework
  "Report (M4)": true,                  // If found by strategy M4: Report
  "Is Gap": false,                      // If the task was a new task (gap tasks)
  "Agreed Upon All Strategies": false,  // If all four strategies were agreed upon
  "Manual v1.1 Mapping": false          // If added in the manual v1.1 mapping
}
```
