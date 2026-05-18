# Results vs. base

- fork: python
- ref: acefff95eab3db6b7cf8
- machine: linux-x86_64
- commit hash: acefff9
- commit date: 2026-05-17
- overall geometric mean: 1.099x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260517-3.16.0a0-acefff9/bm-20260517-vultr-x86_64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9.json | results/bm-20260517-3.16.0a0-acefff9-NOGIL/bm-20260517-vultr-x86_64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| docutils       | 2.41 sec                                                                                                        | 2.97 sec: 1.23x slower                                                                                                |
| html5lib       | 61.0 ms                                                                                                         | 68.3 ms: 1.12x slower                                                                                                 |
| sphinx         | 994 ms                                                                                                          | 1.12 sec: 1.12x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.16x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260517-3.16.0a0-acefff9/bm-20260517-vultr-x86_64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9.json | results/bm-20260517-3.16.0a0-acefff9-NOGIL/bm-20260517-vultr-x86_64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 756 ms                                                                                                          | 689 ms: 1.10x faster                                                                                                  |
| asyncio_websockets         | 545 ms                                                                                                          | 509 ms: 1.07x faster                                                                                                  |
| coroutines                 | 24.8 ms                                                                                                         | 24.9 ms: 1.00x slower                                                                                                 |
| async_tree_none_tg         | 301 ms                                                                                                          | 326 ms: 1.08x slower                                                                                                  |
| async_tree_memoization_tg  | 364 ms                                                                                                          | 399 ms: 1.10x slower                                                                                                  |
| async_tree_memoization     | 377 ms                                                                                                          | 422 ms: 1.12x slower                                                                                                  |
| async_generators           | 342 ms                                                                                                          | 387 ms: 1.13x slower                                                                                                  |
| async_tree_none            | 293 ms                                                                                                          | 343 ms: 1.17x slower                                                                                                  |
| async_tree_cpu_io_mixed_tg | 555 ms                                                                                                          | 670 ms: 1.21x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 539 ms                                                                                                          | 690 ms: 1.28x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.08x slower                                                                                                          |

