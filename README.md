# Resource Pack Optimization Workflow

This repository is configured with a GitHub Actions workflow to automatically optimize Minecraft resource packs using PackSquash. Upon pushing changes, the workflow is triggered, optimizing the resource pack within the `pack` directory and creating a pre-release with the latest build.

## Workflow Overview

Here's what happens when you push changes to the repository:

1. **Clone Repository**: Clones the full repository to access the resource pack data.
2. **Run PackSquash**: Optimizes the resource pack found in the `pack` directory and stores the optimized pack as `pack.zip` in a temporary path.
3. **Publish Pre-release**: Automatically updates a pre-release named "Latest Build" and uploads the optimized `pack.zip` to it, ensuring that the latest version is always available for download without relying on specific version tags.

## How to Use

Simply make changes to your resource pack within the `pack` directory and push your changes. The workflow handles everything else, from optimization to release:

1. Update or add new resources to the `pack` directory.
2. Commit your changes:

   ```bash
   git add .
   git commit -m "Update resource pack"
   ```

3. Push your changes to GitHub:

   ```bash
   git push origin main
   ```

4. The workflow will automatically optimize the resource pack and update the pre-release with the latest build.

## Accessing the Latest Build

The latest optimized resource pack can always be found here: [latest build](https://github.com/voidwars/voidwars-assets/releases/download/latest/pack.zip), where pack.zip can be downloaded.

## Acknowledgments

- This workflow uses [PackSquash-action](https://github.com/ComunidadAylas/PackSquash-action) by ComunidadAylas for efficient resource pack optimization.

This configuration ensures your Minecraft resource packs are consistently optimized for size and performance, simplifying the process of maintaining and distributing updated versions.
