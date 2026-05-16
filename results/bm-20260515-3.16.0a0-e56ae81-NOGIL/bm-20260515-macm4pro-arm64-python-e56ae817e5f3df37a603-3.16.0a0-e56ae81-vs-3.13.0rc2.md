# Results vs. 3.13.0rc2

- fork: python
- ref: e56ae817e5f3df37a603
- machine: darwin-arm64
- commit hash: e56ae81
- commit date: 2026-05-15
- overall geometric mean: 1.022x faster
- HPT reliability: 52.53%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.29x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260515-macm4pro-arm64-python-e56ae817e5f3df37a603-3.16.0a0-e56ae81 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| html5lib       | 23.1 ms                                                        | 23.0 ms: 1.01x faster                                                   |
| sphinx         | 409 ms                                                         | 439 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260515-macm4pro-arm64-python-e56ae817e5f3df37a603-3.16.0a0-e56ae81 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 276 ms: 1.89x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 281 ms: 1.87x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 274 ms: 1.48x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 270 ms: 1.43x faster                                                    |
| async_generators                 | 193 ms                                                         | 152 ms: 1.27x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 171 ms: 1.08x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 133 ms: 1.07x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 283 ms: 1.07x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 176 ms: 1.05x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 128 ms: 1.04x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 119 ms: 1.02x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.7 ms: 1.01x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 45.8 ms: 1.06x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 266 ms: 1.28x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 156 ms: 1.52x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 106 ms: 3.68x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                            |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed, async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260515-macm4pro-arm64-python-e56ae817e5f3df37a603-3.16.0a0-e56ae81 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 158 ms: 1.05x faster                                                    |
| float          | 31.4 ms                                                        | 32.5 ms: 1.04x slower                                                   |
| nbody          | 42.5 ms                                                        | 56.5 ms: 1.33x slower                                                   |
| Geometric mean | (ref)                                                          | 1.09x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260515-macm4pro-arm64-python-e56ae817e5f3df37a603-3.16.0a0-e56ae81 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 8.96 ms: 1.19x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.42 ms: 1.13x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 91.1 ms: 1.04x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 51.3 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                          | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260515-macm4pro-arm64-python-e56ae817e5f3df37a603-3.16.0a0-e56ae81 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.84 ms: 1.21x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 845 ms: 1.18x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 42.1 ms: 1.10x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 60.5 ms: 1.03x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 37.5 ms: 1.05x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 109 us: 1.09x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 28.2 ms: 1.11x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 146 us: 1.12x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260515-macm4pro-arm64-python-e56ae817e5f3df37a603-3.16.0a0-e56ae81 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| django_template | 12.5 ms                                                        | 15.7 ms: 1.26x slower                                                   |
| mako            | 4.41 ms                                                        | 5.58 ms: 1.26x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.26x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260515-macm4pro-arm64-python-e56ae817e5f3df37a603-3.16.0a0-e56ae81 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 790 us: 2.58x faster                                                    |
| pylint                           | 106 ms                                                         | 52.9 ms: 2.00x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 508 us: 1.96x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 276 ms: 1.89x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 281 ms: 1.87x faster                                                    |
| mdp                              | 1.06 sec                                                       | 594 ms: 1.78x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.22 ms: 1.48x faster                                                   |
| k_core                           | 1.46 sec                                                       | 988 ms: 1.48x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 274 ms: 1.48x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 270 ms: 1.43x faster                                                    |
| deepcopy                         | 145 us                                                         | 105 us: 1.38x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.9 us: 1.27x faster                                                   |
| async_generators                 | 193 ms                                                         | 152 ms: 1.27x faster                                                    |
| go                               | 72.6 ms                                                        | 58.2 ms: 1.25x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.84 ms: 1.21x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 789 ns: 1.20x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 8.96 ms: 1.19x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 845 ms: 1.18x faster                                                    |
| pyflate                          | 222 ms                                                         | 189 ms: 1.17x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 55.3 us: 1.17x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 55.8 ms: 1.15x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.42 ms: 1.13x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.89 sec: 1.13x faster                                                  |
| deepcopy_reduce                  | 1.30 us                                                        | 1.16 us: 1.11x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 42.1 ms: 1.10x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.3 ms: 1.09x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 171 ms: 1.08x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 133 ms: 1.07x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 283 ms: 1.07x faster                                                    |
| fannkuch                         | 179 ms                                                         | 169 ms: 1.06x faster                                                    |
| pidigits                         | 166 ms                                                         | 158 ms: 1.05x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 176 ms: 1.05x faster                                                    |
| json                             | 1.94 ms                                                        | 1.86 ms: 1.05x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 91.1 ms: 1.04x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 128 ms: 1.04x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 60.5 ms: 1.03x faster                                                   |
| pycparser                        | 470 ms                                                         | 457 ms: 1.03x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 119 ms: 1.02x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.00 ms: 1.02x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.7 ms: 1.01x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 23.0 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 528 ms: 1.01x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 126 ms: 1.01x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 330 ms: 1.03x slower                                                    |
| float                            | 31.4 ms                                                        | 32.5 ms: 1.04x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.32 us: 1.04x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 674 ms: 1.04x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 42.3 ns: 1.04x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.56 us: 1.05x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 37.5 ms: 1.05x slower                                                   |
| richards                         | 22.1 ms                                                        | 23.2 ms: 1.05x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.94 ms: 1.06x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 45.8 ms: 1.06x slower                                                   |
| thrift                           | 309 us                                                         | 330 us: 1.07x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 51.3 ms: 1.07x slower                                                   |
| sphinx                           | 409 ms                                                         | 439 ms: 1.07x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.5 ms: 1.07x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 40.4 ms: 1.08x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.5 ms: 1.09x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.11 ms: 1.09x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 109 us: 1.09x slower                                                    |
| shortest_path                    | 225 ms                                                         | 249 ms: 1.11x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 28.2 ms: 1.11x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 146 us: 1.12x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 49.3 ms: 1.13x slower                                                   |
| chaos                            | 24.3 ms                                                        | 27.4 ms: 1.13x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 108 ms: 1.13x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 54.5 ms: 1.14x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 60.0 ms: 1.15x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 184 ms: 1.15x slower                                                    |
| raytrace                         | 109 ms                                                         | 126 ms: 1.16x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.68 ms: 1.16x slower                                                   |
| connected_components             | 208 ms                                                         | 242 ms: 1.16x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 44.7 ms: 1.18x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.10 us: 1.19x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.19 ms: 1.23x slower                                                   |
| coverage                         | 31.2 ms                                                        | 38.6 ms: 1.24x slower                                                   |
| django_template                  | 12.5 ms                                                        | 15.7 ms: 1.26x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.58 ms: 1.26x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 266 ms: 1.28x slower                                                    |
| many_optionals                   | 200 us                                                         | 257 us: 1.28x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 43.4 ms: 1.29x slower                                                   |
| generators                       | 15.7 ms                                                        | 20.5 ms: 1.31x slower                                                   |
| nbody                            | 42.5 ms                                                        | 56.5 ms: 1.33x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 572 us: 1.39x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 61.3 ms: 1.43x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 156 ms: 1.52x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 106 ms: 3.68x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (4): async_tree_cpu_io_mixed, docutils, async_tree_eager_cpu_io_mixed, json_loads
Ignored benchmarks (16) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: 2to3, asyncio_websockets, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260515-3.16.0a0-e56ae81-NOGIL/bm-20260515-macm4pro-arm64-python-e56ae817e5f3df37a603-3.16.0a0-e56ae81.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.022x faster

# HPT report

- Reliability score: 52.53% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.29x