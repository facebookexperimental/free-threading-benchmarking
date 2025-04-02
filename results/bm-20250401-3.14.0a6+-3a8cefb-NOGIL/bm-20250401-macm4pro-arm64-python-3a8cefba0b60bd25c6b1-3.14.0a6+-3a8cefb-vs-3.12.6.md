# Results vs. 3.12.6

- fork: python
- ref: 3a8cefba0b60bd25c6b1
- machine: darwin-arm64
- commit hash: 3a8cefb
- commit date: 2025-04-01
- overall geometric mean: 1.028x faster
- HPT reliability: 84.46%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 128 ms: 1.13x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.02x slower                                                   |
| html5lib       | 23.0 ms                                                  | 23.2 ms: 1.01x slower                                                    |
| sphinx         | 434 ms                                                   | 436 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                    | 1.04x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 224 ms: 2.21x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 218 ms: 2.21x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 215 ms: 2.08x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 231 ms: 1.99x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 95.9 ms: 1.79x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 131 ms: 1.76x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.61x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 139 ms: 1.60x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 239 ms: 1.42x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 248 ms: 1.34x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 11.5 ms: 1.18x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 115 ms: 1.14x faster                                                     |
| async_generators                 | 206 ms                                                   | 190 ms: 1.09x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 117 ms: 1.04x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 228 ms: 1.07x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 54.0 ms: 1.19x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 84.7 ms: 2.64x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.30x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 31.7 ms: 1.19x faster                                                    |
| pidigits       | 161 ms                                                   | 159 ms: 1.02x faster                                                     |
| nbody          | 54.2 ms                                                  | 58.9 ms: 1.09x slower                                                    |
| Geometric mean | (ref)                                                    | 1.04x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.40 ms: 1.19x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 91.3 ms: 1.09x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 56.6 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.0 ms: 1.32x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 54.9 ms: 1.24x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 40.2 ms: 1.03x slower                                                    |
| tomli_loads          | 957 ms                                                   | 1.03 sec: 1.07x slower                                                   |
| json_loads           | 10.9 us                                                  | 11.7 us: 1.08x slower                                                    |
| xml_etree_process    | 26.7 ms                                                  | 29.8 ms: 1.11x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 162 us: 1.17x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 125 us: 1.21x slower                                                     |
| json_dumps           | 4.26 ms                                                  | 5.16 ms: 1.21x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.04x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.20 ms: 1.15x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.25 ms: 1.27x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 25.9 ms: 1.19x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 12.7 ms: 1.21x slower                                                    |
| mako            | 4.77 ms                                                  | 6.03 ms: 1.26x slower                                                    |
| django_template | 13.6 ms                                                  | 17.6 ms: 1.29x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.24x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.06 ms: 2.29x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 224 ms: 2.21x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 218 ms: 2.21x faster                                                     |
| gc_traversal                     | 2.01 ms                                                  | 922 us: 2.18x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 215 ms: 2.08x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 231 ms: 1.99x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 95.9 ms: 1.79x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 131 ms: 1.76x faster                                                     |
| mdp                              | 1.09 sec                                                 | 626 ms: 1.74x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 499 us: 1.66x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.61x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 139 ms: 1.60x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 239 ms: 1.42x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 248 ms: 1.34x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.0 ms: 1.32x faster                                                    |
| deepcopy                         | 161 us                                                   | 123 us: 1.31x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 54.9 ms: 1.24x faster                                                    |
| float                            | 37.9 ms                                                  | 31.7 ms: 1.19x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.40 ms: 1.19x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 11.5 ms: 1.18x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 836 ns: 1.16x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 15.9 us: 1.15x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 115 ms: 1.14x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 19.0 ms: 1.12x faster                                                    |
| k_core                           | 1.12 sec                                                 | 1.02 sec: 1.10x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 91.3 ms: 1.09x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.34 us: 1.09x faster                                                    |
| async_generators                 | 206 ms                                                   | 190 ms: 1.09x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 11.6 ms: 1.07x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.15 sec: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                     |
| pycparser                        | 497 ms                                                   | 487 ms: 1.02x faster                                                     |
| go                               | 70.0 ms                                                  | 68.6 ms: 1.02x faster                                                    |
| pidigits                         | 161 ms                                                   | 159 ms: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 9.73 us: 1.01x faster                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 39.5 ms: 1.01x faster                                                    |
| raytrace                         | 145 ms                                                   | 146 ms: 1.00x slower                                                     |
| sphinx                           | 434 ms                                                   | 436 ms: 1.01x slower                                                     |
| html5lib                         | 23.0 ms                                                  | 23.2 ms: 1.01x slower                                                    |
| pyflate                          | 216 ms                                                   | 219 ms: 1.01x slower                                                     |
| logging_silent                   | 50.9 ns                                                  | 52.0 ns: 1.02x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.02x slower                                                   |
| json                             | 1.93 ms                                                  | 1.98 ms: 1.03x slower                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 40.2 ms: 1.03x slower                                                    |
| regex_compile                    | 54.6 ms                                                  | 56.6 ms: 1.04x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 117 ms: 1.04x slower                                                     |
| spectral_norm                    | 54.4 ms                                                  | 57.0 ms: 1.05x slower                                                    |
| scimark_fft                      | 142 ms                                                   | 149 ms: 1.05x slower                                                     |
| chaos                            | 28.9 ms                                                  | 30.7 ms: 1.06x slower                                                    |
| logging_simple                   | 2.57 us                                                  | 2.74 us: 1.07x slower                                                    |
| sqlalchemy_declarative           | 46.8 ms                                                  | 50.2 ms: 1.07x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 1.03 sec: 1.07x slower                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 8.62 ms: 1.07x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 228 ms: 1.07x slower                                                     |
| generators                       | 21.9 ms                                                  | 23.6 ms: 1.08x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.24 ms: 1.08x slower                                                    |
| logging_format                   | 2.80 us                                                  | 3.02 us: 1.08x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.7 us: 1.08x slower                                                    |
| nbody                            | 54.2 ms                                                  | 58.9 ms: 1.09x slower                                                    |
| scimark_sor                      | 61.0 ms                                                  | 66.6 ms: 1.09x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 63.0 ms: 1.09x slower                                                    |
| deltablue                        | 1.73 ms                                                  | 1.89 ms: 1.10x slower                                                    |
| nqueens                          | 43.5 ms                                                  | 47.9 ms: 1.10x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 78.3 us: 1.10x slower                                                    |
| shortest_path                    | 219 ms                                                   | 244 ms: 1.11x slower                                                     |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.76 ms: 1.11x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 29.8 ms: 1.11x slower                                                    |
| sympy_str                        | 104 ms                                                   | 117 ms: 1.12x slower                                                     |
| 2to3                             | 114 ms                                                   | 128 ms: 1.13x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 9.20 ms: 1.15x slower                                                    |
| connected_components             | 201 ms                                                   | 231 ms: 1.15x slower                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 37.4 ms: 1.16x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 162 us: 1.17x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 45.6 ms: 1.17x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 54.0 ms: 1.19x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 25.9 ms: 1.19x slower                                                    |
| richards                         | 22.4 ms                                                  | 26.7 ms: 1.19x slower                                                    |
| fannkuch                         | 176 ms                                                   | 209 ms: 1.19x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 57.0 ms: 1.19x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 30.3 ms: 1.19x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 61.3 ms: 1.20x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 200 ms: 1.20x slower                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 394 ms: 1.20x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 12.7 ms: 1.21x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 803 ms: 1.21x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 125 us: 1.21x slower                                                     |
| json_dumps                       | 4.26 ms                                                  | 5.16 ms: 1.21x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.77 ms: 1.24x slower                                                    |
| mako                             | 4.77 ms                                                  | 6.03 ms: 1.26x slower                                                    |
| many_optionals                   | 195 us                                                   | 247 us: 1.27x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 7.25 ms: 1.27x slower                                                    |
| django_template                  | 13.6 ms                                                  | 17.6 ms: 1.29x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.51 ms: 1.34x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 583 us: 1.39x slower                                                     |
| coverage                         | 26.9 ms                                                  | 40.9 ms: 1.52x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 84.7 ms: 2.64x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.02x faster                                                             |

Benchmark hidden because not significant (2): pylint, regex_v8
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250401-3.14.0a6+-3a8cefb-NOGIL/bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.028x faster

# HPT report

- Reliability score: 84.46% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.23x