# Results vs. 3.12.6

- fork: python
- ref: 2b0c684e0759dc3fec0e
- machine: darwin-arm64
- commit hash: 2b0c684
- commit date: 2025-06-12
- overall geometric mean: 1.110x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 113 ms: 1.01x faster                                                    |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.0 ms: 1.04x slower                                                   |
| sphinx         | 434 ms                                                   | 412 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.00x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 246 ms: 2.02x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 249 ms: 1.93x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 252 ms: 1.82x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 254 ms: 1.75x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.59x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.57x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.52x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 264 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                                    |
| async_generators                 | 206 ms                                                   | 171 ms: 1.21x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.9 ms: 1.09x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.18x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.5 ms: 2.72x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.8 ms: 1.27x faster                                                   |
| nbody          | 54.2 ms                                                  | 47.3 ms: 1.15x faster                                                   |
| pidigits       | 161 ms                                                   | 167 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.12x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 47.8 ms: 1.14x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 97.6 ms: 1.02x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.71 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 43.9 ms: 1.17x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.1 ms: 1.11x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 61.4 ms: 1.11x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 24.8 ms: 1.08x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 98.2 us: 1.05x faster                                                   |
| tomli_loads          | 957 ms                                                   | 918 ms: 1.04x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.8 us: 1.01x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 4.43 ms: 1.04x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 145 us: 1.04x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.71 ms: 1.09x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.23 ms: 1.09x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.79 ms: 1.07x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 21.3 ms: 1.02x faster                                                   |
| mako            | 4.77 ms                                                  | 4.81 ms: 1.01x slower                                                   |
| django_template | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.01x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.57 ms: 2.17x faster                                                   |
| mdp                              | 1.09 sec                                                 | 513 ms: 2.13x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 246 ms: 2.02x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 249 ms: 1.93x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 252 ms: 1.82x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 254 ms: 1.75x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.59x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.57x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.52x faster                                                    |
| deepcopy                         | 161 us                                                   | 110 us: 1.47x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.5 us: 1.46x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.42 us: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 264 ms: 1.28x faster                                                    |
| float                            | 37.9 ms                                                  | 29.8 ms: 1.27x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.3 ms: 1.27x faster                                                   |
| go                               | 70.0 ms                                                  | 55.7 ms: 1.26x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.16 us: 1.25x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                                    |
| raytrace                         | 145 ms                                                   | 117 ms: 1.24x faster                                                    |
| async_generators                 | 206 ms                                                   | 171 ms: 1.21x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 50.8 ms: 1.20x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 17.9 ms: 1.19x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 45.8 ms: 1.19x faster                                                   |
| k_core                           | 1.12 sec                                                 | 950 ms: 1.18x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.9 ms: 1.17x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 61.7 us: 1.15x faster                                                   |
| nbody                            | 54.2 ms                                                  | 47.3 ms: 1.15x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.51 ms: 1.14x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 47.8 ms: 1.14x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.14x faster                                                  |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 38.6 ms: 1.13x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.86 ms: 1.12x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.9 ms: 1.12x faster                                                   |
| pylint                           | 128 ms                                                   | 115 ms: 1.11x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.1 ms: 1.11x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 35.1 ms: 1.11x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 61.4 ms: 1.11x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.75 ms: 1.11x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.2 ms: 1.10x faster                                                   |
| pyflate                          | 216 ms                                                   | 196 ms: 1.10x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 130 ms: 1.09x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.9 ms: 1.09x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 47.5 ms: 1.08x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 24.8 ms: 1.08x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 9.79 ms: 1.07x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.51 ms: 1.07x faster                                                   |
| thrift                           | 322 us                                                   | 302 us: 1.07x faster                                                    |
| sphinx                           | 434 ms                                                   | 412 ms: 1.05x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 98.2 us: 1.05x faster                                                   |
| sympy_str                        | 104 ms                                                   | 99.5 ms: 1.05x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 918 ms: 1.04x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 24.6 ms: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.9 ms: 1.03x faster                                                   |
| richards                         | 22.4 ms                                                  | 21.9 ms: 1.02x faster                                                   |
| genshi_xml                       | 21.8 ms                                                  | 21.3 ms: 1.02x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 97.6 ms: 1.02x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 56.4 ms: 1.02x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.76 us: 1.02x faster                                                   |
| json                             | 1.93 ms                                                  | 1.90 ms: 1.02x faster                                                   |
| shortest_path                    | 219 ms                                                   | 217 ms: 1.01x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.55 us: 1.01x faster                                                   |
| 2to3                             | 114 ms                                                   | 113 ms: 1.01x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 958 ns: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 524 ms: 1.01x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.8 us: 1.01x faster                                                   |
| fannkuch                         | 176 ms                                                   | 176 ms: 1.00x slower                                                    |
| mako                             | 4.77 ms                                                  | 4.81 ms: 1.01x slower                                                   |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.71 ms: 1.01x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 48.4 ms: 1.01x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 430 us: 1.03x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| pidigits                         | 161 ms                                                   | 167 ms: 1.04x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.43 ms: 1.04x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 145 us: 1.04x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 24.0 ms: 1.04x slower                                                   |
| gc_traversal                     | 2.01 ms                                                  | 2.10 ms: 1.04x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 707 ms: 1.06x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 350 ms: 1.07x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.71 ms: 1.09x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.23 ms: 1.09x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.4 ms: 1.12x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 946 us: 1.14x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.00 ms: 1.15x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.18x slower                                                    |
| coverage                         | 26.9 ms                                                  | 33.0 ms: 1.23x slower                                                   |
| many_optionals                   | 195 us                                                   | 244 us: 1.25x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.5 ms: 2.72x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 197 ns: 3.87x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                            |

Benchmark hidden because not significant (3): pycparser, connected_components, sympy_expand
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250612-3.15.0a0-2b0c684/bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.110x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.15x