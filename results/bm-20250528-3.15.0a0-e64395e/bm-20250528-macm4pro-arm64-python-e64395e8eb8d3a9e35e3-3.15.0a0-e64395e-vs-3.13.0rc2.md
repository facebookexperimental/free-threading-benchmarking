# Results vs. 3.13.0rc2

- fork: python
- ref: e64395e8eb8d3a9e35e3
- machine: darwin-arm64
- commit hash: e64395e
- commit date: 2025-05-28
- overall geometric mean: 1.033x faster
- HPT reliability: 98.23%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250528-macm4pro-arm64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 112 ms: 1.00x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                  |
| html5lib       | 23.1 ms                                                        | 23.6 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                          | 1.00x faster                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250528-macm4pro-arm64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 243 ms: 2.16x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 252 ms: 2.06x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 250 ms: 1.62x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 255 ms: 1.51x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.27x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 260 ms: 1.16x faster                                                    |
| async_generators                 | 193 ms                                                         | 170 ms: 1.14x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 261 ms: 1.13x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.4 ms: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.26x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.3 ms: 3.02x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250528-macm4pro-arm64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.5 ms: 1.06x faster                                                   |
| pidigits       | 166 ms                                                         | 162 ms: 1.02x faster                                                    |
| nbody          | 42.5 ms                                                        | 47.3 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250528-macm4pro-arm64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.67 ms: 1.11x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 48.1 ms: 1.00x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 99.4 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250528-macm4pro-arm64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 908 ms: 1.10x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 43.2 ms: 1.07x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 4.46 ms: 1.04x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 60.8 ms: 1.03x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.3 ms: 1.02x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 98.0 us: 1.02x faster                                                   |
| json_loads           | 10.8 us                                                        | 11.7 us: 1.08x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 146 us: 1.12x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250528-macm4pro-arm64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.58 ms: 1.01x faster                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.14 ms: 1.03x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250528-macm4pro-arm64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.72 ms: 1.03x faster                                                   |
| mako            | 4.41 ms                                                        | 4.94 ms: 1.12x slower                                                   |
| django_template | 12.5 ms                                                        | 15.3 ms: 1.22x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.07x slower                                                            |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250528-macm4pro-arm64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 243 ms: 2.16x faster                                                    |
| mdp                              | 1.06 sec                                                       | 509 ms: 2.08x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 252 ms: 2.06x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 250 ms: 1.62x faster                                                    |
| k_core                           | 1.46 sec                                                       | 945 ms: 1.55x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 255 ms: 1.51x faster                                                    |
| deepcopy                         | 145 us                                                         | 108 us: 1.34x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.4 us: 1.33x faster                                                   |
| go                               | 72.6 ms                                                        | 55.9 ms: 1.30x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 49.9 ms: 1.28x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.27x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 260 ms: 1.16x faster                                                    |
| pyflate                          | 222 ms                                                         | 195 ms: 1.14x faster                                                    |
| async_generators                 | 193 ms                                                         | 170 ms: 1.14x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.15 us: 1.13x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 261 ms: 1.13x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 17.8 ms: 1.12x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.67 ms: 1.11x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 908 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.94 sec: 1.10x faster                                                  |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.2 ms: 1.07x faster                                                   |
| float                            | 31.4 ms                                                        | 29.5 ms: 1.06x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 939 us: 1.06x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.46 ms: 1.04x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.4 ms: 1.04x faster                                                   |
| shortest_path                    | 225 ms                                                         | 217 ms: 1.04x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.75 ms: 1.04x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 62.6 us: 1.03x faster                                                   |
| connected_components             | 208 ms                                                         | 201 ms: 1.03x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.1 ms: 1.03x faster                                                   |
| genshi_text                      | 9.97 ms                                                        | 9.72 ms: 1.03x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 60.8 ms: 1.03x faster                                                   |
| pidigits                         | 166 ms                                                         | 162 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                    |
| richards                         | 22.1 ms                                                        | 21.6 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                    |
| thrift                           | 309 us                                                         | 303 us: 1.02x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.38 ms: 1.02x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                  |
| xml_etree_generate               | 35.8 ms                                                        | 35.3 ms: 1.02x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 98.0 us: 1.02x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 24.4 ms: 1.01x faster                                                   |
| telco                            | 3.07 ms                                                        | 3.03 ms: 1.01x faster                                                   |
| meteor_contest                   | 47.9 ms                                                        | 47.5 ms: 1.01x faster                                                   |
| python_startup                   | 8.63 ms                                                        | 8.58 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 522 ms: 1.00x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 48.1 ms: 1.00x slower                                                   |
| 2to3                             | 112 ms                                                         | 112 ms: 1.00x slower                                                    |
| pathlib                          | 11.1 ms                                                        | 11.2 ms: 1.00x slower                                                   |
| json                             | 1.94 ms                                                        | 1.96 ms: 1.01x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.08 ms: 1.02x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 23.6 ms: 1.02x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.14 ms: 1.03x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 98.8 ms: 1.04x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.50 ms: 1.04x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 45.3 ms: 1.04x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 166 ms: 1.04x slower                                                    |
| pycparser                        | 470 ms                                                         | 491 ms: 1.04x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.86 ms: 1.05x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 431 us: 1.05x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 99.4 ms: 1.05x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 130 ms: 1.05x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 39.2 ms: 1.05x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 55.5 ms: 1.06x slower                                                   |
| coverage                         | 31.2 ms                                                        | 33.1 ms: 1.06x slower                                                   |
| chaos                            | 24.3 ms                                                        | 25.9 ms: 1.07x slower                                                   |
| pylint                           | 106 ms                                                         | 113 ms: 1.07x slower                                                    |
| raytrace                         | 109 ms                                                         | 118 ms: 1.08x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.7 us: 1.08x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.40 us: 1.09x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 46.6 ms: 1.09x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 353 ms: 1.10x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 715 ms: 1.10x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.3 ms: 1.11x slower                                                   |
| nbody                            | 42.5 ms                                                        | 47.3 ms: 1.11x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.94 ms: 1.12x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.74 us: 1.12x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 146 us: 1.12x slower                                                    |
| generators                       | 15.7 ms                                                        | 17.7 ms: 1.13x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.53 us: 1.13x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 43.6 ms: 1.15x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                    |
| many_optionals                   | 200 us                                                         | 241 us: 1.20x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.3 ms: 1.22x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.26x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.56 ms: 1.53x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.3 ms: 3.02x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 194 ns: 4.77x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (4): sphinx, fannkuch, genshi_xml, sqlite_synth
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250528-3.15.0a0-e64395e/bm-20250528-macm4pro-arm64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.033x faster

# HPT report

- Reliability score: 98.23% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.09x