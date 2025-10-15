# Results vs. 3.13.0rc2

- fork: python
- ref: d6dd64ac654898b4ce71
- machine: darwin-arm64
- commit hash: d6dd64a
- commit date: 2025-10-12
- overall geometric mean: 1.002x faster
- HPT reliability: 75.15%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.29x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 122 ms: 1.09x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.00 sec: 1.04x faster                                                  |
| html5lib       | 23.1 ms                                                        | 23.6 ms: 1.02x slower                                                   |
| sphinx         | 409 ms                                                         | 416 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 195 ms: 2.67x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.57x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 199 ms: 2.03x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 211 ms: 1.83x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.2 ms: 1.52x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 100 ms: 1.42x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 235 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 242 ms: 1.21x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                    |
| async_generators                 | 193 ms                                                         | 180 ms: 1.07x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 227 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.6 ms: 1.13x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.0 ms: 2.70x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.25x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.6 ms: 1.06x faster                                                   |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| nbody          | 42.5 ms                                                        | 57.7 ms: 1.36x slower                                                   |
| Geometric mean | (ref)                                                          | 1.08x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.63 ms: 1.11x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 96.6 ms: 1.02x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 54.2 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.94 ms: 1.18x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.4 ms: 1.17x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 56.9 ms: 1.10x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 986 ms: 1.01x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.2 ms: 1.04x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.06x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 27.3 ms: 1.08x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 113 us: 1.13x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 152 us: 1.17x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.00x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.71 ms: 1.13x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 7.07 ms: 1.19x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.16x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 24.3 ms: 1.14x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.7 ms: 1.17x slower                                                   |
| mako            | 4.41 ms                                                        | 5.78 ms: 1.31x slower                                                   |
| django_template | 12.5 ms                                                        | 16.8 ms: 1.34x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.24x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 195 ms: 2.67x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 771 us: 2.65x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.57x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 479 us: 2.07x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 199 ms: 2.03x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 211 ms: 1.83x faster                                                    |
| mdp                              | 1.06 sec                                                       | 612 ms: 1.73x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.2 ms: 1.52x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 989 ms: 1.48x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 100 ms: 1.42x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 235 ms: 1.28x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.2 us: 1.25x faster                                                   |
| deepcopy                         | 145 us                                                         | 118 us: 1.23x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 242 ms: 1.21x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.94 ms: 1.18x faster                                                   |
| go                               | 72.6 ms                                                        | 61.9 ms: 1.17x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.4 ms: 1.17x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 818 ns: 1.16x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 55.8 ms: 1.15x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                    |
| pyflate                          | 222 ms                                                         | 200 ms: 1.11x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.63 ms: 1.11x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 56.9 ms: 1.10x faster                                                   |
| async_generators                 | 193 ms                                                         | 180 ms: 1.07x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.99 sec: 1.07x faster                                                  |
| float                            | 31.4 ms                                                        | 29.6 ms: 1.06x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.00 sec: 1.04x faster                                                  |
| dulwich_log                      | 19.8 ms                                                        | 19.1 ms: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.27 us: 1.02x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                   |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 986 ms: 1.01x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 531 ms: 1.01x slower                                                    |
| pycparser                        | 470 ms                                                         | 476 ms: 1.01x slower                                                    |
| sphinx                           | 409 ms                                                         | 416 ms: 1.02x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.6 ms: 1.02x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 96.6 ms: 1.02x slower                                                   |
| json                             | 1.94 ms                                                        | 1.99 ms: 1.03x slower                                                   |
| shortest_path                    | 225 ms                                                         | 233 ms: 1.04x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.2 ms: 1.04x slower                                                   |
| fannkuch                         | 179 ms                                                         | 186 ms: 1.04x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.06x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 8.02 ms: 1.06x slower                                                   |
| connected_components             | 208 ms                                                         | 222 ms: 1.07x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.3 ms: 1.08x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 348 ms: 1.08x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.9 ms: 1.08x slower                                                   |
| thrift                           | 309 us                                                         | 336 us: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 227 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| 2to3                             | 112 ms                                                         | 122 ms: 1.09x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 711 ms: 1.09x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 44.8 ns: 1.10x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.15 ms: 1.11x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 137 ms: 1.11x slower                                                    |
| pylint                           | 106 ms                                                         | 117 ms: 1.11x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 27.5 ms: 1.11x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.62 ms: 1.12x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 42.5 ms: 1.12x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 9.71 ms: 1.13x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 48.6 ms: 1.13x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.52 us: 1.13x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 54.2 ms: 1.13x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.8 ms: 1.13x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 113 us: 1.13x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 73.4 us: 1.14x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.78 us: 1.14x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 24.3 ms: 1.14x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 60.7 ms: 1.16x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 50.8 ms: 1.16x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 152 us: 1.17x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 43.5 ms: 1.17x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.7 ms: 1.17x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 56.7 ms: 1.18x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 7.07 ms: 1.19x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 191 ms: 1.20x slower                                                    |
| chaos                            | 24.3 ms                                                        | 29.2 ms: 1.20x slower                                                   |
| raytrace                         | 109 ms                                                         | 132 ms: 1.21x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.1 ms: 1.22x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.41 us: 1.24x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.1 ms: 1.25x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.23 ms: 1.26x slower                                                   |
| coverage                         | 31.2 ms                                                        | 39.7 ms: 1.27x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.78 ms: 1.31x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 546 us: 1.33x slower                                                    |
| django_template                  | 12.5 ms                                                        | 16.8 ms: 1.34x slower                                                   |
| nbody                            | 42.5 ms                                                        | 57.7 ms: 1.36x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 68.7 ms: 1.61x slower                                                   |
| many_optionals                   | 200 us                                                         | 384 us: 1.92x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.0 ms: 2.70x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 19.0 ms: 3.03x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.00x slower                                                            |

Benchmark hidden because not significant (1): telco
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20251012-3.15.0a0-d6dd64a-NOGIL/bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.002x faster

# HPT report

- Reliability score: 75.15% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.29x