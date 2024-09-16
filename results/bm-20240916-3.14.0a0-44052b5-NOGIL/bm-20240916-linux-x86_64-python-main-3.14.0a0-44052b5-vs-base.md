# Results vs. base

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 44052b5
- commit date: 2024-09-16
- overall geometric mean: not sig
- HPT reliability: 84.13%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

| Benchmark | bm-20240916-linux-x86_64-python-05235e3c16d755e292eb-3.14.0a0-05235e3 | bm-20240916-linux-x86_64-python-main-3.14.0a0-44052b5 |
|-----------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| chaos     | 162 ms                                                                | 174 ms: 1.07x slower                                  |

# HPT report

- Reliability score: 84.13% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown