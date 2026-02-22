# Results vs. 3.13.0rc2

- fork: python
- ref: 2be2dd5fc219a5c252d7
- machine: darwin-arm64
- commit hash: 2be2dd5
- commit date: 2026-02-21
- overall geometric mean: 1.079x faster
- HPT reliability: 99.96%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 114 ms: 1.03x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.01x faster                                                   |
| html5lib       | 23.1 ms                                                        | 21.6 ms: 1.07x faster                                                    |
| sphinx         | 409 ms                                                         | 392 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 221 ms: 2.36x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 226 ms: 2.32x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 229 ms: 1.77x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 226 ms: 1.71x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.42x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 97.1 ms: 1.37x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 136 ms: 1.36x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 138 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 252 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 250 ms: 1.18x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                     |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 39.9 ms: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 121 ms: 1.18x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.8 ms: 2.79x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.20x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.7 ms: 1.09x faster                                                    |
| pidigits       | 166 ms                                                         | 170 ms: 1.02x slower                                                     |
| nbody          | 42.5 ms                                                        | 46.2 ms: 1.09x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 43.8 ms: 1.09x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.94 ms: 1.08x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.50 ms: 1.07x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 99.7 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 783 ms: 1.28x faster                                                     |
| json_dumps           | 4.65 ms                                                        | 3.72 ms: 1.25x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.1 ms: 1.15x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 32.8 ms: 1.09x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 23.5 ms: 1.08x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 93.9 us: 1.06x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.01x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 64.8 ms: 1.04x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 136 us: 1.05x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.09x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.12 ms: 1.06x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.56 ms: 1.10x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.08x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.12 ms: 1.09x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 19.8 ms: 1.08x faster                                                    |
| mako            | 4.41 ms                                                        | 4.76 ms: 1.08x slower                                                    |
| django_template | 12.5 ms                                                        | 13.9 ms: 1.11x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.00x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 221 ms: 2.36x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 226 ms: 2.32x faster                                                     |
| mdp                              | 1.06 sec                                                       | 526 ms: 2.01x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 229 ms: 1.77x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 226 ms: 1.71x faster                                                     |
| k_core                           | 1.46 sec                                                       | 911 ms: 1.61x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 3.95 ms: 1.58x faster                                                    |
| deepcopy                         | 145 us                                                         | 96.3 us: 1.51x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.4 us: 1.44x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.42x faster                                                     |
| go                               | 72.6 ms                                                        | 51.8 ms: 1.40x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 97.1 ms: 1.37x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 136 ms: 1.36x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 138 ms: 1.34x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.6 ms: 1.29x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 783 ms: 1.28x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.03 us: 1.26x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.72 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 252 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 250 ms: 1.18x faster                                                     |
| pyflate                          | 222 ms                                                         | 192 ms: 1.16x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.1 ms: 1.15x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.1 ms: 1.10x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 43.8 ms: 1.09x faster                                                    |
| float                            | 31.4 ms                                                        | 28.7 ms: 1.09x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.12 ms: 1.09x faster                                                    |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                     |
| richards_super                   | 24.7 ms                                                        | 22.6 ms: 1.09x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 32.8 ms: 1.09x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 39.9 ms: 1.08x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.83 ms: 1.08x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 23.5 ms: 1.08x faster                                                    |
| genshi_xml                       | 21.4 ms                                                        | 19.8 ms: 1.08x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.94 ms: 1.08x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.50 ms: 1.07x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 21.6 ms: 1.07x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.68 ms: 1.06x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.7 ms: 1.06x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 93.9 us: 1.06x faster                                                    |
| generators                       | 15.7 ms                                                        | 14.9 ms: 1.06x faster                                                    |
| sphinx                           | 409 ms                                                         | 392 ms: 1.04x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 963 us: 1.03x faster                                                     |
| json                             | 1.94 ms                                                        | 1.89 ms: 1.03x faster                                                    |
| thrift                           | 309 us                                                         | 301 us: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 315 ms: 1.02x faster                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.3 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 63.7 us: 1.02x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 640 ms: 1.02x faster                                                     |
| coverage                         | 31.2 ms                                                        | 30.8 ms: 1.01x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 935 ns: 1.01x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.01x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.45 ms: 1.01x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 43.4 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                     |
| logging_simple                   | 2.24 us                                                        | 2.22 us: 1.01x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.43 us: 1.01x faster                                                    |
| fannkuch                         | 179 ms                                                         | 180 ms: 1.01x slower                                                     |
| bench_thread_pool                | 412 us                                                         | 414 us: 1.01x slower                                                     |
| shortest_path                    | 225 ms                                                         | 227 ms: 1.01x slower                                                     |
| chaos                            | 24.3 ms                                                        | 24.6 ms: 1.01x slower                                                    |
| connected_components             | 208 ms                                                         | 212 ms: 1.02x slower                                                     |
| pidigits                         | 166 ms                                                         | 170 ms: 1.02x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 41.6 ns: 1.02x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 43.8 ms: 1.02x slower                                                    |
| 2to3                             | 112 ms                                                         | 114 ms: 1.03x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 6.98 us: 1.03x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 38.3 ms: 1.03x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 98.2 ms: 1.03x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 164 ms: 1.03x slower                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 64.8 ms: 1.04x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 54.5 ms: 1.04x slower                                                    |
| raytrace                         | 109 ms                                                         | 114 ms: 1.05x slower                                                     |
| gc_traversal                     | 2.04 ms                                                        | 2.14 ms: 1.05x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 136 us: 1.05x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 50.3 ms: 1.05x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 99.7 ms: 1.05x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.12 ms: 1.06x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.76 ms: 1.08x slower                                                    |
| pylint                           | 106 ms                                                         | 114 ms: 1.08x slower                                                     |
| nbody                            | 42.5 ms                                                        | 46.2 ms: 1.09x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.56 ms: 1.10x slower                                                    |
| django_template                  | 12.5 ms                                                        | 13.9 ms: 1.11x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.04 ms: 1.15x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 39.0 ms: 1.16x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 121 ms: 1.18x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 46.3 ms: 1.22x slower                                                    |
| many_optionals                   | 200 us                                                         | 254 us: 1.27x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.8 ms: 2.79x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.08x faster                                                             |

Benchmark hidden because not significant (3): scimark_fft, deltablue, pycparser
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260221-3.15.0a6+-2be2dd5-CLANG/bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.079x faster

# HPT report

- Reliability score: 99.96% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.17x