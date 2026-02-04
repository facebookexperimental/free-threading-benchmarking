# Results vs. 3.13.0rc2

- fork: python
- ref: 9d0c7432ea40ab3f73af
- machine: darwin-arm64
- commit hash: 9d0c743
- commit date: 2026-02-03
- overall geometric mean: 1.050x faster
- HPT reliability: 87.96%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5+-9d0c743 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 114 ms: 1.02x slower                                                     |
| docutils       | 1.05 sec                                                       | 960 ms: 1.09x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.0 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5+-9d0c743 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 230 ms: 2.28x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 232 ms: 2.24x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 229 ms: 1.77x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 244 ms: 1.59x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 139 ms: 1.33x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.29x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.28x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 145 ms: 1.27x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 247 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 256 ms: 1.15x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                     |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 9.98 ms: 1.08x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 182 ms: 1.06x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 45.1 ms: 1.04x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 239 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 126 ms: 1.23x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 89.7 ms: 3.10x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.16x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5+-9d0c743 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.8 ms: 1.13x faster                                                    |
| pidigits       | 166 ms                                                         | 156 ms: 1.07x faster                                                     |
| nbody          | 42.5 ms                                                        | 54.9 ms: 1.29x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5+-9d0c743 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 8.94 ms: 1.20x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.41 ms: 1.14x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 91.0 ms: 1.04x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 49.2 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5+-9d0c743 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.86 ms: 1.20x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 835 ms: 1.20x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.5 ms: 1.17x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 58.5 ms: 1.07x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.9 us: 1.01x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.2 ms: 1.01x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.2 ms: 1.03x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 104 us: 1.05x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 141 us: 1.08x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5+-9d0c743 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.62 ms: 1.11x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.00 ms: 1.18x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5+-9d0c743 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 21.8 ms: 1.02x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 10.6 ms: 1.06x slower                                                    |
| django_template | 12.5 ms                                                        | 14.9 ms: 1.19x slower                                                    |
| mako            | 4.41 ms                                                        | 5.34 ms: 1.21x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.12x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5+-9d0c743 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 763 us: 2.67x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 230 ms: 2.28x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 232 ms: 2.24x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 493 us: 2.01x faster                                                     |
| mdp                              | 1.06 sec                                                       | 589 ms: 1.79x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 229 ms: 1.77x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 3.94 ms: 1.59x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 244 ms: 1.59x faster                                                     |
| k_core                           | 1.46 sec                                                       | 985 ms: 1.49x faster                                                     |
| deepcopy                         | 145 us                                                         | 101 us: 1.44x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.1 us: 1.36x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 139 ms: 1.33x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.29x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.28x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 145 ms: 1.27x faster                                                     |
| go                               | 72.6 ms                                                        | 57.9 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 247 ms: 1.22x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 779 ns: 1.22x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.86 ms: 1.20x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 835 ms: 1.20x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 8.94 ms: 1.20x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 54.1 ms: 1.18x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.10 us: 1.18x faster                                                    |
| pyflate                          | 222 ms                                                         | 189 ms: 1.18x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.5 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 256 ms: 1.15x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.41 ms: 1.14x faster                                                    |
| float                            | 31.4 ms                                                        | 27.8 ms: 1.13x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 17.8 ms: 1.12x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.92 sec: 1.11x faster                                                   |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                     |
| docutils                         | 1.05 sec                                                       | 960 ms: 1.09x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 9.98 ms: 1.08x faster                                                    |
| fannkuch                         | 179 ms                                                         | 167 ms: 1.07x faster                                                     |
| pidigits                         | 166 ms                                                         | 156 ms: 1.07x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 58.5 ms: 1.07x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 182 ms: 1.06x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.5 ms: 1.06x faster                                                    |
| pycparser                        | 470 ms                                                         | 445 ms: 1.06x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 22.0 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                                     |
| regex_dna                        | 94.6 ms                                                        | 91.0 ms: 1.04x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.99 ms: 1.03x faster                                                    |
| json                             | 1.94 ms                                                        | 1.90 ms: 1.02x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 124 ms: 1.00x slower                                                     |
| dask                             | 525 ms                                                         | 528 ms: 1.01x slower                                                     |
| json_loads                       | 10.8 us                                                        | 10.9 us: 1.01x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.2 ms: 1.01x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 25.1 ms: 1.02x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 663 ms: 1.02x slower                                                     |
| genshi_xml                       | 21.4 ms                                                        | 21.8 ms: 1.02x slower                                                    |
| 2to3                             | 112 ms                                                         | 114 ms: 1.02x slower                                                     |
| regex_compile                    | 47.9 ms                                                        | 49.2 ms: 1.03x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.2 ms: 1.03x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.84 ms: 1.04x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 45.1 ms: 1.04x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 104 us: 1.05x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 42.6 ns: 1.05x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.34 us: 1.05x slower                                                    |
| thrift                           | 309 us                                                         | 325 us: 1.05x slower                                                     |
| logging_format                   | 2.45 us                                                        | 2.58 us: 1.05x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 10.6 ms: 1.06x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.03 ms: 1.06x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 31.8 ms: 1.07x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 69.3 us: 1.07x slower                                                    |
| pylint                           | 106 ms                                                         | 114 ms: 1.08x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 141 us: 1.08x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.58 ms: 1.09x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 52.6 ms: 1.10x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.8 ms: 1.10x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.62 ms: 1.11x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 41.7 ms: 1.12x slower                                                    |
| shortest_path                    | 225 ms                                                         | 252 ms: 1.12x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 107 ms: 1.12x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 58.9 ms: 1.13x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 182 ms: 1.14x slower                                                     |
| raytrace                         | 109 ms                                                         | 124 ms: 1.14x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 239 ms: 1.15x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 50.3 ms: 1.15x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 44.3 ms: 1.17x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.00 ms: 1.18x slower                                                    |
| connected_components             | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 8.00 us: 1.18x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.09 ms: 1.18x slower                                                    |
| django_template                  | 12.5 ms                                                        | 14.9 ms: 1.19x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.34 ms: 1.21x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.0 ms: 1.22x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 126 ms: 1.23x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 41.9 ms: 1.25x slower                                                    |
| many_optionals                   | 200 us                                                         | 250 us: 1.25x slower                                                     |
| generators                       | 15.7 ms                                                        | 20.0 ms: 1.27x slower                                                    |
| nbody                            | 42.5 ms                                                        | 54.9 ms: 1.29x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 549 us: 1.33x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 58.1 ms: 1.36x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 89.7 ms: 3.10x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                                             |

Benchmark hidden because not significant (3): sphinx, pprint_safe_repr, richards
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260203-3.15.0a5+-9d0c743-NOGIL/bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5+-9d0c743.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.050x faster

# HPT report

- Reliability score: 87.96% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.31x