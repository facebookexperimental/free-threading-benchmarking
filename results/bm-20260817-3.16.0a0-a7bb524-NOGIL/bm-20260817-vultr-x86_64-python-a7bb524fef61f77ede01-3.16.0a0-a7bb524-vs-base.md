# Results vs. base

- fork: python
- ref: a7bb524fef61f77ede01
- machine: linux-x86_64
- commit hash: a7bb524
- commit date: 2026-08-17
- overall geometric mean: 1.110x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260817-3.16.0a0-a7bb524/bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524.json | results/bm-20260817-3.16.0a0-a7bb524-NOGIL/bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                                                          | 298 ms: 1.15x slower                                                                                                  |
| docutils       | 2.35 sec                                                                                                        | 2.94 sec: 1.25x slower                                                                                                |
| html5lib       | 59.8 ms                                                                                                         | 66.2 ms: 1.11x slower                                                                                                 |
| sphinx         | 994 ms                                                                                                          | 1.11 sec: 1.12x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.16x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260817-3.16.0a0-a7bb524/bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524.json | results/bm-20260817-3.16.0a0-a7bb524-NOGIL/bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 759 ms                                                                                                          | 700 ms: 1.08x faster                                                                                                  |
| asyncio_websockets         | 544 ms                                                                                                          | 510 ms: 1.07x faster                                                                                                  |
| async_tree_io              | 723 ms                                                                                                          | 712 ms: 1.02x faster                                                                                                  |
| coroutines                 | 23.6 ms                                                                                                         | 24.6 ms: 1.04x slower                                                                                                 |
| async_tree_memoization_tg  | 364 ms                                                                                                          | 404 ms: 1.11x slower                                                                                                  |
| async_tree_none_tg         | 298 ms                                                                                                          | 337 ms: 1.13x slower                                                                                                  |
| async_tree_memoization     | 376 ms                                                                                                          | 425 ms: 1.13x slower                                                                                                  |
| async_generators           | 345 ms                                                                                                          | 396 ms: 1.15x slower                                                                                                  |
| async_tree_none            | 298 ms                                                                                                          | 343 ms: 1.15x slower                                                                                                  |
| async_tree_cpu_io_mixed_tg | 551 ms                                                                                                          | 681 ms: 1.23x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 533 ms                                                                                                          | 701 ms: 1.31x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260817-3.16.0a0-a7bb524/bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524.json | results/bm-20260817-3.16.0a0-a7bb524-NOGIL/bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 191 ms                                                                                                          | 215 ms: 1.13x slower                                                                                                  |
| float          | 73.1 ms                                                                                                         | 84.3 ms: 1.15x slower                                                                                                 |
| nbody          | 91.1 ms                                                                                                         | 120 ms: 1.32x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.20x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260817-3.16.0a0-a7bb524/bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524.json | results/bm-20260817-3.16.0a0-a7bb524-NOGIL/bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.7 ms                                                                                                         | 20.9 ms: 1.04x faster                                                                                                 |
| regex_dna      | 180 ms                                                                                                          | 181 ms: 1.01x slower                                                                                                  |
| regex_compile  | 149 ms                                                                                                          | 171 ms: 1.15x slower                                                                                                  |
| regex_effbot   | 2.55 ms                                                                                                         | 2.95 ms: 1.16x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                           | 1.06x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260817-3.16.0a0-a7bb524/bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524.json | results/bm-20260817-3.16.0a0-a7bb524-NOGIL/bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 141 ms                                                                                                          | 139 ms: 1.01x faster                                                                                                  |
| tomli_loads          | 1.87 sec                                                                                                        | 1.96 sec: 1.05x slower                                                                                                |
| xml_etree_iterparse  | 90.5 ms                                                                                                         | 95.1 ms: 1.05x slower                                                                                                 |
| json_dumps           | 9.31 ms                                                                                                         | 10.1 ms: 1.08x slower                                                                                                 |
| json_loads           | 27.4 us                                                                                                         | 30.5 us: 1.11x slower                                                                                                 |
| pickle_pure_python   | 300 us                                                                                                          | 337 us: 1.12x slower                                                                                                  |
| xml_etree_generate   | 88.4 ms                                                                                                         | 101 ms: 1.14x slower                                                                                                  |
| unpickle_pure_python | 209 us                                                                                                          | 240 us: 1.15x slower                                                                                                  |
| xml_etree_process    | 62.2 ms                                                                                                         | 75.0 ms: 1.21x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.10x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260817-3.16.0a0-a7bb524/bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524.json | results/bm-20260817-3.16.0a0-a7bb524-NOGIL/bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.6 ms                                                                                                         | 15.7 ms: 1.25x slower                                                                                                 |
| python_startup_no_site | 7.10 ms                                                                                                         | 9.27 ms: 1.31x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.28x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260817-3.16.0a0-a7bb524/bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524.json | results/bm-20260817-3.16.0a0-a7bb524-NOGIL/bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 36.8 ms                                                                                                         | 41.7 ms: 1.13x slower                                                                                                 |
| mako            | 11.9 ms                                                                                                         | 15.8 ms: 1.33x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.23x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20260817-3.16.0a0-a7bb524/bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524.json | results/bm-20260817-3.16.0a0-a7bb524-NOGIL/bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 237 ms                                                                                                          | 6.78 ms: 34.97x faster                                                                                                |
| gc_traversal               | 3.71 ms                                                                                                         | 1.79 ms: 2.07x faster                                                                                                 |
| create_gc_cycles           | 1.64 ms                                                                                                         | 1.38 ms: 1.19x faster                                                                                                 |
| sqlite_synth               | 2.20 us                                                                                                         | 1.95 us: 1.13x faster                                                                                                 |
| async_tree_io_tg           | 759 ms                                                                                                          | 700 ms: 1.08x faster                                                                                                  |
| asyncio_websockets         | 544 ms                                                                                                          | 510 ms: 1.07x faster                                                                                                  |
| regex_v8                   | 21.7 ms                                                                                                         | 20.9 ms: 1.04x faster                                                                                                 |
| async_tree_io              | 723 ms                                                                                                          | 712 ms: 1.02x faster                                                                                                  |
| xml_etree_parse            | 141 ms                                                                                                          | 139 ms: 1.01x faster                                                                                                  |
| regex_dna                  | 180 ms                                                                                                          | 181 ms: 1.01x slower                                                                                                  |
| pathlib                    | 17.7 ms                                                                                                         | 17.9 ms: 1.01x slower                                                                                                 |
| bpe_tokeniser              | 4.24 sec                                                                                                        | 4.38 sec: 1.03x slower                                                                                                |
| coroutines                 | 23.6 ms                                                                                                         | 24.6 ms: 1.04x slower                                                                                                 |
| pycparser                  | 1.13 sec                                                                                                        | 1.18 sec: 1.05x slower                                                                                                |
| tomli_loads                | 1.87 sec                                                                                                        | 1.96 sec: 1.05x slower                                                                                                |
| xml_etree_iterparse        | 90.5 ms                                                                                                         | 95.1 ms: 1.05x slower                                                                                                 |
| dulwich_log                | 67.2 ms                                                                                                         | 70.7 ms: 1.05x slower                                                                                                 |
| json_dumps                 | 9.31 ms                                                                                                         | 10.1 ms: 1.08x slower                                                                                                 |
| scimark_lu                 | 119 ms                                                                                                          | 129 ms: 1.09x slower                                                                                                  |
| k_core                     | 2.07 sec                                                                                                        | 2.27 sec: 1.09x slower                                                                                                |
| json                       | 4.91 ms                                                                                                         | 5.38 ms: 1.10x slower                                                                                                 |
| scimark_fft                | 311 ms                                                                                                          | 342 ms: 1.10x slower                                                                                                  |
| many_optionals             | 913 us                                                                                                          | 1.01 ms: 1.10x slower                                                                                                 |
| bench_thread_pool          | 1.35 ms                                                                                                         | 1.49 ms: 1.10x slower                                                                                                 |
| html5lib                   | 59.8 ms                                                                                                         | 66.2 ms: 1.11x slower                                                                                                 |
| telco                      | 160 ms                                                                                                          | 178 ms: 1.11x slower                                                                                                  |
| async_tree_memoization_tg  | 364 ms                                                                                                          | 404 ms: 1.11x slower                                                                                                  |
| json_loads                 | 27.4 us                                                                                                         | 30.5 us: 1.11x slower                                                                                                 |
| sqlglot_v2_optimize        | 52.0 ms                                                                                                         | 57.9 ms: 1.11x slower                                                                                                 |
| logging_silent             | 95.9 ns                                                                                                         | 107 ns: 1.12x slower                                                                                                  |
| sphinx                     | 994 ms                                                                                                          | 1.11 sec: 1.12x slower                                                                                                |
| pickle_pure_python         | 300 us                                                                                                          | 337 us: 1.12x slower                                                                                                  |
| pidigits                   | 191 ms                                                                                                          | 215 ms: 1.13x slower                                                                                                  |
| sqlglot_v2_normalize       | 102 ms                                                                                                          | 115 ms: 1.13x slower                                                                                                  |
| sympy_expand               | 479 ms                                                                                                          | 540 ms: 1.13x slower                                                                                                  |
| async_tree_none_tg         | 298 ms                                                                                                          | 337 ms: 1.13x slower                                                                                                  |
| pprint_safe_repr           | 737 ms                                                                                                          | 832 ms: 1.13x slower                                                                                                  |
| async_tree_memoization     | 376 ms                                                                                                          | 425 ms: 1.13x slower                                                                                                  |
| subparsers                 | 9.07 ms                                                                                                         | 10.3 ms: 1.13x slower                                                                                                 |
| deltablue                  | 3.27 ms                                                                                                         | 3.70 ms: 1.13x slower                                                                                                 |
| django_template            | 36.8 ms                                                                                                         | 41.7 ms: 1.13x slower                                                                                                 |
| comprehensions             | 15.7 us                                                                                                         | 17.9 us: 1.14x slower                                                                                                 |
| logging_simple             | 6.14 us                                                                                                         | 6.98 us: 1.14x slower                                                                                                 |
| xml_etree_generate         | 88.4 ms                                                                                                         | 101 ms: 1.14x slower                                                                                                  |
| chaos                      | 53.2 ms                                                                                                         | 60.7 ms: 1.14x slower                                                                                                 |
| sympy_sum                  | 159 ms                                                                                                          | 182 ms: 1.14x slower                                                                                                  |
| sympy_str                  | 282 ms                                                                                                          | 321 ms: 1.14x slower                                                                                                  |
| scimark_sparse_mat_mult    | 4.55 ms                                                                                                         | 5.19 ms: 1.14x slower                                                                                                 |
| sympy_integrate            | 19.3 ms                                                                                                         | 22.0 ms: 1.14x slower                                                                                                 |
| pylint                     | 115 ms                                                                                                          | 131 ms: 1.14x slower                                                                                                  |
| unpickle_pure_python       | 209 us                                                                                                          | 240 us: 1.15x slower                                                                                                  |
| mdp                        | 1.14 sec                                                                                                        | 1.31 sec: 1.15x slower                                                                                                |
| pprint_pformat             | 1.50 sec                                                                                                        | 1.72 sec: 1.15x slower                                                                                                |
| regex_compile              | 149 ms                                                                                                          | 171 ms: 1.15x slower                                                                                                  |
| async_generators           | 345 ms                                                                                                          | 396 ms: 1.15x slower                                                                                                  |
| logging_format             | 7.02 us                                                                                                         | 8.07 us: 1.15x slower                                                                                                 |
| 2to3                       | 259 ms                                                                                                          | 298 ms: 1.15x slower                                                                                                  |
| async_tree_none            | 298 ms                                                                                                          | 343 ms: 1.15x slower                                                                                                  |
| hexiom                     | 5.68 ms                                                                                                         | 6.55 ms: 1.15x slower                                                                                                 |
| scimark_sor                | 105 ms                                                                                                          | 121 ms: 1.15x slower                                                                                                  |
| float                      | 73.1 ms                                                                                                         | 84.3 ms: 1.15x slower                                                                                                 |
| regex_effbot               | 2.55 ms                                                                                                         | 2.95 ms: 1.16x slower                                                                                                 |
| deepcopy_reduce            | 2.58 us                                                                                                         | 2.99 us: 1.16x slower                                                                                                 |
| pyflate                    | 400 ms                                                                                                          | 464 ms: 1.16x slower                                                                                                  |
| go                         | 103 ms                                                                                                          | 120 ms: 1.17x slower                                                                                                  |
| richards                   | 44.9 ms                                                                                                         | 52.4 ms: 1.17x slower                                                                                                 |
| deepcopy                   | 232 us                                                                                                          | 272 us: 1.17x slower                                                                                                  |
| spectral_norm              | 90.8 ms                                                                                                         | 106 ms: 1.17x slower                                                                                                  |
| richards_super             | 51.2 ms                                                                                                         | 60.0 ms: 1.17x slower                                                                                                 |
| raytrace                   | 249 ms                                                                                                          | 293 ms: 1.18x slower                                                                                                  |
| sqlglot_v2_transpile       | 1.47 ms                                                                                                         | 1.73 ms: 1.18x slower                                                                                                 |
| thrift                     | 787 us                                                                                                          | 935 us: 1.19x slower                                                                                                  |
| nqueens                    | 73.8 ms                                                                                                         | 88.8 ms: 1.20x slower                                                                                                 |
| xml_etree_process          | 62.2 ms                                                                                                         | 75.0 ms: 1.21x slower                                                                                                 |
| sqlglot_v2_parse           | 1.17 ms                                                                                                         | 1.41 ms: 1.21x slower                                                                                                 |
| deepcopy_memo              | 26.4 us                                                                                                         | 31.9 us: 1.21x slower                                                                                                 |
| generators                 | 27.6 ms                                                                                                         | 33.5 ms: 1.22x slower                                                                                                 |
| async_tree_cpu_io_mixed_tg | 551 ms                                                                                                          | 681 ms: 1.23x slower                                                                                                  |
| typing_runtime_protocols   | 120 us                                                                                                          | 149 us: 1.24x slower                                                                                                  |
| scimark_monte_carlo        | 63.1 ms                                                                                                         | 78.1 ms: 1.24x slower                                                                                                 |
| meteor_contest             | 101 ms                                                                                                          | 125 ms: 1.24x slower                                                                                                  |
| shortest_path              | 434 ms                                                                                                          | 539 ms: 1.24x slower                                                                                                  |
| fannkuch                   | 374 ms                                                                                                          | 464 ms: 1.24x slower                                                                                                  |
| python_startup             | 12.6 ms                                                                                                         | 15.7 ms: 1.25x slower                                                                                                 |
| docutils                   | 2.35 sec                                                                                                        | 2.94 sec: 1.25x slower                                                                                                |
| connected_components       | 393 ms                                                                                                          | 494 ms: 1.26x slower                                                                                                  |
| python_startup_no_site     | 7.10 ms                                                                                                         | 9.27 ms: 1.31x slower                                                                                                 |
| async_tree_cpu_io_mixed    | 533 ms                                                                                                          | 701 ms: 1.31x slower                                                                                                  |
| nbody                      | 91.1 ms                                                                                                         | 120 ms: 1.32x slower                                                                                                  |
| mako                       | 11.9 ms                                                                                                         | 15.8 ms: 1.33x slower                                                                                                 |
| crypto_pyaes               | 66.9 ms                                                                                                         | 89.3 ms: 1.33x slower                                                                                                 |
| coverage                   | 84.2 ms                                                                                                         | 115 ms: 1.36x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.08x slower                                                                                                          |

- Geometric mean (including insignificant results): 1.110x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.13x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 1.18x