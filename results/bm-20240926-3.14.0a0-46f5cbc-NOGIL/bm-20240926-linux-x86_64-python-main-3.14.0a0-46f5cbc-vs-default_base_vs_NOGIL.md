# Results vs. default_base_vs_NOGIL

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 46f5cbc
- commit date: 2024-09-26
- overall geometric mean: not sig
- HPT reliability: 84.13%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.10x

| Benchmark | bm-20240926-linux-x86_64-python-de929f353c413459834a-3.14.0a0-de929f3 | bm-20240926-linux-x86_64-python-main-3.14.0a0-46f5cbc |
|-----------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| chaos     | 80.9 ms                                                               | 168 ms: 2.08x slower                                  |

# HPT report

- Reliability score: 84.13% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.10x