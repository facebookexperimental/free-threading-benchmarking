# Benchmark results

<!-- START table -->
## linux x86_64 (linux)
| date | fork/ref | hash/flags | vs. 3.11.0: | vs. base: |
| --- | --- | --- | ---: | ---: |
| [2024-08-08](results/bm-20240808-3.14.0a0-e006c73-NOGIL) | python/e006c7371d8e57db2625 | e006c73 (NOGIL) |  | 1.45x ↓<br>[📄](results/bm-20240808-3.14.0a0-e006c73-NOGIL/bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73-vs-base.md)[📈](results/bm-20240808-3.14.0a0-e006c73-NOGIL/bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73-vs-base.svg)[🧠](results/bm-20240808-3.14.0a0-e006c73-NOGIL/bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73-vs-base-mem.svg) |
| [2024-08-08](results/bm-20240808-3.14.0a0-e006c73) | python/e006c7371d8e57db2625 | e006c73 |  |  |
| [2024-08-07](results/bm-20240807-3.14.0a0-f483286) | mpage/gh_122712_fix_call_a | f483286 |  | 1.00x ↑<br>[📄](results/bm-20240807-3.14.0a0-f483286/bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286-vs-base.md)[📈](results/bm-20240807-3.14.0a0-f483286/bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286-vs-base.svg)[🧠](results/bm-20240807-3.14.0a0-f483286/bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286-vs-base-mem.svg) |
| [2024-08-07](results/bm-20240807-3.14.0a0-f483286-NOGIL) | mpage/gh_122712_fix_call_a | f483286 (NOGIL) |  | 1.00x ↓<br>[📄](results/bm-20240807-3.14.0a0-f483286-NOGIL/bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286-vs-base.md)[📈](results/bm-20240807-3.14.0a0-f483286-NOGIL/bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286-vs-base.svg)[🧠](results/bm-20240807-3.14.0a0-f483286-NOGIL/bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286-vs-base-mem.svg) |
| [2024-08-06](results/bm-20240806-3.14.0a0-4767a6e-NOGIL) | python/main | 4767a6e (NOGIL) |  |  |
| [2024-08-04](results/bm-20240804-3.14.0a0-151934a-NOGIL) | python/151934a324789c58cca9 | 151934a (NOGIL) |  | 1.42x ↓<br>[📄](results/bm-20240804-3.14.0a0-151934a-NOGIL/bm-20240804-linux-x86_64-python-151934a324789c58cca9-3.14.0a0-151934a-vs-base.md)[📈](results/bm-20240804-3.14.0a0-151934a-NOGIL/bm-20240804-linux-x86_64-python-151934a324789c58cca9-3.14.0a0-151934a-vs-base.svg)[🧠](results/bm-20240804-3.14.0a0-151934a-NOGIL/bm-20240804-linux-x86_64-python-151934a324789c58cca9-3.14.0a0-151934a-vs-base-mem.svg) |
| [2024-08-04](results/bm-20240804-3.14.0a0-151934a) | python/151934a324789c58cca9 | 151934a |  |  |
| [2024-07-27](results/bm-20240727-3.14.0a0-04eb5c8-NOGIL) | python/04eb5c8db1e24cabd0cb | 04eb5c8 (NOGIL) |  | 1.44x ↓<br>[📄](results/bm-20240727-3.14.0a0-04eb5c8-NOGIL/bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8-vs-base.md)[📈](results/bm-20240727-3.14.0a0-04eb5c8-NOGIL/bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8-vs-base.svg)[🧠](results/bm-20240727-3.14.0a0-04eb5c8-NOGIL/bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8-vs-base-mem.svg) |
| [2024-07-27](results/bm-20240727-3.14.0a0-04eb5c8) | python/04eb5c8db1e24cabd0cb | 04eb5c8 |  |  |
| [2024-07-25](results/bm-20240725-3.14.0a0-d9efa45-NOGIL) | python/main | d9efa45 (NOGIL) |  | 1.01x ↓<br>[📄](results/bm-20240725-3.14.0a0-d9efa45-NOGIL/bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45-vs-base.md)[📈](results/bm-20240725-3.14.0a0-d9efa45-NOGIL/bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45-vs-base.svg)[🧠](results/bm-20240725-3.14.0a0-d9efa45-NOGIL/bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45-vs-base-mem.svg) |
| [2024-07-25](results/bm-20240725-3.14.0a0-1d607fe-NOGIL) | python/1d607fe759ef22177b50 | 1d607fe (NOGIL) |  |  |
| [2024-07-24](results/bm-20240724-3.14.0a0-9ac6060-NOGIL) | python/9ac606080a0074cdf758 | 9ac6060 (NOGIL) |  |  |
| [2024-07-24](results/bm-20240724-3.14.0a0-5592399-NOGIL) | python/main | 5592399 (NOGIL) |  | 1.01x ↓<br>[📄](results/bm-20240724-3.14.0a0-5592399-NOGIL/bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399-vs-base.md)[📈](results/bm-20240724-3.14.0a0-5592399-NOGIL/bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399-vs-base.svg)[🧠](results/bm-20240724-3.14.0a0-5592399-NOGIL/bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399-vs-base-mem.svg) |
| [2024-07-23](results/bm-20240723-3.14.0a0-4606eff-NOGIL) | python/main | 4606eff (NOGIL) |  | 1.01x ↑<br>[📄](results/bm-20240723-3.14.0a0-4606eff-NOGIL/bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff-vs-base.md)[📈](results/bm-20240723-3.14.0a0-4606eff-NOGIL/bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff-vs-base.svg)[🧠](results/bm-20240723-3.14.0a0-4606eff-NOGIL/bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff-vs-base-mem.svg) |
| [2024-07-23](results/bm-20240723-3.14.0a0-a15fede-NOGIL) | python/a15feded71dd47202db1 | a15fede (NOGIL) |  |  |
| [2024-07-23](results/bm-20240723-3.14.0a0-a9bb3c7-NOGIL) | python/main | a9bb3c7 (NOGIL) |  | 1.02x ↑<br>[📄](results/bm-20240723-3.14.0a0-a9bb3c7-NOGIL/bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7-vs-base.md)[📈](results/bm-20240723-3.14.0a0-a9bb3c7-NOGIL/bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7-vs-base.svg)[🧠](results/bm-20240723-3.14.0a0-a9bb3c7-NOGIL/bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7-vs-base-mem.svg) |
| [2024-07-23](results/bm-20240723-3.14.0a0-a9bb3c7) | python/main | a9bb3c7 |  |  |
| [2024-07-22](results/bm-20240722-3.14.0a0-2762c6c-NOGIL) | python/2762c6cc5e4c1c0d6305 | 2762c6c (NOGIL) |  |  |


<!-- END table -->

`*` indicates that the exact same versions of pyperformance was not used.
