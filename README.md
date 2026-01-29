# 3D Medical Segmentation with Diffusion Model

This project leverages 3D Diffusion Models for medical image segmentation, specifically focusing on the augmentation and semi-supervised learning of bladder wall tumors.

## Project Structure

The repository has been restructured for better organization:

- `data/`: Contains medical image datasets (e.g., `.nii` files).
- `docs/`: Stores project documentation, papers (PDF), presentations (PPTX), and Jupyter Notebooks.
- `scripts/`: Contains core training scripts and environment requirements.
- `README.md`: Project overview and documentation.

## Core Features

1. **3D VQ-GAN Training**: Train a Variational Autoencoder to learn latent representations of 3D images via `scripts/train_vqgan.py`.
2. **3D DDPM Training**: Train a Denoising Diffusion Probabilistic Model in the latent space for generation and segmentation tasks via `scripts/train_ddpm.py`.
3. **Medical Image Augmentation**: Enhance limited medical datasets using generative models to improve segmentation model generalization.

## Getting Started

### Environment Setup

Python 3.8+ is recommended. Install the required dependencies:

```bash
pip install -r scripts/requirements.txt
```

### Training Workflow

1. **Train VQ-GAN**:
   ```bash
   python scripts/train_vqgan.py --config config/base_cfg.yaml
   ```

2. **Train DDPM**:
   ```bash
   python scripts/train_ddpm.py --config config/base_cfg.yaml
   ```

> [!IMPORTANT]
> The `ddpm` and `vq_gan_3d` modules currently appear to be missing from the workspace. Ensure the source code for these modules is placed in the project root or appropriately linked.

## Related Work

- 3D Bladder Wall Tumor Augmentation and Semi-supervised Learning based on Medical Diffusion.
- DeepAtlas: Joint Semi-supervised Learning of Image Registration and Segmentation.