Benchmark hidden because not significant (1): async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260517-3.16.0a0-acefff9/bm-20260517-vultr-x86_64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9.json | results/bm-20260517-3.16.0a0-acefff9-NOGIL/bm-20260517-vultr-x86_64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| float          | 75.6 ms                                                                                                         | 87.4 ms: 1.16x slower                                                                                                 |
| pidigits       | 188 ms                                                                                                          | 224 ms: 1.19x slower                                                                                                  |
| nbody          | 97.4 ms                                                                                                         | 126 ms: 1.29x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.21x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260517-3.16.0a0-acefff9/bm-20260517-vultr-x86_64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9.json | results/bm-20260517-3.16.0a0-acefff9-NOGIL/bm-20260517-vultr-x86_64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_dna      | 185 ms                                                                                                          | 175 ms: 1.06x faster                                                                                                  |
| regex_v8       | 21.6 ms                                                                                                         | 20.6 ms: 1.05x faster                                                                                                 |
| regex_effbot   | 2.97 ms                                                                                                         | 2.95 ms: 1.01x faster                                                                                                 |
| regex_compile  | 126 ms                                                                                                          | 145 ms: 1.15x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.01x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260517-3.16.0a0-acefff9/bm-20260517-vultr-x86_64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9.json | results/bm-20260517-3.16.0a0-acefff9-NOGIL/bm-20260517-vultr-x86_64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 141 ms                                                                                                          | 140 ms: 1.01x faster                                                                                                  |
| xml_etree_iterparse  | 89.4 ms                                                                                                         | 95.3 ms: 1.07x slower                                                                                                 |
| pickle_pure_python   | 321 us                                                                                                          | 344 us: 1.07x slower                                                                                                  |
| tomli_loads          | 1.83 sec                                                                                                        | 1.99 sec: 1.09x slower                                                                                                |
| json_dumps           | 9.82 ms                                                                                                         | 10.9 ms: 1.11x slower                                                                                                 |
| unpickle_pure_python | 216 us                                                                                                          | 242 us: 1.12x slower                                                                                                  |
| json_loads           | 27.7 us                                                                                                         | 31.1 us: 1.13x slower                                                                                                 |
| xml_etree_generate   | 86.7 ms                                                                                                         | 102 ms: 1.18x slower                                                                                                  |
| xml_etree_process    | 61.6 ms                                                                                                         | 75.7 ms: 1.23x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.11x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260517-3.16.0a0-acefff9/bm-20260517-vultr-x86_64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9.json | results/bm-20260517-3.16.0a0-acefff9-NOGIL/bm-20260517-vultr-x86_64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 35.8 ms                                                                                                         | 40.1 ms: 1.12x slower                                                                                                 |
| mako            | 12.1 ms                                                                                                         | 16.0 ms: 1.32x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.22x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20260517-3.16.0a0-acefff9/bm-20260517-vultr-x86_64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9.json | results/bm-20260517-3.16.0a0-acefff9-NOGIL/bm-20260517-vultr-x86_64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 237 ms                                                                                                          | 6.97 ms: 34.06x faster                                                                                                |
| gc_traversal               | 4.19 ms                                                                                                         | 1.90 ms: 2.20x faster                                                                                                 |
| create_gc_cycles           | 1.82 ms                                                                                                         | 1.49 ms: 1.22x faster                                                                                                 |
| sqlite_synth               | 2.24 us                                                                                                         | 1.95 us: 1.15x faster                                                                                                 |
| async_tree_io_tg           | 756 ms                                                                                                          | 689 ms: 1.10x faster                                                                                                  |
| asyncio_websockets         | 545 ms                                                                                                          | 509 ms: 1.07x faster                                                                                                  |
| regex_dna                  | 185 ms                                                                                                          | 175 ms: 1.06x faster                                                                                                  |
| regex_v8                   | 21.6 ms                                                                                                         | 20.6 ms: 1.05x faster                                                                                                 |
| pycparser                  | 1.19 sec                                                                                                        | 1.18 sec: 1.01x faster                                                                                                |
| xml_etree_parse            | 141 ms                                                                                                          | 140 ms: 1.01x faster                                                                                                  |
| regex_effbot               | 2.97 ms                                                                                                         | 2.95 ms: 1.01x faster                                                                                                 |
| coroutines                 | 24.8 ms                                                                                                         | 24.9 ms: 1.00x slower                                                                                                 |
| dulwich_log                | 69.9 ms                                                                                                         | 71.5 ms: 1.02x slower                                                                                                 |
| pathlib                    | 17.6 ms                                                                                                         | 18.0 ms: 1.03x slower                                                                                                 |
| json                       | 5.17 ms                                                                                                         | 5.34 ms: 1.03x slower                                                                                                 |
| bpe_tokeniser              | 4.21 sec                                                                                                        | 4.43 sec: 1.05x slower                                                                                                |
| logging_silent             | 100 ns                                                                                                          | 106 ns: 1.06x slower                                                                                                  |
| xml_etree_iterparse        | 89.4 ms                                                                                                         | 95.3 ms: 1.07x slower                                                                                                 |
| pickle_pure_python         | 321 us                                                                                                          | 344 us: 1.07x slower                                                                                                  |
| scimark_fft                | 321 ms                                                                                                          | 344 ms: 1.07x slower                                                                                                  |
| deltablue                  | 3.42 ms                                                                                                         | 3.70 ms: 1.08x slower                                                                                                 |
| async_tree_none_tg         | 301 ms                                                                                                          | 326 ms: 1.08x slower                                                                                                  |
| tomli_loads                | 1.83 sec                                                                                                        | 1.99 sec: 1.09x slower                                                                                                |
| k_core                     | 2.09 sec                                                                                                        | 2.29 sec: 1.09x slower                                                                                                |
| scimark_sor                | 111 ms                                                                                                          | 121 ms: 1.09x slower                                                                                                  |
| comprehensions             | 16.0 us                                                                                                         | 17.5 us: 1.10x slower                                                                                                 |
| async_tree_memoization_tg  | 364 ms                                                                                                          | 399 ms: 1.10x slower                                                                                                  |
| many_optionals             | 922 us                                                                                                          | 1.01 ms: 1.10x slower                                                                                                 |
| telco                      | 162 ms                                                                                                          | 178 ms: 1.10x slower                                                                                                  |
| bench_thread_pool          | 1.33 ms                                                                                                         | 1.47 ms: 1.10x slower                                                                                                 |
| pprint_safe_repr           | 743 ms                                                                                                          | 822 ms: 1.11x slower                                                                                                  |
| scimark_lu                 | 116 ms                                                                                                          | 128 ms: 1.11x slower                                                                                                  |
| json_dumps                 | 9.82 ms                                                                                                         | 10.9 ms: 1.11x slower                                                                                                 |
| hexiom                     | 5.88 ms                                                                                                         | 6.55 ms: 1.11x slower                                                                                                 |
| sympy_expand               | 479 ms                                                                                                          | 536 ms: 1.12x slower                                                                                                  |
| django_template            | 35.8 ms                                                                                                         | 40.1 ms: 1.12x slower                                                                                                 |
| unpickle_pure_python       | 216 us                                                                                                          | 242 us: 1.12x slower                                                                                                  |
| html5lib                   | 61.0 ms                                                                                                         | 68.3 ms: 1.12x slower                                                                                                 |
| async_tree_memoization     | 377 ms                                                                                                          | 422 ms: 1.12x slower                                                                                                  |
| sphinx                     | 994 ms                                                                                                          | 1.12 sec: 1.12x slower                                                                                                |
| json_loads                 | 27.7 us                                                                                                         | 31.1 us: 1.13x slower                                                                                                 |
| sqlglot_v2_optimize        | 51.4 ms                                                                                                         | 57.9 ms: 1.13x slower                                                                                                 |
| thrift                     | 809 us                                                                                                          | 913 us: 1.13x slower                                                                                                  |
| pprint_pformat             | 1.50 sec                                                                                                        | 1.70 sec: 1.13x slower                                                                                                |
| chaos                      | 55.9 ms                                                                                                         | 63.1 ms: 1.13x slower                                                                                                 |
| sqlglot_v2_normalize       | 102 ms                                                                                                          | 115 ms: 1.13x slower                                                                                                  |
| async_generators           | 342 ms                                                                                                          | 387 ms: 1.13x slower                                                                                                  |
| deepcopy                   | 239 us                                                                                                          | 270 us: 1.13x slower                                                                                                  |
| spectral_norm              | 95.3 ms                                                                                                         | 108 ms: 1.13x slower                                                                                                  |
| deepcopy_memo              | 27.6 us                                                                                                         | 31.3 us: 1.13x slower                                                                                                 |
| subparsers                 | 9.50 ms                                                                                                         | 10.8 ms: 1.14x slower                                                                                                 |
| deepcopy_reduce            | 2.60 us                                                                                                         | 2.96 us: 1.14x slower                                                                                                 |
| go                         | 107 ms                                                                                                          | 123 ms: 1.15x slower                                                                                                  |
| scimark_sparse_mat_mult    | 4.64 ms                                                                                                         | 5.34 ms: 1.15x slower                                                                                                 |
| regex_compile              | 126 ms                                                                                                          | 145 ms: 1.15x slower                                                                                                  |
| float                      | 75.6 ms                                                                                                         | 87.4 ms: 1.16x slower                                                                                                 |
| raytrace                   | 260 ms                                                                                                          | 301 ms: 1.16x slower                                                                                                  |
| pyflate                    | 401 ms                                                                                                          | 467 ms: 1.16x slower                                                                                                  |
| pylint                     | 114 ms                                                                                                          | 133 ms: 1.16x slower                                                                                                  |
| logging_simple             | 5.96 us                                                                                                         | 6.95 us: 1.17x slower                                                                                                 |
| mdp                        | 1.14 sec                                                                                                        | 1.33 sec: 1.17x slower                                                                                                |
| sympy_sum                  | 155 ms                                                                                                          | 181 ms: 1.17x slower                                                                                                  |
| sympy_integrate            | 19.1 ms                                                                                                         | 22.3 ms: 1.17x slower                                                                                                 |
| async_tree_none            | 293 ms                                                                                                          | 343 ms: 1.17x slower                                                                                                  |
| logging_format             | 6.69 us                                                                                                         | 7.84 us: 1.17x slower                                                                                                 |
| sympy_str                  | 274 ms                                                                                                          | 321 ms: 1.17x slower                                                                                                  |
| xml_etree_generate         | 86.7 ms                                                                                                         | 102 ms: 1.18x slower                                                                                                  |
| sqlglot_v2_transpile       | 1.47 ms                                                                                                         | 1.74 ms: 1.18x slower                                                                                                 |
| nqueens                    | 74.6 ms                                                                                                         | 88.7 ms: 1.19x slower                                                                                                 |
| pidigits                   | 188 ms                                                                                                          | 224 ms: 1.19x slower                                                                                                  |
| generators                 | 28.0 ms                                                                                                         | 33.5 ms: 1.20x slower                                                                                                 |
| typing_runtime_protocols   | 120 us                                                                                                          | 144 us: 1.20x slower                                                                                                  |
| sqlglot_v2_parse           | 1.17 ms                                                                                                         | 1.41 ms: 1.21x slower                                                                                                 |
| async_tree_cpu_io_mixed_tg | 555 ms                                                                                                          | 670 ms: 1.21x slower                                                                                                  |
| richards_super             | 49.9 ms                                                                                                         | 60.3 ms: 1.21x slower                                                                                                 |
| fannkuch                   | 378 ms                                                                                                          | 459 ms: 1.21x slower                                                                                                  |
| shortest_path              | 441 ms                                                                                                          | 538 ms: 1.22x slower                                                                                                  |
| richards                   | 43.3 ms                                                                                                         | 52.9 ms: 1.22x slower                                                                                                 |
| xml_etree_process          | 61.6 ms                                                                                                         | 75.7 ms: 1.23x slower                                                                                                 |
| docutils                   | 2.41 sec                                                                                                        | 2.97 sec: 1.23x slower                                                                                                |
| scimark_monte_carlo        | 64.3 ms                                                                                                         | 79.3 ms: 1.23x slower                                                                                                 |
| connected_components       | 393 ms                                                                                                          | 494 ms: 1.26x slower                                                                                                  |
| crypto_pyaes               | 70.3 ms                                                                                                         | 89.3 ms: 1.27x slower                                                                                                 |
| async_tree_cpu_io_mixed    | 539 ms                                                                                                          | 690 ms: 1.28x slower                                                                                                  |
| meteor_contest             | 100 ms                                                                                                          | 129 ms: 1.29x slower                                                                                                  |
| nbody                      | 97.4 ms                                                                                                         | 126 ms: 1.29x slower                                                                                                  |
| mako                       | 12.1 ms                                                                                                         | 16.0 ms: 1.32x slower                                                                                                 |
| coverage                   | 84.6 ms                                                                                                         | 115 ms: 1.36x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.07x slower                                                                                                          |

Benchmark hidden because not significant (1): async_tree_io

- Geometric mean (including insignificant results): 1.099x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.19x