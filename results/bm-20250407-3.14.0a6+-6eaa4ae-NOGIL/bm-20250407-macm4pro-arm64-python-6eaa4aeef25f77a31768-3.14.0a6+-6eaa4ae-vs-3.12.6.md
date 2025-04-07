# Results vs. 3.12.6

- fork: python
- ref: 6eaa4aeef25f77a31768
- machine: darwin-arm64
- commit hash: 6eaa4ae
- commit date: 2025-04-07
- overall geometric mean: 1.111x faster
- HPT reliability: 99.83%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6+-6eaa4ae |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 119 ms: 1.04x slower                                                     |
| docutils       | 1.02 sec                                                 | 982 ms: 1.04x faster                                                     |
| sphinx         | 434 ms                                                   | 411 ms: 1.06x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x faster                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6+-6eaa4ae |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 195 ms: 2.46x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 203 ms: 2.44x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 193 ms: 2.31x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 208 ms: 2.21x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 85.8 ms: 2.01x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 229 ms: 1.48x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 239 ms: 1.40x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                    |
| async_generators                 | 206 ms                                                   | 174 ms: 1.19x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.06x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 221 ms: 1.04x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 50.2 ms: 1.10x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.5 ms: 2.41x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.39x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6+-6eaa4ae |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.6 ms: 1.37x faster                                                    |
| pidigits       | 161 ms                                                   | 157 ms: 1.03x faster                                                     |
| nbody          | 54.2 ms                                                  | 53.2 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                    | 1.13x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6+-6eaa4ae |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 52.2 ms: 1.04x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 97.6 ms: 1.02x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.68 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6+-6eaa4ae |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 35.2 ms: 1.46x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 54.9 ms: 1.24x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 36.0 ms: 1.08x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 26.2 ms: 1.02x faster                                                    |
| tomli_loads          | 957 ms                                                   | 946 ms: 1.01x faster                                                     |
| unpickle_pure_python | 103 us                                                   | 107 us: 1.04x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.6 us: 1.07x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 150 us: 1.07x slower                                                     |
| json_dumps           | 4.26 ms                                                  | 4.98 ms: 1.17x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6+-6eaa4ae |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.42 ms: 1.18x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.50 ms: 1.32x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.24x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6+-6eaa4ae |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.3 ms: 1.07x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                    |
| mako            | 4.77 ms                                                  | 5.42 ms: 1.14x slower                                                    |
| django_template | 13.6 ms                                                  | 16.4 ms: 1.21x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.12x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6+-6eaa4ae |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 732 us: 2.74x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 195 ms: 2.46x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 203 ms: 2.44x faster                                                     |
| subparsers                       | 20.8 ms                                                  | 8.74 ms: 2.38x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 193 ms: 2.31x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 208 ms: 2.21x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 85.8 ms: 2.01x faster                                                    |
| mdp                              | 1.09 sec                                                 | 563 ms: 1.94x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 444 us: 1.87x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 229 ms: 1.48x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 35.2 ms: 1.46x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 239 ms: 1.40x faster                                                     |
| float                            | 37.9 ms                                                  | 27.6 ms: 1.37x faster                                                    |
| deepcopy                         | 161 us                                                   | 122 us: 1.32x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 14.5 us: 1.26x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 54.9 ms: 1.24x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 812 ns: 1.19x faster                                                     |
| async_generators                 | 206 ms                                                   | 174 ms: 1.19x faster                                                     |
| generators                       | 21.9 ms                                                  | 18.5 ms: 1.19x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 18.1 ms: 1.17x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.26 us: 1.16x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.53 us: 1.15x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                   |
| k_core                           | 1.12 sec                                                 | 985 ms: 1.14x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                    |
| raytrace                         | 145 ms                                                   | 129 ms: 1.13x faster                                                     |
| go                               | 70.0 ms                                                  | 62.5 ms: 1.12x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 54.7 ms: 1.11x faster                                                    |
| pylint                           | 128 ms                                                   | 116 ms: 1.11x faster                                                     |
| pyflate                          | 216 ms                                                   | 197 ms: 1.10x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 36.0 ms: 1.08x faster                                                    |
| pycparser                        | 497 ms                                                   | 462 ms: 1.08x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 50.9 ms: 1.07x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 47.9 ns: 1.06x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 41.1 ms: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.06x faster                                                     |
| sphinx                           | 434 ms                                                   | 411 ms: 1.06x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.64 ms: 1.05x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 52.2 ms: 1.04x faster                                                    |
| docutils                         | 1.02 sec                                                 | 982 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 138 ms: 1.03x faster                                                     |
| pidigits                         | 161 ms                                                   | 157 ms: 1.03x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.51 us: 1.02x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.2 ms: 1.02x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 97.6 ms: 1.02x faster                                                    |
| nbody                            | 54.2 ms                                                  | 53.2 ms: 1.02x faster                                                    |
| chaos                            | 28.9 ms                                                  | 28.6 ms: 1.01x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 946 ms: 1.01x faster                                                     |
| logging_format                   | 2.80 us                                                  | 2.77 us: 1.01x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.93 ms: 1.01x faster                                                    |
| json                             | 1.93 ms                                                  | 1.95 ms: 1.01x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.68 ms: 1.01x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.10 ms: 1.01x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 72.0 us: 1.01x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.11 ms: 1.02x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.1 ms: 1.03x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 40.9 ms: 1.03x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 59.6 ms: 1.03x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 40.3 ms: 1.04x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 221 ms: 1.04x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 107 us: 1.04x slower                                                     |
| sympy_str                        | 104 ms                                                   | 109 ms: 1.04x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 53.5 ms: 1.04x slower                                                    |
| 2to3                             | 114 ms                                                   | 119 ms: 1.04x slower                                                     |
| sqlalchemy_declarative           | 46.8 ms                                                  | 49.2 ms: 1.05x slower                                                    |
| shortest_path                    | 219 ms                                                   | 231 ms: 1.06x slower                                                     |
| genshi_xml                       | 21.8 ms                                                  | 23.3 ms: 1.07x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.6 us: 1.07x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                    |
| richards                         | 22.4 ms                                                  | 24.1 ms: 1.07x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 150 us: 1.07x slower                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 353 ms: 1.08x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 717 ms: 1.08x slower                                                     |
| richards_super                   | 25.4 ms                                                  | 27.4 ms: 1.08x slower                                                    |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.63 ms: 1.09x slower                                                    |
| connected_components             | 201 ms                                                   | 219 ms: 1.09x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 50.2 ms: 1.10x slower                                                    |
| fannkuch                         | 176 ms                                                   | 194 ms: 1.10x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 186 ms: 1.11x slower                                                     |
| mako                             | 4.77 ms                                                  | 5.42 ms: 1.14x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 55.0 ms: 1.15x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.98 ms: 1.17x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.42 ms: 1.18x slower                                                    |
| django_template                  | 13.6 ms                                                  | 16.4 ms: 1.21x slower                                                    |
| many_optionals                   | 195 us                                                   | 237 us: 1.21x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.19 ms: 1.22x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.50 ms: 1.32x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 577 us: 1.38x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.6 ms: 1.44x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.5 ms: 2.41x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (2): async_tree_eager_memoization_tg, html5lib
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250407-3.14.0a6+-6eaa4ae-NOGIL/bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6+-6eaa4ae.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.111x faster

# HPT report

- Reliability score: 99.83% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.22x