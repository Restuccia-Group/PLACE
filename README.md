# PLACE: Patch-Level Agnostic Concept Extraction

Code for the NeurIPS 2026 paper *PLACE: Patch-Level Agnostic Concept Extraction*.
PLACE is a label-free method for extracting concepts from the patch tokens of Vision Transformers and
foundation models. It produces concept heatmaps without needing a classifier.

The method, results and paper are on the project page: **https://gabrieleonorato.com/PLACE**

## Notebooks

- `concept_extraction_demo.ipynb`: a short demo on the ImageNet *church* class with ViT-B/16, DINOv2
  and ViT-MAE.
- `task_agnostic_experiments.ipynb`: reproduces the task-agnostic experiments, where one concept
  bank is learned from many classes.

## Setup

```bash
git clone https://github.com/Restuccia-Group/PLACE.git
cd PLACE
uv sync
uv run jupyter lab
```

Or use `pip install -r requirements.txt`.

The data, classifier heads and saved concept banks are too large for git. Download
`task_agnostic_assets.zip` 
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23890282.svg)](https://doi.org/10.5281/zenodo.23890282) from Zenodo
and extract it in the repository root:

```bash
unzip task_agnostic_assets.zip -d .
```

## Citation

```bibtex
@inproceedings{onorato2026place,
  title     = {{PLACE}: Patch-Level Agnostic Concept Extraction},
  author    = {Onorato, Gabriele and Silvestri, Fabrizio and Bastian, Nathaniel D. and Restuccia, Francesco},
  booktitle = {Advances in Neural Information Processing Systems},
  year      = {2026},
  url       = {https://openreview.net/forum?id=8QlhKxCYSB}
}
```

## License

[CC BY-NC-ND 4.0](LICENSE)

## Acknowledgements

This work was supported in part by the U.S. National Science Foundation (NSF) under Grants
CNS-2312875 and OAC-2530896, the Defense Advanced Research Projects Agency (DARPA) under Cooperative
Agreement D25AC00374-00, the Office of Naval Research (ONR) under Award N00014-23-1-2221, and the Air
Force Office of Scientific Research (AFOSR) under Award FA9550-23-1-0261. Special thanks to the
authors of CRAFT, FACE and RSVC for releasing their code.
