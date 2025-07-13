# Results vs. 3.13.0rc2

- fork: python
- ref: 47b01da4ccedd9c00fad
- machine: darwin-arm64
- commit hash: 47b01da
- commit date: 2025-07-12
- overall geometric mean: 1.061x faster
- HPT reliability: 99.97%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 110 ms: 1.01x faster                                                    |
| sphinx         | 409 ms                                                         | 401 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (2): docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 243 ms: 2.17x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 254 ms: 2.05x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 248 ms: 1.64x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 249 ms: 1.55x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.28x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 145 ms: 1.27x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.27x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 267 ms: 1.13x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.12x faster                                                    |
| async_generators                 | 193 ms                                                         | 173 ms: 1.12x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 268 ms: 1.10x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 39.4 ms: 1.10x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 9.84 ms: 1.09x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 194 ms: 1.00x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 251 ms: 1.21x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.5 ms: 3.02x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.3 ms: 1.07x faster                                                   |
| pidigits       | 166 ms                                                         | 171 ms: 1.03x slower                                                    |
| nbody          | 42.5 ms                                                        | 47.4 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 43.8 ms: 1.10x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.88 ms: 1.08x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 102 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 809 ms: 1.24x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 23.1 ms: 1.10x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 32.8 ms: 1.09x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 91.2 us: 1.09x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 4.37 ms: 1.06x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.1 ms: 1.05x faster                                                   |
| pickle_pure_python   | 130 us                                                         | 136 us: 1.04x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.06x faster                                                            |

Benchmark hidden because not significant (2): json_loads, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.78 ms: 1.02x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.25 ms: 1.05x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.06 ms: 1.10x faster                                                   |
| genshi_xml      | 21.4 ms                                                        | 19.4 ms: 1.10x faster                                                   |
| mako            | 4.41 ms                                                        | 4.56 ms: 1.03x slower                                                   |
| django_template | 12.5 ms                                                        | 13.9 ms: 1.12x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.01x faster                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 243 ms: 2.17x faster                                                    |
| mdp                              | 1.06 sec                                                       | 510 ms: 2.07x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 254 ms: 2.05x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 248 ms: 1.64x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 249 ms: 1.55x faster                                                    |
| k_core                           | 1.46 sec                                                       | 961 ms: 1.52x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.3 us: 1.46x faster                                                   |
| deepcopy                         | 145 us                                                         | 100 us: 1.45x faster                                                    |
| go                               | 72.6 ms                                                        | 51.1 ms: 1.42x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.28x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 145 ms: 1.27x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.27x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 50.7 ms: 1.26x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.26x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 809 ms: 1.24x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.08 us: 1.20x faster                                                   |
| pyflate                          | 222 ms                                                         | 190 ms: 1.17x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 17.3 ms: 1.15x faster                                                   |
| richards                         | 22.1 ms                                                        | 19.3 ms: 1.14x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.52 ms: 1.13x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 267 ms: 1.13x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.12x faster                                                    |
| async_generators                 | 193 ms                                                         | 173 ms: 1.12x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 22.1 ms: 1.12x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.93 sec: 1.10x faster                                                  |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| genshi_text                      | 9.97 ms                                                        | 9.06 ms: 1.10x faster                                                   |
| genshi_xml                       | 21.4 ms                                                        | 19.4 ms: 1.10x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 23.1 ms: 1.10x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 268 ms: 1.10x faster                                                    |
| generators                       | 15.7 ms                                                        | 14.3 ms: 1.10x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 39.4 ms: 1.10x faster                                                   |
| regex_compile                    | 47.9 ms                                                        | 43.8 ms: 1.10x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 9.84 ms: 1.09x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 32.8 ms: 1.09x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 91.2 us: 1.09x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.88 ms: 1.08x faster                                                   |
| thrift                           | 309 us                                                         | 287 us: 1.08x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 60.1 us: 1.07x faster                                                   |
| float                            | 31.4 ms                                                        | 29.3 ms: 1.07x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.37 ms: 1.06x faster                                                   |
| fannkuch                         | 179 ms                                                         | 171 ms: 1.05x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.1 ms: 1.05x faster                                                   |
| pprint_pformat                   | 650 ms                                                         | 624 ms: 1.04x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 309 ms: 1.04x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.8 ms: 1.04x faster                                                   |
| logging_silent                   | 40.6 ns                                                        | 39.3 ns: 1.03x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.32 ms: 1.03x faster                                                   |
| telco                            | 3.07 ms                                                        | 3.00 ms: 1.02x faster                                                   |
| json                             | 1.94 ms                                                        | 1.90 ms: 1.02x faster                                                   |
| sphinx                           | 409 ms                                                         | 401 ms: 1.02x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.41 us: 1.02x faster                                                   |
| sympy_expand                     | 159 ms                                                         | 157 ms: 1.01x faster                                                    |
| shortest_path                    | 225 ms                                                         | 222 ms: 1.01x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                   |
| sympy_str                        | 95.5 ms                                                        | 94.5 ms: 1.01x faster                                                   |
| 2to3                             | 112 ms                                                         | 110 ms: 1.01x faster                                                    |
| connected_components             | 208 ms                                                         | 206 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 988 us: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.23 us: 1.00x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 194 ms: 1.00x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 48.4 ms: 1.01x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 8.78 ms: 1.02x slower                                                   |
| pycparser                        | 470 ms                                                         | 478 ms: 1.02x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 419 us: 1.02x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 6.94 us: 1.02x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.48 ms: 1.02x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 53.6 ms: 1.03x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 38.4 ms: 1.03x slower                                                   |
| pidigits                         | 166 ms                                                         | 171 ms: 1.03x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.56 ms: 1.03x slower                                                   |
| coverage                         | 31.2 ms                                                        | 32.3 ms: 1.04x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 45.6 ms: 1.04x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 136 us: 1.04x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 129 ms: 1.05x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.25 ms: 1.05x slower                                                   |
| pylint                           | 106 ms                                                         | 111 ms: 1.05x slower                                                    |
| raytrace                         | 109 ms                                                         | 115 ms: 1.06x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.7 ms: 1.06x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.16 ms: 1.06x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 45.9 ms: 1.07x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 102 ms: 1.08x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.98 ms: 1.11x slower                                                   |
| nbody                            | 42.5 ms                                                        | 47.4 ms: 1.12x slower                                                   |
| django_template                  | 12.5 ms                                                        | 13.9 ms: 1.12x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.7 ms: 1.12x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.7 ms: 1.18x slower                                                   |
| many_optionals                   | 200 us                                                         | 242 us: 1.21x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 251 ms: 1.21x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.40 ms: 1.50x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.5 ms: 3.02x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.06x faster                                                            |

Benchmark hidden because not significant (5): html5lib, sqlite_synth, docutils, json_loads, xml_etree_parse
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250712-3.15.0a0-47b01da-CLANG/bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.061x faster

# HPT report

- Reliability score: 99.97% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.09x