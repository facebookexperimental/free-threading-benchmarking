# Results vs. 3.12.6

- fork: python
- ref: 1a0edb1fa899c067f19b
- machine: darwin-arm64
- commit hash: 1a0edb1
- commit date: 2026-04-09
- overall geometric mean: 1.102x faster
- HPT reliability: 99.91%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.38x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8+-1a0edb1 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 123 ms: 1.08x slower                                                     |
| docutils       | 1.02 sec                                                 | 977 ms: 1.05x faster                                                     |
| html5lib       | 23.0 ms                                                  | 22.7 ms: 1.01x faster                                                    |
| sphinx         | 434 ms                                                   | 416 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8+-1a0edb1 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 242 ms: 2.05x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 241 ms: 1.99x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 245 ms: 1.87x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 240 ms: 1.86x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 143 ms: 1.62x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.60x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.53x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.49x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 255 ms: 1.33x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 264 ms: 1.26x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 113 ms: 1.17x faster                                                     |
| async_generators                 | 206 ms                                                   | 186 ms: 1.11x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 184 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 47.5 ms: 1.04x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 242 ms: 1.14x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.1 ms: 2.90x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8+-1a0edb1 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.5 ms: 1.33x faster                                                    |
| pidigits       | 161 ms                                                   | 159 ms: 1.01x faster                                                     |
| nbody          | 54.2 ms                                                  | 56.5 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8+-1a0edb1 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 50.8 ms: 1.07x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.08 ms: 1.06x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.9 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8+-1a0edb1 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.4 ms: 1.34x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 56.1 ms: 1.21x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.76 ms: 1.13x faster                                                    |
| tomli_loads          | 957 ms                                                   | 874 ms: 1.10x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 37.2 ms: 1.05x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 26.7 ms: 1.00x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 108 us: 1.05x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 147 us: 1.06x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8+-1a0edb1 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.68 ms: 1.21x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.04 ms: 1.23x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.22x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8+-1a0edb1 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 22.4 ms: 1.03x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.0 ms: 1.05x slower                                                    |
| django_template | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                    |
| mako            | 4.77 ms                                                  | 5.62 ms: 1.18x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.09x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8+-1a0edb1 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.10 ms: 5.07x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 788 us: 2.55x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 242 ms: 2.05x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 241 ms: 1.99x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 245 ms: 1.87x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 240 ms: 1.86x faster                                                     |
| mdp                              | 1.09 sec                                                 | 597 ms: 1.83x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 512 us: 1.62x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 143 ms: 1.62x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.60x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.53x faster                                                     |
| deepcopy                         | 161 us                                                   | 108 us: 1.50x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.49x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 13.0 us: 1.41x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.4 ms: 1.34x faster                                                    |
| float                            | 37.9 ms                                                  | 28.5 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 255 ms: 1.33x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 264 ms: 1.26x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.17 us: 1.25x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 780 ns: 1.24x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 56.1 ms: 1.21x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.28 us: 1.19x faster                                                    |
| go                               | 70.0 ms                                                  | 59.1 ms: 1.18x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 43.0 ns: 1.18x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 113 ms: 1.17x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.16x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.94 sec: 1.16x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.5 ms: 1.15x faster                                                    |
| raytrace                         | 145 ms                                                   | 126 ms: 1.15x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.76 ms: 1.13x faster                                                    |
| k_core                           | 1.12 sec                                                 | 989 ms: 1.13x faster                                                     |
| pyflate                          | 216 ms                                                   | 191 ms: 1.13x faster                                                     |
| pylint                           | 128 ms                                                   | 115 ms: 1.11x faster                                                     |
| async_generators                 | 206 ms                                                   | 186 ms: 1.11x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 874 ms: 1.10x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 129 ms: 1.10x faster                                                     |
| pycparser                        | 497 ms                                                   | 455 ms: 1.09x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.36 us: 1.09x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 56.1 ms: 1.09x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 40.3 ms: 1.08x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.60 us: 1.08x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.5 ms: 1.08x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 50.8 ms: 1.07x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.1 ms: 1.07x faster                                                    |
| generators                       | 21.9 ms                                                  | 20.8 ms: 1.06x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.63 ms: 1.06x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.08 ms: 1.06x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 94.9 ms: 1.05x faster                                                    |
| docutils                         | 1.02 sec                                                 | 977 ms: 1.05x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 37.2 ms: 1.05x faster                                                    |
| sphinx                           | 434 ms                                                   | 416 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 184 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                     |
| fannkuch                         | 176 ms                                                   | 172 ms: 1.02x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.7 ms: 1.01x faster                                                    |
| pidigits                         | 161 ms                                                   | 159 ms: 1.01x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.97 ms: 1.01x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.7 ms: 1.00x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 671 ms: 1.01x slower                                                     |
| json                             | 1.93 ms                                                  | 1.96 ms: 1.02x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.12 ms: 1.03x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.1 ms: 1.03x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.4 ms: 1.03x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 73.2 us: 1.03x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.2 ms: 1.04x slower                                                    |
| nbody                            | 54.2 ms                                                  | 56.5 ms: 1.04x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 47.5 ms: 1.04x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 60.1 ms: 1.04x slower                                                    |
| sympy_str                        | 104 ms                                                   | 109 ms: 1.05x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 11.0 ms: 1.05x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 26.7 ms: 1.05x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 108 us: 1.05x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 147 us: 1.06x slower                                                     |
| thrift                           | 322 us                                                   | 343 us: 1.07x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 55.1 ms: 1.07x slower                                                    |
| 2to3                             | 114 ms                                                   | 123 ms: 1.08x slower                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.30 ms: 1.11x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 186 ms: 1.11x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 44.0 ms: 1.13x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 242 ms: 1.14x slower                                                     |
| shortest_path                    | 219 ms                                                   | 250 ms: 1.14x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 55.0 ms: 1.15x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.01 ms: 1.15x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.62 ms: 1.18x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 47.4 ms: 1.19x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.68 ms: 1.21x slower                                                    |
| connected_components             | 201 ms                                                   | 244 ms: 1.22x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 7.04 ms: 1.23x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 566 us: 1.35x slower                                                     |
| many_optionals                   | 195 us                                                   | 266 us: 1.36x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.9 ms: 1.45x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.1 ms: 2.90x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (2): pprint_safe_repr, dask
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260409-3.15.0a8+-1a0edb1-NOGIL/bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8+-1a0edb1.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.102x faster

# HPT report

- Reliability score: 99.91% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.38x