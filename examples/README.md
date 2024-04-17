# Examples

Each directory contains an example usage of the simple slurm profile. You can run
them on your cluster to confirm the expected behavior.

* `cluster-cancel` - Cancel all submitted jobs with `scancel` when the main
  Snakemake process is cancelled (requires Snakemake 7.0.0+)

* `conditional-resource` - Conditionally specify a resource for a subset of
  rules

* `dynamic-resources` - Increase memory for a rule on restart after each failed
  attempt

* `job-array` - Use a Slurm job array to quickly execute a rule that must be run
  thousands of times

* `job-grouping` - Adapt profile to allow job grouping

* `jobs-per-second` - Measure how many jobs Snakemake can submit to Slurm per
  second

* `list-partitions` - List multiple partitions for Slurm to choose from

* `log-file-date` - Insert the current date into the log file path

* `many-input-files` - Use a custom jobscript when a rule has many thousands of
  input files

* `mem-gb` - Specify memory in GB

* `multi-cluster` - Submit jobs to more than one cluster (requires Snakemake
  7.1.1+)

* `out-of-memory` - Trigger an out-of-memory error. Snakemake can handle this by
  default

* `pinned-conda-envs` - Pin packages in conda environments

* `separate-stderr` - Log stdout and stderr to separate files

* `shared-logs` - Share the same profile `config.yaml` between multiple
  pipelines, but include the name of the Snakefile in the path to the log files

* `singularity` - Run a rule inside a singularity container

* `slurm-native` - Use Snakemake's native Slurm support (`--slurm`, requires
  Snakemake 7.19.0+)

* `threads` - Increase the `threads` for a rule. It is responsive to `--jobs`.
  In other words, it will scale down the number of threads used if there aren't
  enough available (thus make sure to pass `{threads}` to the software you are
  running). This mainly applies when running the rules locally (i.e. without the
  profile). When submitting to the cluster, `--jobs` refers literally to jobs,
  not cores like in local mode

* `time-integer` - Specify `--time` as an integer (minutes)

* `time-string` - Specify the time as `"days-hours:minutes:seconds"`

* `timeout` - Trigger a timeout error. Snakemake requires the assistance of a
  custom script to `--cluster-status` to handle this error. Otherwise it just
  stalls indefinitely
