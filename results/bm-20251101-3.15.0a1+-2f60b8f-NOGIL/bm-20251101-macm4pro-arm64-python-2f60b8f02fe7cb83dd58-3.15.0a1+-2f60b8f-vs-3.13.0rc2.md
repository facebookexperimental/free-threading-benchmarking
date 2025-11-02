# Results vs. 3.13.0rc2

- fork: python
- ref: 2f60b8f02fe7cb83dd58
- machine: darwin-arm64
- commit hash: 2f60b8f
- commit date: 2025-11-01
- overall geometric mean: 1.006x slower
- HPT reliability: 83.83%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.30x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 125 ms: 1.12x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                   |
| html5lib       | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                    |
| sphinx         | 409 ms                                                         | 419 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 196 ms: 2.65x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 206 ms: 2.55x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 200 ms: 2.03x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 212 ms: 1.83x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 87.6 ms: 1.51x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.49x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.40x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 239 ms: 1.26x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 247 ms: 1.19x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                     |
| async_generators                 | 193 ms                                                         | 183 ms: 1.05x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.00x slower                                                     |
| coroutines                       | 10.8 ms                                                        | 11.0 ms: 1.03x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 230 ms: 1.11x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 49.6 ms: 1.15x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.8 ms: 2.72x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.23x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.7 ms: 1.06x faster                                                    |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| nbody          | 42.5 ms                                                        | 57.3 ms: 1.35x slower                                                    |
| Geometric mean | (ref)                                                          | 1.08x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.43 ms: 1.13x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.42 ms: 1.13x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 54.7 ms: 1.14x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 39.9 ms: 1.16x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.11 ms: 1.13x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 59.3 ms: 1.05x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 979 ms: 1.02x faster                                                     |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.9 ms: 1.06x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.7 ms: 1.09x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 112 us: 1.13x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 154 us: 1.18x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.66 ms: 1.12x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.03 ms: 1.18x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.15x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 24.9 ms: 1.17x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 12.0 ms: 1.20x slower                                                    |
| mako            | 4.41 ms                                                        | 5.92 ms: 1.34x slower                                                    |
| django_template | 12.5 ms                                                        | 17.0 ms: 1.36x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.27x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 764 us: 2.67x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 196 ms: 2.65x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 206 ms: 2.55x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 478 us: 2.08x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 200 ms: 2.03x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 212 ms: 1.83x faster                                                     |
| mdp                              | 1.06 sec                                                       | 614 ms: 1.72x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 87.6 ms: 1.51x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.49x faster                                                     |
| k_core                           | 1.46 sec                                                       | 993 ms: 1.47x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.40x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 239 ms: 1.26x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 13.2 us: 1.25x faster                                                    |
| deepcopy                         | 145 us                                                         | 118 us: 1.23x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 247 ms: 1.19x faster                                                     |
| go                               | 72.6 ms                                                        | 62.4 ms: 1.16x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.9 ms: 1.16x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 55.9 ms: 1.14x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.43 ms: 1.13x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.42 ms: 1.13x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.11 ms: 1.13x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 837 ns: 1.13x faster                                                     |
| pyflate                          | 222 ms                                                         | 199 ms: 1.11x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                     |
| float                            | 31.4 ms                                                        | 29.7 ms: 1.06x faster                                                    |
| async_generators                 | 193 ms                                                         | 183 ms: 1.05x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 59.3 ms: 1.05x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.04 sec: 1.04x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 19.1 ms: 1.04x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 979 ms: 1.02x faster                                                     |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.28 us: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.00x slower                                                     |
| telco                            | 3.07 ms                                                        | 3.10 ms: 1.01x slower                                                    |
| dask                             | 525 ms                                                         | 533 ms: 1.01x slower                                                     |
| pycparser                        | 470 ms                                                         | 478 ms: 1.02x slower                                                     |
| html5lib                         | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                    |
| sphinx                           | 409 ms                                                         | 419 ms: 1.02x slower                                                     |
| coroutines                       | 10.8 ms                                                        | 11.0 ms: 1.03x slower                                                    |
| shortest_path                    | 225 ms                                                         | 233 ms: 1.04x slower                                                     |
| json                             | 1.94 ms                                                        | 2.01 ms: 1.04x slower                                                    |
| fannkuch                         | 179 ms                                                         | 185 ms: 1.04x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.9 ms: 1.06x slower                                                    |
| connected_components             | 208 ms                                                         | 222 ms: 1.07x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 8.10 ms: 1.08x slower                                                    |
| richards                         | 22.1 ms                                                        | 24.0 ms: 1.09x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.7 ms: 1.09x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 135 ms: 1.09x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                                     |
| thrift                           | 309 us                                                         | 340 us: 1.10x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 230 ms: 1.11x slower                                                     |
| richards_super                   | 24.7 ms                                                        | 27.4 ms: 1.11x slower                                                    |
| pylint                           | 106 ms                                                         | 118 ms: 1.12x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 360 ms: 1.12x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 9.66 ms: 1.12x slower                                                    |
| 2to3                             | 112 ms                                                         | 125 ms: 1.12x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.63 ms: 1.12x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 45.6 ns: 1.12x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 730 ms: 1.12x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.20 ms: 1.13x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 112 us: 1.13x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 43.0 ms: 1.14x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.55 us: 1.14x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 54.7 ms: 1.14x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 34.2 ms: 1.14x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.6 ms: 1.15x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 50.3 ms: 1.15x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.81 us: 1.15x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 75.0 us: 1.16x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 24.9 ms: 1.17x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 61.3 ms: 1.17x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 112 ms: 1.18x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 7.03 ms: 1.18x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 154 us: 1.18x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 56.7 ms: 1.18x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 44.6 ms: 1.20x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 12.0 ms: 1.20x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 192 ms: 1.21x slower                                                     |
| chaos                            | 24.3 ms                                                        | 29.6 ms: 1.22x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.1 ms: 1.22x slower                                                    |
| raytrace                         | 109 ms                                                         | 133 ms: 1.22x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.23 ms: 1.26x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.59 us: 1.26x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 42.8 ms: 1.27x slower                                                    |
| coverage                         | 31.2 ms                                                        | 40.1 ms: 1.29x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 534 us: 1.30x slower                                                     |
| mako                             | 4.41 ms                                                        | 5.92 ms: 1.34x slower                                                    |
| nbody                            | 42.5 ms                                                        | 57.3 ms: 1.35x slower                                                    |
| django_template                  | 12.5 ms                                                        | 17.0 ms: 1.36x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 67.1 ms: 1.57x slower                                                    |
| many_optionals                   | 200 us                                                         | 389 us: 1.94x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.8 ms: 2.72x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 19.2 ms: 3.07x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                             |

Benchmark hidden because not significant (1): regex_dna
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20251101-3.15.0a1+-2f60b8f-NOGIL/bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.006x slower

# HPT report

- Reliability score: 83.83% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.30x