# Results vs. base

- fork: python
- ref: a5be0d81cb74fabe563b
- machine: linux-x86_64
- commit hash: a5be0d8
- commit date: 2026-06-30
- overall geometric mean: 1.107x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260630-3.16.0a0-a5be0d8/bm-20260630-vultr-x86_64-python-a5be0d81cb74fabe563b-3.16.0a0-a5be0d8.json | results/bm-20260630-3.16.0a0-a5be0d8-NOGIL/bm-20260630-vultr-x86_64-python-a5be0d81cb74fabe563b-3.16.0a0-a5be0d8.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 258 ms                                                                                                          | 294 ms: 1.14x slower                                                                                                  |
| docutils       | 2.37 sec                                                                                                        | 2.95 sec: 1.24x slower                                                                                                |
| html5lib       | 59.4 ms                                                                                                         | 65.9 ms: 1.11x slower                                                                                                 |
| sphinx         | 973 ms                                                                                                          | 1.11 sec: 1.14x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.16x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260630-3.16.0a0-a5be0d8/bm-20260630-vultr-x86_64-python-a5be0d81cb74fabe563b-3.16.0a0-a5be0d8.json | results/bm-20260630-3.16.0a0-a5be0d8-NOGIL/bm-20260630-vultr-x86_64-python-a5be0d81cb74fabe563b-3.16.0a0-a5be0d8.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 753 ms                                                                                                          | 684 ms: 1.10x faster                                                                                                  |
| asyncio_websockets         | 544 ms                                                                                                          | 514 ms: 1.06x faster                                                                                                  |
| async_tree_io              | 717 ms                                                                                                          | 703 ms: 1.02x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 552 ms                                                                                                          | 581 ms: 1.05x slower                                                                                                  |
| coroutines                 | 23.8 ms                                                                                                         | 25.1 ms: 1.05x slower                                                                                                 |
| async_tree_memoization_tg  | 362 ms                                                                                                          | 394 ms: 1.09x slower                                                                                                  |
| async_tree_none_tg         | 296 ms                                                                                                          | 324 ms: 1.09x slower                                                                                                  |
| async_tree_memoization     | 374 ms                                                                                                          | 418 ms: 1.12x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 537 ms                                                                                                          | 601 ms: 1.12x slower                                                                                                  |
| async_generators           | 339 ms                                                                                                          | 388 ms: 1.14x slower                                                                                                  |
| async_tree_none            | 291 ms                                                                                                          | 340 ms: 1.17x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.06x slower                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260630-3.16.0a0-a5be0d8/bm-20260630-vultr-x86_64-python-a5be0d81cb74fabe563b-3.16.0a0-a5be0d8.json | results/bm-20260630-3.16.0a0-a5be0d8-NOGIL/bm-20260630-vultr-x86_64-python-a5be0d81cb74fabe563b-3.16.0a0-a5be0d8.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 184 ms                                                                                                          | 180 ms: 1.02x faster                                                                                                  |
| float          | 73.7 ms                                                                                                         | 86.3 ms: 1.17x slower                                                                                                 |
| nbody          | 93.8 ms                                                                                                         | 127 ms: 1.36x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.16x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260630-3.16.0a0-a5be0d8/bm-20260630-vultr-x86_64-python-a5be0d81cb74fabe563b-3.16.0a0-a5be0d8.json | results/bm-20260630-3.16.0a0-a5be0d8-NOGIL/bm-20260630-vultr-x86_64-python-a5be0d81cb74fabe563b-3.16.0a0-a5be0d8.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.9 ms                                                                                                         | 20.5 ms: 1.07x faster                                                                                                 |
| regex_dna      | 178 ms                                                                                                          | 182 ms: 1.02x slower                                                                                                  |
| regex_compile  | 147 ms                                                                                                          | 167 ms: 1.14x slower                                                                                                  |
| regex_effbot   | 2.54 ms                                                                                                         | 2.92 ms: 1.15x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                           | 1.06x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260630-3.16.0a0-a5be0d8/bm-20260630-vultr-x86_64-python-a5be0d81cb74fabe563b-3.16.0a0-a5be0d8.json | results/bm-20260630-3.16.0a0-a5be0d8-NOGIL/bm-20260630-vultr-x86_64-python-a5be0d81cb74fabe563b-3.16.0a0-a5be0d8.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 143 ms                                                                                                          | 141 ms: 1.01x faster                                                                                                  |
| json_dumps           | 9.95 ms                                                                                                         | 10.5 ms: 1.05x slower                                                                                                 |
| xml_etree_iterparse  | 88.8 ms                                                                                                         | 95.0 ms: 1.07x slower                                                                                                 |
| tomli_loads          | 1.80 sec                                                                                                        | 1.94 sec: 1.08x slower                                                                                                |
| pickle_pure_python   | 308 us                                                                                                          | 335 us: 1.09x slower                                                                                                  |
| json_loads           | 27.0 us                                                                                                         | 30.1 us: 1.11x slower                                                                                                 |
| unpickle_pure_python | 210 us                                                                                                          | 235 us: 1.12x slower                                                                                                  |
| xml_etree_generate   | 85.6 ms                                                                                                         | 98.7 ms: 1.15x slower                                                                                                 |
| xml_etree_process    | 60.5 ms                                                                                                         | 73.9 ms: 1.22x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.10x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260630-3.16.0a0-a5be0d8/bm-20260630-vultr-x86_64-python-a5be0d81cb74fabe563b-3.16.0a0-a5be0d8.json | results/bm-20260630-3.16.0a0-a5be0d8-NOGIL/bm-20260630-vultr-x86_64-python-a5be0d81cb74fabe563b-3.16.0a0-a5be0d8.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.3 ms                                                                                                         | 15.4 ms: 1.25x slower                                                                                                 |
| python_startup_no_site | 6.94 ms                                                                                                         | 9.14 ms: 1.32x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.28x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260630-3.16.0a0-a5be0d8/bm-20260630-vultr-x86_64-python-a5be0d81cb74fabe563b-3.16.0a0-a5be0d8.json | results/bm-20260630-3.16.0a0-a5be0d8-NOGIL/bm-20260630-vultr-x86_64-python-a5be0d81cb74fabe563b-3.16.0a0-a5be0d8.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 35.1 ms                                                                                                         | 40.2 ms: 1.14x slower                                                                                                 |
| mako            | 12.1 ms                                                                                                         | 16.2 ms: 1.34x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.24x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20260630-3.16.0a0-a5be0d8/bm-20260630-vultr-x86_64-python-a5be0d81cb74fabe563b-3.16.0a0-a5be0d8.json | results/bm-20260630-3.16.0a0-a5be0d8-NOGIL/bm-20260630-vultr-x86_64-python-a5be0d81cb74fabe563b-3.16.0a0-a5be0d8.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 216 ms                                                                                                          | 6.91 ms: 31.26x faster                                                                                                |
| gc_traversal               | 3.79 ms                                                                                                         | 1.77 ms: 2.14x faster                                                                                                 |
| create_gc_cycles           | 1.65 ms                                                                                                         | 1.37 ms: 1.20x faster                                                                                                 |
| sqlite_synth               | 2.21 us                                                                                                         | 1.94 us: 1.14x faster                                                                                                 |
| async_tree_io_tg           | 753 ms                                                                                                          | 684 ms: 1.10x faster                                                                                                  |
| regex_v8                   | 21.9 ms                                                                                                         | 20.5 ms: 1.07x faster                                                                                                 |
| asyncio_websockets         | 544 ms                                                                                                          | 514 ms: 1.06x faster                                                                                                  |
| async_tree_io              | 717 ms                                                                                                          | 703 ms: 1.02x faster                                                                                                  |
| pidigits                   | 184 ms                                                                                                          | 180 ms: 1.02x faster                                                                                                  |
| xml_etree_parse            | 143 ms                                                                                                          | 141 ms: 1.01x faster                                                                                                  |
| pycparser                  | 1.11 sec                                                                                                        | 1.12 sec: 1.01x slower                                                                                                |
| pathlib                    | 17.6 ms                                                                                                         | 17.8 ms: 1.01x slower                                                                                                 |
| regex_dna                  | 178 ms                                                                                                          | 182 ms: 1.02x slower                                                                                                  |
| dulwich_log                | 68.9 ms                                                                                                         | 70.8 ms: 1.03x slower                                                                                                 |
| bpe_tokeniser              | 4.20 sec                                                                                                        | 4.35 sec: 1.04x slower                                                                                                |
| logging_silent             | 99.6 ns                                                                                                         | 105 ns: 1.05x slower                                                                                                  |
| async_tree_cpu_io_mixed_tg | 552 ms                                                                                                          | 581 ms: 1.05x slower                                                                                                  |
| coroutines                 | 23.8 ms                                                                                                         | 25.1 ms: 1.05x slower                                                                                                 |
| json_dumps                 | 9.95 ms                                                                                                         | 10.5 ms: 1.05x slower                                                                                                 |
| xml_etree_iterparse        | 88.8 ms                                                                                                         | 95.0 ms: 1.07x slower                                                                                                 |
| json                       | 4.91 ms                                                                                                         | 5.27 ms: 1.07x slower                                                                                                 |
| k_core                     | 2.09 sec                                                                                                        | 2.24 sec: 1.07x slower                                                                                                |
| tomli_loads                | 1.80 sec                                                                                                        | 1.94 sec: 1.08x slower                                                                                                |
| async_tree_memoization_tg  | 362 ms                                                                                                          | 394 ms: 1.09x slower                                                                                                  |
| pickle_pure_python         | 308 us                                                                                                          | 335 us: 1.09x slower                                                                                                  |
| async_tree_none_tg         | 296 ms                                                                                                          | 324 ms: 1.09x slower                                                                                                  |
| telco                      | 158 ms                                                                                                          | 174 ms: 1.10x slower                                                                                                  |
| bench_thread_pool          | 1.33 ms                                                                                                         | 1.47 ms: 1.11x slower                                                                                                 |
| html5lib                   | 59.4 ms                                                                                                         | 65.9 ms: 1.11x slower                                                                                                 |
| many_optionals             | 907 us                                                                                                          | 1.01 ms: 1.11x slower                                                                                                 |
| json_loads                 | 27.0 us                                                                                                         | 30.1 us: 1.11x slower                                                                                                 |
| pprint_safe_repr           | 716 ms                                                                                                          | 799 ms: 1.12x slower                                                                                                  |
| async_tree_memoization     | 374 ms                                                                                                          | 418 ms: 1.12x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 537 ms                                                                                                          | 601 ms: 1.12x slower                                                                                                  |
| unpickle_pure_python       | 210 us                                                                                                          | 235 us: 1.12x slower                                                                                                  |
| scimark_fft                | 318 ms                                                                                                          | 359 ms: 1.13x slower                                                                                                  |
| sqlglot_v2_optimize        | 50.7 ms                                                                                                         | 57.3 ms: 1.13x slower                                                                                                 |
| comprehensions             | 15.7 us                                                                                                         | 17.7 us: 1.13x slower                                                                                                 |
| scimark_lu                 | 114 ms                                                                                                          | 129 ms: 1.13x slower                                                                                                  |
| pprint_pformat             | 1.46 sec                                                                                                        | 1.66 sec: 1.13x slower                                                                                                |
| regex_compile              | 147 ms                                                                                                          | 167 ms: 1.14x slower                                                                                                  |
| deepcopy_reduce            | 2.51 us                                                                                                         | 2.86 us: 1.14x slower                                                                                                 |
| sphinx                     | 973 ms                                                                                                          | 1.11 sec: 1.14x slower                                                                                                |
| 2to3                       | 258 ms                                                                                                          | 294 ms: 1.14x slower                                                                                                  |
| sympy_expand               | 457 ms                                                                                                          | 523 ms: 1.14x slower                                                                                                  |
| async_generators           | 339 ms                                                                                                          | 388 ms: 1.14x slower                                                                                                  |
| deepcopy                   | 229 us                                                                                                          | 262 us: 1.14x slower                                                                                                  |
| django_template            | 35.1 ms                                                                                                         | 40.2 ms: 1.14x slower                                                                                                 |
| deltablue                  | 3.25 ms                                                                                                         | 3.72 ms: 1.14x slower                                                                                                 |
| sqlglot_v2_normalize       | 99.7 ms                                                                                                         | 114 ms: 1.14x slower                                                                                                  |
| sympy_integrate            | 18.9 ms                                                                                                         | 21.7 ms: 1.15x slower                                                                                                 |
| regex_effbot               | 2.54 ms                                                                                                         | 2.92 ms: 1.15x slower                                                                                                 |
| deepcopy_memo              | 26.5 us                                                                                                         | 30.6 us: 1.15x slower                                                                                                 |
| subparsers                 | 9.21 ms                                                                                                         | 10.6 ms: 1.15x slower                                                                                                 |
| chaos                      | 54.3 ms                                                                                                         | 62.6 ms: 1.15x slower                                                                                                 |
| xml_etree_generate         | 85.6 ms                                                                                                         | 98.7 ms: 1.15x slower                                                                                                 |
| sympy_str                  | 271 ms                                                                                                          | 312 ms: 1.15x slower                                                                                                  |
| mdp                        | 1.13 sec                                                                                                        | 1.31 sec: 1.16x slower                                                                                                |
| pylint                     | 114 ms                                                                                                          | 131 ms: 1.16x slower                                                                                                  |
| pyflate                    | 398 ms                                                                                                          | 461 ms: 1.16x slower                                                                                                  |
| thrift                     | 781 us                                                                                                          | 905 us: 1.16x slower                                                                                                  |
| sympy_sum                  | 155 ms                                                                                                          | 181 ms: 1.16x slower                                                                                                  |
| async_tree_none            | 291 ms                                                                                                          | 340 ms: 1.17x slower                                                                                                  |
| scimark_sor                | 107 ms                                                                                                          | 125 ms: 1.17x slower                                                                                                  |
| float                      | 73.7 ms                                                                                                         | 86.3 ms: 1.17x slower                                                                                                 |
| go                         | 103 ms                                                                                                          | 121 ms: 1.17x slower                                                                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                                                                         | 5.53 ms: 1.17x slower                                                                                                 |
| hexiom                     | 5.61 ms                                                                                                         | 6.60 ms: 1.18x slower                                                                                                 |
| sqlglot_v2_transpile       | 1.46 ms                                                                                                         | 1.72 ms: 1.18x slower                                                                                                 |
| nqueens                    | 74.4 ms                                                                                                         | 87.7 ms: 1.18x slower                                                                                                 |
| logging_simple             | 5.90 us                                                                                                         | 7.01 us: 1.19x slower                                                                                                 |
| logging_format             | 6.64 us                                                                                                         | 7.91 us: 1.19x slower                                                                                                 |
| generators                 | 27.9 ms                                                                                                         | 33.5 ms: 1.20x slower                                                                                                 |
| fannkuch                   | 380 ms                                                                                                          | 457 ms: 1.20x slower                                                                                                  |
| spectral_norm              | 92.9 ms                                                                                                         | 112 ms: 1.21x slower                                                                                                  |
| raytrace                   | 251 ms                                                                                                          | 305 ms: 1.22x slower                                                                                                  |
| shortest_path              | 438 ms                                                                                                          | 534 ms: 1.22x slower                                                                                                  |
| xml_etree_process          | 60.5 ms                                                                                                         | 73.9 ms: 1.22x slower                                                                                                 |
| sqlglot_v2_parse           | 1.14 ms                                                                                                         | 1.39 ms: 1.22x slower                                                                                                 |
| typing_runtime_protocols   | 116 us                                                                                                          | 143 us: 1.23x slower                                                                                                  |
| meteor_contest             | 101 ms                                                                                                          | 124 ms: 1.23x slower                                                                                                  |
| connected_components       | 396 ms                                                                                                          | 489 ms: 1.24x slower                                                                                                  |
| richards_super             | 48.1 ms                                                                                                         | 59.6 ms: 1.24x slower                                                                                                 |
| richards                   | 42.0 ms                                                                                                         | 52.1 ms: 1.24x slower                                                                                                 |
| docutils                   | 2.37 sec                                                                                                        | 2.95 sec: 1.24x slower                                                                                                |
| python_startup             | 12.3 ms                                                                                                         | 15.4 ms: 1.25x slower                                                                                                 |
| scimark_monte_carlo        | 63.4 ms                                                                                                         | 80.1 ms: 1.26x slower                                                                                                 |
| crypto_pyaes               | 69.1 ms                                                                                                         | 88.9 ms: 1.29x slower                                                                                                 |
| python_startup_no_site     | 6.94 ms                                                                                                         | 9.14 ms: 1.32x slower                                                                                                 |
| mako                       | 12.1 ms                                                                                                         | 16.2 ms: 1.34x slower                                                                                                 |
| nbody                      | 93.8 ms                                                                                                         | 127 ms: 1.36x slower                                                                                                  |
| coverage                   | 81.8 ms                                                                                                         | 113 ms: 1.38x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.08x slower                                                                                                          |

- Geometric mean (including insignificant results): 1.107x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.13x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.18x