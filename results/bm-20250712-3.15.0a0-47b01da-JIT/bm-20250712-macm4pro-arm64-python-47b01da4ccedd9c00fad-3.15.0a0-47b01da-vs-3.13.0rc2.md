# Results vs. 3.13.0rc2

- fork: python
- ref: 47b01da4ccedd9c00fad
- machine: darwin-arm64
- commit hash: 47b01da
- commit date: 2025-07-12
- overall geometric mean: 1.005x slower
- HPT reliability: 77.44%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 122 ms: 1.09x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.10 sec: 1.05x slower                                                  |
| html5lib       | 23.1 ms                                                        | 25.4 ms: 1.10x slower                                                   |
| sphinx         | 409 ms                                                         | 424 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                          | 1.07x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 262 ms: 2.00x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 263 ms: 1.98x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 258 ms: 1.57x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 261 ms: 1.48x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 151 ms: 1.23x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 117 ms: 1.22x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 110 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 270 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 274 ms: 1.07x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.7 ms: 1.01x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 194 ms: 1.00x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 43.7 ms: 1.01x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 229 ms: 1.02x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 256 ms: 1.23x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 135 ms: 1.31x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.1 ms: 3.15x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.09x faster                                                            |

Benchmark hidden because not significant (1): async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 171 ms: 1.03x slower                                                    |
| float          | 31.4 ms                                                        | 33.7 ms: 1.07x slower                                                   |
| nbody          | 42.5 ms                                                        | 57.2 ms: 1.35x slower                                                   |
| Geometric mean | (ref)                                                          | 1.14x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 10.0 ms: 1.07x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 49.8 ms: 1.04x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 100 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 857 ms: 1.17x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 93.5 us: 1.06x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 24.0 ms: 1.05x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 34.6 ms: 1.03x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 4.54 ms: 1.03x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 45.5 ms: 1.01x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 61.5 ms: 1.01x faster                                                   |
| json_loads           | 10.8 us                                                        | 11.1 us: 1.02x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 146 us: 1.12x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.90 ms: 1.03x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.34 ms: 1.07x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 10.2 ms: 1.02x slower                                                   |
| genshi_xml      | 21.4 ms                                                        | 22.3 ms: 1.05x slower                                                   |
| django_template | 12.5 ms                                                        | 16.1 ms: 1.29x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.08x slower                                                            |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 262 ms: 2.00x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 263 ms: 1.98x faster                                                    |
| mdp                              | 1.06 sec                                                       | 537 ms: 1.97x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 258 ms: 1.57x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 261 ms: 1.48x faster                                                    |
| k_core                           | 1.46 sec                                                       | 998 ms: 1.47x faster                                                    |
| deepcopy                         | 145 us                                                         | 114 us: 1.27x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 51.8 ms: 1.24x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 151 ms: 1.23x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.5 us: 1.22x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 117 ms: 1.22x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 110 ms: 1.20x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 857 ms: 1.17x faster                                                    |
| go                               | 72.6 ms                                                        | 64.7 ms: 1.12x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 270 ms: 1.12x faster                                                    |
| pyflate                          | 222 ms                                                         | 200 ms: 1.11x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.19 us: 1.09x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 274 ms: 1.07x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.5 ms: 1.07x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 10.0 ms: 1.07x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 93.5 us: 1.06x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.01 sec: 1.06x faster                                                  |
| xml_etree_process                | 25.4 ms                                                        | 24.0 ms: 1.05x faster                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 310 ms: 1.04x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 628 ms: 1.03x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 34.6 ms: 1.03x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.54 ms: 1.03x faster                                                   |
| telco                            | 3.07 ms                                                        | 3.00 ms: 1.02x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 45.5 ms: 1.01x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 61.5 ms: 1.01x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 982 us: 1.01x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.7 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 194 ms: 1.00x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 65.1 us: 1.01x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 43.7 ms: 1.01x slower                                                   |
| pathlib                          | 11.1 ms                                                        | 11.3 ms: 1.01x slower                                                   |
| thrift                           | 309 us                                                         | 314 us: 1.02x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 229 ms: 1.02x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 30.5 ms: 1.02x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.1 us: 1.02x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 10.2 ms: 1.02x slower                                                   |
| sqlite_synth                     | 948 ns                                                         | 971 ns: 1.02x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.90 ms: 1.03x slower                                                   |
| pidigits                         | 166 ms                                                         | 171 ms: 1.03x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 128 ms: 1.04x slower                                                    |
| sphinx                           | 409 ms                                                         | 424 ms: 1.04x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 49.8 ms: 1.04x slower                                                   |
| connected_components             | 208 ms                                                         | 216 ms: 1.04x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.83 ms: 1.04x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 45.7 ms: 1.04x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 22.3 ms: 1.05x slower                                                   |
| shortest_path                    | 225 ms                                                         | 235 ms: 1.05x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.14 ms: 1.05x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 50.3 ms: 1.05x slower                                                   |
| docutils                         | 1.05 sec                                                       | 1.10 sec: 1.05x slower                                                  |
| richards                         | 22.1 ms                                                        | 23.3 ms: 1.06x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 100 ms: 1.06x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 437 us: 1.06x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.34 ms: 1.07x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 26.4 ms: 1.07x slower                                                   |
| float                            | 31.4 ms                                                        | 33.7 ms: 1.07x slower                                                   |
| coverage                         | 31.2 ms                                                        | 33.5 ms: 1.07x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 40.3 ms: 1.08x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 44.0 ns: 1.08x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 104 ms: 1.09x slower                                                    |
| 2to3                             | 112 ms                                                         | 122 ms: 1.09x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 25.4 ms: 1.10x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 175 ms: 1.10x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.51 us: 1.10x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.71 us: 1.11x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.16 ms: 1.11x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 58.1 ms: 1.11x slower                                                   |
| pycparser                        | 470 ms                                                         | 525 ms: 1.12x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.50 us: 1.12x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 146 us: 1.12x slower                                                    |
| pylint                           | 106 ms                                                         | 119 ms: 1.12x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.7 ms: 1.14x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 38.9 ms: 1.16x slower                                                   |
| raytrace                         | 109 ms                                                         | 126 ms: 1.16x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 49.7 ms: 1.16x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.70 ms: 1.17x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.13 ms: 1.20x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 45.4 ms: 1.20x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 256 ms: 1.23x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.4 ms: 1.23x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.1 ms: 1.29x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 135 ms: 1.31x slower                                                    |
| many_optionals                   | 200 us                                                         | 264 us: 1.32x slower                                                    |
| nbody                            | 42.5 ms                                                        | 57.2 ms: 1.35x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 10.2 ms: 1.62x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.1 ms: 3.15x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (4): async_generators, json, fannkuch, mako
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250712-3.15.0a0-47b01da-JIT/bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.005x slower

# HPT report

- Reliability score: 77.44% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.11x