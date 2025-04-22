# Results vs. 3.12.6

- fork: python
- ref: 3cfab449ab1e3c1472d2
- machine: darwin-arm64
- commit hash: 3cfab44
- commit date: 2025-04-21
- overall geometric mean: 1.100x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250421-macm4pro-arm64-python-3cfab449ab1e3c1472d2-3.14.0a7+-3cfab44 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 113 ms: 1.01x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                   |
| html5lib       | 23.0 ms                                                  | 23.9 ms: 1.04x slower                                                    |
| sphinx         | 434 ms                                                   | 409 ms: 1.06x faster                                                     |
| Geometric mean | (ref)                                                    | 1.00x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250421-macm4pro-arm64-python-3cfab449ab1e3c1472d2-3.14.0a7+-3cfab44 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 251 ms: 1.98x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 252 ms: 1.90x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 257 ms: 1.79x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 254 ms: 1.76x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.56x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.50x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 264 ms: 1.28x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 270 ms: 1.24x faster                                                     |
| async_generators                 | 206 ms                                                   | 171 ms: 1.20x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.17x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 43.3 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 191 ms: 1.00x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 133 ms: 1.18x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 254 ms: 1.20x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 90.3 ms: 2.81x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250421-macm4pro-arm64-python-3cfab449ab1e3c1472d2-3.14.0a7+-3cfab44 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.4 ms: 1.25x faster                                                    |
| nbody          | 54.2 ms                                                  | 49.8 ms: 1.09x faster                                                    |
| pidigits       | 161 ms                                                   | 162 ms: 1.00x slower                                                     |
| Geometric mean | (ref)                                                    | 1.11x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250421-macm4pro-arm64-python-3cfab449ab1e3c1472d2-3.14.0a7+-3cfab44 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 48.9 ms: 1.12x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 99.4 ms: 1.00x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 10.2 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250421-macm4pro-arm64-python-3cfab449ab1e3c1472d2-3.14.0a7+-3cfab44 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 44.0 ms: 1.17x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 63.4 ms: 1.07x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 36.4 ms: 1.07x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 25.7 ms: 1.04x faster                                                    |
| tomli_loads          | 957 ms                                                   | 927 ms: 1.03x faster                                                     |
| unpickle_pure_python | 103 us                                                   | 100 us: 1.02x faster                                                     |
| pickle_pure_python   | 139 us                                                   | 146 us: 1.05x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 5.00 ms: 1.17x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.01x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250421-macm4pro-arm64-python-3cfab449ab1e3c1472d2-3.14.0a7+-3cfab44 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.97 ms: 1.12x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.72 ms: 1.18x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.15x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250421-macm4pro-arm64-python-3cfab449ab1e3c1472d2-3.14.0a7+-3cfab44 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.2 ms: 1.03x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 22.0 ms: 1.01x slower                                                    |
| mako            | 4.77 ms                                                  | 4.88 ms: 1.02x slower                                                    |
| django_template | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.03x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250421-macm4pro-arm64-python-3cfab449ab1e3c1472d2-3.14.0a7+-3cfab44 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 8.88 ms: 2.34x faster                                                    |
| mdp                              | 1.09 sec                                                 | 517 ms: 2.11x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 251 ms: 1.98x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 252 ms: 1.90x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 257 ms: 1.79x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 254 ms: 1.76x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.56x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.50x faster                                                     |
| deepcopy                         | 161 us                                                   | 111 us: 1.45x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 13.2 us: 1.39x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.14 us: 1.29x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 264 ms: 1.28x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 7.75 us: 1.27x faster                                                    |
| float                            | 37.9 ms                                                  | 30.4 ms: 1.25x faster                                                    |
| generators                       | 21.9 ms                                                  | 17.7 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 270 ms: 1.24x faster                                                     |
| raytrace                         | 145 ms                                                   | 118 ms: 1.23x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 44.4 ms: 1.22x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 41.7 ns: 1.22x faster                                                    |
| async_generators                 | 206 ms                                                   | 171 ms: 1.20x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 17.7 ms: 1.20x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 50.9 ms: 1.20x faster                                                    |
| go                               | 70.0 ms                                                  | 58.9 ms: 1.19x faster                                                    |
| k_core                           | 1.12 sec                                                 | 943 ms: 1.18x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.17x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.0 ms: 1.17x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 37.8 ms: 1.15x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                    |
| pylint                           | 128 ms                                                   | 114 ms: 1.13x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.12x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 48.9 ms: 1.12x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.56 ms: 1.11x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 64.4 us: 1.10x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.4 ms: 1.10x faster                                                    |
| pyflate                          | 216 ms                                                   | 198 ms: 1.09x faster                                                     |
| nbody                            | 54.2 ms                                                  | 49.8 ms: 1.09x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.37 ms: 1.09x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.82 ms: 1.08x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 132 ms: 1.08x faster                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.9 ms: 1.08x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 63.4 ms: 1.07x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.4 ms: 1.07x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 48.1 ms: 1.07x faster                                                    |
| sphinx                           | 434 ms                                                   | 409 ms: 1.06x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.43 us: 1.06x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.66 us: 1.06x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 43.3 ms: 1.05x faster                                                    |
| sympy_str                        | 104 ms                                                   | 99.2 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.05x faster                                                     |
| sympy_sum                        | 57.6 ms                                                  | 55.1 ms: 1.05x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.2 ms: 1.04x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.99 ms: 1.04x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.7 ms: 1.04x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 927 ms: 1.03x faster                                                     |
| sqlalchemy_declarative           | 46.8 ms                                                  | 45.3 ms: 1.03x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 938 ns: 1.03x faster                                                     |
| genshi_text                      | 10.5 ms                                                  | 10.2 ms: 1.03x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 100 us: 1.02x faster                                                     |
| shortest_path                    | 219 ms                                                   | 215 ms: 1.02x faster                                                     |
| 2to3                             | 114 ms                                                   | 113 ms: 1.01x faster                                                     |
| connected_components             | 201 ms                                                   | 200 ms: 1.00x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 99.4 ms: 1.00x faster                                                    |
| pidigits                         | 161 ms                                                   | 162 ms: 1.00x slower                                                     |
| asyncio_websockets               | 190 ms                                                   | 191 ms: 1.00x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 168 ms: 1.00x slower                                                     |
| richards                         | 22.4 ms                                                  | 22.6 ms: 1.01x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.0 ms: 1.01x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 677 ms: 1.02x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 40.5 ms: 1.02x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                   |
| mako                             | 4.77 ms                                                  | 4.88 ms: 1.02x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 336 ms: 1.02x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 49.3 ms: 1.03x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.9 ms: 1.04x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 146 us: 1.05x slower                                                     |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.45 ms: 1.05x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 441 us: 1.05x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 10.2 ms: 1.06x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 882 us: 1.06x slower                                                     |
| fannkuch                         | 176 ms                                                   | 187 ms: 1.06x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 8.97 ms: 1.12x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.04 ms: 1.17x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 5.00 ms: 1.17x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.72 ms: 1.18x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 133 ms: 1.18x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 254 ms: 1.20x slower                                                     |
| coverage                         | 26.9 ms                                                  | 32.7 ms: 1.22x slower                                                    |
| many_optionals                   | 195 us                                                   | 240 us: 1.23x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 90.3 ms: 2.81x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (4): pycparser, richards_super, gc_traversal, json
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250421-3.14.0a7+-3cfab44/bm-20250421-macm4pro-arm64-python-3cfab449ab1e3c1472d2-3.14.0a7+-3cfab44.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.100x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.12x