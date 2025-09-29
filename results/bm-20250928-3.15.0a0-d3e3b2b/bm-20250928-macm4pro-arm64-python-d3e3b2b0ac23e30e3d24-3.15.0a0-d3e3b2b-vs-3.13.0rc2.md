# Results vs. 3.13.0rc2

- fork: python
- ref: d3e3b2b0ac23e30e3d24
- machine: darwin-arm64
- commit hash: d3e3b2b
- commit date: 2025-09-28
- overall geometric mean: 1.016x faster
- HPT reliability: 84.81%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250928-macm4pro-arm64-python-d3e3b2b0ac23e30e3d24-3.15.0a0-d3e3b2b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.03x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.00x faster                                                  |
| html5lib       | 23.1 ms                                                        | 24.3 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250928-macm4pro-arm64-python-d3e3b2b0ac23e30e3d24-3.15.0a0-d3e3b2b |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 252 ms: 2.09x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 258 ms: 2.02x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 255 ms: 1.59x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 256 ms: 1.51x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 149 ms: 1.24x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 265 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.97 ms: 1.08x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.1 ms: 1.03x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 249 ms: 1.19x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.9 ms: 3.07x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250928-macm4pro-arm64-python-d3e3b2b0ac23e30e3d24-3.15.0a0-d3e3b2b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| float          | 31.4 ms                                                        | 31.3 ms: 1.00x faster                                                   |
| nbody          | 42.5 ms                                                        | 48.6 ms: 1.14x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250928-macm4pro-arm64-python-d3e3b2b0ac23e30e3d24-3.15.0a0-d3e3b2b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.86 ms: 1.09x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 95.7 ms: 1.01x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 49.3 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250928-macm4pro-arm64-python-d3e3b2b0ac23e30e3d24-3.15.0a0-d3e3b2b |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.89 ms: 1.20x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 912 ms: 1.10x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.6 ms: 1.03x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.5 ms: 1.00x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 102 us: 1.03x slower                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 65.7 ms: 1.05x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 149 us: 1.15x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (2): xml_etree_generate, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250928-macm4pro-arm64-python-d3e3b2b0ac23e30e3d24-3.15.0a0-d3e3b2b |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.67 ms: 1.00x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.20 ms: 1.04x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250928-macm4pro-arm64-python-d3e3b2b0ac23e30e3d24-3.15.0a0-d3e3b2b |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 10.1 ms: 1.01x slower                                                   |
| genshi_xml      | 21.4 ms                                                        | 22.2 ms: 1.04x slower                                                   |
| mako            | 4.41 ms                                                        | 4.96 ms: 1.12x slower                                                   |
| django_template | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.10x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250928-macm4pro-arm64-python-d3e3b2b0ac23e30e3d24-3.15.0a0-d3e3b2b |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 252 ms: 2.09x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 258 ms: 2.02x faster                                                    |
| mdp                              | 1.06 sec                                                       | 543 ms: 1.95x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 255 ms: 1.59x faster                                                    |
| k_core                           | 1.46 sec                                                       | 955 ms: 1.53x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 256 ms: 1.51x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.5 us: 1.32x faster                                                   |
| deepcopy                         | 145 us                                                         | 111 us: 1.31x faster                                                    |
| go                               | 72.6 ms                                                        | 56.9 ms: 1.27x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 50.3 ms: 1.27x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 149 ms: 1.24x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.89 ms: 1.20x faster                                                   |
| pyflate                          | 222 ms                                                         | 194 ms: 1.14x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 265 ms: 1.14x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.16 us: 1.12x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.10x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.1 ms: 1.10x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 912 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.09x faster                                                  |
| regex_v8                         | 10.7 ms                                                        | 9.86 ms: 1.09x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 9.97 ms: 1.08x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 923 us: 1.08x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.5 ms: 1.06x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.89 ms: 1.06x faster                                                   |
| shortest_path                    | 225 ms                                                         | 216 ms: 1.04x faster                                                    |
| connected_components             | 208 ms                                                         | 200 ms: 1.04x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.6 ms: 1.03x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.1 ms: 1.03x faster                                                   |
| richards                         | 22.1 ms                                                        | 21.6 ms: 1.02x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.37 ms: 1.02x faster                                                   |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.02x faster                                                    |
| json                             | 1.94 ms                                                        | 1.91 ms: 1.01x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 24.4 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.00x faster                                                  |
| float                            | 31.4 ms                                                        | 31.3 ms: 1.00x faster                                                   |
| python_startup                   | 8.63 ms                                                        | 8.67 ms: 1.00x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.5 ms: 1.00x slower                                                   |
| sqlite_synth                     | 948 ns                                                         | 953 ns: 1.01x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 30.1 ms: 1.01x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 125 ms: 1.01x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 10.1 ms: 1.01x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 95.7 ms: 1.01x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.07 ms: 1.01x slower                                                   |
| thrift                           | 309 us                                                         | 313 us: 1.01x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 41.3 ns: 1.02x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 420 us: 1.02x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 44.7 ms: 1.02x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 102 us: 1.03x slower                                                    |
| 2to3                             | 112 ms                                                         | 115 ms: 1.03x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 49.3 ms: 1.03x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 49.5 ms: 1.03x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.84 ms: 1.03x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 22.2 ms: 1.04x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 674 ms: 1.04x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 99.3 ms: 1.04x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.20 ms: 1.04x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 39.0 ms: 1.05x slower                                                   |
| coverage                         | 31.2 ms                                                        | 32.7 ms: 1.05x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 338 ms: 1.05x slower                                                    |
| pycparser                        | 470 ms                                                         | 494 ms: 1.05x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 24.3 ms: 1.05x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 65.7 ms: 1.05x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.58 us: 1.05x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.36 us: 1.06x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 55.4 ms: 1.06x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 169 ms: 1.06x slower                                                    |
| pylint                           | 106 ms                                                         | 112 ms: 1.06x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.55 ms: 1.07x slower                                                   |
| raytrace                         | 109 ms                                                         | 120 ms: 1.10x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.8 ms: 1.11x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 42.1 ms: 1.11x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.5 ms: 1.11x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.96 ms: 1.12x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 48.3 ms: 1.13x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.8 ms: 1.14x slower                                                   |
| nbody                            | 42.5 ms                                                        | 48.6 ms: 1.14x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.81 us: 1.15x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 149 us: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 249 ms: 1.19x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                    |
| many_optionals                   | 200 us                                                         | 331 us: 1.65x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 18.3 ms: 2.92x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.9 ms: 3.07x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (6): sphinx, typing_runtime_protocols, hexiom, xml_etree_generate, fannkuch, json_loads
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250928-3.15.0a0-d3e3b2b/bm-20250928-macm4pro-arm64-python-d3e3b2b0ac23e30e3d24-3.15.0a0-d3e3b2b.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.016x faster

# HPT report

- Reliability score: 84.81% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x