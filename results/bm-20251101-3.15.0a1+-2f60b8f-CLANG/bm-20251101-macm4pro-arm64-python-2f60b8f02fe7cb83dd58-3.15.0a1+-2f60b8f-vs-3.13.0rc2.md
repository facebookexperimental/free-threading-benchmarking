# Results vs. 3.13.0rc2

- fork: python
- ref: 2f60b8f02fe7cb83dd58
- machine: darwin-arm64
- commit hash: 2f60b8f
- commit date: 2025-11-01
- overall geometric mean: 1.064x faster
- HPT reliability: 99.97%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 110 ms: 1.01x faster                                                     |
| html5lib       | 23.1 ms                                                        | 21.0 ms: 1.10x faster                                                    |
| sphinx         | 409 ms                                                         | 397 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 221 ms: 2.38x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 221 ms: 2.35x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 219 ms: 1.85x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 225 ms: 1.71x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 98.4 ms: 1.45x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 96.6 ms: 1.37x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 138 ms: 1.35x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 139 ms: 1.33x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 253 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 253 ms: 1.16x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                     |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 40.1 ms: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 242 ms: 1.16x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 125 ms: 1.22x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.7 ms: 2.75x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.20x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.8 ms: 1.13x faster                                                    |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 47.9 ms: 1.13x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 43.8 ms: 1.10x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 11.2 ms: 1.05x slower                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.76 ms: 1.09x slower                                                    |
| regex_dna      | 94.6 ms                                                        | 105 ms: 1.11x slower                                                     |
| Geometric mean | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 786 ms: 1.27x faster                                                     |
| json_dumps           | 4.65 ms                                                        | 3.84 ms: 1.21x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.3 ms: 1.17x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 89.9 us: 1.11x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 32.7 ms: 1.10x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 23.2 ms: 1.09x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.6 us: 1.02x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 63.4 ms: 1.02x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 137 us: 1.05x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.10x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.72 ms: 1.01x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.20 ms: 1.04x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.32 ms: 1.07x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 20.4 ms: 1.05x faster                                                    |
| mako            | 4.41 ms                                                        | 4.58 ms: 1.04x slower                                                    |
| django_template | 12.5 ms                                                        | 14.1 ms: 1.13x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.01x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 221 ms: 2.38x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 221 ms: 2.35x faster                                                     |
| mdp                              | 1.06 sec                                                       | 524 ms: 2.02x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 219 ms: 1.85x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 225 ms: 1.71x faster                                                     |
| k_core                           | 1.46 sec                                                       | 897 ms: 1.63x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 11.1 us: 1.48x faster                                                    |
| deepcopy                         | 145 us                                                         | 98.2 us: 1.48x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 98.4 ms: 1.45x faster                                                    |
| go                               | 72.6 ms                                                        | 51.2 ms: 1.42x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 96.6 ms: 1.37x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 138 ms: 1.35x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 139 ms: 1.33x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.0 ms: 1.31x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 786 ms: 1.27x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.04 us: 1.24x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.84 ms: 1.21x faster                                                    |
| pyflate                          | 222 ms                                                         | 185 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 253 ms: 1.19x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.3 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 253 ms: 1.16x faster                                                     |
| richards                         | 22.1 ms                                                        | 19.2 ms: 1.15x faster                                                    |
| float                            | 31.4 ms                                                        | 27.8 ms: 1.13x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                     |
| richards_super                   | 24.7 ms                                                        | 21.9 ms: 1.13x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 89.9 us: 1.11x faster                                                    |
| generators                       | 15.7 ms                                                        | 14.2 ms: 1.10x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 21.0 ms: 1.10x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 32.7 ms: 1.10x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 43.8 ms: 1.10x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.60 ms: 1.09x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 23.2 ms: 1.09x faster                                                    |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.09x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 40.1 ms: 1.08x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.86 ms: 1.07x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.32 ms: 1.07x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.5 ms: 1.07x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 934 us: 1.06x faster                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 305 ms: 1.06x faster                                                     |
| pprint_pformat                   | 650 ms                                                         | 616 ms: 1.05x faster                                                     |
| thrift                           | 309 us                                                         | 293 us: 1.05x faster                                                     |
| genshi_xml                       | 21.4 ms                                                        | 20.4 ms: 1.05x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.7 ms: 1.04x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                    |
| bench_thread_pool                | 412 us                                                         | 399 us: 1.03x faster                                                     |
| sphinx                           | 409 ms                                                         | 397 ms: 1.03x faster                                                     |
| logging_simple                   | 2.24 us                                                        | 2.18 us: 1.03x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.03x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 121 ms: 1.03x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| logging_format                   | 2.45 us                                                        | 2.39 us: 1.02x faster                                                    |
| json                             | 1.94 ms                                                        | 1.90 ms: 1.02x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 63.1 us: 1.02x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.36 ms: 1.02x faster                                                    |
| pycparser                        | 470 ms                                                         | 461 ms: 1.02x faster                                                     |
| json_loads                       | 10.8 us                                                        | 10.6 us: 1.02x faster                                                    |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| 2to3                             | 112 ms                                                         | 110 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| deltablue                        | 1.45 ms                                                        | 1.44 ms: 1.00x faster                                                    |
| shortest_path                    | 225 ms                                                         | 224 ms: 1.00x faster                                                     |
| connected_components             | 208 ms                                                         | 210 ms: 1.01x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 8.72 ms: 1.01x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 6.90 us: 1.01x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 63.4 ms: 1.02x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.08 ms: 1.02x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 163 ms: 1.02x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 41.5 ns: 1.02x slower                                                    |
| coverage                         | 31.2 ms                                                        | 31.9 ms: 1.02x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 49.1 ms: 1.02x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 98.0 ms: 1.03x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 973 ns: 1.03x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 54.1 ms: 1.03x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 45.2 ms: 1.03x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 44.3 ms: 1.04x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.58 ms: 1.04x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.85 ms: 1.04x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 38.8 ms: 1.04x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.20 ms: 1.04x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 137 us: 1.05x slower                                                     |
| raytrace                         | 109 ms                                                         | 114 ms: 1.05x slower                                                     |
| regex_v8                         | 10.7 ms                                                        | 11.2 ms: 1.05x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.5 ms: 1.05x slower                                                    |
| pylint                           | 106 ms                                                         | 113 ms: 1.07x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 41.3 ms: 1.09x slower                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.76 ms: 1.09x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 105 ms: 1.11x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 37.9 ms: 1.13x slower                                                    |
| django_template                  | 12.5 ms                                                        | 14.1 ms: 1.13x slower                                                    |
| nbody                            | 42.5 ms                                                        | 47.9 ms: 1.13x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 242 ms: 1.16x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 125 ms: 1.22x slower                                                     |
| many_optionals                   | 200 us                                                         | 348 us: 1.74x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.7 ms: 2.75x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 17.4 ms: 2.78x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.06x faster                                                             |

Benchmark hidden because not significant (3): docutils, fannkuch, dask
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20251101-3.15.0a1+-2f60b8f-CLANG/bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.064x faster

# HPT report

- Reliability score: 99.97% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.16x