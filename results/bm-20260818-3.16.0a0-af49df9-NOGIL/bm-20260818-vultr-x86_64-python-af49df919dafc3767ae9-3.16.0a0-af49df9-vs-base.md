# Results vs. base

- fork: python
- ref: af49df919dafc3767ae9
- machine: linux-x86_64
- commit hash: af49df9
- commit date: 2026-08-18
- overall geometric mean: 1.105x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260818-3.16.0a0-af49df9/bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9.json | results/bm-20260818-3.16.0a0-af49df9-NOGIL/bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                                                          | 296 ms: 1.14x slower                                                                                                  |
| docutils       | 2.37 sec                                                                                                        | 2.90 sec: 1.22x slower                                                                                                |
| html5lib       | 59.5 ms                                                                                                         | 65.4 ms: 1.10x slower                                                                                                 |
| sphinx         | 993 ms                                                                                                          | 1.10 sec: 1.11x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.14x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260818-3.16.0a0-af49df9/bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9.json | results/bm-20260818-3.16.0a0-af49df9-NOGIL/bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 758 ms                                                                                                          | 691 ms: 1.10x faster                                                                                                  |
| asyncio_websockets         | 544 ms                                                                                                          | 507 ms: 1.07x faster                                                                                                  |
| async_tree_io              | 720 ms                                                                                                          | 703 ms: 1.02x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 555 ms                                                                                                          | 581 ms: 1.05x slower                                                                                                  |
| coroutines                 | 23.8 ms                                                                                                         | 25.0 ms: 1.05x slower                                                                                                 |
| async_tree_memoization_tg  | 363 ms                                                                                                          | 401 ms: 1.11x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 539 ms                                                                                                          | 599 ms: 1.11x slower                                                                                                  |
| async_tree_none_tg         | 297 ms                                                                                                          | 333 ms: 1.12x slower                                                                                                  |
| async_tree_memoization     | 375 ms                                                                                                          | 421 ms: 1.12x slower                                                                                                  |
| async_generators           | 343 ms                                                                                                          | 393 ms: 1.15x slower                                                                                                  |
| async_tree_none            | 292 ms                                                                                                          | 343 ms: 1.17x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.06x slower                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260818-3.16.0a0-af49df9/bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9.json | results/bm-20260818-3.16.0a0-af49df9-NOGIL/bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 187 ms                                                                                                          | 180 ms: 1.04x faster                                                                                                  |
| float          | 72.1 ms                                                                                                         | 83.8 ms: 1.16x slower                                                                                                 |
| nbody          | 89.1 ms                                                                                                         | 120 ms: 1.35x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.15x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260818-3.16.0a0-af49df9/bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9.json | results/bm-20260818-3.16.0a0-af49df9-NOGIL/bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.8 ms                                                                                                         | 21.0 ms: 1.04x faster                                                                                                 |
| regex_dna      | 181 ms                                                                                                          | 184 ms: 1.02x slower                                                                                                  |
| regex_compile  | 149 ms                                                                                                          | 168 ms: 1.13x slower                                                                                                  |
| regex_effbot   | 2.54 ms                                                                                                         | 2.98 ms: 1.17x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                           | 1.07x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260818-3.16.0a0-af49df9/bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9.json | results/bm-20260818-3.16.0a0-af49df9-NOGIL/bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 143 ms                                                                                                          | 140 ms: 1.02x faster                                                                                                  |
| tomli_loads          | 1.84 sec                                                                                                        | 1.91 sec: 1.04x slower                                                                                                |
| xml_etree_iterparse  | 91.1 ms                                                                                                         | 95.6 ms: 1.05x slower                                                                                                 |
| json_dumps           | 9.33 ms                                                                                                         | 10.0 ms: 1.08x slower                                                                                                 |
| json_loads           | 27.4 us                                                                                                         | 30.5 us: 1.11x slower                                                                                                 |
| pickle_pure_python   | 300 us                                                                                                          | 336 us: 1.12x slower                                                                                                  |
| unpickle_pure_python | 210 us                                                                                                          | 239 us: 1.14x slower                                                                                                  |
| xml_etree_generate   | 88.3 ms                                                                                                         | 101 ms: 1.14x slower                                                                                                  |
| xml_etree_process    | 62.6 ms                                                                                                         | 74.9 ms: 1.20x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260818-3.16.0a0-af49df9/bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9.json | results/bm-20260818-3.16.0a0-af49df9-NOGIL/bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.6 ms                                                                                                         | 15.8 ms: 1.25x slower                                                                                                 |
| python_startup_no_site | 7.09 ms                                                                                                         | 9.29 ms: 1.31x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.28x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260818-3.16.0a0-af49df9/bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9.json | results/bm-20260818-3.16.0a0-af49df9-NOGIL/bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 36.6 ms                                                                                                         | 40.9 ms: 1.12x slower                                                                                                 |
| mako            | 11.9 ms                                                                                                         | 16.0 ms: 1.34x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.23x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20260818-3.16.0a0-af49df9/bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9.json | results/bm-20260818-3.16.0a0-af49df9-NOGIL/bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 242 ms                                                                                                          | 6.71 ms: 36.09x faster                                                                                                |
| gc_traversal               | 3.84 ms                                                                                                         | 1.78 ms: 2.16x faster                                                                                                 |
| create_gc_cycles           | 1.66 ms                                                                                                         | 1.38 ms: 1.21x faster                                                                                                 |
| sqlite_synth               | 2.19 us                                                                                                         | 1.93 us: 1.13x faster                                                                                                 |
| async_tree_io_tg           | 758 ms                                                                                                          | 691 ms: 1.10x faster                                                                                                  |
| asyncio_websockets         | 544 ms                                                                                                          | 507 ms: 1.07x faster                                                                                                  |
| pidigits                   | 187 ms                                                                                                          | 180 ms: 1.04x faster                                                                                                  |
| regex_v8                   | 21.8 ms                                                                                                         | 21.0 ms: 1.04x faster                                                                                                 |
| async_tree_io              | 720 ms                                                                                                          | 703 ms: 1.02x faster                                                                                                  |
| xml_etree_parse            | 143 ms                                                                                                          | 140 ms: 1.02x faster                                                                                                  |
| regex_dna                  | 181 ms                                                                                                          | 184 ms: 1.02x slower                                                                                                  |
| bpe_tokeniser              | 4.22 sec                                                                                                        | 4.36 sec: 1.03x slower                                                                                                |
| dulwich_log                | 67.4 ms                                                                                                         | 69.7 ms: 1.03x slower                                                                                                 |
| tomli_loads                | 1.84 sec                                                                                                        | 1.91 sec: 1.04x slower                                                                                                |
| pycparser                  | 1.12 sec                                                                                                        | 1.17 sec: 1.05x slower                                                                                                |
| async_tree_cpu_io_mixed_tg | 555 ms                                                                                                          | 581 ms: 1.05x slower                                                                                                  |
| xml_etree_iterparse        | 91.1 ms                                                                                                         | 95.6 ms: 1.05x slower                                                                                                 |
| coroutines                 | 23.8 ms                                                                                                         | 25.0 ms: 1.05x slower                                                                                                 |
| json_dumps                 | 9.33 ms                                                                                                         | 10.0 ms: 1.08x slower                                                                                                 |
| k_core                     | 2.07 sec                                                                                                        | 2.24 sec: 1.08x slower                                                                                                |
| many_optionals             | 909 us                                                                                                          | 995 us: 1.10x slower                                                                                                  |
| json                       | 4.89 ms                                                                                                         | 5.35 ms: 1.10x slower                                                                                                 |
| html5lib                   | 59.5 ms                                                                                                         | 65.4 ms: 1.10x slower                                                                                                 |
| telco                      | 159 ms                                                                                                          | 175 ms: 1.10x slower                                                                                                  |
| async_tree_memoization_tg  | 363 ms                                                                                                          | 401 ms: 1.11x slower                                                                                                  |
| bench_thread_pool          | 1.35 ms                                                                                                         | 1.49 ms: 1.11x slower                                                                                                 |
| sphinx                     | 993 ms                                                                                                          | 1.10 sec: 1.11x slower                                                                                                |
| async_tree_cpu_io_mixed    | 539 ms                                                                                                          | 599 ms: 1.11x slower                                                                                                  |
| logging_silent             | 94.7 ns                                                                                                         | 105 ns: 1.11x slower                                                                                                  |
| sqlglot_v2_normalize       | 102 ms                                                                                                          | 114 ms: 1.11x slower                                                                                                  |
| sqlglot_v2_optimize        | 51.8 ms                                                                                                         | 57.7 ms: 1.11x slower                                                                                                 |
| json_loads                 | 27.4 us                                                                                                         | 30.5 us: 1.11x slower                                                                                                 |
| pprint_safe_repr           | 735 ms                                                                                                          | 823 ms: 1.12x slower                                                                                                  |
| django_template            | 36.6 ms                                                                                                         | 40.9 ms: 1.12x slower                                                                                                 |
| pickle_pure_python         | 300 us                                                                                                          | 336 us: 1.12x slower                                                                                                  |
| sympy_expand               | 476 ms                                                                                                          | 533 ms: 1.12x slower                                                                                                  |
| async_tree_none_tg         | 297 ms                                                                                                          | 333 ms: 1.12x slower                                                                                                  |
| deepcopy_reduce            | 2.58 us                                                                                                         | 2.90 us: 1.12x slower                                                                                                 |
| sympy_str                  | 282 ms                                                                                                          | 316 ms: 1.12x slower                                                                                                  |
| async_tree_memoization     | 375 ms                                                                                                          | 421 ms: 1.12x slower                                                                                                  |
| chaos                      | 53.3 ms                                                                                                         | 60.1 ms: 1.13x slower                                                                                                 |
| regex_compile              | 149 ms                                                                                                          | 168 ms: 1.13x slower                                                                                                  |
| deltablue                  | 3.31 ms                                                                                                         | 3.76 ms: 1.13x slower                                                                                                 |
| scimark_fft                | 301 ms                                                                                                          | 342 ms: 1.13x slower                                                                                                  |
| sympy_integrate            | 19.3 ms                                                                                                         | 21.9 ms: 1.14x slower                                                                                                 |
| subparsers                 | 9.05 ms                                                                                                         | 10.3 ms: 1.14x slower                                                                                                 |
| sympy_sum                  | 159 ms                                                                                                          | 181 ms: 1.14x slower                                                                                                  |
| pprint_pformat             | 1.50 sec                                                                                                        | 1.70 sec: 1.14x slower                                                                                                |
| scimark_lu                 | 116 ms                                                                                                          | 133 ms: 1.14x slower                                                                                                  |
| logging_simple             | 6.19 us                                                                                                         | 7.06 us: 1.14x slower                                                                                                 |
| unpickle_pure_python       | 210 us                                                                                                          | 239 us: 1.14x slower                                                                                                  |
| 2to3                       | 259 ms                                                                                                          | 296 ms: 1.14x slower                                                                                                  |
| pylint                     | 114 ms                                                                                                          | 130 ms: 1.14x slower                                                                                                  |
| xml_etree_generate         | 88.3 ms                                                                                                         | 101 ms: 1.14x slower                                                                                                  |
| comprehensions             | 15.6 us                                                                                                         | 17.9 us: 1.14x slower                                                                                                 |
| async_generators           | 343 ms                                                                                                          | 393 ms: 1.15x slower                                                                                                  |
| mdp                        | 1.13 sec                                                                                                        | 1.30 sec: 1.15x slower                                                                                                |
| scimark_sor                | 104 ms                                                                                                          | 120 ms: 1.15x slower                                                                                                  |
| deepcopy                   | 232 us                                                                                                          | 268 us: 1.15x slower                                                                                                  |
| richards                   | 45.0 ms                                                                                                         | 52.1 ms: 1.16x slower                                                                                                 |
| float                      | 72.1 ms                                                                                                         | 83.8 ms: 1.16x slower                                                                                                 |
| richards_super             | 51.3 ms                                                                                                         | 59.8 ms: 1.17x slower                                                                                                 |
| nqueens                    | 74.5 ms                                                                                                         | 87.0 ms: 1.17x slower                                                                                                 |
| go                         | 103 ms                                                                                                          | 120 ms: 1.17x slower                                                                                                  |
| hexiom                     | 5.62 ms                                                                                                         | 6.57 ms: 1.17x slower                                                                                                 |
| regex_effbot               | 2.54 ms                                                                                                         | 2.98 ms: 1.17x slower                                                                                                 |
| async_tree_none            | 292 ms                                                                                                          | 343 ms: 1.17x slower                                                                                                  |
| generators                 | 28.0 ms                                                                                                         | 32.9 ms: 1.17x slower                                                                                                 |
| pyflate                    | 389 ms                                                                                                          | 458 ms: 1.18x slower                                                                                                  |
| thrift                     | 781 us                                                                                                          | 920 us: 1.18x slower                                                                                                  |
| scimark_sparse_mat_mult    | 4.36 ms                                                                                                         | 5.14 ms: 1.18x slower                                                                                                 |
| raytrace                   | 247 ms                                                                                                          | 292 ms: 1.18x slower                                                                                                  |
| logging_format             | 6.95 us                                                                                                         | 8.22 us: 1.18x slower                                                                                                 |
| sqlglot_v2_transpile       | 1.46 ms                                                                                                         | 1.73 ms: 1.18x slower                                                                                                 |
| deepcopy_memo              | 26.5 us                                                                                                         | 31.7 us: 1.20x slower                                                                                                 |
| xml_etree_process          | 62.6 ms                                                                                                         | 74.9 ms: 1.20x slower                                                                                                 |
| spectral_norm              | 89.1 ms                                                                                                         | 107 ms: 1.20x slower                                                                                                  |
| shortest_path              | 440 ms                                                                                                          | 534 ms: 1.22x slower                                                                                                  |
| sqlglot_v2_parse           | 1.16 ms                                                                                                         | 1.41 ms: 1.22x slower                                                                                                 |
| docutils                   | 2.37 sec                                                                                                        | 2.90 sec: 1.22x slower                                                                                                |
| typing_runtime_protocols   | 118 us                                                                                                          | 145 us: 1.23x slower                                                                                                  |
| scimark_monte_carlo        | 62.2 ms                                                                                                         | 77.5 ms: 1.25x slower                                                                                                 |
| python_startup             | 12.6 ms                                                                                                         | 15.8 ms: 1.25x slower                                                                                                 |
| meteor_contest             | 102 ms                                                                                                          | 128 ms: 1.26x slower                                                                                                  |
| connected_components       | 393 ms                                                                                                          | 495 ms: 1.26x slower                                                                                                  |
| fannkuch                   | 370 ms                                                                                                          | 467 ms: 1.26x slower                                                                                                  |
| python_startup_no_site     | 7.09 ms                                                                                                         | 9.29 ms: 1.31x slower                                                                                                 |
| crypto_pyaes               | 66.9 ms                                                                                                         | 87.9 ms: 1.31x slower                                                                                                 |
| mako                       | 11.9 ms                                                                                                         | 16.0 ms: 1.34x slower                                                                                                 |
| nbody                      | 89.1 ms                                                                                                         | 120 ms: 1.35x slower                                                                                                  |
| coverage                   | 82.6 ms                                                                                                         | 116 ms: 1.40x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.07x slower                                                                                                          |

Benchmark hidden because not significant (1): pathlib

- Geometric mean (including insignificant results): 1.105x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.12x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.18x