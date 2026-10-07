# JSSPTS Benchmark Instances

This repository contains the problem instances used in the computational study of the associated manuscript
 **Job-shop scheduling with tool wear: Minimizing replacement events under completion-time constraints** 


**Simon Emde and Humyun Fuad Rahman**,  

The repository provides the benchmark and sensitivity-analysis instances used in the study so that the computational experiments can be inspected and reproduced.

## Repository contents

The instance data are provided in three ZIP archives:

- `Synthetic_Instances_GitHub.zip` — **40 synthetic benchmark instances**
- `Realistic_Instances_GitHub.zip` — **20 realistic benchmark instances**
- `Sensitivity_Instances_GitHub.zip` — **5 reduced realistic instances used in the sensitivity analysis**

In total, the repository contains **65 problem instances**.

## 1. Synthetic benchmark instances

The synthetic benchmark set contains 40 instances:

```text
LA_TS_S01.txt
LA_TS_S02.txt
...
LA_TS_S40.txt
```

The string `CPLEX` was removed from the original filenames for a cleaner public naming convention.  
The numerical contents of the synthetic files were not changed.

## 2. Realistic benchmark instances

The realistic benchmark set contains 20 instances:

```text
LA_TS_R01.txt
LA_TS_R02.txt
...
LA_TS_R20.txt
```

Each realistic benchmark instance contains:

- **40 jobs**
- **15 machines**
- instance-specific numbers of tools

The original numerical data were retained exactly. The files were reformatted for readability by adding variable names, brackets, commas, and delimiters.

## 3. Sensitivity-analysis instances

The sensitivity-analysis set contains five reduced realistic instances:

```text
LA_TS_R01.txt
LA_TS_R02.txt
LA_TS_R03.txt
LA_TS_R04.txt
LA_TS_R05.txt
```

Each sensitivity instance contains:

- **15 jobs**
- **10 machines**
- instance-specific numbers of tools

### Important naming note

The sensitivity-analysis files use the names `R01`–`R05` because those names are used in the manuscript.

They are **not the same files** as benchmark realistic instances `R01`–`R05` in the 40-job/15-machine set.

For this reason, the sensitivity instances are distributed separately in `Sensitivity_Instances_GitHub.zip`.

## Instance variables

The formatted realistic and sensitivity-analysis files use the following variable names:

| Variable | Description |
|---|---|
| `NUM_MACHINES` | Number of machines |
| `NUM_JOBS` | Number of jobs |
| `NUM_TOOLS` | Number of tools |
| `p` | Processing-time matrix |
| `b` | Tool-wear / tool-life-consumption matrix |
| `tau` | Tool-swap setup-time data |
| `W` | Tool life after replacement |
| `W0` | Initial tool life |
| `sigma` | Machine/routing assignment data stored in the instance |
| `ik` | Machine associated with each tool |
| `w` | Job weights used in total weighted completion time |

## Setup-time representation

For the realistic benchmark instances with 40 jobs, the original raw files store `tau` as:

```text
15 × 41 × 41
```

For the sensitivity-analysis instances with 15 jobs, the original raw files store `tau` as:

```text
10 × 16 × 16
```

The extra index corresponds to the dummy-job convention used in the source data.  
These dimensions have been preserved exactly rather than altered for formatting consistency.

## Data integrity

Before public release, all GitHub-formatted files were crosschecked against their original counterparts.

Final verification result:

- Synthetic benchmark: **40/40 matched**
- Realistic benchmark: **20/20 matched**
- Sensitivity analysis: **5/5 matched**





## Use of the data

These files are provided for academic research, benchmarking, replication, and methodological comparison.

If you use these instances in academic work, please cite the associated paper once its final bibliographic details are available.

## Citation

Citation details will be updated after publication.
