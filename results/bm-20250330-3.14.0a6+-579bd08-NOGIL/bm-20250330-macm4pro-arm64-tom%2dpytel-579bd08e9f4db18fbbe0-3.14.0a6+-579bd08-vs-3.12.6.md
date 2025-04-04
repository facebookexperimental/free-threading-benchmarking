# Results vs. 3.12.6

- fork: tom-pytel
- ref: 579bd08e9f4db18fbbe0
- machine: darwin-arm64
- commit hash: 579bd08
- commit date: 2025-03-30
- overall geometric mean: 1.057x faster
- HPT reliability: 63.16%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 122 ms: 1.07x slower                                                          |
| docutils       | 1.02 sec                                                 | 1.00 sec: 1.02x faster                                                        |
| html5lib       | 23.0 ms                                                  | 24.1 ms: 1.05x slower                                                         |
| sphinx         | 434 ms                                                   | 425 ms: 1.02x faster                                                          |
| Geometric mean | (ref)                                                    | 1.02x slower                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 202 ms: 2.38x faster                                                          |
| async_tree_eager_io              | 496 ms                                                   | 213 ms: 2.33x faster                                                          |
| async_tree_eager_io_tg           | 446 ms                                                   | 201 ms: 2.22x faster                                                          |
| async_tree_io                    | 459 ms                                                   | 218 ms: 2.11x faster                                                          |
| async_tree_none_tg               | 172 ms                                                   | 89.0 ms: 1.93x faster                                                         |
| async_tree_memoization_tg        | 231 ms                                                   | 126 ms: 1.82x faster                                                          |
| async_tree_none                  | 178 ms                                                   | 105 ms: 1.70x faster                                                          |
| async_tree_memoization           | 223 ms                                                   | 134 ms: 1.66x faster                                                          |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 233 ms: 1.45x faster                                                          |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 242 ms: 1.38x faster                                                          |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                         |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                          |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                          |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                          |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                          |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 115 ms: 1.02x slower                                                          |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 224 ms: 1.05x slower                                                          |
| async_tree_eager                 | 45.6 ms                                                  | 51.8 ms: 1.14x slower                                                         |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.9 ms: 2.49x slower                                                         |
| Geometric mean                   | (ref)                                                    | 1.35x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 32.3 ms: 1.17x faster                                                         |
| pidigits       | 161 ms                                                   | 162 ms: 1.01x slower                                                          |
| nbody          | 54.2 ms                                                  | 61.3 ms: 1.13x slower                                                         |
| Geometric mean | (ref)                                                    | 1.01x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.56 ms: 1.07x faster                                                         |
| regex_compile  | 54.6 ms                                                  | 55.6 ms: 1.02x slower                                                         |
| regex_dna      | 99.6 ms                                                  | 103 ms: 1.03x slower                                                          |
| regex_v8       | 9.59 ms                                                  | 10.2 ms: 1.06x slower                                                         |
| Geometric mean | (ref)                                                    | 1.01x slower                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 36.4 ms: 1.42x faster                                                         |
| xml_etree_parse      | 67.9 ms                                                  | 57.2 ms: 1.19x faster                                                         |
| xml_etree_generate   | 38.9 ms                                                  | 37.5 ms: 1.04x faster                                                         |
| xml_etree_process    | 26.7 ms                                                  | 27.5 ms: 1.03x slower                                                         |
| tomli_loads          | 957 ms                                                   | 1.00 sec: 1.05x slower                                                        |
| unpickle_pure_python | 103 us                                                   | 112 us: 1.09x slower                                                          |
| json_loads           | 10.9 us                                                  | 12.0 us: 1.11x slower                                                         |
| pickle_pure_python   | 139 us                                                   | 159 us: 1.14x slower                                                          |
| json_dumps           | 4.26 ms                                                  | 5.12 ms: 1.20x slower                                                         |
| Geometric mean       | (ref)                                                    | 1.00x slower                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.48 ms: 1.18x slower                                                         |
| python_startup_no_site | 5.71 ms                                                  | 7.60 ms: 1.33x slower                                                         |
| Geometric mean         | (ref)                                                    | 1.25x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 24.5 ms: 1.12x slower                                                         |
| genshi_text     | 10.5 ms                                                  | 11.9 ms: 1.13x slower                                                         |
| mako            | 4.77 ms                                                  | 5.80 ms: 1.22x slower                                                         |
| django_template | 13.6 ms                                                  | 16.9 ms: 1.24x slower                                                         |
| Geometric mean  | (ref)                                                    | 1.18x slower                                                                  |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 760 us: 2.64x faster                                                          |
| async_tree_io_tg                 | 480 ms                                                   | 202 ms: 2.38x faster                                                          |
| async_tree_eager_io              | 496 ms                                                   | 213 ms: 2.33x faster                                                          |
| subparsers                       | 20.8 ms                                                  | 8.96 ms: 2.32x faster                                                         |
| async_tree_eager_io_tg           | 446 ms                                                   | 201 ms: 2.22x faster                                                          |
| async_tree_io                    | 459 ms                                                   | 218 ms: 2.11x faster                                                          |
| async_tree_none_tg               | 172 ms                                                   | 89.0 ms: 1.93x faster                                                         |
| async_tree_memoization_tg        | 231 ms                                                   | 126 ms: 1.82x faster                                                          |
| create_gc_cycles                 | 830 us                                                   | 461 us: 1.80x faster                                                          |
| async_tree_none                  | 178 ms                                                   | 105 ms: 1.70x faster                                                          |
| async_tree_memoization           | 223 ms                                                   | 134 ms: 1.66x faster                                                          |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 233 ms: 1.45x faster                                                          |
| xml_etree_iterparse              | 51.6 ms                                                  | 36.4 ms: 1.42x faster                                                         |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 242 ms: 1.38x faster                                                          |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                         |
| deepcopy                         | 161 us                                                   | 127 us: 1.27x faster                                                          |
| xml_etree_parse                  | 67.9 ms                                                  | 57.2 ms: 1.19x faster                                                         |
| deepcopy_memo                    | 18.3 us                                                  | 15.5 us: 1.18x faster                                                         |
| float                            | 37.9 ms                                                  | 32.3 ms: 1.17x faster                                                         |
| sqlite_synth                     | 967 ns                                                   | 824 ns: 1.17x faster                                                          |
| generators                       | 21.9 ms                                                  | 18.8 ms: 1.17x faster                                                         |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                          |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                          |
| dulwich_log                      | 21.3 ms                                                  | 18.9 ms: 1.12x faster                                                         |
| deepcopy_reduce                  | 1.46 us                                                  | 1.30 us: 1.12x faster                                                         |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.11x faster                                                         |
| comprehensions                   | 9.84 us                                                  | 8.85 us: 1.11x faster                                                         |
| k_core                           | 1.12 sec                                                 | 1.02 sec: 1.10x faster                                                        |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.05 sec: 1.09x faster                                                        |
| pylint                           | 128 ms                                                   | 119 ms: 1.08x faster                                                          |
| regex_effbot                     | 1.67 ms                                                  | 1.56 ms: 1.07x faster                                                         |
| scimark_sor                      | 61.0 ms                                                  | 57.9 ms: 1.05x faster                                                         |
| go                               | 70.0 ms                                                  | 67.1 ms: 1.04x faster                                                         |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                          |
| spectral_norm                    | 54.4 ms                                                  | 52.3 ms: 1.04x faster                                                         |
| raytrace                         | 145 ms                                                   | 140 ms: 1.04x faster                                                          |
| xml_etree_generate               | 38.9 ms                                                  | 37.5 ms: 1.04x faster                                                         |
| logging_silent                   | 50.9 ns                                                  | 49.1 ns: 1.04x faster                                                         |
| pycparser                        | 497 ms                                                   | 482 ms: 1.03x faster                                                          |
| sphinx                           | 434 ms                                                   | 425 ms: 1.02x faster                                                          |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                          |
| docutils                         | 1.02 sec                                                 | 1.00 sec: 1.02x faster                                                        |
| pyflate                          | 216 ms                                                   | 213 ms: 1.02x faster                                                          |
| nqueens                          | 43.5 ms                                                  | 42.9 ms: 1.01x faster                                                         |
| pidigits                         | 161 ms                                                   | 162 ms: 1.01x slower                                                          |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 115 ms: 1.02x slower                                                          |
| regex_compile                    | 54.6 ms                                                  | 55.6 ms: 1.02x slower                                                         |
| xml_etree_process                | 26.7 ms                                                  | 27.5 ms: 1.03x slower                                                         |
| regex_dna                        | 99.6 ms                                                  | 103 ms: 1.03x slower                                                          |
| json                             | 1.93 ms                                                  | 2.01 ms: 1.04x slower                                                         |
| sympy_integrate                  | 8.02 ms                                                  | 8.34 ms: 1.04x slower                                                         |
| mdp                              | 1.09 sec                                                 | 1.14 sec: 1.04x slower                                                        |
| html5lib                         | 23.0 ms                                                  | 24.1 ms: 1.05x slower                                                         |
| tomli_loads                      | 957 ms                                                   | 1.00 sec: 1.05x slower                                                        |
| logging_simple                   | 2.57 us                                                  | 2.69 us: 1.05x slower                                                         |
| scimark_fft                      | 142 ms                                                   | 149 ms: 1.05x slower                                                          |
| typing_runtime_protocols         | 71.0 us                                                  | 74.6 us: 1.05x slower                                                         |
| logging_format                   | 2.80 us                                                  | 2.95 us: 1.05x slower                                                         |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 224 ms: 1.05x slower                                                          |
| crypto_pyaes                     | 38.8 ms                                                  | 41.0 ms: 1.06x slower                                                         |
| thrift                           | 322 us                                                   | 340 us: 1.06x slower                                                          |
| bench_mp_pool                    | 39.7 ms                                                  | 42.0 ms: 1.06x slower                                                         |
| regex_v8                         | 9.59 ms                                                  | 10.2 ms: 1.06x slower                                                         |
| sympy_sum                        | 57.6 ms                                                  | 61.4 ms: 1.07x slower                                                         |
| chaos                            | 28.9 ms                                                  | 30.9 ms: 1.07x slower                                                         |
| shortest_path                    | 219 ms                                                   | 234 ms: 1.07x slower                                                          |
| 2to3                             | 114 ms                                                   | 122 ms: 1.07x slower                                                          |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.23 ms: 1.07x slower                                                         |
| sympy_str                        | 104 ms                                                   | 112 ms: 1.08x slower                                                          |
| scimark_lu                       | 51.3 ms                                                  | 55.5 ms: 1.08x slower                                                         |
| sqlalchemy_declarative           | 46.8 ms                                                  | 50.8 ms: 1.09x slower                                                         |
| unpickle_pure_python             | 103 us                                                   | 112 us: 1.09x slower                                                          |
| hexiom                           | 3.04 ms                                                  | 3.31 ms: 1.09x slower                                                         |
| scimark_monte_carlo              | 32.2 ms                                                  | 35.3 ms: 1.10x slower                                                         |
| json_loads                       | 10.9 us                                                  | 12.0 us: 1.11x slower                                                         |
| connected_components             | 201 ms                                                   | 222 ms: 1.11x slower                                                          |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.79 ms: 1.12x slower                                                         |
| genshi_xml                       | 21.8 ms                                                  | 24.5 ms: 1.12x slower                                                         |
| nbody                            | 54.2 ms                                                  | 61.3 ms: 1.13x slower                                                         |
| genshi_text                      | 10.5 ms                                                  | 11.9 ms: 1.13x slower                                                         |
| async_tree_eager                 | 45.6 ms                                                  | 51.8 ms: 1.14x slower                                                         |
| richards_super                   | 25.4 ms                                                  | 28.9 ms: 1.14x slower                                                         |
| pickle_pure_python               | 139 us                                                   | 159 us: 1.14x slower                                                          |
| richards                         | 22.4 ms                                                  | 25.5 ms: 1.14x slower                                                         |
| sympy_expand                     | 167 ms                                                   | 191 ms: 1.14x slower                                                          |
| fannkuch                         | 176 ms                                                   | 203 ms: 1.16x slower                                                          |
| pprint_safe_repr                 | 328 ms                                                   | 386 ms: 1.18x slower                                                          |
| pprint_pformat                   | 665 ms                                                   | 784 ms: 1.18x slower                                                          |
| python_startup                   | 8.01 ms                                                  | 9.48 ms: 1.18x slower                                                         |
| meteor_contest                   | 47.7 ms                                                  | 56.6 ms: 1.19x slower                                                         |
| json_dumps                       | 4.26 ms                                                  | 5.12 ms: 1.20x slower                                                         |
| mako                             | 4.77 ms                                                  | 5.80 ms: 1.22x slower                                                         |
| django_template                  | 13.6 ms                                                  | 16.9 ms: 1.24x slower                                                         |
| many_optionals                   | 195 us                                                   | 244 us: 1.25x slower                                                          |
| telco                            | 2.61 ms                                                  | 3.37 ms: 1.29x slower                                                         |
| python_startup_no_site           | 5.71 ms                                                  | 7.60 ms: 1.33x slower                                                         |
| bench_thread_pool                | 419 us                                                   | 587 us: 1.40x slower                                                          |
| coverage                         | 26.9 ms                                                  | 39.1 ms: 1.46x slower                                                         |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.9 ms: 2.49x slower                                                         |
| Geometric mean                   | (ref)                                                    | 1.05x faster                                                                  |

Benchmark hidden because not significant (1): deltablue
Ignored benchmarks (9) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250330-3.14.0a6+-579bd08-NOGIL/bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.057x faster

# HPT report

- Reliability score: 63.16% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.22x