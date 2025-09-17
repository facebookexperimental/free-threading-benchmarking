# Results vs. 3.12.6

- fork: python
- ref: cf9ef73121cd2b96dd51
- machine: darwin-arm64
- commit hash: cf9ef73
- commit date: 2025-09-16
- overall geometric mean: 1.116x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250916-macm4pro-arm64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 112 ms: 1.02x faster                                                    |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                  |
| html5lib       | 23.0 ms                                                  | 23.7 ms: 1.03x slower                                                   |
| sphinx         | 434 ms                                                   | 402 ms: 1.08x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250916-macm4pro-arm64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 242 ms: 2.05x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 247 ms: 1.94x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 248 ms: 1.85x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 249 ms: 1.79x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.66x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 110 ms: 1.62x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.51x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.77 ms: 1.39x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 257 ms: 1.32x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 259 ms: 1.29x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                    |
| async_generators                 | 206 ms                                                   | 171 ms: 1.21x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.9 ms: 1.11x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 218 ms: 1.06x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 128 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 242 ms: 1.14x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 85.4 ms: 2.66x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.27x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250916-macm4pro-arm64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.2 ms: 1.26x faster                                                   |
| nbody          | 54.2 ms                                                  | 48.5 ms: 1.12x faster                                                   |
| Geometric mean | (ref)                                                    | 1.12x faster                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250916-macm4pro-arm64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 48.1 ms: 1.14x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 95.0 ms: 1.05x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.84 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250916-macm4pro-arm64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 44.2 ms: 1.17x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.78 ms: 1.13x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.1 ms: 1.11x faster                                                   |
| tomli_loads          | 957 ms                                                   | 895 ms: 1.07x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 25.0 ms: 1.07x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 63.9 ms: 1.06x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 98.4 us: 1.05x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 144 us: 1.04x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.07x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250916-macm4pro-arm64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.67 ms: 1.08x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.21 ms: 1.09x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.08x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250916-macm4pro-arm64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.82 ms: 1.07x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 21.5 ms: 1.01x faster                                                   |
| mako            | 4.77 ms                                                  | 4.88 ms: 1.02x slower                                                   |
| django_template | 13.6 ms                                                  | 15.2 ms: 1.12x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.01x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250916-macm4pro-arm64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.09 sec                                                 | 528 ms: 2.07x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 242 ms: 2.05x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 247 ms: 1.94x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 248 ms: 1.85x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 249 ms: 1.79x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.66x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 110 ms: 1.62x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.51x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.1 us: 1.51x faster                                                   |
| deepcopy                         | 161 us                                                   | 108 us: 1.50x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.77 ms: 1.39x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.33 us: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 257 ms: 1.32x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 259 ms: 1.29x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.15 us: 1.27x faster                                                   |
| go                               | 70.0 ms                                                  | 55.5 ms: 1.26x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.4 ms: 1.26x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 40.5 ns: 1.26x faster                                                   |
| float                            | 37.9 ms                                                  | 30.2 ms: 1.26x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 43.8 ms: 1.24x faster                                                   |
| raytrace                         | 145 ms                                                   | 118 ms: 1.23x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 49.6 ms: 1.23x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                    |
| async_generators                 | 206 ms                                                   | 171 ms: 1.21x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 17.8 ms: 1.19x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.5 ms: 1.18x faster                                                   |
| subparsers                       | 20.8 ms                                                  | 17.6 ms: 1.18x faster                                                   |
| k_core                           | 1.12 sec                                                 | 948 ms: 1.18x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.2 ms: 1.17x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 37.6 ms: 1.16x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.49 ms: 1.15x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.94 sec: 1.15x faster                                                  |
| pylint                           | 128 ms                                                   | 112 ms: 1.15x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 48.1 ms: 1.14x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.48 us: 1.13x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 62.9 us: 1.13x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.28 us: 1.13x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.78 ms: 1.13x faster                                                   |
| nbody                            | 54.2 ms                                                  | 48.5 ms: 1.12x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 40.9 ms: 1.11x faster                                                   |
| pyflate                          | 216 ms                                                   | 195 ms: 1.11x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.1 ms: 1.11x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 35.1 ms: 1.11x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.89 ms: 1.10x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.78 ms: 1.09x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.34 ms: 1.09x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.5 ms: 1.09x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 130 ms: 1.09x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 47.5 ms: 1.08x faster                                                   |
| sphinx                           | 434 ms                                                   | 402 ms: 1.08x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 895 ms: 1.07x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.0 ms: 1.07x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 9.82 ms: 1.07x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 23.8 ms: 1.06x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 63.9 ms: 1.06x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 36.6 ms: 1.06x faster                                                   |
| richards                         | 22.4 ms                                                  | 21.2 ms: 1.06x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 218 ms: 1.06x faster                                                    |
| sympy_str                        | 104 ms                                                   | 98.9 ms: 1.05x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 95.0 ms: 1.05x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 98.4 us: 1.05x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 55.2 ms: 1.04x faster                                                   |
| thrift                           | 322 us                                                   | 309 us: 1.04x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 942 ns: 1.03x faster                                                    |
| 2to3                             | 114 ms                                                   | 112 ms: 1.02x faster                                                    |
| json                             | 1.93 ms                                                  | 1.90 ms: 1.02x faster                                                   |
| pycparser                        | 497 ms                                                   | 489 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.5 ms: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                    |
| shortest_path                    | 219 ms                                                   | 217 ms: 1.01x faster                                                    |
| sympy_expand                     | 167 ms                                                   | 168 ms: 1.00x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 330 ms: 1.01x slower                                                    |
| fannkuch                         | 176 ms                                                   | 177 ms: 1.01x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.02 ms: 1.01x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                  |
| bench_thread_pool                | 419 us                                                   | 427 us: 1.02x slower                                                    |
| mako                             | 4.77 ms                                                  | 4.88 ms: 1.02x slower                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.84 ms: 1.03x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 23.7 ms: 1.03x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 49.5 ms: 1.04x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 144 us: 1.04x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 41.3 ms: 1.04x slower                                                   |
| telco                            | 2.61 ms                                                  | 2.77 ms: 1.06x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.67 ms: 1.08x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.21 ms: 1.09x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 910 us: 1.10x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.2 ms: 1.12x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 128 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 242 ms: 1.14x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.8 ms: 1.22x slower                                                   |
| many_optionals                   | 195 us                                                   | 316 us: 1.62x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 85.4 ms: 2.66x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.12x faster                                                            |

Benchmark hidden because not significant (4): pidigits, connected_components, pprint_pformat, json_loads
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250916-3.15.0a0-cf9ef73/bm-20250916-macm4pro-arm64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.116x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.16x