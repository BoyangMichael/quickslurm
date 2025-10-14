# quickslurm
Quick submission of a single job to slurm queue. Can be useful when you just want to test something quickly.

## Installation
Clone this repository.
```bash
git clone https://gitlab.ifpen.fr/xub/quickslurm.git
```
Add path to this repository in your `.bashrc` (or `.bash_profile` for MacOS).
```bash
export PATH="/path/to/quickslurm:$PATH"
```
Reload your profile.
```bash
exec bash
```

## Usage
```text
quickslurm - A wrapper to quickly submit a single job using Slurm

Usage:
  quickslurm COMMANDS
  quickslurm [-sbatch|--sbatch-options "<SBATCH_OPTIONS>"] COMMANDS
  quickslurm --help | -h

Examples:
  quickslurm g16 < input.gjf > output.g16
  quickslurm --sbatch-options "-n 16 -J test_run" g16 < input.gjf > output.g16
  quickslurm g16 -v -s < water.gjf > water.log

Notes:
  - default.conf => default configuration file
  - user.conf => user configuration file (if exists, will override default.conf)
  - First field of COMMANDS is recognized as PROGRAM
  - Configuration for PROGRAM wil be used if PROGRAM_config exist in the configuration file.
```

> Note: SAVE YOUR FINGERS by using the alias **`qs`** instead of `quickslurm`!