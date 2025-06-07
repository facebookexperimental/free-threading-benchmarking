# Results vs. 3.13.0rc2

- fork: python
- ref: 46151648ca8ba1edd2a2
- machine: darwin-arm64
- commit hash: 4615164
- commit date: 2025-06-06
- overall geometric mean: 1.025x faster
- HPT reliability: 52.48%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250606-macm4pro-arm64-python-46151648ca8ba1edd2a2-3.15.0a0-4615164 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 118 ms: 1.06x slower                                                    |
| docutils       | 1.05 sec                                                       | 982 ms: 1.07x faster                                                    |
| html5lib       | 23.1 ms                                                        | 22.9 ms: 1.01x faster                                                   |
| sphinx         | 409 ms                                                         | 414 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                          | 1.00x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250606-macm4pro-arm64-python-46151648ca8ba1edd2a2-3.15.0a0-4615164 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 189 ms: 2.75x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 199 ms: 2.64x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 195 ms: 2.08x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 207 ms: 1.87x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 85.7 ms: 1.55x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 122 ms: 1.52x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 99.4 ms: 1.43x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 232 ms: 1.30x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 240 ms: 1.22x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                    |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 223 ms: 1.07x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 110 ms: 1.08x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.5 ms: 1.12x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 76.5 ms: 2.64x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.26x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250606-macm4pro-arm64-python-46151648ca8ba1edd2a2-3.15.0a0-4615164 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.1 ms: 1.12x faster                                                   |
| pidigits       | 166 ms                                                         | 160 ms: 1.04x faster                                                    |
| nbody          | 42.5 ms                                                        | 54.3 ms: 1.28x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250606-macm4pro-arm64-python-46151648ca8ba1edd2a2-3.15.0a0-4615164 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.06 ms: 1.18x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.12x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 95.7 ms: 1.01x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 52.8 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250606-macm4pro-arm64-python-46151648ca8ba1edd2a2-3.15.0a0-4615164 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 39.2 ms: 1.18x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 58.5 ms: 1.07x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 978 ms: 1.02x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.61 ms: 1.01x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 37.3 ms: 1.04x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.05x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 27.0 ms: 1.06x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 111 us: 1.12x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 152 us: 1.17x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250606-macm4pro-arm64-python-46151648ca8ba1edd2a2-3.15.0a0-4615164 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.39 ms: 1.09x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.84 ms: 1.15x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.12x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250606-macm4pro-arm64-python-46151648ca8ba1edd2a2-3.15.0a0-4615164 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.2 ms: 1.08x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.1 ms: 1.11x slower                                                   |
| mako            | 4.41 ms                                                        | 5.71 ms: 1.29x slower                                                   |
| django_template | 12.5 ms                                                        | 16.6 ms: 1.33x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.20x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250606-macm4pro-arm64-python-46151648ca8ba1edd2a2-3.15.0a0-4615164 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 189 ms: 2.75x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 764 us: 2.67x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 199 ms: 2.64x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 195 ms: 2.08x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 481 us: 2.07x faster                                                    |
| mdp                              | 1.06 sec                                                       | 555 ms: 1.91x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 207 ms: 1.87x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 85.7 ms: 1.55x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 122 ms: 1.52x faster                                                    |
| k_core                           | 1.46 sec                                                       | 986 ms: 1.48x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 99.4 ms: 1.43x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 232 ms: 1.30x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 240 ms: 1.22x faster                                                    |
| deepcopy                         | 145 us                                                         | 119 us: 1.22x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.8 us: 1.20x faster                                                   |
| go                               | 72.6 ms                                                        | 60.7 ms: 1.20x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.06 ms: 1.18x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.2 ms: 1.18x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 55.4 ms: 1.15x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 824 ns: 1.15x faster                                                    |
| pyflate                          | 222 ms                                                         | 197 ms: 1.13x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                    |
| float                            | 31.4 ms                                                        | 28.1 ms: 1.12x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.12x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.92 sec: 1.11x faster                                                  |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.4 ms: 1.08x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 58.5 ms: 1.07x faster                                                   |
| docutils                         | 1.05 sec                                                       | 982 ms: 1.07x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.24 us: 1.04x faster                                                   |
| pidigits                         | 166 ms                                                         | 160 ms: 1.04x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 978 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 22.9 ms: 1.01x faster                                                   |
| pycparser                        | 470 ms                                                         | 465 ms: 1.01x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.61 ms: 1.01x faster                                                   |
| fannkuch                         | 179 ms                                                         | 180 ms: 1.01x slower                                                    |
| json                             | 1.94 ms                                                        | 1.96 ms: 1.01x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 95.7 ms: 1.01x slower                                                   |
| sphinx                           | 409 ms                                                         | 414 ms: 1.01x slower                                                    |
| shortest_path                    | 225 ms                                                         | 233 ms: 1.04x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.3 ms: 1.04x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.88 ms: 1.05x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.00 ms: 1.05x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.05x slower                                                   |
| 2to3                             | 112 ms                                                         | 118 ms: 1.06x slower                                                    |
| connected_components             | 208 ms                                                         | 220 ms: 1.06x slower                                                    |
| thrift                           | 309 us                                                         | 327 us: 1.06x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.0 ms: 1.06x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.27 ms: 1.07x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 223 ms: 1.07x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 110 ms: 1.08x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.2 ms: 1.08x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 9.39 ms: 1.09x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 40.8 ms: 1.09x slower                                                   |
| richards                         | 22.1 ms                                                        | 24.3 ms: 1.10x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 52.8 ms: 1.10x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 53.0 ms: 1.11x slower                                                   |
| pylint                           | 106 ms                                                         | 117 ms: 1.11x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.61 ms: 1.11x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.1 ms: 1.11x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.4 ms: 1.12x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 27.6 ms: 1.12x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 111 us: 1.12x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.5 ms: 1.12x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 72.8 us: 1.13x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 108 ms: 1.13x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 140 ms: 1.13x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 59.5 ms: 1.14x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.75 us: 1.14x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.84 ms: 1.15x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 43.5 ms: 1.15x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 372 ms: 1.16x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 50.9 ms: 1.16x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 186 ms: 1.16x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 759 ms: 1.17x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 152 us: 1.17x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.5 ms: 1.18x slower                                                   |
| raytrace                         | 109 ms                                                         | 130 ms: 1.19x slower                                                    |
| chaos                            | 24.3 ms                                                        | 29.2 ms: 1.20x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.17 ms: 1.22x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 41.2 ms: 1.23x slower                                                   |
| many_optionals                   | 200 us                                                         | 247 us: 1.23x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.78 us: 1.24x slower                                                   |
| logging_format                   | 2.45 us                                                        | 3.06 us: 1.25x slower                                                   |
| coverage                         | 31.2 ms                                                        | 39.8 ms: 1.28x slower                                                   |
| nbody                            | 42.5 ms                                                        | 54.3 ms: 1.28x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.71 ms: 1.29x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.6 ms: 1.33x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 594 us: 1.44x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.57 ms: 1.53x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 66.5 ms: 1.55x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 76.5 ms: 2.64x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 214 ns: 5.28x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x faster                                                            |

Benchmark hidden because not significant (1): pathlib
Ignored benchmarks (11) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250606-3.15.0a0-4615164-NOGIL/bm-20250606-macm4pro-arm64-python-46151648ca8ba1edd2a2-3.15.0a0-4615164.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.025x faster

# HPT report

- Reliability score: 52.48% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.22x