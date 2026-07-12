# Dataset Setup

Raw hyperspectral datasets are intentionally excluded from this repository.

Recommended local structure:

```text
data/
├── IndianPines/
│   ├── Indian_pines_corrected.mat
│   └── Indian_pines_gt.mat
├── PaviaUniversity/
│   ├── PaviaU.mat
│   └── PaviaU_gt.mat
└── Salinas/
    ├── Salinas_corrected.mat
    └── Salinas_gt.mat
```

## Rules

- Do not commit raw datasets unless their redistribution terms explicitly allow it.
- Add local dataset files to `.gitignore`.
- Document the official source and preprocessing steps in the final code release.
- Keep the train/validation/test split generation identical across ablation variants and comparison models.
