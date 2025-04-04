# Results vs. 3.13.0rc2

- fork: tom-pytel
- ref: 579bd08e9f4db18fbbe0
- machine: darwin-arm64
- commit hash: 579bd08
- commit date: 2025-03-30
- overall geometric mean: 1.020x slower
- HPT reliability: 96.12%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 122 ms: 1.10x slower                                                          |
| docutils       | 1.05 sec                                                       | 1.00 sec: 1.04x faster                                                        |
| html5lib       | 23.1 ms                                                        | 24.1 ms: 1.04x slower                                                         |
| sphinx         | 409 ms                                                         | 425 ms: 1.04x slower                                                          |
| Geometric mean | (ref)                                                          | 1.03x slower                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 201 ms: 2.59x faster                                                          |
| async_tree_eager_io              | 525 ms                                                         | 213 ms: 2.47x faster                                                          |
| async_tree_io_tg                 | 405 ms                                                         | 202 ms: 2.01x faster                                                          |
| async_tree_io                    | 386 ms                                                         | 218 ms: 1.77x faster                                                          |
| async_tree_none_tg               | 133 ms                                                         | 89.0 ms: 1.49x faster                                                         |
| async_tree_memoization_tg        | 186 ms                                                         | 126 ms: 1.47x faster                                                          |
| async_tree_memoization           | 184 ms                                                         | 134 ms: 1.38x faster                                                          |
| async_tree_none                  | 142 ms                                                         | 105 ms: 1.36x faster                                                          |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 233 ms: 1.29x faster                                                          |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 242 ms: 1.21x faster                                                          |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                          |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                          |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                          |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                          |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.01x faster                                                         |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 224 ms: 1.07x slower                                                          |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 115 ms: 1.12x slower                                                          |
| async_tree_eager                 | 43.2 ms                                                        | 51.8 ms: 1.20x slower                                                         |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.9 ms: 2.76x slower                                                         |
| Geometric mean                   | (ref)                                                          | 1.22x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 162 ms: 1.02x faster                                                          |
| float          | 31.4 ms                                                        | 32.3 ms: 1.03x slower                                                         |
| nbody          | 42.5 ms                                                        | 61.3 ms: 1.44x slower                                                         |
| Geometric mean | (ref)                                                          | 1.13x slower                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 10.2 ms: 1.05x faster                                                         |
| regex_effbot   | 1.61 ms                                                        | 1.56 ms: 1.03x faster                                                         |
| regex_dna      | 94.6 ms                                                        | 103 ms: 1.08x slower                                                          |
| regex_compile  | 47.9 ms                                                        | 55.6 ms: 1.16x slower                                                         |
| Geometric mean | (ref)                                                          | 1.04x slower                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 36.4 ms: 1.27x faster                                                         |
| xml_etree_parse      | 62.4 ms                                                        | 57.2 ms: 1.09x faster                                                         |
| xml_etree_generate   | 35.8 ms                                                        | 37.5 ms: 1.05x slower                                                         |
| xml_etree_process    | 25.4 ms                                                        | 27.5 ms: 1.08x slower                                                         |
| json_dumps           | 4.65 ms                                                        | 5.12 ms: 1.10x slower                                                         |
| json_loads           | 10.8 us                                                        | 12.0 us: 1.11x slower                                                         |
| unpickle_pure_python | 99.5 us                                                        | 112 us: 1.13x slower                                                          |
| pickle_pure_python   | 130 us                                                         | 159 us: 1.22x slower                                                          |
| Geometric mean       | (ref)                                                          | 1.04x slower                                                                  |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.48 ms: 1.10x slower                                                         |
| python_startup_no_site | 5.95 ms                                                        | 7.60 ms: 1.28x slower                                                         |
| Geometric mean         | (ref)                                                          | 1.18x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 24.5 ms: 1.15x slower                                                         |
| genshi_text     | 9.97 ms                                                        | 11.9 ms: 1.19x slower                                                         |
| mako            | 4.41 ms                                                        | 5.80 ms: 1.32x slower                                                         |
| django_template | 12.5 ms                                                        | 16.9 ms: 1.35x slower                                                         |
| Geometric mean  | (ref)                                                          | 1.25x slower                                                                  |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 760 us: 2.69x faster                                                          |
| async_tree_eager_io_tg           | 521 ms                                                         | 201 ms: 2.59x faster                                                          |
| async_tree_eager_io              | 525 ms                                                         | 213 ms: 2.47x faster                                                          |
| create_gc_cycles                 | 993 us                                                         | 461 us: 2.16x faster                                                          |
| async_tree_io_tg                 | 405 ms                                                         | 202 ms: 2.01x faster                                                          |
| async_tree_io                    | 386 ms                                                         | 218 ms: 1.77x faster                                                          |
| async_tree_none_tg               | 133 ms                                                         | 89.0 ms: 1.49x faster                                                         |
| async_tree_memoization_tg        | 186 ms                                                         | 126 ms: 1.47x faster                                                          |
| k_core                           | 1.46 sec                                                       | 1.02 sec: 1.44x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 134 ms: 1.38x faster                                                          |
| async_tree_none                  | 142 ms                                                         | 105 ms: 1.36x faster                                                          |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 233 ms: 1.29x faster                                                          |
| xml_etree_iterparse              | 46.1 ms                                                        | 36.4 ms: 1.27x faster                                                         |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 242 ms: 1.21x faster                                                          |
| sqlite_synth                     | 948 ns                                                         | 824 ns: 1.15x faster                                                          |
| deepcopy                         | 145 us                                                         | 127 us: 1.14x faster                                                          |
| scimark_sor                      | 64.0 ms                                                        | 57.9 ms: 1.10x faster                                                         |
| xml_etree_parse                  | 62.4 ms                                                        | 57.2 ms: 1.09x faster                                                         |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                          |
| go                               | 72.6 ms                                                        | 67.1 ms: 1.08x faster                                                         |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                          |
| deepcopy_memo                    | 16.5 us                                                        | 15.5 us: 1.06x faster                                                         |
| regex_v8                         | 10.7 ms                                                        | 10.2 ms: 1.05x faster                                                         |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                         |
| pyflate                          | 222 ms                                                         | 213 ms: 1.04x faster                                                          |
| docutils                         | 1.05 sec                                                       | 1.00 sec: 1.04x faster                                                        |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.05 sec: 1.04x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                          |
| regex_effbot                     | 1.61 ms                                                        | 1.56 ms: 1.03x faster                                                         |
| pidigits                         | 166 ms                                                         | 162 ms: 1.02x faster                                                          |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                          |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.01x faster                                                         |
| pathlib                          | 11.1 ms                                                        | 11.1 ms: 1.00x faster                                                         |
| deepcopy_reduce                  | 1.30 us                                                        | 1.30 us: 1.01x slower                                                         |
| pycparser                        | 470 ms                                                         | 482 ms: 1.03x slower                                                          |
| float                            | 31.4 ms                                                        | 32.3 ms: 1.03x slower                                                         |
| json                             | 1.94 ms                                                        | 2.01 ms: 1.03x slower                                                         |
| sphinx                           | 409 ms                                                         | 425 ms: 1.04x slower                                                          |
| shortest_path                    | 225 ms                                                         | 234 ms: 1.04x slower                                                          |
| html5lib                         | 23.1 ms                                                        | 24.1 ms: 1.04x slower                                                         |
| xml_etree_generate               | 35.8 ms                                                        | 37.5 ms: 1.05x slower                                                         |
| connected_components             | 208 ms                                                         | 222 ms: 1.07x slower                                                          |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 224 ms: 1.07x slower                                                          |
| mdp                              | 1.06 sec                                                       | 1.14 sec: 1.08x slower                                                        |
| xml_etree_process                | 25.4 ms                                                        | 27.5 ms: 1.08x slower                                                         |
| regex_dna                        | 94.6 ms                                                        | 103 ms: 1.08x slower                                                          |
| 2to3                             | 112 ms                                                         | 122 ms: 1.10x slower                                                          |
| python_startup                   | 8.63 ms                                                        | 9.48 ms: 1.10x slower                                                         |
| telco                            | 3.07 ms                                                        | 3.37 ms: 1.10x slower                                                         |
| json_dumps                       | 4.65 ms                                                        | 5.12 ms: 1.10x slower                                                         |
| thrift                           | 309 us                                                         | 340 us: 1.10x slower                                                          |
| sympy_integrate                  | 7.53 ms                                                        | 8.34 ms: 1.11x slower                                                         |
| json_loads                       | 10.8 us                                                        | 12.0 us: 1.11x slower                                                         |
| bench_mp_pool                    | 37.8 ms                                                        | 42.0 ms: 1.11x slower                                                         |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 115 ms: 1.12x slower                                                          |
| unpickle_pure_python             | 99.5 us                                                        | 112 us: 1.13x slower                                                          |
| pylint                           | 106 ms                                                         | 119 ms: 1.13x slower                                                          |
| fannkuch                         | 179 ms                                                         | 203 ms: 1.14x slower                                                          |
| sqlalchemy_declarative           | 44.4 ms                                                        | 50.8 ms: 1.15x slower                                                         |
| genshi_xml                       | 21.4 ms                                                        | 24.5 ms: 1.15x slower                                                         |
| nqueens                          | 37.2 ms                                                        | 42.9 ms: 1.15x slower                                                         |
| typing_runtime_protocols         | 64.6 us                                                        | 74.6 us: 1.15x slower                                                         |
| richards                         | 22.1 ms                                                        | 25.5 ms: 1.16x slower                                                         |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.79 ms: 1.16x slower                                                         |
| regex_compile                    | 47.9 ms                                                        | 55.6 ms: 1.16x slower                                                         |
| hexiom                           | 2.85 ms                                                        | 3.31 ms: 1.16x slower                                                         |
| richards_super                   | 24.7 ms                                                        | 28.9 ms: 1.17x slower                                                         |
| sympy_sum                        | 52.3 ms                                                        | 61.4 ms: 1.17x slower                                                         |
| sympy_str                        | 95.5 ms                                                        | 112 ms: 1.18x slower                                                          |
| scimark_monte_carlo              | 29.9 ms                                                        | 35.3 ms: 1.18x slower                                                         |
| meteor_contest                   | 47.9 ms                                                        | 56.6 ms: 1.18x slower                                                         |
| genshi_text                      | 9.97 ms                                                        | 11.9 ms: 1.19x slower                                                         |
| deltablue                        | 1.45 ms                                                        | 1.73 ms: 1.19x slower                                                         |
| sympy_expand                     | 159 ms                                                         | 191 ms: 1.20x slower                                                          |
| generators                       | 15.7 ms                                                        | 18.8 ms: 1.20x slower                                                         |
| spectral_norm                    | 43.7 ms                                                        | 52.3 ms: 1.20x slower                                                         |
| pprint_safe_repr                 | 322 ms                                                         | 386 ms: 1.20x slower                                                          |
| async_tree_eager                 | 43.2 ms                                                        | 51.8 ms: 1.20x slower                                                         |
| scimark_fft                      | 124 ms                                                         | 149 ms: 1.20x slower                                                          |
| logging_simple                   | 2.24 us                                                        | 2.69 us: 1.20x slower                                                         |
| logging_format                   | 2.45 us                                                        | 2.95 us: 1.21x slower                                                         |
| pprint_pformat                   | 650 ms                                                         | 784 ms: 1.21x slower                                                          |
| logging_silent                   | 40.6 ns                                                        | 49.1 ns: 1.21x slower                                                         |
| many_optionals                   | 200 us                                                         | 244 us: 1.22x slower                                                          |
| pickle_pure_python               | 130 us                                                         | 159 us: 1.22x slower                                                          |
| crypto_pyaes                     | 33.6 ms                                                        | 41.0 ms: 1.22x slower                                                         |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.23 ms: 1.25x slower                                                         |
| coverage                         | 31.2 ms                                                        | 39.1 ms: 1.25x slower                                                         |
| chaos                            | 24.3 ms                                                        | 30.9 ms: 1.27x slower                                                         |
| python_startup_no_site           | 5.95 ms                                                        | 7.60 ms: 1.28x slower                                                         |
| raytrace                         | 109 ms                                                         | 140 ms: 1.28x slower                                                          |
| scimark_lu                       | 42.8 ms                                                        | 55.5 ms: 1.30x slower                                                         |
| comprehensions                   | 6.80 us                                                        | 8.85 us: 1.30x slower                                                         |
| mako                             | 4.41 ms                                                        | 5.80 ms: 1.32x slower                                                         |
| django_template                  | 12.5 ms                                                        | 16.9 ms: 1.35x slower                                                         |
| bench_thread_pool                | 412 us                                                         | 587 us: 1.42x slower                                                          |
| subparsers                       | 6.26 ms                                                        | 8.96 ms: 1.43x slower                                                         |
| nbody                            | 42.5 ms                                                        | 61.3 ms: 1.44x slower                                                         |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.9 ms: 2.76x slower                                                         |
| Geometric mean                   | (ref)                                                          | 1.03x slower                                                                  |

Benchmark hidden because not significant (1): tomli_loads
Ignored benchmarks (9) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250330-3.14.0a6+-579bd08-NOGIL/bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.020x slower

# HPT report

- Reliability score: 96.12% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.18x