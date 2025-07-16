# Results vs. 3.13.0rc2

- fork: python
- ref: cb59eaefeda5ff44ac0c
- machine: darwin-arm64
- commit hash: cb59eae
- commit date: 2025-07-15
- overall geometric mean: 1.021x faster
- HPT reliability: 80.64%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 116 ms: 1.04x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.05 sec: 1.01x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.0 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 251 ms: 2.09x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 256 ms: 2.03x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 257 ms: 1.57x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 259 ms: 1.49x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 149 ms: 1.25x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.24x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 112 ms: 1.19x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 266 ms: 1.13x faster                                                    |
| async_generators                 | 193 ms                                                         | 175 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 268 ms: 1.10x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.03x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.01x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.9 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 251 ms: 1.21x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 132 ms: 1.28x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.8 ms: 3.07x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.11x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.9 ms: 1.02x faster                                                   |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| nbody          | 42.5 ms                                                        | 49.5 ms: 1.16x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.84 ms: 1.09x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 48.7 ms: 1.02x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 97.6 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|---------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads         | 1000 ms                                                        | 930 ms: 1.07x faster                                                    |
| xml_etree_iterparse | 46.1 ms                                                        | 43.7 ms: 1.06x faster                                                   |
| json_dumps          | 4.65 ms                                                        | 4.44 ms: 1.05x faster                                                   |
| xml_etree_parse     | 62.4 ms                                                        | 61.6 ms: 1.01x faster                                                   |
| xml_etree_process   | 25.4 ms                                                        | 25.6 ms: 1.01x slower                                                   |
| pickle_pure_python  | 130 us                                                         | 149 us: 1.14x slower                                                    |
| Geometric mean      | (ref)                                                          | 1.00x faster                                                            |

Benchmark hidden because not significant (3): unpickle_pure_python, json_loads, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.56 ms: 1.01x faster                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.12 ms: 1.03x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 10.1 ms: 1.01x slower                                                   |
| genshi_xml      | 21.4 ms                                                        | 22.1 ms: 1.03x slower                                                   |
| mako            | 4.41 ms                                                        | 4.85 ms: 1.10x slower                                                   |
| django_template | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.09x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 251 ms: 2.09x faster                                                    |
| mdp                              | 1.06 sec                                                       | 518 ms: 2.04x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 256 ms: 2.03x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 257 ms: 1.57x faster                                                    |
| k_core                           | 1.46 sec                                                       | 948 ms: 1.54x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 259 ms: 1.49x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.6 us: 1.30x faster                                                   |
| deepcopy                         | 145 us                                                         | 111 us: 1.30x faster                                                    |
| go                               | 72.6 ms                                                        | 56.4 ms: 1.29x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 51.1 ms: 1.25x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 149 ms: 1.25x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.24x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 112 ms: 1.19x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 266 ms: 1.13x faster                                                    |
| pyflate                          | 222 ms                                                         | 196 ms: 1.13x faster                                                    |
| async_generators                 | 193 ms                                                         | 175 ms: 1.10x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.0 ms: 1.10x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.18 us: 1.10x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 268 ms: 1.10x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.84 ms: 1.09x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 930 ms: 1.07x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.99 sec: 1.07x faster                                                  |
| create_gc_cycles                 | 993 us                                                         | 939 us: 1.06x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.7 ms: 1.06x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.44 ms: 1.05x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.03x faster                                                   |
| richards                         | 22.1 ms                                                        | 21.5 ms: 1.03x faster                                                   |
| shortest_path                    | 225 ms                                                         | 220 ms: 1.02x faster                                                    |
| float                            | 31.4 ms                                                        | 30.9 ms: 1.02x faster                                                   |
| json                             | 1.94 ms                                                        | 1.91 ms: 1.02x faster                                                   |
| thrift                           | 309 us                                                         | 304 us: 1.02x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 61.6 ms: 1.01x faster                                                   |
| connected_components             | 208 ms                                                         | 205 ms: 1.01x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.01x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 63.8 us: 1.01x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 24.4 ms: 1.01x faster                                                   |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.82 ms: 1.01x faster                                                   |
| fannkuch                         | 179 ms                                                         | 177 ms: 1.01x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.04 ms: 1.01x faster                                                   |
| python_startup                   | 8.63 ms                                                        | 8.56 ms: 1.01x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.47 ms: 1.01x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.9 ms: 1.01x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 11.1 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 522 ms: 1.00x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.05 sec: 1.01x slower                                                  |
| genshi_text                      | 9.97 ms                                                        | 10.1 ms: 1.01x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.6 ms: 1.01x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 41.0 ns: 1.01x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 48.7 ms: 1.02x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.08 ms: 1.02x slower                                                   |
| sqlite_synth                     | 948 ns                                                         | 968 ns: 1.02x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.12 ms: 1.03x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 97.6 ms: 1.03x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 45.2 ms: 1.03x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 22.1 ms: 1.03x slower                                                   |
| 2to3                             | 112 ms                                                         | 116 ms: 1.04x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 24.0 ms: 1.04x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 335 ms: 1.04x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 677 ms: 1.04x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 39.0 ms: 1.05x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 100 ms: 1.05x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 168 ms: 1.05x slower                                                    |
| pycparser                        | 470 ms                                                         | 497 ms: 1.06x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 132 ms: 1.06x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.60 us: 1.06x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.90 ms: 1.07x slower                                                   |
| coverage                         | 31.2 ms                                                        | 33.3 ms: 1.07x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 440 us: 1.07x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.40 us: 1.07x slower                                                   |
| pylint                           | 106 ms                                                         | 114 ms: 1.08x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.56 ms: 1.08x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 56.4 ms: 1.08x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.42 us: 1.09x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.85 ms: 1.10x slower                                                   |
| chaos                            | 24.3 ms                                                        | 26.7 ms: 1.10x slower                                                   |
| raytrace                         | 109 ms                                                         | 122 ms: 1.12x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.9 ms: 1.13x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 149 us: 1.14x slower                                                    |
| nbody                            | 42.5 ms                                                        | 49.5 ms: 1.16x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.1 ms: 1.17x slower                                                   |
| generators                       | 15.7 ms                                                        | 18.5 ms: 1.18x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 50.5 ms: 1.18x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 251 ms: 1.21x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                   |
| many_optionals                   | 200 us                                                         | 251 us: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 132 ms: 1.28x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.86 ms: 1.57x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.8 ms: 3.07x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (7): unpickle_pure_python, meteor_contest, async_tree_eager_cpu_io_mixed, scimark_monte_carlo, json_loads, sphinx, xml_etree_generate
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250715-3.15.0a0-cb59eae/bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.021x faster

# HPT report

- Reliability score: 80.64% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x