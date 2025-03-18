# Results vs. 3.12.6

- fork: python
- ref: v3.13.0rc2
- machine: darwin-arm64
- commit hash: ec61006
- commit date: 2024-09-06
- overall geometric mean: 1.077x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.06x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:--------------------------------------------------------:|:--------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 112 ms: 1.02x faster                                           |
| chameleon      | 3.13 ms                                                  | 2.99 ms: 1.05x faster                                          |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.02x slower                                         |
| sphinx         | 434 ms                                                   | 409 ms: 1.06x faster                                           |
| tornado_http   | 45.1 ms                                                  | 43.2 ms: 1.04x faster                                          |
| Geometric mean | (ref)                                                    | 1.02x faster                                                   |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------------------------|:--------------------------------------------------------:|:--------------------------------------------------------------:|
| async_tree_none_tg               | 172 ms                                                   | 133 ms: 1.30x faster                                           |
| coroutines                       | 13.6 ms                                                  | 10.8 ms: 1.26x faster                                          |
| async_tree_none                  | 178 ms                                                   | 142 ms: 1.25x faster                                           |
| async_tree_memoization_tg        | 231 ms                                                   | 186 ms: 1.24x faster                                           |
| async_tree_memoization           | 223 ms                                                   | 184 ms: 1.21x faster                                           |
| async_tree_io                    | 459 ms                                                   | 386 ms: 1.19x faster                                           |
| async_tree_io_tg                 | 480 ms                                                   | 405 ms: 1.18x faster                                           |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 294 ms: 1.14x faster                                           |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 301 ms: 1.12x faster                                           |
| async_tree_eager_tg              | 32.1 ms                                                  | 28.9 ms: 1.11x faster                                          |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 103 ms: 1.10x faster                                           |
| async_tree_eager_memoization     | 132 ms                                                   | 122 ms: 1.08x faster                                           |
| async_generators                 | 206 ms                                                   | 193 ms: 1.07x faster                                           |
| async_tree_eager                 | 45.6 ms                                                  | 43.2 ms: 1.06x faster                                          |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                           |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 208 ms: 1.02x faster                                           |
| asyncio_websockets               | 190 ms                                                   | 194 ms: 1.02x slower                                           |
| async_tree_eager_io              | 496 ms                                                   | 525 ms: 1.06x slower                                           |
| async_tree_eager_io_tg           | 446 ms                                                   | 521 ms: 1.17x slower                                           |
| Geometric mean                   | (ref)                                                    | 1.11x faster                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:--------------------------------------------------------:|:--------------------------------------------------------------:|
| nbody          | 54.2 ms                                                  | 42.5 ms: 1.28x faster                                          |
| float          | 37.9 ms                                                  | 31.4 ms: 1.21x faster                                          |
| pidigits       | 161 ms                                                   | 166 ms: 1.03x slower                                           |
| Geometric mean | (ref)                                                    | 1.14x faster                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:--------------------------------------------------------:|:--------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 47.9 ms: 1.14x faster                                          |
| regex_dna      | 99.6 ms                                                  | 94.6 ms: 1.05x faster                                          |
| regex_effbot   | 1.67 ms                                                  | 1.61 ms: 1.03x faster                                          |
| regex_v8       | 9.59 ms                                                  | 10.7 ms: 1.12x slower                                          |
| Geometric mean | (ref)                                                    | 1.03x faster                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------------|:--------------------------------------------------------:|:--------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 46.1 ms: 1.12x faster                                          |
| xml_etree_parse      | 67.9 ms                                                  | 62.4 ms: 1.09x faster                                          |
| xml_etree_generate   | 38.9 ms                                                  | 35.8 ms: 1.09x faster                                          |
| pickle_pure_python   | 139 us                                                   | 130 us: 1.07x faster                                           |
| xml_etree_process    | 26.7 ms                                                  | 25.4 ms: 1.05x faster                                          |
| unpickle_pure_python | 103 us                                                   | 99.5 us: 1.03x faster                                          |
| tomli_loads          | 957 ms                                                   | 1000 ms: 1.04x slower                                          |
| json_dumps           | 4.26 ms                                                  | 4.65 ms: 1.09x slower                                          |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                   |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|------------------------|:--------------------------------------------------------:|:--------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 5.95 ms: 1.04x slower                                          |
| python_startup         | 8.01 ms                                                  | 8.63 ms: 1.08x slower                                          |
| Geometric mean         | (ref)                                                    | 1.06x slower                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|-----------------|:--------------------------------------------------------:|:--------------------------------------------------------------:|
| django_template | 13.6 ms                                                  | 12.5 ms: 1.09x faster                                          |
| mako            | 4.77 ms                                                  | 4.41 ms: 1.08x faster                                          |
| genshi_text     | 10.5 ms                                                  | 9.97 ms: 1.05x faster                                          |
| genshi_xml      | 21.8 ms                                                  | 21.4 ms: 1.02x faster                                          |
| Geometric mean  | (ref)                                                    | 1.06x faster                                                   |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------------------------|:--------------------------------------------------------:|:--------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 6.26 ms: 3.32x faster                                          |
| comprehensions                   | 9.84 us                                                  | 6.80 us: 1.45x faster                                          |
| generators                       | 21.9 ms                                                  | 15.7 ms: 1.40x faster                                          |
| raytrace                         | 145 ms                                                   | 109 ms: 1.33x faster                                           |
| async_tree_none_tg               | 172 ms                                                   | 133 ms: 1.30x faster                                           |
| nbody                            | 54.2 ms                                                  | 42.5 ms: 1.28x faster                                          |
| coroutines                       | 13.6 ms                                                  | 10.8 ms: 1.26x faster                                          |
| logging_silent                   | 50.9 ns                                                  | 40.6 ns: 1.25x faster                                          |
| async_tree_none                  | 178 ms                                                   | 142 ms: 1.25x faster                                           |
| spectral_norm                    | 54.4 ms                                                  | 43.7 ms: 1.24x faster                                          |
| async_tree_memoization_tg        | 231 ms                                                   | 186 ms: 1.24x faster                                           |
| pylint                           | 128 ms                                                   | 106 ms: 1.21x faster                                           |
| async_tree_memoization           | 223 ms                                                   | 184 ms: 1.21x faster                                           |
| float                            | 37.9 ms                                                  | 31.4 ms: 1.21x faster                                          |
| scimark_lu                       | 51.3 ms                                                  | 42.8 ms: 1.20x faster                                          |
| chaos                            | 28.9 ms                                                  | 24.3 ms: 1.19x faster                                          |
| deltablue                        | 1.73 ms                                                  | 1.45 ms: 1.19x faster                                          |
| async_tree_io                    | 459 ms                                                   | 386 ms: 1.19x faster                                           |
| async_tree_io_tg                 | 480 ms                                                   | 405 ms: 1.18x faster                                           |
| nqueens                          | 43.5 ms                                                  | 37.2 ms: 1.17x faster                                          |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.78 ms: 1.17x faster                                          |
| crypto_pyaes                     | 38.8 ms                                                  | 33.6 ms: 1.16x faster                                          |
| logging_simple                   | 2.57 us                                                  | 2.24 us: 1.15x faster                                          |
| scimark_fft                      | 142 ms                                                   | 124 ms: 1.15x faster                                           |
| logging_format                   | 2.80 us                                                  | 2.45 us: 1.15x faster                                          |
| regex_compile                    | 54.6 ms                                                  | 47.9 ms: 1.14x faster                                          |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 294 ms: 1.14x faster                                           |
| deepcopy_reduce                  | 1.46 us                                                  | 1.30 us: 1.13x faster                                          |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 301 ms: 1.12x faster                                           |
| xml_etree_iterparse              | 51.6 ms                                                  | 46.1 ms: 1.12x faster                                          |
| sqlglot_parse                    | 577 us                                                   | 519 us: 1.11x faster                                           |
| deepcopy                         | 161 us                                                   | 145 us: 1.11x faster                                           |
| deepcopy_memo                    | 18.3 us                                                  | 16.5 us: 1.11x faster                                          |
| async_tree_eager_tg              | 32.1 ms                                                  | 28.9 ms: 1.11x faster                                          |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.11x faster                                          |
| gevent_hub                       | 0.50 ns                                                  | 0.45 ns: 1.11x faster                                          |
| sympy_sum                        | 57.6 ms                                                  | 52.3 ms: 1.10x faster                                          |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 103 ms: 1.10x faster                                           |
| typing_runtime_protocols         | 71.0 us                                                  | 64.6 us: 1.10x faster                                          |
| sqlglot_transpile                | 696 us                                                   | 637 us: 1.09x faster                                           |
| sympy_str                        | 104 ms                                                   | 95.5 ms: 1.09x faster                                          |
| django_template                  | 13.6 ms                                                  | 12.5 ms: 1.09x faster                                          |
| xml_etree_parse                  | 67.9 ms                                                  | 62.4 ms: 1.09x faster                                          |
| xml_etree_generate               | 38.9 ms                                                  | 35.8 ms: 1.09x faster                                          |
| sqlglot_normalize                | 126 ms                                                   | 116 ms: 1.08x faster                                           |
| mako                             | 4.77 ms                                                  | 4.41 ms: 1.08x faster                                          |
| async_tree_eager_memoization     | 132 ms                                                   | 122 ms: 1.08x faster                                           |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.9 ms: 1.08x faster                                          |
| dulwich_log                      | 21.3 ms                                                  | 19.8 ms: 1.07x faster                                          |
| pickle_pure_python               | 139 us                                                   | 130 us: 1.07x faster                                           |
| async_generators                 | 206 ms                                                   | 193 ms: 1.07x faster                                           |
| hexiom                           | 3.04 ms                                                  | 2.85 ms: 1.07x faster                                          |
| sympy_integrate                  | 8.02 ms                                                  | 7.53 ms: 1.07x faster                                          |
| sphinx                           | 434 ms                                                   | 409 ms: 1.06x faster                                           |
| pycparser                        | 497 ms                                                   | 470 ms: 1.06x faster                                           |
| sqlglot_optimize                 | 23.4 ms                                                  | 22.2 ms: 1.06x faster                                          |
| async_tree_eager                 | 45.6 ms                                                  | 43.2 ms: 1.06x faster                                          |
| xml_etree_process                | 26.7 ms                                                  | 25.4 ms: 1.05x faster                                          |
| sqlalchemy_declarative           | 46.8 ms                                                  | 44.4 ms: 1.05x faster                                          |
| regex_dna                        | 99.6 ms                                                  | 94.6 ms: 1.05x faster                                          |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.13 sec: 1.05x faster                                         |
| genshi_text                      | 10.5 ms                                                  | 9.97 ms: 1.05x faster                                          |
| bench_mp_pool                    | 39.7 ms                                                  | 37.8 ms: 1.05x faster                                          |
| sympy_expand                     | 167 ms                                                   | 159 ms: 1.05x faster                                           |
| chameleon                        | 3.13 ms                                                  | 2.99 ms: 1.05x faster                                          |
| tornado_http                     | 45.1 ms                                                  | 43.2 ms: 1.04x faster                                          |
| thrift                           | 322 us                                                   | 309 us: 1.04x faster                                           |
| unpickle_pure_python             | 103 us                                                   | 99.5 us: 1.03x faster                                          |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.00 ms: 1.03x faster                                          |
| regex_effbot                     | 1.67 ms                                                  | 1.61 ms: 1.03x faster                                          |
| mdp                              | 1.09 sec                                                 | 1.06 sec: 1.03x faster                                         |
| richards_super                   | 25.4 ms                                                  | 24.7 ms: 1.03x faster                                          |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                           |
| pprint_pformat                   | 665 ms                                                   | 650 ms: 1.02x faster                                           |
| 2to3                             | 114 ms                                                   | 112 ms: 1.02x faster                                           |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 208 ms: 1.02x faster                                           |
| sqlite_synth                     | 967 ns                                                   | 948 ns: 1.02x faster                                           |
| genshi_xml                       | 21.8 ms                                                  | 21.4 ms: 1.02x faster                                          |
| pprint_safe_repr                 | 328 ms                                                   | 322 ms: 1.02x faster                                           |
| bench_thread_pool                | 419 us                                                   | 412 us: 1.02x faster                                           |
| richards                         | 22.4 ms                                                  | 22.1 ms: 1.02x faster                                          |
| dask                             | 528 ms                                                   | 525 ms: 1.01x faster                                           |
| meteor_contest                   | 47.7 ms                                                  | 47.9 ms: 1.00x slower                                          |
| gc_traversal                     | 2.01 ms                                                  | 2.04 ms: 1.02x slower                                          |
| asyncio_websockets               | 190 ms                                                   | 194 ms: 1.02x slower                                           |
| fannkuch                         | 176 ms                                                   | 179 ms: 1.02x slower                                           |
| djangocms                        | 3.59 us                                                  | 3.67 us: 1.02x slower                                          |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.02x slower                                         |
| shortest_path                    | 219 ms                                                   | 225 ms: 1.03x slower                                           |
| many_optionals                   | 195 us                                                   | 200 us: 1.03x slower                                           |
| pyflate                          | 216 ms                                                   | 222 ms: 1.03x slower                                           |
| pidigits                         | 161 ms                                                   | 166 ms: 1.03x slower                                           |
| connected_components             | 201 ms                                                   | 208 ms: 1.04x slower                                           |
| go                               | 70.0 ms                                                  | 72.6 ms: 1.04x slower                                          |
| python_startup_no_site           | 5.71 ms                                                  | 5.95 ms: 1.04x slower                                          |
| tomli_loads                      | 957 ms                                                   | 1000 ms: 1.04x slower                                          |
| scimark_sor                      | 61.0 ms                                                  | 64.0 ms: 1.05x slower                                          |
| async_tree_eager_io              | 496 ms                                                   | 525 ms: 1.06x slower                                           |
| python_startup                   | 8.01 ms                                                  | 8.63 ms: 1.08x slower                                          |
| json_dumps                       | 4.26 ms                                                  | 4.65 ms: 1.09x slower                                          |
| regex_v8                         | 9.59 ms                                                  | 10.7 ms: 1.12x slower                                          |
| coverage                         | 26.9 ms                                                  | 31.2 ms: 1.16x slower                                          |
| async_tree_eager_io_tg           | 446 ms                                                   | 521 ms: 1.17x slower                                           |
| telco                            | 2.61 ms                                                  | 3.07 ms: 1.17x slower                                          |
| create_gc_cycles                 | 830 us                                                   | 993 us: 1.20x slower                                           |
| k_core                           | 1.12 sec                                                 | 1.46 sec: 1.31x slower                                         |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                   |

Benchmark hidden because not significant (3): json_loads, json, html5lib

- Geometric mean (including insignificant results): 1.077x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.06x