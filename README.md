# amr_wrapper.py usage:

## Paths:

Must include path to `amr_wrapper.py` in `$PATH`.<br>
Must also include this path in `$PYTHONPATH`.

Within the directory containing `amr_wrapper.py` these other 9 files are included:

- `abricate_wrapper.py`
- `amr_wrapper.py`
- `amrfinder_wrapper.py`
- `latex_reporter.py`
- `lookup_genome_size.json`
- `mlst_wrapper.py`
- `rmlst.py`
- `seqsero2_wrapper.py`
- `sequence_score.py`

In addition to the above files the following Python files must be in `$PYTHONPATH`.

- `vsnp_fastq_quality.py`
- `spades_assembly.py`
- `spades_stats_parse.py`
- `kraken2_run.py`

For example:

```zsh
export PYTHONPATH="${PYTHONPATH}:${HOME}/git/gitlab/stuber/python_scripts"
export PYTHONPATH="${PYTHONPATH}:${HOME}/git/gitlab/amr"
export PYTHONPATH="${PYTHONPATH}:${HOME}/.conda/envs/tod/bin"
```

## Run:

See `amr_wrapper.py` for run options.

Basic usage:

```zsh
amr_wrapper.py -r1 *_R1*fastq.gz -r2 *_R2*fastq.gz
```

## HPC:

A batch file for running a single sample is here:

```zsh
${HOME}/git/gitlab/batch_scripts/amr.sh
```

options can be passed within a single pair of quotes:

```zsh
${HOME}/git/gitlab/batch_scripts/amr.sh "-a -d"
```

If multple paired FASTQ files are to be ran at the same time:

```zsh
${HOME}/git/gitlab/stuber/hpc/cluster_amr.sh
```

As with a single sample batch script, options can be passed:

```zsh
${HOME}/git/gitlab/stuber/hpc/cluster_amr.sh "-ad"
```

`cluster_amr.sh` runs one sample per node.

A typical sample will run in approximately 20 minutes.
# NAHLN_AMR
