# ATs-to-Ts: MITRE ATT&CK to P-SSCRM Mapping

This repository contains mappings between **MITRE ATT&CK** techniques and **P-SSCRM** (Proactive Security for Software Cybersecurity Risk Management) tasks.

## Repository Structure

```
ats-to-ts/
├── README.md          # This file
├── CITATION.cff       # Citation metadata
├── license            # CC BY-SA 4.0 License
├── script.py
└── data/
    └── vX.Y.Z/              # A specific released version
        ├── all/             # Complete mapping data for this version
        │   ├── README.md    # Version-specific details for the complete data structure
        │   ├── mappings.csv
        │   └── mappings.json
        └── simple/          # Simplified mapping data for easier lookup and analysis
            ├── mappings.csv
            └── mappings.json
```

## Version History

Every released version is kept in its own directory under `data/`, following the `data/vX.Y.Z/{all,simple}` layout shown in [Repository Structure](#repository-structure), so prior results remain reproducible alongside the current release.

| Version | Location | Description |
|---------|----------|--------------|
| **1.1 (current)** | [`data/v1.1/`](data/v1.1/) | Adds a `Manual v1.1 Mapping` field to the `all/` view to flag pairings added by manual review, growing the mapping from 251 to 330 (97 to 136 MITRE ATT&CK attack technique-to-task mappings). |
| 1.0 | [`data/v1.0/`](data/v1.0/) | Initial release, with the `all/` view combining the mapping, per-strategy (M1–M4) flags, gap-task indicator, and cross-strategy agreement field. |

## Version

Each version directory contains two views of the same mapping release. Each view is provided in CSV and JSON formats.

- `all/`: Detailed mapping data with extended information about where each mapping originated, as documented in [Section 1.3 of the arXiv paper](https://arxiv.org/abs/2507.18037). The `README.md` in this directory explains the detailed schema for that specific version.
- `simple/`: Mapping of only the MITRE ATT&CK techniques to P-SSCRM tasks. The simple mappings are provided in the release.

For example:

```
data/
└── v1.1/
    ├── all/
    │   ├── README.md
    │   ├── mappings.csv
    │   └── mappings.json
    └── simple/
        ├── mappings.csv
        └── mappings.json
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

For questions, suggestions, or collaboration opportunities, please contact the P-SSCRM maintainers detailed [here](https://p-sscrm.github.io/contact) :)
