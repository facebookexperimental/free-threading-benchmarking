# Results vs. 3.13.0rc2

- fork: python
- ref: cf9ef73121cd2b96dd51
- machine: darwin-arm64
- commit hash: cf9ef73
- commit date: 2025-09-16
- overall geometric mean: 1.036x faster
- HPT reliability: 98.67%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250916-macm4pro-arm64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 112 ms: 1.00x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                  |
| html5lib       | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                   |
| sphinx         | 409 ms                                                         | 402 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                          | 1.00x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250916-macm4pro-arm64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 242 ms: 2.17x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 249 ms: 2.09x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 247 ms: 1.64x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 248 ms: 1.56x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 110 ms: 1.29x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.28x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.27x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 257 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 259 ms: 1.13x faster                                                    |
| async_generators                 | 193 ms                                                         | 171 ms: 1.13x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.77 ms: 1.10x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 40.9 ms: 1.06x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 242 ms: 1.17x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 85.4 ms: 2.95x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.15x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250916-macm4pro-arm64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.2 ms: 1.04x faster                                                   |
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                    |
| nbody          | 42.5 ms                                                        | 48.5 ms: 1.14x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250916-macm4pro-arm64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.84 ms: 1.09x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 48.1 ms: 1.00x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 95.0 ms: 1.00x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250916-macm4pro-arm64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.78 ms: 1.23x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 895 ms: 1.12x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.2 ms: 1.04x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.1 ms: 1.02x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.0 ms: 1.01x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 98.4 us: 1.01x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.9 us: 1.01x slower                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 63.9 ms: 1.02x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 144 us: 1.11x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250916-macm4pro-arm64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.67 ms: 1.00x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.21 ms: 1.04x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250916-macm4pro-arm64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.82 ms: 1.02x faster                                                   |
| genshi_xml      | 21.4 ms                                                        | 21.5 ms: 1.01x slower                                                   |
| mako            | 4.41 ms                                                        | 4.88 ms: 1.11x slower                                                   |
| django_template | 12.5 ms                                                        | 15.2 ms: 1.22x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.07x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250916-macm4pro-arm64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 242 ms: 2.17x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 249 ms: 2.09x faster                                                    |
| mdp                              | 1.06 sec                                                       | 528 ms: 2.00x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 247 ms: 1.64x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 248 ms: 1.56x faster                                                    |
| k_core                           | 1.46 sec                                                       | 948 ms: 1.54x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.1 us: 1.36x faster                                                   |
| deepcopy                         | 145 us                                                         | 108 us: 1.35x faster                                                    |
| go                               | 72.6 ms                                                        | 55.5 ms: 1.31x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 110 ms: 1.29x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 49.6 ms: 1.29x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.28x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.27x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.78 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 257 ms: 1.17x faster                                                    |
| pyflate                          | 222 ms                                                         | 195 ms: 1.14x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 259 ms: 1.13x faster                                                    |
| async_generators                 | 193 ms                                                         | 171 ms: 1.13x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.15 us: 1.12x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 895 ms: 1.12x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 17.8 ms: 1.11x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.77 ms: 1.11x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 9.77 ms: 1.10x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.94 sec: 1.10x faster                                                  |
| create_gc_cycles                 | 993 us                                                         | 910 us: 1.09x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.84 ms: 1.09x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.5 ms: 1.06x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 40.9 ms: 1.06x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.2 ms: 1.04x faster                                                   |
| richards                         | 22.1 ms                                                        | 21.2 ms: 1.04x faster                                                   |
| float                            | 31.4 ms                                                        | 30.2 ms: 1.04x faster                                                   |
| shortest_path                    | 225 ms                                                         | 217 ms: 1.04x faster                                                    |
| connected_components             | 208 ms                                                         | 201 ms: 1.04x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 23.8 ms: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                    |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 62.9 us: 1.03x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.34 ms: 1.03x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.78 ms: 1.02x faster                                                   |
| json                             | 1.94 ms                                                        | 1.90 ms: 1.02x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 35.1 ms: 1.02x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                  |
| sphinx                           | 409 ms                                                         | 402 ms: 1.02x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.82 ms: 1.02x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.5 ms: 1.01x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.0 ms: 1.01x faster                                                   |
| fannkuch                         | 179 ms                                                         | 177 ms: 1.01x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 98.4 us: 1.01x faster                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.02 ms: 1.01x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 942 ns: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 522 ms: 1.00x faster                                                    |
| 2to3                             | 112 ms                                                         | 112 ms: 1.00x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 48.1 ms: 1.00x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 95.0 ms: 1.00x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 8.67 ms: 1.00x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 21.5 ms: 1.01x slower                                                   |
| json_loads                       | 10.8 us                                                        | 10.9 us: 1.01x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 37.6 ms: 1.01x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.48 us: 1.01x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.28 us: 1.02x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 63.9 ms: 1.02x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 666 ms: 1.02x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 330 ms: 1.03x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.49 ms: 1.03x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 49.5 ms: 1.03x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 427 us: 1.04x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 98.9 ms: 1.04x slower                                                   |
| pycparser                        | 470 ms                                                         | 489 ms: 1.04x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.21 ms: 1.04x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 130 ms: 1.05x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 168 ms: 1.05x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.8 ms: 1.05x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 55.2 ms: 1.05x slower                                                   |
| pylint                           | 106 ms                                                         | 112 ms: 1.06x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.89 ms: 1.06x slower                                                   |
| chaos                            | 24.3 ms                                                        | 26.1 ms: 1.07x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.33 us: 1.08x slower                                                   |
| raytrace                         | 109 ms                                                         | 118 ms: 1.08x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 36.6 ms: 1.09x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 41.3 ms: 1.09x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.88 ms: 1.11x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.4 ms: 1.11x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 144 us: 1.11x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 47.5 ms: 1.11x slower                                                   |
| nbody                            | 42.5 ms                                                        | 48.5 ms: 1.14x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 242 ms: 1.17x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.2 ms: 1.22x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                    |
| many_optionals                   | 200 us                                                         | 316 us: 1.57x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 17.6 ms: 2.81x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 85.4 ms: 2.95x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                            |

Benchmark hidden because not significant (3): logging_silent, thrift, spectral_norm
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250916-3.15.0a0-cf9ef73/bm-20250916-macm4pro-arm64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.036x faster

# HPT report

- Reliability score: 98.67% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.11x