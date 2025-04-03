# Results vs. base

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: 275056a
- commit date: 2025-04-03
- overall geometric mean: 1.006x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6+-b3e3cc0 | bm-20250403-macm4pro-arm64-python-main-3.14.0a6+-275056a |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------:|
| 2to3           | 122 ms                                                                   | 120 ms: 1.02x faster                                     |
| docutils       | 1.01 sec                                                                 | 1.00 sec: 1.01x faster                                   |
| html5lib       | 23.6 ms                                                                  | 23.4 ms: 1.01x faster                                    |
| sphinx         | 425 ms                                                                   | 423 ms: 1.00x faster                                     |
| Geometric mean | (ref)                                                                    | 1.01x faster                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6+-b3e3cc0 | bm-20250403-macm4pro-arm64-python-main-3.14.0a6+-275056a |
|----------------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------:|
| coroutines                       | 10.6 ms                                                                  | 10.2 ms: 1.04x faster                                    |
| async_generators                 | 181 ms                                                                   | 178 ms: 1.02x faster                                     |
| async_tree_eager_io_tg           | 199 ms                                                                   | 196 ms: 1.02x faster                                     |
| async_tree_cpu_io_mixed_tg       | 235 ms                                                                   | 231 ms: 1.02x faster                                     |
| async_tree_eager_cpu_io_mixed_tg | 225 ms                                                                   | 222 ms: 1.02x faster                                     |
| async_tree_cpu_io_mixed          | 244 ms                                                                   | 241 ms: 1.01x faster                                     |
| async_tree_eager_cpu_io_mixed    | 223 ms                                                                   | 220 ms: 1.01x faster                                     |
| async_tree_none                  | 103 ms                                                                   | 102 ms: 1.01x faster                                     |
| async_tree_eager_tg              | 79.2 ms                                                                  | 78.3 ms: 1.01x faster                                    |
| asyncio_websockets               | 189 ms                                                                   | 187 ms: 1.01x faster                                     |
| async_tree_eager_io              | 210 ms                                                                   | 209 ms: 1.01x faster                                     |
| async_tree_none_tg               | 88.2 ms                                                                  | 87.6 ms: 1.01x faster                                    |
| async_tree_eager_memoization_tg  | 114 ms                                                                   | 113 ms: 1.01x faster                                     |
| async_tree_memoization           | 133 ms                                                                   | 132 ms: 1.01x faster                                     |
| async_tree_eager_memoization     | 113 ms                                                                   | 112 ms: 1.01x faster                                     |
| async_tree_io                    | 214 ms                                                                   | 213 ms: 1.01x faster                                     |
| async_tree_io_tg                 | 200 ms                                                                   | 200 ms: 1.00x faster                                     |
| Geometric mean                   | (ref)                                                                    | 1.01x faster                                             |

Benchmark hidden because not significant (2): async_tree_memoization_tg, async_tree_eager

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6+-b3e3cc0 | bm-20250403-macm4pro-arm64-python-main-3.14.0a6+-275056a |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------:|
| pidigits       | 165 ms                                                                   | 163 ms: 1.01x faster                                     |
| nbody          | 54.3 ms                                                                  | 53.8 ms: 1.01x faster                                    |
| Geometric mean | (ref)                                                                    | 1.01x faster                                             |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6+-b3e3cc0 | bm-20250403-macm4pro-arm64-python-main-3.14.0a6+-275056a |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------:|
| regex_effbot   | 1.50 ms                                                                  | 1.49 ms: 1.01x faster                                    |
| regex_dna      | 101 ms                                                                   | 101 ms: 1.01x faster                                     |
| regex_compile  | 53.8 ms                                                                  | 53.6 ms: 1.00x faster                                    |
| Geometric mean | (ref)                                                                    | 1.00x faster                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6+-b3e3cc0 | bm-20250403-macm4pro-arm64-python-main-3.14.0a6+-275056a |
|----------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------:|
| pickle_pure_python   | 153 us                                                                   | 151 us: 1.01x faster                                     |
| tomli_loads          | 976 ms                                                                   | 965 ms: 1.01x faster                                     |
| unpickle_pure_python | 108 us                                                                   | 107 us: 1.01x faster                                     |
| xml_etree_process    | 26.9 ms                                                                  | 26.7 ms: 1.01x faster                                    |
| xml_etree_generate   | 36.9 ms                                                                  | 36.8 ms: 1.00x faster                                    |
| xml_etree_parse      | 56.1 ms                                                                  | 57.5 ms: 1.03x slower                                    |
| xml_etree_iterparse  | 36.7 ms                                                                  | 38.0 ms: 1.04x slower                                    |
| Geometric mean       | (ref)                                                                    | 1.00x slower                                             |

