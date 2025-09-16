# Results vs. 3.12.6

- fork: python
- ref: 4e00e2504fdcf06b5d55
- machine: darwin-arm64
- commit hash: 4e00e25
- commit date: 2025-09-16
- overall geometric mean: 1.119x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250916-macm4pro-arm64-python-4e00e2504fdcf06b5d55-3.15.0a0-4e00e25 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 111 ms: 1.03x faster                                                    |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.01x slower                                                  |
| html5lib       | 23.0 ms                                                  | 23.4 ms: 1.02x slower                                                   |
| sphinx         | 434 ms                                                   | 401 ms: 1.08x faster                                                    |
| Geometric mean | (ref)                                                    | 1.02x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250916-macm4pro-arm64-python-4e00e2504fdcf06b5d55-3.15.0a0-4e00e25 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 242 ms: 2.05x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 247 ms: 1.94x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 248 ms: 1.86x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 246 ms: 1.81x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.67x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 110 ms: 1.62x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.51x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.94 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 258 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 259 ms: 1.29x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                    |
| async_generators                 | 206 ms                                                   | 173 ms: 1.19x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.5 ms: 1.13x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 218 ms: 1.06x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 128 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 243 ms: 1.14x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 85.2 ms: 2.65x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.28x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250916-macm4pro-arm64-python-4e00e2504fdcf06b5d55-3.15.0a0-4e00e25 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.7 ms: 1.27x faster                                                   |
| nbody          | 54.2 ms                                                  | 48.1 ms: 1.13x faster                                                   |
| pidigits       | 161 ms                                                   | 162 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                    | 1.13x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250916-macm4pro-arm64-python-4e00e2504fdcf06b5d55-3.15.0a0-4e00e25 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 47.6 ms: 1.15x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 95.6 ms: 1.04x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.85 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250916-macm4pro-arm64-python-4e00e2504fdcf06b5d55-3.15.0a0-4e00e25 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 44.6 ms: 1.16x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.73 ms: 1.14x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 34.9 ms: 1.11x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 24.8 ms: 1.08x faster                                                   |
| tomli_loads          | 957 ms                                                   | 892 ms: 1.07x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 63.9 ms: 1.06x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 98.2 us: 1.05x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 143 us: 1.02x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.07x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250916-macm4pro-arm64-python-4e00e2504fdcf06b5d55-3.15.0a0-4e00e25 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.61 ms: 1.07x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.19 ms: 1.08x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.08x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250916-macm4pro-arm64-python-4e00e2504fdcf06b5d55-3.15.0a0-4e00e25 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.71 ms: 1.08x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 21.3 ms: 1.03x faster                                                   |
| mako            | 4.77 ms                                                  | 4.91 ms: 1.03x slower                                                   |
| django_template | 13.6 ms                                                  | 15.1 ms: 1.11x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.01x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250916-macm4pro-arm64-python-4e00e2504fdcf06b5d55-3.15.0a0-4e00e25 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.09 sec                                                 | 529 ms: 2.06x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 242 ms: 2.05x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 247 ms: 1.94x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 248 ms: 1.86x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 246 ms: 1.81x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.67x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 110 ms: 1.62x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 11.9 us: 1.54x faster                                                   |
| deepcopy                         | 161 us                                                   | 105 us: 1.53x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.51x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.94 ms: 1.36x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.32 us: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 258 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 259 ms: 1.29x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.14 us: 1.28x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.2 ms: 1.28x faster                                                   |
| float                            | 37.9 ms                                                  | 29.7 ms: 1.27x faster                                                   |
| go                               | 70.0 ms                                                  | 55.2 ms: 1.27x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 40.4 ns: 1.26x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 43.4 ms: 1.25x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 49.3 ms: 1.24x faster                                                   |
| raytrace                         | 145 ms                                                   | 118 ms: 1.23x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                    |
| async_generators                 | 206 ms                                                   | 173 ms: 1.19x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.4 ms: 1.18x faster                                                   |
| subparsers                       | 20.8 ms                                                  | 17.6 ms: 1.18x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.0 ms: 1.18x faster                                                   |
| k_core                           | 1.12 sec                                                 | 950 ms: 1.18x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.49 ms: 1.16x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.6 ms: 1.16x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 37.6 ms: 1.16x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.94 sec: 1.15x faster                                                  |
| typing_runtime_protocols         | 71.0 us                                                  | 61.6 us: 1.15x faster                                                   |
| pylint                           | 128 ms                                                   | 112 ms: 1.15x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 47.6 ms: 1.15x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.73 ms: 1.14x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.48 us: 1.13x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.27 us: 1.13x faster                                                   |
| nbody                            | 54.2 ms                                                  | 48.1 ms: 1.13x faster                                                   |
| chaos                            | 28.9 ms                                                  | 25.7 ms: 1.13x faster                                                   |
| pyflate                          | 216 ms                                                   | 192 ms: 1.13x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.5 ms: 1.13x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 34.9 ms: 1.11x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.74 ms: 1.11x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 46.7 ms: 1.10x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.4 ms: 1.10x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.89 ms: 1.10x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.33 ms: 1.09x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 130 ms: 1.09x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.71 ms: 1.08x faster                                                   |
| sphinx                           | 434 ms                                                   | 401 ms: 1.08x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.8 ms: 1.08x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 892 ms: 1.07x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 23.8 ms: 1.07x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 36.5 ms: 1.06x faster                                                   |
| richards                         | 22.4 ms                                                  | 21.1 ms: 1.06x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 63.9 ms: 1.06x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 218 ms: 1.06x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 98.2 us: 1.05x faster                                                   |
| sympy_str                        | 104 ms                                                   | 99.4 ms: 1.05x faster                                                   |
| thrift                           | 322 us                                                   | 309 us: 1.04x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 95.6 ms: 1.04x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 55.7 ms: 1.03x faster                                                   |
| 2to3                             | 114 ms                                                   | 111 ms: 1.03x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.3 ms: 1.03x faster                                                   |
| pycparser                        | 497 ms                                                   | 487 ms: 1.02x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 950 ns: 1.02x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 656 ms: 1.01x faster                                                    |
| json                             | 1.93 ms                                                  | 1.91 ms: 1.01x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                    |
| shortest_path                    | 219 ms                                                   | 217 ms: 1.01x faster                                                    |
| pidigits                         | 161 ms                                                   | 162 ms: 1.01x slower                                                    |
| connected_components             | 201 ms                                                   | 202 ms: 1.01x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 168 ms: 1.01x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 424 us: 1.01x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.01x slower                                                  |
| html5lib                         | 23.0 ms                                                  | 23.4 ms: 1.02x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 143 us: 1.02x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.85 ms: 1.03x slower                                                   |
| mako                             | 4.77 ms                                                  | 4.91 ms: 1.03x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 41.1 ms: 1.04x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 49.6 ms: 1.04x slower                                                   |
| telco                            | 2.61 ms                                                  | 2.74 ms: 1.05x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.61 ms: 1.07x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.19 ms: 1.08x slower                                                   |
| gc_traversal                     | 2.01 ms                                                  | 2.19 ms: 1.09x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 909 us: 1.09x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.1 ms: 1.11x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 128 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 243 ms: 1.14x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.5 ms: 1.21x slower                                                   |
| many_optionals                   | 195 us                                                   | 316 us: 1.62x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 85.2 ms: 2.65x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.12x faster                                                            |

Benchmark hidden because not significant (3): fannkuch, pprint_safe_repr, json_loads
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250916-3.15.0a0-4e00e25/bm-20250916-macm4pro-arm64-python-4e00e2504fdcf06b5d55-3.15.0a0-4e00e25.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.119x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.15x