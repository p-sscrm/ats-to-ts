# ATs-to-Ts: MITRE ATT&CK to P-SSCRM Mapping

This repository contains mappings between **MITRE ATT&CK** techniques and **P-SSCRM** (Proactive Security for Software Cybersecurity Risk Management) tasks.

## Repository Structure

```
ats-to-ts/
├── README.md          # This file
├── license            # CC BY-SA 4.0 License
└── data/
    └── mappings.json  # Main mapping data
```

## Data Structure

The `mappings.json` file contains an array of mapping objects with the following schema:


### Field Descriptions

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

### Example

```json
{
  "MITRE ATTACK Technique": "T1001",    // MITRE ATT&CK Technique ID
  "P-SSCRM Task": "E.3.7",              // P-SSCRM Task identifier
  "Transitive (M1)": true,              // If found by strategy M1: Transitive
  "LLM (M2)": false,                    // If found by strategy M2: LLM
  "Framework (M3)": true,               // If found by strategy M3: Framework
  "Report (M4)": true,                  // If found by strategy M4: Report
  "Is Gap": false,                      // If the task was a new task (gap tasks)
  "Agreed Upon All Strategies": false   // If all four strategies were agreed upon
}
```

##  Citation

If you use the mapping data in your research or work, please cite this repository. Citation information is available in the `CITATION.cff` file in the root of this repository.

You can also reference the related research paper:

```bibtex
@misc{hamer2025closingchainreducerisk,
      title={Closing the Chain: How to reduce your risk of being SolarWinds, Log4j, or XZ Utils}, 
      author={Sivana Hamer and Jacob Bowen and Md Nazmul Haque and Robert Hines and Chris Madden and Laurie Williams},
      year={2025},
      eprint={2503.12192},
      archivePrefix={arXiv},
      primaryClass={cs.SE},
      url={https://arxiv.org/abs/2503.12192}, 
}
```

## Related Resources

- [MITRE ATT&CK Framework](https://attack.mitre.org/)
- [P-SSCRM Documentation](https://p-sscrm.org/) 

## Contact

For questions, suggestions, or collaboration opportunities, please contact the P-SSCRM maintainers :)