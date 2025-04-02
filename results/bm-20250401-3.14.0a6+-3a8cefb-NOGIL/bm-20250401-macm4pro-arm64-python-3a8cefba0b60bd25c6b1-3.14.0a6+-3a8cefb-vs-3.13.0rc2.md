# Results vs. 3.13.0rc2

- fork: python
- ref: 3a8cefba0b60bd25c6b1
- machine: darwin-arm64
- commit hash: 3a8cefb
- commit date: 2025-04-01
- overall geometric mean: 1.046x slower
- HPT reliability: 99.19%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 128 ms: 1.15x slower                                                     |
| sphinx         | 409 ms                                                         | 436 ms: 1.07x slower                                                     |
| Geometric mean | (ref)                                                          | 1.05x slower                                                             |

Benchmark hidden because not significant (2): docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 215 ms: 2.43x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 224 ms: 2.34x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 218 ms: 1.86x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 231 ms: 1.67x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 131 ms: 1.42x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 95.9 ms: 1.38x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 139 ms: 1.33x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.29x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 239 ms: 1.26x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 248 ms: 1.18x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 115 ms: 1.06x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| async_generators                 | 193 ms                                                         | 190 ms: 1.02x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 11.5 ms: 1.07x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 228 ms: 1.10x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 117 ms: 1.15x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 54.0 ms: 1.25x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 84.7 ms: 2.93x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.17x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 159 ms: 1.05x faster                                                     |
| float          | 31.4 ms                                                        | 31.7 ms: 1.01x slower                                                    |
| nbody          | 42.5 ms                                                        | 58.9 ms: 1.39x slower                                                    |
| Geometric mean | (ref)                                                          | 1.10x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.40 ms: 1.15x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.64 ms: 1.11x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 91.3 ms: 1.04x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 56.6 ms: 1.18x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 39.0 ms: 1.18x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 54.9 ms: 1.14x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 1.03 sec: 1.03x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.7 us: 1.09x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 5.16 ms: 1.11x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 40.2 ms: 1.12x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 29.8 ms: 1.18x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 162 us: 1.25x slower                                                     |
| unpickle_pure_python | 99.5 us                                                        | 125 us: 1.25x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.07x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.20 ms: 1.07x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.25 ms: 1.22x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 25.9 ms: 1.21x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 12.7 ms: 1.27x slower                                                    |
| mako            | 4.41 ms                                                        | 6.03 ms: 1.37x slower                                                    |
| django_template | 12.5 ms                                                        | 17.6 ms: 1.41x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.31x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 215 ms: 2.43x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 224 ms: 2.34x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 922 us: 2.21x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 499 us: 1.99x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 218 ms: 1.86x faster                                                     |
| mdp                              | 1.06 sec                                                       | 626 ms: 1.69x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 231 ms: 1.67x faster                                                     |
| k_core                           | 1.46 sec                                                       | 1.02 sec: 1.44x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 131 ms: 1.42x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 95.9 ms: 1.38x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 139 ms: 1.33x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.29x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 239 ms: 1.26x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 248 ms: 1.18x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.0 ms: 1.18x faster                                                    |
| deepcopy                         | 145 us                                                         | 123 us: 1.18x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.40 ms: 1.15x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 54.9 ms: 1.14x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 836 ns: 1.13x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.64 ms: 1.11x faster                                                    |
| go                               | 72.6 ms                                                        | 68.6 ms: 1.06x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 115 ms: 1.06x faster                                                     |
| pidigits                         | 166 ms                                                         | 159 ms: 1.05x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 19.0 ms: 1.05x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 91.3 ms: 1.04x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 15.9 us: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| async_generators                 | 193 ms                                                         | 190 ms: 1.02x faster                                                     |
| pyflate                          | 222 ms                                                         | 219 ms: 1.01x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.15 sec: 1.01x slower                                                   |
| float                            | 31.4 ms                                                        | 31.7 ms: 1.01x slower                                                    |
| json                             | 1.94 ms                                                        | 1.98 ms: 1.02x slower                                                    |
| tomli_loads                      | 1000 ms                                                        | 1.03 sec: 1.03x slower                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.34 us: 1.03x slower                                                    |
| pycparser                        | 470 ms                                                         | 487 ms: 1.04x slower                                                     |
| pathlib                          | 11.1 ms                                                        | 11.6 ms: 1.04x slower                                                    |
| scimark_sor                      | 64.0 ms                                                        | 66.6 ms: 1.04x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 39.5 ms: 1.04x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.20 ms: 1.07x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 11.5 ms: 1.07x slower                                                    |
| sphinx                           | 409 ms                                                         | 436 ms: 1.07x slower                                                     |
| shortest_path                    | 225 ms                                                         | 244 ms: 1.08x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.7 us: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 228 ms: 1.10x slower                                                     |
| connected_components             | 208 ms                                                         | 231 ms: 1.11x slower                                                     |
| json_dumps                       | 4.65 ms                                                        | 5.16 ms: 1.11x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 40.2 ms: 1.12x slower                                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 50.2 ms: 1.13x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.51 ms: 1.14x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.62 ms: 1.14x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 117 ms: 1.15x slower                                                     |
| 2to3                             | 112 ms                                                         | 128 ms: 1.15x slower                                                     |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.76 ms: 1.15x slower                                                    |
| pylint                           | 106 ms                                                         | 123 ms: 1.17x slower                                                     |
| fannkuch                         | 179 ms                                                         | 209 ms: 1.17x slower                                                     |
| xml_etree_process                | 25.4 ms                                                        | 29.8 ms: 1.18x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 56.6 ms: 1.18x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 57.0 ms: 1.19x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 63.0 ms: 1.20x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 149 ms: 1.20x slower                                                     |
| richards                         | 22.1 ms                                                        | 26.7 ms: 1.21x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 78.3 us: 1.21x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 25.9 ms: 1.21x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.25 ms: 1.22x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 394 ms: 1.23x slower                                                     |
| logging_simple                   | 2.24 us                                                        | 2.74 us: 1.23x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 117 ms: 1.23x slower                                                     |
| richards_super                   | 24.7 ms                                                        | 30.3 ms: 1.23x slower                                                    |
| many_optionals                   | 200 us                                                         | 247 us: 1.23x slower                                                     |
| logging_format                   | 2.45 us                                                        | 3.02 us: 1.24x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 803 ms: 1.24x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 162 us: 1.25x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 54.0 ms: 1.25x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 37.4 ms: 1.25x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 200 ms: 1.25x slower                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 125 us: 1.25x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.24 ms: 1.26x slower                                                    |
| chaos                            | 24.3 ms                                                        | 30.7 ms: 1.26x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 12.7 ms: 1.27x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 52.0 ns: 1.28x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 47.9 ms: 1.29x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 57.0 ms: 1.30x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.89 ms: 1.30x slower                                                    |
| coverage                         | 31.2 ms                                                        | 40.9 ms: 1.31x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.77 ms: 1.32x slower                                                    |
| raytrace                         | 109 ms                                                         | 146 ms: 1.34x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 45.6 ms: 1.36x slower                                                    |
| mako                             | 4.41 ms                                                        | 6.03 ms: 1.37x slower                                                    |
| nbody                            | 42.5 ms                                                        | 58.9 ms: 1.39x slower                                                    |
| django_template                  | 12.5 ms                                                        | 17.6 ms: 1.41x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 583 us: 1.42x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 9.73 us: 1.43x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 61.3 ms: 1.43x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.06 ms: 1.45x slower                                                    |
| generators                       | 15.7 ms                                                        | 23.6 ms: 1.50x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 84.7 ms: 2.93x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.05x slower                                                             |

Benchmark hidden because not significant (3): docutils, html5lib, async_tree_eager_cpu_io_mixed
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250401-3.14.0a6+-3a8cefb-NOGIL/bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.046x slower

# HPT report

- Reliability score: 99.19% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.18x