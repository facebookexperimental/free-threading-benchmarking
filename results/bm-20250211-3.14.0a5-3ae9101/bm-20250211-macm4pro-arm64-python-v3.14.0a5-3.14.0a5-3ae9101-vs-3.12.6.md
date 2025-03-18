# Results vs. 3.12.6

- fork: python
- ref: v3.14.0a5
- machine: darwin-arm64
- commit hash: 3ae9101
- commit date: 2025-02-11
- overall geometric mean: 1.092x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 110 ms: 1.03x faster                                         |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                       |
| html5lib       | 23.0 ms                                                  | 22.1 ms: 1.04x faster                                        |
| sphinx         | 434 ms                                                   | 409 ms: 1.06x faster                                         |
| Geometric mean | (ref)                                                    | 1.03x faster                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 255 ms: 1.94x faster                                         |
| async_tree_io_tg                 | 480 ms                                                   | 262 ms: 1.83x faster                                         |
| async_tree_io                    | 459 ms                                                   | 262 ms: 1.75x faster                                         |
| async_tree_eager_io_tg           | 446 ms                                                   | 267 ms: 1.67x faster                                         |
| async_tree_none_tg               | 172 ms                                                   | 111 ms: 1.55x faster                                         |
| async_tree_none                  | 178 ms                                                   | 118 ms: 1.52x faster                                         |
| async_tree_memoization_tg        | 231 ms                                                   | 153 ms: 1.51x faster                                         |
| async_tree_memoization           | 223 ms                                                   | 153 ms: 1.45x faster                                         |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 266 ms: 1.27x faster                                         |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                         |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                         |
| async_tree_eager_memoization     | 132 ms                                                   | 115 ms: 1.15x faster                                         |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.05x faster                                         |
| async_tree_eager                 | 45.6 ms                                                  | 44.0 ms: 1.04x faster                                        |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.01x slower                                         |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                         |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 139 ms: 1.23x slower                                         |
| async_tree_eager_tg              | 32.1 ms                                                  | 92.7 ms: 2.88x slower                                        |
| Geometric mean                   | (ref)                                                    | 1.21x faster                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 31.5 ms: 1.20x faster                                        |
| nbody          | 54.2 ms                                                  | 50.0 ms: 1.08x faster                                        |
| pidigits       | 161 ms                                                   | 164 ms: 1.02x slower                                         |
| Geometric mean | (ref)                                                    | 1.09x faster                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 47.4 ms: 1.15x faster                                        |
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                        |
| regex_dna      | 99.6 ms                                                  | 93.6 ms: 1.06x faster                                        |
| regex_v8       | 9.59 ms                                                  | 10.8 ms: 1.13x slower                                        |
| Geometric mean | (ref)                                                    | 1.06x faster                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------:|
| tomli_loads          | 957 ms                                                   | 826 ms: 1.16x faster                                         |
| xml_etree_iterparse  | 51.6 ms                                                  | 46.1 ms: 1.12x faster                                        |
| xml_etree_parse      | 67.9 ms                                                  | 62.1 ms: 1.09x faster                                        |
| xml_etree_generate   | 38.9 ms                                                  | 36.5 ms: 1.06x faster                                        |
| unpickle_pure_python | 103 us                                                   | 99.7 us: 1.03x faster                                        |
| xml_etree_process    | 26.7 ms                                                  | 26.4 ms: 1.01x faster                                        |
| json_loads           | 10.9 us                                                  | 11.4 us: 1.05x slower                                        |
| json_dumps           | 4.26 ms                                                  | 5.02 ms: 1.18x slower                                        |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                 |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 5.98 ms: 1.05x slower                                        |
| python_startup         | 8.01 ms                                                  | 8.60 ms: 1.07x slower                                        |
| Geometric mean         | (ref)                                                    | 1.06x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 20.7 ms: 1.05x faster                                        |
| genshi_text     | 10.5 ms                                                  | 10.1 ms: 1.04x faster                                        |
| mako            | 4.77 ms                                                  | 4.73 ms: 1.01x faster                                        |
| django_template | 13.6 ms                                                  | 15.2 ms: 1.11x slower                                        |
| Geometric mean  | (ref)                                                    | 1.00x slower                                                 |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 8.42 ms: 2.47x faster                                        |
| async_tree_eager_io              | 496 ms                                                   | 255 ms: 1.94x faster                                         |
| async_tree_io_tg                 | 480 ms                                                   | 262 ms: 1.83x faster                                         |
| async_tree_io                    | 459 ms                                                   | 262 ms: 1.75x faster                                         |
| async_tree_eager_io_tg           | 446 ms                                                   | 267 ms: 1.67x faster                                         |
| deepcopy                         | 161 us                                                   | 104 us: 1.56x faster                                         |
| async_tree_none_tg               | 172 ms                                                   | 111 ms: 1.55x faster                                         |
| async_tree_none                  | 178 ms                                                   | 118 ms: 1.52x faster                                         |
| async_tree_memoization_tg        | 231 ms                                                   | 153 ms: 1.51x faster                                         |
| deepcopy_memo                    | 18.3 us                                                  | 12.5 us: 1.47x faster                                        |
| async_tree_memoization           | 223 ms                                                   | 153 ms: 1.45x faster                                         |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                        |
| comprehensions                   | 9.84 us                                                  | 7.44 us: 1.32x faster                                        |
| deepcopy_reduce                  | 1.46 us                                                  | 1.11 us: 1.32x faster                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 266 ms: 1.27x faster                                         |
| generators                       | 21.9 ms                                                  | 17.5 ms: 1.26x faster                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                         |
| go                               | 70.0 ms                                                  | 56.9 ms: 1.23x faster                                        |
| spectral_norm                    | 54.4 ms                                                  | 44.8 ms: 1.21x faster                                        |
| float                            | 37.9 ms                                                  | 31.5 ms: 1.20x faster                                        |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.74 ms: 1.19x faster                                        |
| k_core                           | 1.12 sec                                                 | 943 ms: 1.18x faster                                         |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                         |
| logging_silent                   | 50.9 ns                                                  | 43.4 ns: 1.17x faster                                        |
| raytrace                         | 145 ms                                                   | 124 ms: 1.17x faster                                         |
| tomli_loads                      | 957 ms                                                   | 826 ms: 1.16x faster                                         |
| regex_compile                    | 54.6 ms                                                  | 47.4 ms: 1.15x faster                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 115 ms: 1.15x faster                                         |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                        |
| scimark_sor                      | 61.0 ms                                                  | 53.4 ms: 1.14x faster                                        |
| scimark_fft                      | 142 ms                                                   | 124 ms: 1.14x faster                                         |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.99 sec: 1.12x faster                                       |
| xml_etree_iterparse              | 51.6 ms                                                  | 46.1 ms: 1.12x faster                                        |
| pylint                           | 128 ms                                                   | 115 ms: 1.12x faster                                         |
| deltablue                        | 1.73 ms                                                  | 1.55 ms: 1.11x faster                                        |
| pathlib                          | 12.4 ms                                                  | 11.2 ms: 1.10x faster                                        |
| logging_simple                   | 2.57 us                                                  | 2.33 us: 1.10x faster                                        |
| xml_etree_parse                  | 67.9 ms                                                  | 62.1 ms: 1.09x faster                                        |
| typing_runtime_protocols         | 71.0 us                                                  | 64.9 us: 1.09x faster                                        |
| pyflate                          | 216 ms                                                   | 199 ms: 1.09x faster                                         |
| bench_mp_pool                    | 39.7 ms                                                  | 36.6 ms: 1.08x faster                                        |
| nbody                            | 54.2 ms                                                  | 50.0 ms: 1.08x faster                                        |
| sqlglot_parse                    | 577 us                                                   | 533 us: 1.08x faster                                         |
| logging_format                   | 2.80 us                                                  | 2.59 us: 1.08x faster                                        |
| nqueens                          | 43.5 ms                                                  | 40.6 ms: 1.07x faster                                        |
| dulwich_log                      | 21.3 ms                                                  | 19.9 ms: 1.07x faster                                        |
| sqlglot_transpile                | 696 us                                                   | 653 us: 1.07x faster                                         |
| regex_dna                        | 99.6 ms                                                  | 93.6 ms: 1.06x faster                                        |
| xml_etree_generate               | 38.9 ms                                                  | 36.5 ms: 1.06x faster                                        |
| scimark_lu                       | 51.3 ms                                                  | 48.3 ms: 1.06x faster                                        |
| crypto_pyaes                     | 38.8 ms                                                  | 36.6 ms: 1.06x faster                                        |
| sphinx                           | 434 ms                                                   | 409 ms: 1.06x faster                                         |
| chaos                            | 28.9 ms                                                  | 27.3 ms: 1.06x faster                                        |
| sqlalchemy_declarative           | 46.8 ms                                                  | 44.3 ms: 1.06x faster                                        |
| sympy_sum                        | 57.6 ms                                                  | 54.6 ms: 1.05x faster                                        |
| scimark_monte_carlo              | 32.2 ms                                                  | 30.6 ms: 1.05x faster                                        |
| genshi_xml                       | 21.8 ms                                                  | 20.7 ms: 1.05x faster                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.05x faster                                         |
| sympy_str                        | 104 ms                                                   | 99.8 ms: 1.04x faster                                        |
| hexiom                           | 3.04 ms                                                  | 2.91 ms: 1.04x faster                                        |
| html5lib                         | 23.0 ms                                                  | 22.1 ms: 1.04x faster                                        |
| richards_super                   | 25.4 ms                                                  | 24.4 ms: 1.04x faster                                        |
| genshi_text                      | 10.5 ms                                                  | 10.1 ms: 1.04x faster                                        |
| async_tree_eager                 | 45.6 ms                                                  | 44.0 ms: 1.04x faster                                        |
| pycparser                        | 497 ms                                                   | 481 ms: 1.03x faster                                         |
| 2to3                             | 114 ms                                                   | 110 ms: 1.03x faster                                         |
| pprint_pformat                   | 665 ms                                                   | 644 ms: 1.03x faster                                         |
| unpickle_pure_python             | 103 us                                                   | 99.7 us: 1.03x faster                                        |
| richards                         | 22.4 ms                                                  | 21.7 ms: 1.03x faster                                        |
| thrift                           | 322 us                                                   | 312 us: 1.03x faster                                         |
| pprint_safe_repr                 | 328 ms                                                   | 320 ms: 1.03x faster                                         |
| fannkuch                         | 176 ms                                                   | 172 ms: 1.02x faster                                         |
| mdp                              | 1.09 sec                                                 | 1.08 sec: 1.02x faster                                       |
| sqlglot_optimize                 | 23.4 ms                                                  | 23.1 ms: 1.01x faster                                        |
| sqlite_synth                     | 967 ns                                                   | 954 ns: 1.01x faster                                         |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.11 ms: 1.01x faster                                        |
| shortest_path                    | 219 ms                                                   | 216 ms: 1.01x faster                                         |
| xml_etree_process                | 26.7 ms                                                  | 26.4 ms: 1.01x faster                                        |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                         |
| sqlglot_normalize                | 126 ms                                                   | 124 ms: 1.01x faster                                         |
| mako                             | 4.77 ms                                                  | 4.73 ms: 1.01x faster                                        |
| sympy_integrate                  | 8.02 ms                                                  | 7.96 ms: 1.01x faster                                        |
| connected_components             | 201 ms                                                   | 199 ms: 1.01x faster                                         |
| meteor_contest                   | 47.7 ms                                                  | 48.0 ms: 1.00x slower                                        |
| sympy_expand                     | 167 ms                                                   | 168 ms: 1.01x slower                                         |
| json                             | 1.93 ms                                                  | 1.95 ms: 1.01x slower                                        |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.01x slower                                         |
| pidigits                         | 161 ms                                                   | 164 ms: 1.02x slower                                         |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                       |
| bench_thread_pool                | 419 us                                                   | 429 us: 1.02x slower                                         |
| gc_traversal                     | 2.01 ms                                                  | 2.10 ms: 1.05x slower                                        |
| python_startup_no_site           | 5.71 ms                                                  | 5.98 ms: 1.05x slower                                        |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                        |
| python_startup                   | 8.01 ms                                                  | 8.60 ms: 1.07x slower                                        |
| create_gc_cycles                 | 830 us                                                   | 903 us: 1.09x slower                                         |
| django_template                  | 13.6 ms                                                  | 15.2 ms: 1.11x slower                                        |
| regex_v8                         | 9.59 ms                                                  | 10.8 ms: 1.13x slower                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                         |
| many_optionals                   | 195 us                                                   | 229 us: 1.17x slower                                         |
| json_dumps                       | 4.26 ms                                                  | 5.02 ms: 1.18x slower                                        |
| telco                            | 2.61 ms                                                  | 3.17 ms: 1.21x slower                                        |
| coverage                         | 26.9 ms                                                  | 32.8 ms: 1.22x slower                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 139 ms: 1.23x slower                                         |
| async_tree_eager_tg              | 32.1 ms                                                  | 92.7 ms: 2.88x slower                                        |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                 |

Benchmark hidden because not significant (1): pickle_pure_python
Ignored benchmarks (4) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, tornado_http

- Geometric mean (including insignificant results): 1.092x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.11x