Benchmark hidden because not significant (2): json_loads, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6+-b3e3cc0 | bm-20250403-macm4pro-arm64-python-main-3.14.0a6+-275056a |
|------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------:|
| python_startup_no_site | 7.58 ms                                                                  | 7.52 ms: 1.01x faster                                    |
| python_startup         | 9.53 ms                                                                  | 9.47 ms: 1.01x faster                                    |
| Geometric mean         | (ref)                                                                    | 1.01x faster                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6+-b3e3cc0 | bm-20250403-macm4pro-arm64-python-main-3.14.0a6+-275056a |
|-----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------:|
| django_template | 17.0 ms                                                                  | 16.7 ms: 1.02x faster                                    |
| genshi_text     | 11.5 ms                                                                  | 11.4 ms: 1.01x faster                                    |
| genshi_xml      | 23.6 ms                                                                  | 23.7 ms: 1.00x slower                                    |
| mako            | 5.58 ms                                                                  | 5.64 ms: 1.01x slower                                    |
| Geometric mean  | (ref)                                                                    | 1.00x faster                                             |

All benchmarks:
===============

| Benchmark                        | bm-20250402-macm4pro-arm64-python-b3e3cc054c2c7718c0ad-3.14.0a6+-b3e3cc0 | bm-20250403-macm4pro-arm64-python-main-3.14.0a6+-275056a |
|----------------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------:|
| logging_silent                   | 49.2 ns                                                                  | 46.9 ns: 1.05x faster                                    |
| coroutines                       | 10.6 ms                                                                  | 10.2 ms: 1.04x faster                                    |
| dulwich_log                      | 19.0 ms                                                                  | 18.4 ms: 1.03x faster                                    |
| meteor_contest                   | 57.1 ms                                                                  | 55.6 ms: 1.03x faster                                    |
| many_optionals                   | 246 us                                                                   | 240 us: 1.02x faster                                     |
| pprint_pformat                   | 752 ms                                                                   | 737 ms: 1.02x faster                                     |
| 2to3                             | 122 ms                                                                   | 120 ms: 1.02x faster                                     |
| async_generators                 | 181 ms                                                                   | 178 ms: 1.02x faster                                     |
| django_template                  | 17.0 ms                                                                  | 16.7 ms: 1.02x faster                                    |
| subparsers                       | 8.90 ms                                                                  | 8.75 ms: 1.02x faster                                    |
| async_tree_eager_io_tg           | 199 ms                                                                   | 196 ms: 1.02x faster                                     |
| async_tree_cpu_io_mixed_tg       | 235 ms                                                                   | 231 ms: 1.02x faster                                     |
| async_tree_eager_cpu_io_mixed_tg | 225 ms                                                                   | 222 ms: 1.02x faster                                     |
| bench_mp_pool                    | 42.1 ms                                                                  | 41.4 ms: 1.02x faster                                    |
| sqlglot_v2_normalize             | 50.2 ms                                                                  | 49.5 ms: 1.02x faster                                    |
| async_tree_cpu_io_mixed          | 244 ms                                                                   | 241 ms: 1.01x faster                                     |
| chaos                            | 29.5 ms                                                                  | 29.1 ms: 1.01x faster                                    |
| logging_format                   | 2.87 us                                                                  | 2.84 us: 1.01x faster                                    |
| sqlglot_v2_optimize              | 24.8 ms                                                                  | 24.5 ms: 1.01x faster                                    |
| async_tree_eager_cpu_io_mixed    | 223 ms                                                                   | 220 ms: 1.01x faster                                     |
| async_tree_none                  | 103 ms                                                                   | 102 ms: 1.01x faster                                     |
| deepcopy                         | 125 us                                                                   | 124 us: 1.01x faster                                     |
| pickle_pure_python               | 153 us                                                                   | 151 us: 1.01x faster                                     |
| async_tree_eager_tg              | 79.2 ms                                                                  | 78.3 ms: 1.01x faster                                    |
| go                               | 63.5 ms                                                                  | 62.8 ms: 1.01x faster                                    |
| tomli_loads                      | 976 ms                                                                   | 965 ms: 1.01x faster                                     |
| generators                       | 19.1 ms                                                                  | 18.8 ms: 1.01x faster                                    |
| sqlalchemy_declarative           | 50.8 ms                                                                  | 50.2 ms: 1.01x faster                                    |
| pprint_safe_repr                 | 369 ms                                                                   | 365 ms: 1.01x faster                                     |
| sympy_sum                        | 62.3 ms                                                                  | 61.6 ms: 1.01x faster                                    |
| pidigits                         | 165 ms                                                                   | 163 ms: 1.01x faster                                     |
| comprehensions                   | 8.74 us                                                                  | 8.65 us: 1.01x faster                                    |
| pycparser                        | 473 ms                                                                   | 468 ms: 1.01x faster                                     |
| html5lib                         | 23.6 ms                                                                  | 23.4 ms: 1.01x faster                                    |
| regex_effbot                     | 1.50 ms                                                                  | 1.49 ms: 1.01x faster                                    |
| scimark_monte_carlo              | 33.4 ms                                                                  | 33.1 ms: 1.01x faster                                    |
| sympy_str                        | 112 ms                                                                   | 111 ms: 1.01x faster                                     |
| docutils                         | 1.01 sec                                                                 | 1.00 sec: 1.01x faster                                   |
| asyncio_websockets               | 189 ms                                                                   | 187 ms: 1.01x faster                                     |
| async_tree_eager_io              | 210 ms                                                                   | 209 ms: 1.01x faster                                     |
| scimark_sor                      | 55.4 ms                                                                  | 54.9 ms: 1.01x faster                                    |
| crypto_pyaes                     | 41.4 ms                                                                  | 41.0 ms: 1.01x faster                                    |
| nbody                            | 54.3 ms                                                                  | 53.8 ms: 1.01x faster                                    |
| hexiom                           | 3.18 ms                                                                  | 3.15 ms: 1.01x faster                                    |
| regex_dna                        | 101 ms                                                                   | 101 ms: 1.01x faster                                     |
| richards_super                   | 28.3 ms                                                                  | 28.1 ms: 1.01x faster                                    |
| async_tree_none_tg               | 88.2 ms                                                                  | 87.6 ms: 1.01x faster                                    |
| unpickle_pure_python             | 108 us                                                                   | 107 us: 1.01x faster                                     |
| async_tree_eager_memoization_tg  | 114 ms                                                                   | 113 ms: 1.01x faster                                     |
| async_tree_memoization           | 133 ms                                                                   | 132 ms: 1.01x faster                                     |
| raytrace                         | 132 ms                                                                   | 131 ms: 1.01x faster                                     |
| python_startup_no_site           | 7.58 ms                                                                  | 7.52 ms: 1.01x faster                                    |
| sympy_integrate                  | 8.22 ms                                                                  | 8.17 ms: 1.01x faster                                    |
| async_tree_eager_memoization     | 113 ms                                                                   | 112 ms: 1.01x faster                                     |
| deepcopy_reduce                  | 1.29 us                                                                  | 1.28 us: 1.01x faster                                    |
| python_startup                   | 9.53 ms                                                                  | 9.47 ms: 1.01x faster                                    |
| spectral_norm                    | 51.3 ms                                                                  | 51.0 ms: 1.01x faster                                    |
| sqlalchemy_imperative            | 5.77 ms                                                                  | 5.74 ms: 1.01x faster                                    |
| genshi_text                      | 11.5 ms                                                                  | 11.4 ms: 1.01x faster                                    |
| sympy_expand                     | 191 ms                                                                   | 190 ms: 1.01x faster                                     |
| async_tree_io                    | 214 ms                                                                   | 213 ms: 1.01x faster                                     |
| xml_etree_process                | 26.9 ms                                                                  | 26.7 ms: 1.01x faster                                    |
| sphinx                           | 425 ms                                                                   | 423 ms: 1.00x faster                                     |
| regex_compile                    | 53.8 ms                                                                  | 53.6 ms: 1.00x faster                                    |
| scimark_sparse_mat_mult          | 2.13 ms                                                                  | 2.12 ms: 1.00x faster                                    |
| sqlglot_v2_transpile             | 733 us                                                                   | 729 us: 1.00x faster                                     |
| async_tree_io_tg                 | 200 ms                                                                   | 200 ms: 1.00x faster                                     |
| sqlglot_v2_parse                 | 608 us                                                                   | 606 us: 1.00x faster                                     |
| connected_components             | 219 ms                                                                   | 218 ms: 1.00x faster                                     |
| xml_etree_generate               | 36.9 ms                                                                  | 36.8 ms: 1.00x faster                                    |
| nqueens                          | 42.5 ms                                                                  | 42.4 ms: 1.00x faster                                    |
| richards                         | 24.8 ms                                                                  | 24.7 ms: 1.00x faster                                    |
| genshi_xml                       | 23.6 ms                                                                  | 23.7 ms: 1.00x slower                                    |
| fannkuch                         | 193 ms                                                                   | 194 ms: 1.00x slower                                     |
| pyflate                          | 200 ms                                                                   | 201 ms: 1.01x slower                                     |
| k_core                           | 981 ms                                                                   | 990 ms: 1.01x slower                                     |
| scimark_fft                      | 141 ms                                                                   | 142 ms: 1.01x slower                                     |
| mako                             | 5.58 ms                                                                  | 5.64 ms: 1.01x slower                                    |
| telco                            | 3.41 ms                                                                  | 3.46 ms: 1.01x slower                                    |
| xml_etree_parse                  | 56.1 ms                                                                  | 57.5 ms: 1.03x slower                                    |
| xml_etree_iterparse              | 36.7 ms                                                                  | 38.0 ms: 1.04x slower                                    |
| Geometric mean                   | (ref)                                                                    | 1.01x faster                                             |

Benchmark hidden because not significant (22): async_tree_memoization_tg, scimark_lu, gc_traversal, json_loads, pylint, typing_runtime_protocols, async_tree_eager, deepcopy_memo, sqlite_synth, pathlib, mdp, shortest_path, coverage, bench_thread_pool, json, bpe_tokeniser, float, create_gc_cycles, regex_v8, json_dumps, logging_simple, deltablue

- Geometric mean (including insignificant results): 1.006x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x