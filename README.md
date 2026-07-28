# ATs-to-Ts: MITRE ATT&CK to P-SSCRM Mapping

This repository contains mappings between **MITRE ATT&CK** techniques and **P-SSCRM** (Proactive Security for Software Cybersecurity Risk Management) tasks.

**Current version: 1.1** (tracked on the `main` branch). See [Version History](#version-history) below for previous releases.

## Version History

Each released version of the mapping is preserved on its own branch so that prior results remain reproducible.

| Version | Branch | Description |
|---------|--------|--------------|
| **1.1 (current)** | [`main`](https://github.com/p-sscrm/ats-to-ts/tree/main) / [`version_1_1`](https://github.com/p-sscrm/ats-to-ts/tree/version_1_1) | Split the mapping into separate `technique_2_task_mappings.json`/`.csv` files, and added a `data/strategies_results/` breakdown showing which of the four mapping strategies (M1–M4) identified each pairing. |
| 1.0 | [`version_1_0`](https://github.com/p-sscrm/ats-to-ts/tree/version_1_0) | Initial release, with a single `data/mappings.json` combining the mapping, per-strategy flags, gap-task indicator, and cross-strategy agreement field. |

## Repository Structure

```
ats-to-ts/
├── README.md                              # This file
├── license                                # CC BY-SA 4.0 License
└── data/
    ├── technique_2_task_mappings.json     # Main mapping data (JSON)
    ├── technique_2_task_mappings.csv      # Main mapping data (CSV)
    └── strategies_results/
        ├── technique_2_task_mapping_with_M1_2_M4.json  # Mappings broken down by strategy (JSON)
        └── technique_2_task_mapping_with_M1_2_M4.csv    # Mappings broken down by strategy (CSV)
```

## Data Structure

The mapping data is provided in two equivalent formats: a CSV (`technique_2_task_mappings.csv`) and a JSON (`technique_2_task_mappings.json`), covering 136 unique MITRE ATT&CK techniques mapped to 43 unique P-SSCRM tasks (330 mappings in total).

### JSON

The JSON file contains a flat array of mapping objects, one per technique-task pair, with the following schema:

| Field | Type | Description |
|-------|------|-------------|
| `MITRE ATTACK Technique` | String | MITRE ATT&CK technique identifier |
| `P-SSCRM Task` | String | P-SSCRM task identifier |

#### Example

```json
{
  "MITRE ATTACK Technique": "T1001",    // MITRE ATT&CK Technique ID
  "P-SSCRM Task": "E.3.7"               // P-SSCRM Task identifier
}
```

### CSV

The CSV file has one row per MITRE ATT&CK technique, with its mapped P-SSCRM task(s) listed in a single comma-separated column.

| Column | Description |
|--------|-------------|
| `MITRE_technique` | MITRE ATT&CK technique identifier |
| `PSSCRM_control` | One or more P-SSCRM task identifiers (comma-separated if there are multiple) |

#### Example

```csv
MITRE_technique,PSSCRM_control
T1001,E.3.7
T1003,"D.2.1, E.3.3"
```

## Strategy-Level Results

The `data/strategies_results/` folder contains the same 330 technique-task mappings, but broken down by which of the four mapping strategies described in the paper identified each pairing. Each row/object represents one MITRE ATT&CK technique to P-SSCRM task mapping, with a boolean flag per strategy indicating whether that strategy surfaced the mapping.

| Field | Type | Description |
|-------|------|-------------|
| `MITRE ATTACK Technique` | String | MITRE ATT&CK technique identifier |
| `P-SSCRM Task` | String | P-SSCRM task identifier |
| `Transitive (M1)` | Boolean | Found via strategy M1: Transitive |
| `LLM (M2)` | Boolean | Found via strategy M2: LLM |
| `Framework (M3)` | Boolean | Found via strategy M3: Framework |
| `Report (M4)` | Boolean | Found via strategy M4: Report |

### Example

```json
{
  "MITRE ATTACK Technique": "T1001",
  "P-SSCRM Task": "E.3.7",
  "Transitive (M1)": true,
  "LLM (M2)": false,
  "Framework (M3)": true,
  "Report (M4)": true
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