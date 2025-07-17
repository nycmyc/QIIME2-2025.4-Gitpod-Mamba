# QIIME2-Gitpod
Deployment of QIIME2 via Gitpod Workspaces with Mamba

## Overview
This repository provides a ready-to-use Gitpod workspace configuration for QIIME 2 2025.4 Amplicon Distribution, featuring **Mamba** for ultra-fast package management and **fully automated installation** with no user prompts.

## Features
- **🚀 Mamba Integration** - Ultra-fast package management (10-100x faster than conda)
- **🤖 Fully Automated Setup** - Zero user prompts, all ToS and confirmations auto-accepted
- **QIIME 2 2025.4 Amplicon Distribution** - Latest version with all amplicon analysis tools
- **Tab Completion** - Full bash tab completion for all QIIME 2 commands
- **q2-krona Plugin** - Interactive taxonomic visualization with Krona
- **Pre-configured Environment** - Ready to use immediately upon workspace launch
- **Gitpod Classic Compatible** - Optimized for Gitpod Classic workspaces

## Quick Start
1. Fork this repository to your GitHub account
2. Open in Gitpod by prefixing the URL with `gitpod.io/#`
   ```
   https://gitpod.io/#https://github.com/YOUR_USERNAME/QIIME2-Gitpod
   ```
3. Wait for the automated setup to complete (approximately **3-5 minutes** with Mamba!)
4. The workspace will automatically activate the QIIME 2 environment

## What's Included
- **Mambaforge** (includes Mamba + Conda)
- **QIIME 2 2025.4 Amplicon Distribution**
- **Full bash tab completion** for QIIME 2 commands
- **Krona visualization tools** (with updated taxonomy database)
- **q2-krona plugin**
- **Python 3.10 environment**
- **VS Code extensions** for Python development

## Performance Improvements
| Feature | Old (Conda) | New (Mamba) | Improvement |
|---------|-------------|-------------|-------------|
| Environment Creation | ~10-15 min | ~3-5 min | **3-4x faster** |
| Package Installation | Slow | Very Fast | **10-100x faster** |
| Dependency Resolution | Complex/Slow | Optimized | **Much better** |
| Error Messages | Basic | Detailed | **Clearer debugging** |

## Verification Commands
Once the setup is complete, you can verify the installation:
```bash
# Check versions
qiime --version
mamba --version

# Test tab completion (type 'qiime ' and press TAB)
qiime [TAB]

# List installed QIIME 2 plugins
qiime --help

# Verify Krona installation
which ktImportText

# Check q2-krona plugin
qiime krona --help
```

## Environment Details
- **Package Manager**: Mamba (with Conda compatibility)
- **Conda Environment Name**: `qiime2-amplicon-2025.4`
- **Python Version**: 3.10
- **Installation Path**: `/workspace/mambaforge`
- **Auto-activation**: Yes (new terminals automatically activate QIIME 2)

## Key Automation Features
✅ **Zero Prompts** - All installations proceed without user interaction  
✅ **Auto-accept ToS** - Terms of Service automatically accepted  
✅ **Error Recovery** - Automatic retries for network issues  
✅ **Environment Activation** - QIIME 2 environment auto-loads in new terminals  
✅ **Tab Completion** - Automatically configured and enabled  

## Updates from Previous Version
This repository has been significantly upgraded:
- **Switched from Miniconda to Mamba** for dramatic speed improvements
- **Fully automated installation** with no user prompts
- **Updated to QIIME 2 2025.4** with new GitHub-hosted environment files
- **Enhanced error handling** and retry logic
- **Improved tab completion** setup
- **Better user experience** with clear progress indicators

## Troubleshooting
If you encounter any issues:

### General Issues
1. Check that the conda environment is activated: `conda env list`
2. Manually activate if needed: `conda activate qiime2-amplicon-2025.4`
3. For Krona taxonomy issues, run: `ktUpdateTaxonomy.sh`
4. Clear package cache: `mamba clean --all`

### Tab Completion Issues
If tab completion is not working:
1. Ensure the environment is activated: `conda activate qiime2-amplicon-2025.4`
2. Manually source the tab completion: `source $CONDA_DIR/envs/qiime2-amplicon-2025.4/bin/tab-qiime`
3. Refresh your bash session: `source ~/.bashrc`
4. Regenerate QIIME 2 cache: `qiime dev refresh-cache`

### Mamba Issues
If you encounter Mamba-specific issues:
1. Check Mamba version: `mamba --version`
2. Update Mamba: `mamba update mamba`
3. Fall back to conda if needed: `conda install` instead of `mamba install`

## Why Mamba?
**Mamba** is a drop-in replacement for conda that provides:
- **Faster dependency resolution** using libsolv
- **Parallel downloads** for packages
- **Better error reporting** for conflicts
- **Same commands and syntax** as conda
- **Especially beneficial** for complex environments like QIIME 2

## Resources
- [QIIME 2 Documentation](https://docs.qiime2.org/)
- [QIIME 2 Amplicon Tutorial](https://amplicon-docs.qiime2.org/)
- [Krona Documentation](https://github.com/marbl/Krona/wiki)
- [q2-krona Plugin](https://github.com/kaanb93/q2-krona)
- [Mamba Documentation](https://mamba.readthedocs.io/)

## License
This Gitpod configuration is provided as-is for educational and research purposes.
