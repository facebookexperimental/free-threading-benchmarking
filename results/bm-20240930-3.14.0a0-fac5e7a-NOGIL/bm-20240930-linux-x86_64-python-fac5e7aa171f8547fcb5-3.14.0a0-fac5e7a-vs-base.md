# Results vs. base

- fork: python
- ref: fac5e7aa171f8547fcb5
- machine: linux-x86_64
- commit hash: fac5e7a
- commit date: 2024-09-30
- overall geometric mean: not sig
- HPT reliability: 84.13%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.12x

| Benchmark | results/bm-20240930-3.14.0a0-fac5e7a/bm-20240930-linux-x86_64-python-fac5e7aa171f8547fcb5-3.14.0a0-fac5e7a.json | results/bm-20240930-3.14.0a0-fac5e7a-NOGIL/bm-20240930-linux-x86_64-python-fac5e7aa171f8547fcb5-3.14.0a0-fac5e7a.json |
|-----------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| chaos     | 80.7 ms                                                                                                         | 164 ms: 2.03x slower                                                                                                  |

# HPT report

- Reliability score: 84.13% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.12x