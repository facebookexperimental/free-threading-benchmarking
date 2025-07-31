# Results vs. 3.13.0rc2

- fork: python
- ref: d591b5effb8ec8177a95
- machine: darwin-arm64
- commit hash: d591b5e
- commit date: 2025-07-30
- overall geometric mean: 1.022x faster
- HPT reliability: 88.11%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.03x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.05 sec: 1.01x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.0 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 245 ms: 2.14x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 252 ms: 2.07x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 249 ms: 1.63x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 254 ms: 1.52x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.27x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.27x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 263 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.97 ms: 1.08x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.6 ms: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 249 ms: 1.20x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.3 ms: 3.02x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.3 ms: 1.04x faster                                                   |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| nbody          | 42.5 ms                                                        | 48.7 ms: 1.15x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.67 ms: 1.11x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 48.4 ms: 1.01x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 97.0 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 925 ms: 1.08x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.41 ms: 1.06x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.2 ms: 1.04x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.0 ms: 1.02x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.1 ms: 1.01x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.9 us: 1.01x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 100 us: 1.01x slower                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 63.1 ms: 1.01x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 142 us: 1.09x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.66 ms: 1.00x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.20 ms: 1.04x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.86 ms: 1.01x faster                                                   |
| mako            | 4.41 ms                                                        | 4.86 ms: 1.10x slower                                                   |
| django_template | 12.5 ms                                                        | 15.3 ms: 1.22x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.07x slower                                                            |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 245 ms: 2.14x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 252 ms: 2.07x faster                                                    |
| mdp                              | 1.06 sec                                                       | 540 ms: 1.96x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 249 ms: 1.63x faster                                                    |
| k_core                           | 1.46 sec                                                       | 956 ms: 1.53x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 254 ms: 1.52x faster                                                    |
| deepcopy                         | 145 us                                                         | 111 us: 1.31x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.6 us: 1.30x faster                                                   |
| go                               | 72.6 ms                                                        | 55.7 ms: 1.30x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.27x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.27x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 50.8 ms: 1.26x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 263 ms: 1.14x faster                                                    |
| pyflate                          | 222 ms                                                         | 195 ms: 1.14x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.16 us: 1.12x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.67 ms: 1.11x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.1 ms: 1.10x faster                                                   |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 925 ms: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.97 ms: 1.08x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.99 sec: 1.07x faster                                                  |
| create_gc_cycles                 | 993 us                                                         | 940 us: 1.06x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.41 ms: 1.06x faster                                                   |
| richards                         | 22.1 ms                                                        | 21.1 ms: 1.05x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.2 ms: 1.04x faster                                                   |
| connected_components             | 208 ms                                                         | 199 ms: 1.04x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.6 ms: 1.04x faster                                                   |
| shortest_path                    | 225 ms                                                         | 217 ms: 1.04x faster                                                    |
| float                            | 31.4 ms                                                        | 30.3 ms: 1.04x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 23.8 ms: 1.04x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.78 ms: 1.03x faster                                                   |
| thrift                           | 309 us                                                         | 302 us: 1.02x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 35.0 ms: 1.02x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 63.4 us: 1.02x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.01x faster                                                    |
| json                             | 1.94 ms                                                        | 1.92 ms: 1.01x faster                                                   |
| genshi_text                      | 9.97 ms                                                        | 9.86 ms: 1.01x faster                                                   |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 25.1 ms: 1.01x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.6 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.47 ms: 1.01x faster                                                   |
| telco                            | 3.07 ms                                                        | 3.04 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                    |
| python_startup                   | 8.63 ms                                                        | 8.66 ms: 1.00x slower                                                   |
| docutils                         | 1.05 sec                                                       | 1.05 sec: 1.01x slower                                                  |
| json_loads                       | 10.8 us                                                        | 10.9 us: 1.01x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 654 ms: 1.01x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 100 us: 1.01x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 324 ms: 1.01x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 956 ns: 1.01x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 48.4 ms: 1.01x slower                                                   |
| fannkuch                         | 179 ms                                                         | 180 ms: 1.01x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.06 ms: 1.01x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 63.1 ms: 1.01x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 44.3 ms: 1.01x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 41.4 ns: 1.02x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 97.0 ms: 1.02x slower                                                   |
| 2to3                             | 112 ms                                                         | 115 ms: 1.03x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.50 ms: 1.03x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 38.5 ms: 1.03x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 24.0 ms: 1.04x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 49.8 ms: 1.04x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.20 ms: 1.04x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 99.9 ms: 1.05x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.56 us: 1.05x slower                                                   |
| coverage                         | 31.2 ms                                                        | 32.8 ms: 1.05x slower                                                   |
| pycparser                        | 470 ms                                                         | 494 ms: 1.05x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.35 us: 1.05x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 168 ms: 1.05x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 436 us: 1.06x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 132 ms: 1.07x slower                                                    |
| pylint                           | 106 ms                                                         | 114 ms: 1.08x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 56.4 ms: 1.08x slower                                                   |
| raytrace                         | 109 ms                                                         | 118 ms: 1.08x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.93 ms: 1.09x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 142 us: 1.09x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.5 ms: 1.09x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.86 ms: 1.10x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.0 ms: 1.10x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.50 us: 1.10x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.4 ms: 1.11x slower                                                   |
| nbody                            | 42.5 ms                                                        | 48.7 ms: 1.15x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 49.2 ms: 1.15x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 43.9 ms: 1.16x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 249 ms: 1.20x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.3 ms: 1.22x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                    |
| many_optionals                   | 200 us                                                         | 320 us: 1.60x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 17.3 ms: 2.76x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.3 ms: 3.02x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (2): sphinx, genshi_xml
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250730-3.15.0a0-d591b5e/bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.022x faster

# HPT report

- Reliability score: 88.11% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.09x