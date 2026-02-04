# Results vs. 3.13.0rc2

- fork: python
- ref: 9d0c7432ea40ab3f73af
- machine: darwin-arm64
- commit hash: 9d0c743
- commit date: 2026-02-03
- overall geometric mean: 1.103x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5+-9d0c743 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 110 ms: 1.02x faster                                                     |
| docutils       | 1.05 sec                                                       | 981 ms: 1.07x faster                                                     |
| html5lib       | 23.1 ms                                                        | 20.8 ms: 1.11x faster                                                    |
| sphinx         | 409 ms                                                         | 380 ms: 1.08x faster                                                     |
| Geometric mean | (ref)                                                          | 1.07x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5+-9d0c743 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 217 ms: 2.42x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 221 ms: 2.36x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 225 ms: 1.80x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 224 ms: 1.73x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 134 ms: 1.39x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 95.7 ms: 1.39x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 137 ms: 1.35x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 247 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 253 ms: 1.16x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                     |
| async_generators                 | 193 ms                                                         | 173 ms: 1.12x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 39.6 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.91 ms: 1.08x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 183 ms: 1.06x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 215 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 231 ms: 1.11x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 119 ms: 1.16x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.9 ms: 2.73x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.22x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5+-9d0c743 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 26.9 ms: 1.17x faster                                                    |
| pidigits       | 166 ms                                                         | 156 ms: 1.06x faster                                                     |
| nbody          | 42.5 ms                                                        | 43.1 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                          | 1.07x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5+-9d0c743 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.41 ms: 1.14x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.43 ms: 1.13x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 44.8 ms: 1.07x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 92.4 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                          | 1.09x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5+-9d0c743 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 813 ms: 1.23x faster                                                     |
| json_dumps           | 4.65 ms                                                        | 3.79 ms: 1.23x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 38.2 ms: 1.21x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 33.8 ms: 1.06x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.0 ms: 1.06x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 95.4 us: 1.04x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 60.0 ms: 1.04x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.5 us: 1.03x faster                                                    |
| pickle_pure_python   | 130 us                                                         | 137 us: 1.05x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.09x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5+-9d0c743 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.66 ms: 1.00x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.25 ms: 1.05x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5+-9d0c743 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.49 ms: 1.05x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 20.7 ms: 1.03x faster                                                    |
| mako            | 4.41 ms                                                        | 4.68 ms: 1.06x slower                                                    |
| django_template | 12.5 ms                                                        | 14.4 ms: 1.16x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.03x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5+-9d0c743 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 217 ms: 2.42x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 221 ms: 2.36x faster                                                     |
| mdp                              | 1.06 sec                                                       | 526 ms: 2.01x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 225 ms: 1.80x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 224 ms: 1.73x faster                                                     |
| k_core                           | 1.46 sec                                                       | 894 ms: 1.64x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 3.94 ms: 1.59x faster                                                    |
| deepcopy                         | 145 us                                                         | 95.1 us: 1.53x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.4 us: 1.44x faster                                                    |
| go                               | 72.6 ms                                                        | 51.4 ms: 1.41x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 134 ms: 1.39x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 95.7 ms: 1.39x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 137 ms: 1.35x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 48.7 ms: 1.31x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.05 us: 1.24x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 813 ms: 1.23x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.79 ms: 1.23x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 247 ms: 1.22x faster                                                     |
| pyflate                          | 222 ms                                                         | 182 ms: 1.22x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.2 ms: 1.21x faster                                                    |
| float                            | 31.4 ms                                                        | 26.9 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 253 ms: 1.16x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                     |
| richards                         | 22.1 ms                                                        | 19.2 ms: 1.15x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.41 ms: 1.14x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 21.7 ms: 1.14x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.43 ms: 1.13x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 882 us: 1.13x faster                                                     |
| async_generators                 | 193 ms                                                         | 173 ms: 1.12x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 20.8 ms: 1.11x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.77 ms: 1.11x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.0 ms: 1.10x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.2 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 39.6 ms: 1.09x faster                                                    |
| fannkuch                         | 179 ms                                                         | 164 ms: 1.09x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 9.91 ms: 1.08x faster                                                    |
| sphinx                           | 409 ms                                                         | 380 ms: 1.08x faster                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 300 ms: 1.07x faster                                                     |
| regex_compile                    | 47.9 ms                                                        | 44.8 ms: 1.07x faster                                                    |
| docutils                         | 1.05 sec                                                       | 981 ms: 1.07x faster                                                     |
| pprint_pformat                   | 650 ms                                                         | 609 ms: 1.07x faster                                                     |
| pidigits                         | 166 ms                                                         | 156 ms: 1.06x faster                                                     |
| scimark_fft                      | 124 ms                                                         | 116 ms: 1.06x faster                                                     |
| json                             | 1.94 ms                                                        | 1.83 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 183 ms: 1.06x faster                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 33.8 ms: 1.06x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.0 ms: 1.06x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.13 us: 1.05x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 61.5 us: 1.05x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.49 ms: 1.05x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.71 ms: 1.05x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.33 us: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 215 ms: 1.04x faster                                                     |
| pycparser                        | 470 ms                                                         | 450 ms: 1.04x faster                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 95.4 us: 1.04x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.23 ms: 1.04x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 60.0 ms: 1.04x faster                                                    |
| thrift                           | 309 us                                                         | 298 us: 1.04x faster                                                     |
| json_loads                       | 10.8 us                                                        | 10.5 us: 1.03x faster                                                    |
| genshi_xml                       | 21.4 ms                                                        | 20.7 ms: 1.03x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 922 ns: 1.03x faster                                                     |
| regex_dna                        | 94.6 ms                                                        | 92.4 ms: 1.02x faster                                                    |
| shortest_path                    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| connected_components             | 208 ms                                                         | 204 ms: 1.02x faster                                                     |
| spectral_norm                    | 43.7 ms                                                        | 43.0 ms: 1.02x faster                                                    |
| 2to3                             | 112 ms                                                         | 110 ms: 1.02x faster                                                     |
| logging_silent                   | 40.6 ns                                                        | 40.1 ns: 1.01x faster                                                    |
| deltablue                        | 1.45 ms                                                        | 1.44 ms: 1.01x faster                                                    |
| meteor_contest                   | 47.9 ms                                                        | 47.5 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 521 ms: 1.01x faster                                                     |
| python_startup                   | 8.63 ms                                                        | 8.66 ms: 1.00x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 37.4 ms: 1.00x slower                                                    |
| nbody                            | 42.5 ms                                                        | 43.1 ms: 1.01x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 43.6 ms: 1.02x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.08 ms: 1.02x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 6.96 us: 1.02x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 98.2 ms: 1.03x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 53.8 ms: 1.03x slower                                                    |
| raytrace                         | 109 ms                                                         | 112 ms: 1.03x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 166 ms: 1.04x slower                                                     |
| bench_thread_pool                | 412 us                                                         | 430 us: 1.05x slower                                                     |
| chaos                            | 24.3 ms                                                        | 25.4 ms: 1.05x slower                                                    |
| pylint                           | 106 ms                                                         | 111 ms: 1.05x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 137 us: 1.05x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.25 ms: 1.05x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.68 ms: 1.06x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 36.7 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 231 ms: 1.11x slower                                                     |
| generators                       | 15.7 ms                                                        | 18.0 ms: 1.15x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 43.7 ms: 1.16x slower                                                    |
| django_template                  | 12.5 ms                                                        | 14.4 ms: 1.16x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 119 ms: 1.16x slower                                                     |
| many_optionals                   | 200 us                                                         | 245 us: 1.22x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.9 ms: 2.73x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.10x faster                                                             |

Benchmark hidden because not significant (2): scimark_sparse_mat_mult, coverage
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260203-3.15.0a5+-9d0c743/bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5+-9d0c743.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.103x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.18x