## dev

## v1.4.0 - 2024-03-18

> [!WARNING]
> This is the final release to support Snakemake versions 5, 6, and 7.

Example that specifies memory in GB instead of MB (`mem-gb`)

Example that shares a profile between pipelines, and includes the name of the
Snakefile in the path to the logs (`shared-logs`) ([Issue #12][issue-12])

[issue-12]: https://github.com/jdblischak/smk-simple-slurm/issues/12

Update [job grouping][grouping] example to better allocate resources (requires
minimum of Snakemake version 7.11.0) ([Snakemake Issue
#872][snakemake-issue-872])

[snakemake-issue-872]: https://github.com/snakemake/snakemake/issues/872

Example that uses a job array to submit many jobs at once (`job-array`)

Example that uses `--slurm` (`slurm-native`, requires Snakemake 7.19.0+)

Example that logs stdout and stderr to separate files (`separate-stderr`)
([Issue #14][issue-14])

[issue-14]: https://github.com/jdblischak/smk-simple-slurm/issues/14

Example that conditionally specifies a resource for a subset of rules
([TomHarrop][], [#16][issue-16], [#17][pr-17])

Example that lists multiple partitions for Slurm to choose from ([TomHarrop][],
[#16][issue-16], [#17][pr-17])

[TomHarrop]: https://github.com/TomHarrop
[issue-16]: https://github.com/jdblischak/smk-simple-slurm/issues/16
[pr-17]: https://github.com/jdblischak/smk-simple-slurm/pull/17

## v1.3.0 - 2022-08-09

New status script `status-sacct-robust.sh` that re-runs `sacct` multiple times
if it fails to return a valid status. This is more robust and is recommended if
you notice Snakemake unexpectedly re-submits jobs that are still pending or
running. See [Issue #9][issue-9] for discussion

[issue-9]: https://github.com/jdblischak/smk-simple-slurm/issues/9

Example with [job grouping][grouping]

[grouping]: https://snakemake.readthedocs.io/en/stable/executing/grouping.html

Link to [Christian's profile for AWS ParallelCluster][snakemake-aws-parallelcluster-slurm]

[snakemake-aws-parallelcluster-slurm]: https://github.com/cbrueffer/snakemake-aws-parallelcluster-slurm

Example that uses pinned conda environments (`pinned-conda-envs`) (requires
minimum of Snakemake version 7.8.0)

Example that inserts the current date in the log file paths (`log-file-date`)

Example rule with thousands of input files (`many-input-files`)

## v1.2.0 - 2022-03-09

Full support for custom status scripts in a multi-cluster setup (requires
minimum of Snakemake version 7.1.1)

Example with [cluster-cancel][] (requires minimum of Snakemake version 7.0.0)

[cluster-cancel]: https://snakemake.readthedocs.io/en/stable/tutorial/additional_features.html#using-cluster-cancel

## v1.1.0 - 2021-09-17

Reduce the default settings for `max-jobs-per-second` and
`max-status-checks-per-second` to avoid stressing Slurm

Example of running rules in Singularity containers
([CreRecombinase](https://github.com/CreRecombinase),
[#2](https://github.com/jdblischak/smk-simple-slurm/pull/2))

## v1.0.0 - 2021-06-07

Initial release
