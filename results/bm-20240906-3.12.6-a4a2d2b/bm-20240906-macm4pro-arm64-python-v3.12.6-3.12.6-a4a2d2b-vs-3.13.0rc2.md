# Results vs. 3.13.0rc2

- fork: python
- ref: v3.12.6
- machine: darwin-arm64
- commit hash: a4a2d2b
- commit date: 2024-09-06
- overall geometric mean: 1.071x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x slower
- Memory change: 0.95x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b |
|----------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 114 ms: 1.02x slower                                     |
| chameleon      | 2.99 ms                                                        | 3.13 ms: 1.05x slower                                    |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.02x faster                                   |
| sphinx         | 409 ms                                                         | 434 ms: 1.06x slower                                     |
| tornado_http   | 43.2 ms                                                        | 45.1 ms: 1.04x slower                                    |
| Geometric mean | (ref)                                                          | 1.02x slower                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b |
|----------------------------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 446 ms: 1.17x faster                                     |
| async_tree_eager_io              | 525 ms                                                         | 496 ms: 1.06x faster                                     |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 213 ms: 1.02x slower                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 231 ms: 1.03x slower                                     |
| async_tree_eager                 | 43.2 ms                                                        | 45.6 ms: 1.06x slower                                    |
| async_generators                 | 193 ms                                                         | 206 ms: 1.07x slower                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 132 ms: 1.08x slower                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 32.1 ms: 1.11x slower                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 338 ms: 1.12x slower                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 333 ms: 1.14x slower                                     |
| async_tree_io_tg                 | 405 ms                                                         | 480 ms: 1.18x slower                                     |
| async_tree_io                    | 386 ms                                                         | 459 ms: 1.19x slower                                     |
| async_tree_memoization           | 184 ms                                                         | 223 ms: 1.21x slower                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 231 ms: 1.24x slower                                     |
| async_tree_none                  | 142 ms                                                         | 178 ms: 1.25x slower                                     |
| coroutines                       | 10.8 ms                                                        | 13.6 ms: 1.26x slower                                    |
| async_tree_none_tg               | 133 ms                                                         | 172 ms: 1.30x slower                                     |
| Geometric mean                   | (ref)                                                          | 1.11x slower                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b |
|----------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                     |
| float          | 31.4 ms                                                        | 37.9 ms: 1.21x slower                                    |
| nbody          | 42.5 ms                                                        | 54.2 ms: 1.28x slower                                    |
| Geometric mean | (ref)                                                          | 1.14x slower                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b |
|----------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.59 ms: 1.12x faster                                    |
| regex_effbot   | 1.61 ms                                                        | 1.67 ms: 1.03x slower                                    |
| regex_dna      | 94.6 ms                                                        | 99.6 ms: 1.05x slower                                    |
| regex_compile  | 47.9 ms                                                        | 54.6 ms: 1.14x slower                                    |
| Geometric mean | (ref)                                                          | 1.03x slower                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b |
|----------------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 4.26 ms: 1.09x faster                                    |
| tomli_loads          | 1000 ms                                                        | 957 ms: 1.04x faster                                     |
| unpickle_pure_python | 99.5 us                                                        | 103 us: 1.03x slower                                     |
| xml_etree_process    | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                    |
| pickle_pure_python   | 130 us                                                         | 139 us: 1.07x slower                                     |
| xml_etree_generate   | 35.8 ms                                                        | 38.9 ms: 1.09x slower                                    |
| xml_etree_parse      | 62.4 ms                                                        | 67.9 ms: 1.09x slower                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 51.6 ms: 1.12x slower                                    |
| Geometric mean       | (ref)                                                          | 1.03x slower                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b |
|------------------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.01 ms: 1.08x faster                                    |
| python_startup_no_site | 5.95 ms                                                        | 5.71 ms: 1.04x faster                                    |
| Geometric mean         | (ref)                                                          | 1.06x faster                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b |
|-----------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 21.8 ms: 1.02x slower                                    |
| genshi_text     | 9.97 ms                                                        | 10.5 ms: 1.05x slower                                    |
| mako            | 4.41 ms                                                        | 4.77 ms: 1.08x slower                                    |
| django_template | 12.5 ms                                                        | 13.6 ms: 1.09x slower                                    |
| Geometric mean  | (ref)                                                          | 1.06x slower                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b |
|----------------------------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| k_core                           | 1.46 sec                                                       | 1.12 sec: 1.31x faster                                   |
| create_gc_cycles                 | 993 us                                                         | 830 us: 1.20x faster                                     |
| telco                            | 3.07 ms                                                        | 2.61 ms: 1.17x faster                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 446 ms: 1.17x faster                                     |
| coverage                         | 31.2 ms                                                        | 26.9 ms: 1.16x faster                                    |
| regex_v8                         | 10.7 ms                                                        | 9.59 ms: 1.12x faster                                    |
| json_dumps                       | 4.65 ms                                                        | 4.26 ms: 1.09x faster                                    |
| python_startup                   | 8.63 ms                                                        | 8.01 ms: 1.08x faster                                    |
| async_tree_eager_io              | 525 ms                                                         | 496 ms: 1.06x faster                                     |
| scimark_sor                      | 64.0 ms                                                        | 61.0 ms: 1.05x faster                                    |
| tomli_loads                      | 1000 ms                                                        | 957 ms: 1.04x faster                                     |
| python_startup_no_site           | 5.95 ms                                                        | 5.71 ms: 1.04x faster                                    |
| go                               | 72.6 ms                                                        | 70.0 ms: 1.04x faster                                    |
| connected_components             | 208 ms                                                         | 201 ms: 1.04x faster                                     |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                     |
| pyflate                          | 222 ms                                                         | 216 ms: 1.03x faster                                     |
| many_optionals                   | 200 us                                                         | 195 us: 1.03x faster                                     |
| shortest_path                    | 225 ms                                                         | 219 ms: 1.03x faster                                     |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.02x faster                                   |
| djangocms                        | 3.67 us                                                        | 3.59 us: 1.02x faster                                    |
| fannkuch                         | 179 ms                                                         | 176 ms: 1.02x faster                                     |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                     |
| gc_traversal                     | 2.04 ms                                                        | 2.01 ms: 1.02x faster                                    |
| meteor_contest                   | 47.9 ms                                                        | 47.7 ms: 1.00x faster                                    |
| dask                             | 525 ms                                                         | 528 ms: 1.01x slower                                     |
| richards                         | 22.1 ms                                                        | 22.4 ms: 1.02x slower                                    |
| bench_thread_pool                | 412 us                                                         | 419 us: 1.02x slower                                     |
| pprint_safe_repr                 | 322 ms                                                         | 328 ms: 1.02x slower                                     |
| genshi_xml                       | 21.4 ms                                                        | 21.8 ms: 1.02x slower                                    |
| sqlite_synth                     | 948 ns                                                         | 967 ns: 1.02x slower                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 213 ms: 1.02x slower                                     |
| 2to3                             | 112 ms                                                         | 114 ms: 1.02x slower                                     |
| pprint_pformat                   | 650 ms                                                         | 665 ms: 1.02x slower                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 231 ms: 1.03x slower                                     |
| richards_super                   | 24.7 ms                                                        | 25.4 ms: 1.03x slower                                    |
| mdp                              | 1.06 sec                                                       | 1.09 sec: 1.03x slower                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.67 ms: 1.03x slower                                    |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.17 ms: 1.03x slower                                    |
| unpickle_pure_python             | 99.5 us                                                        | 103 us: 1.03x slower                                     |
| thrift                           | 309 us                                                         | 322 us: 1.04x slower                                     |
| tornado_http                     | 43.2 ms                                                        | 45.1 ms: 1.04x slower                                    |
| chameleon                        | 2.99 ms                                                        | 3.13 ms: 1.05x slower                                    |
| sympy_expand                     | 159 ms                                                         | 167 ms: 1.05x slower                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 39.7 ms: 1.05x slower                                    |
| genshi_text                      | 9.97 ms                                                        | 10.5 ms: 1.05x slower                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.24 sec: 1.05x slower                                   |
| regex_dna                        | 94.6 ms                                                        | 99.6 ms: 1.05x slower                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 46.8 ms: 1.05x slower                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                    |
| async_tree_eager                 | 43.2 ms                                                        | 45.6 ms: 1.06x slower                                    |
| sqlglot_optimize                 | 22.2 ms                                                        | 23.4 ms: 1.06x slower                                    |
| pycparser                        | 470 ms                                                         | 497 ms: 1.06x slower                                     |
| sphinx                           | 409 ms                                                         | 434 ms: 1.06x slower                                     |
| sympy_integrate                  | 7.53 ms                                                        | 8.02 ms: 1.07x slower                                    |
| hexiom                           | 2.85 ms                                                        | 3.04 ms: 1.07x slower                                    |
| async_generators                 | 193 ms                                                         | 206 ms: 1.07x slower                                     |
| pickle_pure_python               | 130 us                                                         | 139 us: 1.07x slower                                     |
| dulwich_log                      | 19.8 ms                                                        | 21.3 ms: 1.07x slower                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.2 ms: 1.08x slower                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 132 ms: 1.08x slower                                     |
| mako                             | 4.41 ms                                                        | 4.77 ms: 1.08x slower                                    |
| sqlglot_normalize                | 116 ms                                                         | 126 ms: 1.08x slower                                     |
| xml_etree_generate               | 35.8 ms                                                        | 38.9 ms: 1.09x slower                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 67.9 ms: 1.09x slower                                    |
| django_template                  | 12.5 ms                                                        | 13.6 ms: 1.09x slower                                    |
| sympy_str                        | 95.5 ms                                                        | 104 ms: 1.09x slower                                     |
| sqlglot_transpile                | 637 us                                                         | 696 us: 1.09x slower                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 71.0 us: 1.10x slower                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                     |
| sympy_sum                        | 52.3 ms                                                        | 57.6 ms: 1.10x slower                                    |
| gevent_hub                       | 0.45 ns                                                        | 0.50 ns: 1.11x slower                                    |
| pathlib                          | 11.1 ms                                                        | 12.4 ms: 1.11x slower                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 32.1 ms: 1.11x slower                                    |
| deepcopy_memo                    | 16.5 us                                                        | 18.3 us: 1.11x slower                                    |
| deepcopy                         | 145 us                                                         | 161 us: 1.11x slower                                     |
| sqlglot_parse                    | 519 us                                                         | 577 us: 1.11x slower                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 51.6 ms: 1.12x slower                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 338 ms: 1.12x slower                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.46 us: 1.13x slower                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 333 ms: 1.14x slower                                     |
| regex_compile                    | 47.9 ms                                                        | 54.6 ms: 1.14x slower                                    |
| logging_format                   | 2.45 us                                                        | 2.80 us: 1.15x slower                                    |
| scimark_fft                      | 124 ms                                                         | 142 ms: 1.15x slower                                     |
| logging_simple                   | 2.24 us                                                        | 2.57 us: 1.15x slower                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 38.8 ms: 1.16x slower                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.08 ms: 1.17x slower                                    |
| nqueens                          | 37.2 ms                                                        | 43.5 ms: 1.17x slower                                    |
| async_tree_io_tg                 | 405 ms                                                         | 480 ms: 1.18x slower                                     |
| async_tree_io                    | 386 ms                                                         | 459 ms: 1.19x slower                                     |
| deltablue                        | 1.45 ms                                                        | 1.73 ms: 1.19x slower                                    |
| chaos                            | 24.3 ms                                                        | 28.9 ms: 1.19x slower                                    |
| scimark_lu                       | 42.8 ms                                                        | 51.3 ms: 1.20x slower                                    |
| float                            | 31.4 ms                                                        | 37.9 ms: 1.21x slower                                    |
| async_tree_memoization           | 184 ms                                                         | 223 ms: 1.21x slower                                     |
| pylint                           | 106 ms                                                         | 128 ms: 1.21x slower                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 231 ms: 1.24x slower                                     |
| spectral_norm                    | 43.7 ms                                                        | 54.4 ms: 1.24x slower                                    |
| async_tree_none                  | 142 ms                                                         | 178 ms: 1.25x slower                                     |
| logging_silent                   | 40.6 ns                                                        | 50.9 ns: 1.25x slower                                    |
| coroutines                       | 10.8 ms                                                        | 13.6 ms: 1.26x slower                                    |
| nbody                            | 42.5 ms                                                        | 54.2 ms: 1.28x slower                                    |
| async_tree_none_tg               | 133 ms                                                         | 172 ms: 1.30x slower                                     |
| raytrace                         | 109 ms                                                         | 145 ms: 1.33x slower                                     |
| generators                       | 15.7 ms                                                        | 21.9 ms: 1.40x slower                                    |
| comprehensions                   | 6.80 us                                                        | 9.84 us: 1.45x slower                                    |
| subparsers                       | 6.26 ms                                                        | 20.8 ms: 3.32x slower                                    |
| Geometric mean                   | (ref)                                                          | 1.08x slower                                             |

Benchmark hidden because not significant (3): html5lib, json, json_loads

- Geometric mean (including insignificant results): 1.071x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 0.95x