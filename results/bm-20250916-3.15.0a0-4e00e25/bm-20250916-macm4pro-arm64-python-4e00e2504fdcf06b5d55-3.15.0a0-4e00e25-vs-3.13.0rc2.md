# Results vs. 3.13.0rc2

- fork: python
- ref: 4e00e2504fdcf06b5d55
- machine: darwin-arm64
- commit hash: 4e00e25
- commit date: 2025-09-16
- overall geometric mean: 1.038x faster
- HPT reliability: 99.47%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250916-macm4pro-arm64-python-4e00e2504fdcf06b5d55-3.15.0a0-4e00e25 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 111 ms: 1.00x faster                                                    |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                  |
| html5lib       | 23.1 ms                                                        | 23.4 ms: 1.01x slower                                                   |
| sphinx         | 409 ms                                                         | 401 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                          | 1.01x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250916-macm4pro-arm64-python-4e00e2504fdcf06b5d55-3.15.0a0-4e00e25 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 242 ms: 2.17x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 246 ms: 2.11x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 247 ms: 1.64x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 248 ms: 1.56x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 110 ms: 1.29x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.29x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.28x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 258 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 259 ms: 1.13x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                    |
| async_generators                 | 193 ms                                                         | 173 ms: 1.12x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.94 ms: 1.08x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 40.5 ms: 1.07x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 243 ms: 1.17x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 85.2 ms: 2.94x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.15x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250916-macm4pro-arm64-python-4e00e2504fdcf06b5d55-3.15.0a0-4e00e25 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.7 ms: 1.06x faster                                                   |
| pidigits       | 166 ms                                                         | 162 ms: 1.02x faster                                                    |
| nbody          | 42.5 ms                                                        | 48.1 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250916-macm4pro-arm64-python-4e00e2504fdcf06b5d55-3.15.0a0-4e00e25 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.85 ms: 1.09x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 47.6 ms: 1.01x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 95.6 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250916-macm4pro-arm64-python-4e00e2504fdcf06b5d55-3.15.0a0-4e00e25 |
|---------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps          | 4.65 ms                                                        | 3.73 ms: 1.25x faster                                                   |
| tomli_loads         | 1000 ms                                                        | 892 ms: 1.12x faster                                                    |
| xml_etree_iterparse | 46.1 ms                                                        | 44.6 ms: 1.03x faster                                                   |
| xml_etree_generate  | 35.8 ms                                                        | 34.9 ms: 1.03x faster                                                   |
| xml_etree_process   | 25.4 ms                                                        | 24.8 ms: 1.02x faster                                                   |
| json_loads          | 10.8 us                                                        | 10.9 us: 1.01x slower                                                   |
| xml_etree_parse     | 62.4 ms                                                        | 63.9 ms: 1.02x slower                                                   |
| pickle_pure_python  | 130 us                                                         | 143 us: 1.09x slower                                                    |
| Geometric mean      | (ref)                                                          | 1.03x faster                                                            |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250916-macm4pro-arm64-python-4e00e2504fdcf06b5d55-3.15.0a0-4e00e25 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.61 ms: 1.00x faster                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.19 ms: 1.04x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250916-macm4pro-arm64-python-4e00e2504fdcf06b5d55-3.15.0a0-4e00e25 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.71 ms: 1.03x faster                                                   |
| genshi_xml      | 21.4 ms                                                        | 21.3 ms: 1.01x faster                                                   |
| mako            | 4.41 ms                                                        | 4.91 ms: 1.11x slower                                                   |
| django_template | 12.5 ms                                                        | 15.1 ms: 1.21x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.07x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250916-macm4pro-arm64-python-4e00e2504fdcf06b5d55-3.15.0a0-4e00e25 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 242 ms: 2.17x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 246 ms: 2.11x faster                                                    |
| mdp                              | 1.06 sec                                                       | 529 ms: 2.00x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 247 ms: 1.64x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 248 ms: 1.56x faster                                                    |
| k_core                           | 1.46 sec                                                       | 950 ms: 1.54x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.9 us: 1.38x faster                                                   |
| deepcopy                         | 145 us                                                         | 105 us: 1.38x faster                                                    |
| go                               | 72.6 ms                                                        | 55.2 ms: 1.31x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 49.3 ms: 1.30x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 110 ms: 1.29x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.29x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.28x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.26x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.73 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 258 ms: 1.17x faster                                                    |
| pyflate                          | 222 ms                                                         | 192 ms: 1.16x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.14 us: 1.14x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 259 ms: 1.13x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 892 ms: 1.12x faster                                                    |
| async_generators                 | 193 ms                                                         | 173 ms: 1.12x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.74 ms: 1.12x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.0 ms: 1.10x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.94 sec: 1.10x faster                                                  |
| create_gc_cycles                 | 993 us                                                         | 909 us: 1.09x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.85 ms: 1.09x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 9.94 ms: 1.08x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 40.5 ms: 1.07x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.4 ms: 1.07x faster                                                   |
| float                            | 31.4 ms                                                        | 29.7 ms: 1.06x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 61.6 us: 1.05x faster                                                   |
| richards                         | 22.1 ms                                                        | 21.1 ms: 1.05x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.74 ms: 1.04x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 23.8 ms: 1.04x faster                                                   |
| shortest_path                    | 225 ms                                                         | 217 ms: 1.03x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.6 ms: 1.03x faster                                                   |
| connected_components             | 208 ms                                                         | 202 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.33 ms: 1.03x faster                                                   |
| genshi_text                      | 9.97 ms                                                        | 9.71 ms: 1.03x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 34.9 ms: 1.03x faster                                                   |
| pidigits                         | 166 ms                                                         | 162 ms: 1.02x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.8 ms: 1.02x faster                                                   |
| fannkuch                         | 179 ms                                                         | 175 ms: 1.02x faster                                                    |
| sphinx                           | 409 ms                                                         | 401 ms: 1.02x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.4 ms: 1.02x faster                                                   |
| json                             | 1.94 ms                                                        | 1.91 ms: 1.02x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                  |
| spectral_norm                    | 43.7 ms                                                        | 43.4 ms: 1.01x faster                                                   |
| regex_compile                    | 47.9 ms                                                        | 47.6 ms: 1.01x faster                                                   |
| genshi_xml                       | 21.4 ms                                                        | 21.3 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                    |
| 2to3                             | 112 ms                                                         | 111 ms: 1.00x faster                                                    |
| python_startup                   | 8.63 ms                                                        | 8.61 ms: 1.00x faster                                                   |
| json_loads                       | 10.8 us                                                        | 10.9 us: 1.01x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 656 ms: 1.01x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 37.6 ms: 1.01x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 95.6 ms: 1.01x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 23.4 ms: 1.01x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.48 us: 1.01x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.27 us: 1.02x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 328 ms: 1.02x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 63.9 ms: 1.02x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.49 ms: 1.03x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 424 us: 1.03x slower                                                    |
| pycparser                        | 470 ms                                                         | 487 ms: 1.04x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 49.6 ms: 1.04x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.19 ms: 1.04x slower                                                   |
| coverage                         | 31.2 ms                                                        | 32.5 ms: 1.04x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 99.4 ms: 1.04x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 130 ms: 1.05x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 168 ms: 1.05x slower                                                    |
| pylint                           | 106 ms                                                         | 112 ms: 1.06x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.7 ms: 1.06x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.89 ms: 1.07x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 55.7 ms: 1.07x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.19 ms: 1.08x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.32 us: 1.08x slower                                                   |
| raytrace                         | 109 ms                                                         | 118 ms: 1.08x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 36.5 ms: 1.09x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 41.1 ms: 1.09x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 46.7 ms: 1.09x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.2 ms: 1.09x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 143 us: 1.09x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.91 ms: 1.11x slower                                                   |
| nbody                            | 42.5 ms                                                        | 48.1 ms: 1.13x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 243 ms: 1.17x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.1 ms: 1.21x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                    |
| many_optionals                   | 200 us                                                         | 316 us: 1.58x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 17.6 ms: 2.81x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 85.2 ms: 2.94x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                                            |

Benchmark hidden because not significant (4): unpickle_pure_python, logging_silent, thrift, sqlite_synth
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250916-3.15.0a0-4e00e25/bm-20250916-macm4pro-arm64-python-4e00e2504fdcf06b5d55-3.15.0a0-4e00e25.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.038x faster

# HPT report

- Reliability score: 99.47% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x