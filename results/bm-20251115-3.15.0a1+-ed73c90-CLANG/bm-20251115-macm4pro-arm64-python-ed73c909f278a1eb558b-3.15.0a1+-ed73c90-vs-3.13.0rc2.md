# Results vs. 3.13.0rc2

- fork: python
- ref: ed73c909f278a1eb558b
- machine: darwin-arm64
- commit hash: ed73c90
- commit date: 2025-11-15
- overall geometric mean: 1.068x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 110 ms: 1.01x faster                                                     |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                   |
| html5lib       | 23.1 ms                                                        | 21.1 ms: 1.10x faster                                                    |
| sphinx         | 409 ms                                                         | 390 ms: 1.05x faster                                                     |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 220 ms: 2.38x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 222 ms: 2.34x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 218 ms: 1.86x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 226 ms: 1.71x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 98.1 ms: 1.45x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 96.9 ms: 1.37x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 138 ms: 1.35x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 139 ms: 1.33x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 253 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 252 ms: 1.16x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 105 ms: 1.16x faster                                                     |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 39.8 ms: 1.09x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 241 ms: 1.16x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 124 ms: 1.21x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.9 ms: 2.76x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.20x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.6 ms: 1.14x faster                                                    |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| nbody          | 42.5 ms                                                        | 47.2 ms: 1.11x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 43.7 ms: 1.10x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.54 ms: 1.05x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 10.3 ms: 1.04x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 98.2 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 773 ms: 1.29x faster                                                     |
| json_dumps           | 4.65 ms                                                        | 3.84 ms: 1.21x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 38.9 ms: 1.18x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 32.6 ms: 1.10x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 91.7 us: 1.09x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 23.5 ms: 1.08x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.5 us: 1.03x faster                                                    |
| pickle_pure_python   | 130 us                                                         | 135 us: 1.04x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.10x faster                                                             |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.74 ms: 1.01x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.20 ms: 1.04x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.40 ms: 1.06x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 20.2 ms: 1.06x faster                                                    |
| mako            | 4.41 ms                                                        | 4.62 ms: 1.05x slower                                                    |
| django_template | 12.5 ms                                                        | 14.1 ms: 1.13x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.01x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 220 ms: 2.38x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 222 ms: 2.34x faster                                                     |
| mdp                              | 1.06 sec                                                       | 521 ms: 2.03x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 218 ms: 1.86x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 226 ms: 1.71x faster                                                     |
| deepcopy                         | 145 us                                                         | 97.0 us: 1.49x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.1 us: 1.49x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 98.1 ms: 1.45x faster                                                    |
| go                               | 72.6 ms                                                        | 51.0 ms: 1.42x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 96.9 ms: 1.37x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 138 ms: 1.35x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 139 ms: 1.33x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.2 ms: 1.30x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 773 ms: 1.29x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.04 us: 1.25x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.84 ms: 1.21x faster                                                    |
| pyflate                          | 222 ms                                                         | 185 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 253 ms: 1.19x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.9 ms: 1.18x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 252 ms: 1.16x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 105 ms: 1.16x faster                                                     |
| richards                         | 22.1 ms                                                        | 19.1 ms: 1.16x faster                                                    |
| float                            | 31.4 ms                                                        | 27.6 ms: 1.14x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 22.1 ms: 1.12x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.58 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 32.6 ms: 1.10x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 21.1 ms: 1.10x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 43.7 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 39.8 ms: 1.09x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 91.7 us: 1.09x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.83 ms: 1.08x faster                                                    |
| generators                       | 15.7 ms                                                        | 14.5 ms: 1.08x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.4 ms: 1.08x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 23.5 ms: 1.08x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 927 us: 1.07x faster                                                     |
| genshi_text                      | 9.97 ms                                                        | 9.40 ms: 1.06x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 303 ms: 1.06x faster                                                     |
| genshi_xml                       | 21.4 ms                                                        | 20.2 ms: 1.06x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 615 ms: 1.06x faster                                                     |
| thrift                           | 309 us                                                         | 295 us: 1.05x faster                                                     |
| sphinx                           | 409 ms                                                         | 390 ms: 1.05x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.54 ms: 1.05x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.7 ms: 1.04x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                    |
| pycparser                        | 470 ms                                                         | 452 ms: 1.04x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 10.3 ms: 1.04x faster                                                    |
| json                             | 1.94 ms                                                        | 1.88 ms: 1.03x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.5 us: 1.03x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.17 us: 1.03x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.33 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| logging_format                   | 2.45 us                                                        | 2.39 us: 1.02x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 121 ms: 1.02x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                   |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 63.5 us: 1.02x faster                                                    |
| deltablue                        | 1.45 ms                                                        | 1.43 ms: 1.02x faster                                                    |
| 2to3                             | 112 ms                                                         | 110 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| comprehensions                   | 6.80 us                                                        | 6.85 us: 1.01x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 416 us: 1.01x slower                                                     |
| sqlite_synth                     | 948 ns                                                         | 957 ns: 1.01x slower                                                     |
| gc_traversal                     | 2.04 ms                                                        | 2.06 ms: 1.01x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 43.3 ms: 1.01x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.74 ms: 1.01x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 97.0 ms: 1.02x slower                                                    |
| fannkuch                         | 179 ms                                                         | 182 ms: 1.02x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 48.8 ms: 1.02x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 163 ms: 1.02x slower                                                     |
| pylint                           | 106 ms                                                         | 108 ms: 1.02x slower                                                     |
| dask                             | 525 ms                                                         | 538 ms: 1.02x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 53.6 ms: 1.03x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 45.1 ms: 1.03x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 41.9 ns: 1.03x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.3 ms: 1.03x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 98.2 ms: 1.04x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 38.7 ms: 1.04x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 135 us: 1.04x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.85 ms: 1.04x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.20 ms: 1.04x slower                                                    |
| raytrace                         | 109 ms                                                         | 114 ms: 1.05x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.62 ms: 1.05x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.5 ms: 1.05x slower                                                    |
| nbody                            | 42.5 ms                                                        | 47.2 ms: 1.11x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.6 ms: 1.12x slower                                                    |
| django_template                  | 12.5 ms                                                        | 14.1 ms: 1.13x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 43.4 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 241 ms: 1.16x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 124 ms: 1.21x slower                                                     |
| many_optionals                   | 200 us                                                         | 349 us: 1.74x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.9 ms: 2.76x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 17.4 ms: 2.78x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x faster                                                             |

Benchmark hidden because not significant (1): xml_etree_parse
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20251115-3.15.0a1+-ed73c90-CLANG/bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1+-ed73c90.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.068x faster

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.17x