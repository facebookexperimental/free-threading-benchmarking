# Results vs. 3.13.0rc2

- fork: python
- ref: 645f5c4a737b3eab29d0
- machine: darwin-arm64
- commit hash: 645f5c4
- commit date: 2026-02-14
- overall geometric mean: 1.098x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 109 ms: 1.03x faster                                                     |
| docutils       | 1.05 sec                                                       | 994 ms: 1.05x faster                                                     |
| html5lib       | 23.1 ms                                                        | 20.8 ms: 1.11x faster                                                    |
| sphinx         | 409 ms                                                         | 383 ms: 1.07x faster                                                     |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 213 ms: 2.47x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 211 ms: 2.46x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 219 ms: 1.85x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 218 ms: 1.77x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 97.0 ms: 1.47x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 132 ms: 1.41x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 94.4 ms: 1.40x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 134 ms: 1.38x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 245 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 250 ms: 1.17x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                     |
| async_generators                 | 193 ms                                                         | 172 ms: 1.13x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 39.3 ms: 1.10x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 231 ms: 1.11x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 117 ms: 1.14x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.6 ms: 2.72x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.23x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.9 ms: 1.09x faster                                                    |
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| nbody          | 42.5 ms                                                        | 46.4 ms: 1.09x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 43.3 ms: 1.11x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.80 ms: 1.09x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 96.8 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 783 ms: 1.28x faster                                                     |
| json_dumps           | 4.65 ms                                                        | 3.73 ms: 1.25x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 38.3 ms: 1.20x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 32.4 ms: 1.10x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 23.4 ms: 1.08x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 92.6 us: 1.07x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.5 us: 1.03x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 60.8 ms: 1.03x faster                                                    |
| pickle_pure_python   | 130 us                                                         | 136 us: 1.04x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.11x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.66 ms: 1.00x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.27 ms: 1.05x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.08 ms: 1.10x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 19.8 ms: 1.08x faster                                                    |
| mako            | 4.41 ms                                                        | 4.73 ms: 1.07x slower                                                    |
| django_template | 12.5 ms                                                        | 13.9 ms: 1.11x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.00x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 213 ms: 2.47x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 211 ms: 2.46x faster                                                     |
| mdp                              | 1.06 sec                                                       | 519 ms: 2.04x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 219 ms: 1.85x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 218 ms: 1.77x faster                                                     |
| k_core                           | 1.46 sec                                                       | 891 ms: 1.64x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 3.82 ms: 1.64x faster                                                    |
| deepcopy                         | 145 us                                                         | 93.8 us: 1.55x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 97.0 ms: 1.47x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.3 us: 1.46x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 132 ms: 1.41x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 94.4 ms: 1.40x faster                                                    |
| go                               | 72.6 ms                                                        | 51.7 ms: 1.40x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 134 ms: 1.38x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 48.4 ms: 1.32x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.00 us: 1.29x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 783 ms: 1.28x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.73 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 245 ms: 1.23x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.3 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 250 ms: 1.17x faster                                                     |
| pyflate                          | 222 ms                                                         | 189 ms: 1.17x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                     |
| async_generators                 | 193 ms                                                         | 172 ms: 1.13x faster                                                     |
| richards                         | 22.1 ms                                                        | 19.6 ms: 1.12x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 20.8 ms: 1.11x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 22.3 ms: 1.11x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 43.3 ms: 1.11x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 32.4 ms: 1.10x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 39.3 ms: 1.10x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.08 ms: 1.10x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 905 us: 1.10x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.80 ms: 1.09x faster                                                    |
| float                            | 31.4 ms                                                        | 28.9 ms: 1.09x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.09x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 23.4 ms: 1.08x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.63 ms: 1.08x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                    |
| genshi_xml                       | 21.4 ms                                                        | 19.8 ms: 1.08x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 92.6 us: 1.07x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.5 ms: 1.07x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.87 ms: 1.07x faster                                                    |
| sphinx                           | 409 ms                                                         | 383 ms: 1.07x faster                                                     |
| generators                       | 15.7 ms                                                        | 14.8 ms: 1.06x faster                                                    |
| docutils                         | 1.05 sec                                                       | 994 ms: 1.05x faster                                                     |
| logging_silent                   | 40.6 ns                                                        | 38.7 ns: 1.05x faster                                                    |
| json                             | 1.94 ms                                                        | 1.85 ms: 1.05x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 307 ms: 1.05x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| pprint_pformat                   | 650 ms                                                         | 628 ms: 1.03x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.03x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.28 ms: 1.03x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.5 us: 1.03x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.37 us: 1.03x faster                                                    |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| logging_simple                   | 2.24 us                                                        | 2.18 us: 1.03x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 60.8 ms: 1.03x faster                                                    |
| 2to3                             | 112 ms                                                         | 109 ms: 1.03x faster                                                     |
| pycparser                        | 470 ms                                                         | 458 ms: 1.03x faster                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.3 ms: 1.02x faster                                                    |
| deltablue                        | 1.45 ms                                                        | 1.42 ms: 1.02x faster                                                    |
| thrift                           | 309 us                                                         | 303 us: 1.02x faster                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 63.5 us: 1.02x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 936 ns: 1.01x faster                                                     |
| scimark_fft                      | 124 ms                                                         | 122 ms: 1.01x faster                                                     |
| fannkuch                         | 179 ms                                                         | 177 ms: 1.01x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 2.02 ms: 1.01x faster                                                    |
| coverage                         | 31.2 ms                                                        | 30.9 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                     |
| python_startup                   | 8.63 ms                                                        | 8.66 ms: 1.00x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 43.9 ms: 1.00x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 413 us: 1.00x slower                                                     |
| shortest_path                    | 225 ms                                                         | 226 ms: 1.00x slower                                                     |
| connected_components             | 208 ms                                                         | 210 ms: 1.01x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 6.88 us: 1.01x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 48.5 ms: 1.01x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 97.2 ms: 1.02x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 96.8 ms: 1.02x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 164 ms: 1.03x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 38.3 ms: 1.03x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 53.9 ms: 1.03x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 136 us: 1.04x slower                                                     |
| chaos                            | 24.3 ms                                                        | 25.5 ms: 1.05x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.27 ms: 1.05x slower                                                    |
| pylint                           | 106 ms                                                         | 112 ms: 1.06x slower                                                     |
| raytrace                         | 109 ms                                                         | 115 ms: 1.06x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 45.4 ms: 1.06x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.73 ms: 1.07x slower                                                    |
| nbody                            | 42.5 ms                                                        | 46.4 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 231 ms: 1.11x slower                                                     |
| django_template                  | 12.5 ms                                                        | 13.9 ms: 1.11x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 117 ms: 1.14x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.03 ms: 1.14x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 38.5 ms: 1.15x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 44.2 ms: 1.17x slower                                                    |
| many_optionals                   | 200 us                                                         | 241 us: 1.20x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.6 ms: 2.72x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.10x faster                                                             |
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260214-3.15.0a6+-645f5c4-CLANG/bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.098x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.17x