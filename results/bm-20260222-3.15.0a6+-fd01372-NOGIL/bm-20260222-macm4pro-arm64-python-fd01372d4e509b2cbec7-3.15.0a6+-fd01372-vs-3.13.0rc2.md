# Results vs. 3.13.0rc2

- fork: python
- ref: fd01372d4e509b2cbec7
- machine: darwin-arm64
- commit hash: fd01372
- commit date: 2026-02-22
- overall geometric mean: 1.007x faster
- HPT reliability: 70.86%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260222-macm4pro-arm64-python-fd01372d4e509b2cbec7-3.15.0a6+-fd01372 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 124 ms: 1.11x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.02x faster                                                   |
| html5lib       | 23.1 ms                                                        | 24.6 ms: 1.06x slower                                                    |
| sphinx         | 409 ms                                                         | 429 ms: 1.05x slower                                                     |
| Geometric mean | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260222-macm4pro-arm64-python-fd01372d4e509b2cbec7-3.15.0a6+-fd01372 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 248 ms: 2.10x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 254 ms: 2.07x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 239 ms: 1.69x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 255 ms: 1.52x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 116 ms: 1.23x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 154 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 264 ms: 1.14x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 272 ms: 1.08x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| async_generators                 | 193 ms                                                         | 190 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 229 ms: 1.02x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 47.2 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 251 ms: 1.21x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 94.4 ms: 3.26x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.11x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260222-macm4pro-arm64-python-fd01372d4e509b2cbec7-3.15.0a6+-fd01372 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.9 ms: 1.09x faster                                                    |
| pidigits       | 166 ms                                                         | 167 ms: 1.01x slower                                                     |
| nbody          | 42.5 ms                                                        | 56.7 ms: 1.33x slower                                                    |
| Geometric mean | (ref)                                                          | 1.07x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260222-macm4pro-arm64-python-fd01372d4e509b2cbec7-3.15.0a6+-fd01372 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.25 ms: 1.16x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 97.6 ms: 1.03x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 51.2 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260222-macm4pro-arm64-python-fd01372d4e509b2cbec7-3.15.0a6+-fd01372 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.4 ms: 1.20x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 3.97 ms: 1.17x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 881 ms: 1.13x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 58.0 ms: 1.08x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.3 ms: 1.04x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.8 ms: 1.06x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 110 us: 1.10x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 147 us: 1.13x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260222-macm4pro-arm64-python-fd01372d4e509b2cbec7-3.15.0a6+-fd01372 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 10.1 ms: 1.17x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.32 ms: 1.23x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.20x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260222-macm4pro-arm64-python-fd01372d4e509b2cbec7-3.15.0a6+-fd01372 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.8 ms: 1.07x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.3 ms: 1.13x slower                                                    |
| django_template | 12.5 ms                                                        | 15.7 ms: 1.26x slower                                                    |
| mako            | 4.41 ms                                                        | 5.66 ms: 1.28x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.18x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260222-macm4pro-arm64-python-fd01372d4e509b2cbec7-3.15.0a6+-fd01372 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 838 us: 2.44x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 248 ms: 2.10x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 254 ms: 2.07x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 529 us: 1.88x faster                                                     |
| mdp                              | 1.06 sec                                                       | 617 ms: 1.71x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 239 ms: 1.69x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 255 ms: 1.52x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.17 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 998 ms: 1.47x faster                                                     |
| deepcopy                         | 145 us                                                         | 108 us: 1.34x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.8 us: 1.28x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 116 ms: 1.23x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.4 ms: 1.20x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 154 ms: 1.20x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 793 ns: 1.20x faster                                                     |
| go                               | 72.6 ms                                                        | 60.7 ms: 1.20x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.97 ms: 1.17x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 55.3 ms: 1.16x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.25 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 264 ms: 1.14x faster                                                     |
| pyflate                          | 222 ms                                                         | 196 ms: 1.13x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 881 ms: 1.13x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.16 us: 1.12x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                    |
| float                            | 31.4 ms                                                        | 28.9 ms: 1.09x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 272 ms: 1.08x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 58.0 ms: 1.08x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.00 sec: 1.06x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.8 ms: 1.05x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| fannkuch                         | 179 ms                                                         | 173 ms: 1.03x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.02x faster                                                   |
| async_generators                 | 193 ms                                                         | 190 ms: 1.02x faster                                                     |
| pidigits                         | 166 ms                                                         | 167 ms: 1.01x slower                                                     |
| dask                             | 525 ms                                                         | 530 ms: 1.01x slower                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 229 ms: 1.02x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 126 ms: 1.02x slower                                                     |
| json                             | 1.94 ms                                                        | 2.00 ms: 1.03x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 332 ms: 1.03x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 97.6 ms: 1.03x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.3 ms: 1.04x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 678 ms: 1.04x slower                                                     |
| sphinx                           | 409 ms                                                         | 429 ms: 1.05x slower                                                     |
| richards                         | 22.1 ms                                                        | 23.1 ms: 1.05x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.8 ms: 1.06x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 24.6 ms: 1.06x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.8 ms: 1.07x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 51.2 ms: 1.07x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.6 ms: 1.08x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 43.9 ns: 1.08x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.42 us: 1.08x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.19 ms: 1.09x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 47.2 ms: 1.09x slower                                                    |
| thrift                           | 309 us                                                         | 338 us: 1.09x slower                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.7 ms: 1.09x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 110 us: 1.10x slower                                                     |
| 2to3                             | 112 ms                                                         | 124 ms: 1.11x slower                                                     |
| logging_format                   | 2.45 us                                                        | 2.71 us: 1.11x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.18 ms: 1.12x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.2 ms: 1.12x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 49.1 ms: 1.12x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 72.6 us: 1.12x slower                                                    |
| shortest_path                    | 225 ms                                                         | 253 ms: 1.13x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 11.3 ms: 1.13x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 147 us: 1.13x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.64 ms: 1.13x slower                                                    |
| pylint                           | 106 ms                                                         | 120 ms: 1.14x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 42.7 ms: 1.15x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 10.1 ms: 1.17x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 112 ms: 1.17x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 56.1 ms: 1.17x slower                                                    |
| raytrace                         | 109 ms                                                         | 127 ms: 1.17x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 61.6 ms: 1.18x slower                                                    |
| connected_components             | 208 ms                                                         | 246 ms: 1.18x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.14 ms: 1.20x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 192 ms: 1.21x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 251 ms: 1.21x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 8.32 us: 1.22x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.32 ms: 1.23x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.6 ms: 1.24x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.7 ms: 1.26x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 47.9 ms: 1.27x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.66 ms: 1.28x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 43.2 ms: 1.28x slower                                                    |
| nbody                            | 42.5 ms                                                        | 56.7 ms: 1.33x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 57.3 ms: 1.34x slower                                                    |
| generators                       | 15.7 ms                                                        | 21.1 ms: 1.35x slower                                                    |
| many_optionals                   | 200 us                                                         | 274 us: 1.36x slower                                                     |
| bench_thread_pool                | 412 us                                                         | 590 us: 1.43x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 94.4 ms: 3.26x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x faster                                                             |

Benchmark hidden because not significant (2): pycparser, telco
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260222-3.15.0a6+-fd01372-NOGIL/bm-20260222-macm4pro-arm64-python-fd01372d4e509b2cbec7-3.15.0a6+-fd01372.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.007x faster

# HPT report

- Reliability score: 70.86% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.31x