# Results vs. base

- fork: tom-pytel
- ref: 579bd08e9f4db18fbbe0
- machine: darwin-arm64
- commit hash: 579bd08
- commit date: 2025-03-30
- overall geometric mean: 1.007x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 125 ms                                                                   | 122 ms: 1.03x faster                                                          |
| docutils       | 1.01 sec                                                                 | 1.00 sec: 1.01x faster                                                        |
| html5lib       | 25.3 ms                                                                  | 24.1 ms: 1.05x faster                                                         |
| sphinx         | 426 ms                                                                   | 425 ms: 1.00x faster                                                          |
| Geometric mean | (ref)                                                                    | 1.02x faster                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none                  | 107 ms                                                                   | 105 ms: 1.02x faster                                                          |
| async_tree_eager_io_tg           | 204 ms                                                                   | 201 ms: 1.02x faster                                                          |
| async_tree_cpu_io_mixed          | 246 ms                                                                   | 242 ms: 1.02x faster                                                          |
| async_tree_eager_cpu_io_mixed_tg | 227 ms                                                                   | 224 ms: 1.02x faster                                                          |
| async_tree_eager                 | 52.6 ms                                                                  | 51.8 ms: 1.02x faster                                                         |
| async_tree_eager_cpu_io_mixed    | 226 ms                                                                   | 222 ms: 1.02x faster                                                          |
| async_tree_cpu_io_mixed_tg       | 236 ms                                                                   | 233 ms: 1.02x faster                                                          |
| async_tree_eager_io              | 216 ms                                                                   | 213 ms: 1.01x faster                                                          |
| async_tree_eager_tg              | 80.9 ms                                                                  | 79.9 ms: 1.01x faster                                                         |
| async_tree_memoization           | 135 ms                                                                   | 134 ms: 1.01x faster                                                          |
| async_tree_io                    | 220 ms                                                                   | 218 ms: 1.01x faster                                                          |
| async_generators                 | 180 ms                                                                   | 178 ms: 1.01x faster                                                          |
| asyncio_websockets               | 189 ms                                                                   | 187 ms: 1.01x faster                                                          |
| async_tree_eager_memoization_tg  | 116 ms                                                                   | 115 ms: 1.01x faster                                                          |
| async_tree_eager_memoization     | 115 ms                                                                   | 114 ms: 1.01x faster                                                          |
| async_tree_io_tg                 | 204 ms                                                                   | 202 ms: 1.01x faster                                                          |
| async_tree_none_tg               | 89.8 ms                                                                  | 89.0 ms: 1.01x faster                                                         |
| async_tree_memoization_tg        | 127 ms                                                                   | 126 ms: 1.01x faster                                                          |
| coroutines                       | 10.3 ms                                                                  | 10.6 ms: 1.04x slower                                                         |
| Geometric mean                   | (ref)                                                                    | 1.01x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pidigits       | 165 ms                                                                   | 162 ms: 1.01x faster                                                          |
| nbody          | 62.1 ms                                                                  | 61.3 ms: 1.01x faster                                                         |
| float          | 32.1 ms                                                                  | 32.3 ms: 1.00x slower                                                         |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_effbot   | 1.59 ms                                                                  | 1.56 ms: 1.02x faster                                                         |
| regex_v8       | 9.93 ms                                                                  | 10.2 ms: 1.03x slower                                                         |
| Geometric mean | (ref)                                                                    | 1.00x slower                                                                  |

Benchmark hidden because not significant (2): regex_dna, regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| xml_etree_parse      | 58.8 ms                                                                  | 57.2 ms: 1.03x faster                                                         |
| xml_etree_iterparse  | 37.3 ms                                                                  | 36.4 ms: 1.03x faster                                                         |
| json_loads           | 12.2 us                                                                  | 12.0 us: 1.02x faster                                                         |
| pickle_pure_python   | 161 us                                                                   | 159 us: 1.01x faster                                                          |
| xml_etree_generate   | 37.8 ms                                                                  | 37.5 ms: 1.01x faster                                                         |
| json_dumps           | 5.16 ms                                                                  | 5.12 ms: 1.01x faster                                                         |
| xml_etree_process    | 27.6 ms                                                                  | 27.5 ms: 1.01x faster                                                         |
| unpickle_pure_python | 112 us                                                                   | 112 us: 1.00x slower                                                          |
| Geometric mean       | (ref)                                                                    | 1.01x faster                                                                  |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup | 9.57 ms                                                                  | 9.48 ms: 1.01x faster                                                         |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                                  |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|-----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| genshi_text     | 12.0 ms                                                                  | 11.9 ms: 1.01x faster                                                         |
| django_template | 16.7 ms                                                                  | 16.9 ms: 1.01x slower                                                         |
| Geometric mean  | (ref)                                                                    | 1.00x faster                                                                  |

Benchmark hidden because not significant (2): genshi_xml, mako

All benchmarks:
===============

| Benchmark                        | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| html5lib                         | 25.3 ms                                                                  | 24.1 ms: 1.05x faster                                                         |
| telco                            | 3.52 ms                                                                  | 3.37 ms: 1.04x faster                                                         |
| xml_etree_parse                  | 58.8 ms                                                                  | 57.2 ms: 1.03x faster                                                         |
| xml_etree_iterparse              | 37.3 ms                                                                  | 36.4 ms: 1.03x faster                                                         |
| 2to3                             | 125 ms                                                                   | 122 ms: 1.03x faster                                                          |
| many_optionals                   | 250 us                                                                   | 244 us: 1.02x faster                                                          |
| async_tree_none                  | 107 ms                                                                   | 105 ms: 1.02x faster                                                          |
| regex_effbot                     | 1.59 ms                                                                  | 1.56 ms: 1.02x faster                                                         |
| subparsers                       | 9.14 ms                                                                  | 8.96 ms: 1.02x faster                                                         |
| mdp                              | 1.16 sec                                                                 | 1.14 sec: 1.02x faster                                                        |
| json_loads                       | 12.2 us                                                                  | 12.0 us: 1.02x faster                                                         |
| bench_mp_pool                    | 42.8 ms                                                                  | 42.0 ms: 1.02x faster                                                         |
| async_tree_eager_io_tg           | 204 ms                                                                   | 201 ms: 1.02x faster                                                          |
| async_tree_cpu_io_mixed          | 246 ms                                                                   | 242 ms: 1.02x faster                                                          |
| scimark_lu                       | 56.5 ms                                                                  | 55.5 ms: 1.02x faster                                                         |
| async_tree_eager_cpu_io_mixed_tg | 227 ms                                                                   | 224 ms: 1.02x faster                                                          |
| async_tree_eager                 | 52.6 ms                                                                  | 51.8 ms: 1.02x faster                                                         |
| async_tree_eager_cpu_io_mixed    | 226 ms                                                                   | 222 ms: 1.02x faster                                                          |
| deepcopy_memo                    | 15.8 us                                                                  | 15.5 us: 1.02x faster                                                         |
| async_tree_cpu_io_mixed_tg       | 236 ms                                                                   | 233 ms: 1.02x faster                                                          |
| go                               | 68.1 ms                                                                  | 67.1 ms: 1.02x faster                                                         |
| async_tree_eager_io              | 216 ms                                                                   | 213 ms: 1.01x faster                                                          |
| pidigits                         | 165 ms                                                                   | 162 ms: 1.01x faster                                                          |
| dulwich_log                      | 19.2 ms                                                                  | 18.9 ms: 1.01x faster                                                         |
| nbody                            | 62.1 ms                                                                  | 61.3 ms: 1.01x faster                                                         |
| pickle_pure_python               | 161 us                                                                   | 159 us: 1.01x faster                                                          |
| async_tree_eager_tg              | 80.9 ms                                                                  | 79.9 ms: 1.01x faster                                                         |
| async_tree_memoization           | 135 ms                                                                   | 134 ms: 1.01x faster                                                          |
| richards                         | 25.8 ms                                                                  | 25.5 ms: 1.01x faster                                                         |
| deepcopy_reduce                  | 1.32 us                                                                  | 1.30 us: 1.01x faster                                                         |
| async_tree_io                    | 220 ms                                                                   | 218 ms: 1.01x faster                                                          |
| meteor_contest                   | 57.3 ms                                                                  | 56.6 ms: 1.01x faster                                                         |
| pprint_safe_repr                 | 390 ms                                                                   | 386 ms: 1.01x faster                                                          |
| async_generators                 | 180 ms                                                                   | 178 ms: 1.01x faster                                                          |
| asyncio_websockets               | 189 ms                                                                   | 187 ms: 1.01x faster                                                          |
| deepcopy                         | 128 us                                                                   | 127 us: 1.01x faster                                                          |
| async_tree_eager_memoization_tg  | 116 ms                                                                   | 115 ms: 1.01x faster                                                          |
| async_tree_eager_memoization     | 115 ms                                                                   | 114 ms: 1.01x faster                                                          |
| python_startup                   | 9.57 ms                                                                  | 9.48 ms: 1.01x faster                                                         |
| json                             | 2.03 ms                                                                  | 2.01 ms: 1.01x faster                                                         |
| genshi_text                      | 12.0 ms                                                                  | 11.9 ms: 1.01x faster                                                         |
| xml_etree_generate               | 37.8 ms                                                                  | 37.5 ms: 1.01x faster                                                         |
| sqlalchemy_imperative            | 5.84 ms                                                                  | 5.79 ms: 1.01x faster                                                         |
| pprint_pformat                   | 791 ms                                                                   | 784 ms: 1.01x faster                                                          |
| async_tree_io_tg                 | 204 ms                                                                   | 202 ms: 1.01x faster                                                          |
| async_tree_none_tg               | 89.8 ms                                                                  | 89.0 ms: 1.01x faster                                                         |
| raytrace                         | 141 ms                                                                   | 140 ms: 1.01x faster                                                          |
| json_dumps                       | 5.16 ms                                                                  | 5.12 ms: 1.01x faster                                                         |
| sqlalchemy_declarative           | 51.2 ms                                                                  | 50.8 ms: 1.01x faster                                                         |
| docutils                         | 1.01 sec                                                                 | 1.00 sec: 1.01x faster                                                        |
| async_tree_memoization_tg        | 127 ms                                                                   | 126 ms: 1.01x faster                                                          |
| xml_etree_process                | 27.6 ms                                                                  | 27.5 ms: 1.01x faster                                                         |
| logging_silent                   | 49.4 ns                                                                  | 49.1 ns: 1.01x faster                                                         |
| logging_simple                   | 2.71 us                                                                  | 2.69 us: 1.00x faster                                                         |
| sphinx                           | 426 ms                                                                   | 425 ms: 1.00x faster                                                          |
| generators                       | 18.8 ms                                                                  | 18.8 ms: 1.00x faster                                                         |
| bench_thread_pool                | 588 us                                                                   | 587 us: 1.00x faster                                                          |
| hexiom                           | 3.31 ms                                                                  | 3.31 ms: 1.00x faster                                                         |
| bpe_tokeniser                    | 2.05 sec                                                                 | 2.05 sec: 1.00x slower                                                        |
| coverage                         | 39.0 ms                                                                  | 39.1 ms: 1.00x slower                                                         |
| crypto_pyaes                     | 40.9 ms                                                                  | 41.0 ms: 1.00x slower                                                         |
| float                            | 32.1 ms                                                                  | 32.3 ms: 1.00x slower                                                         |
| unpickle_pure_python             | 112 us                                                                   | 112 us: 1.00x slower                                                          |
| scimark_fft                      | 148 ms                                                                   | 149 ms: 1.01x slower                                                          |
| django_template                  | 16.7 ms                                                                  | 16.9 ms: 1.01x slower                                                         |
| spectral_norm                    | 51.8 ms                                                                  | 52.3 ms: 1.01x slower                                                         |
| scimark_sor                      | 57.4 ms                                                                  | 57.9 ms: 1.01x slower                                                         |
| regex_v8                         | 9.93 ms                                                                  | 10.2 ms: 1.03x slower                                                         |
| coroutines                       | 10.3 ms                                                                  | 10.6 ms: 1.04x slower                                                         |
| Geometric mean                   | (ref)                                                                    | 1.01x faster                                                                  |

Benchmark hidden because not significant (35): gc_traversal, scimark_sparse_mat_mult, genshi_xml, pycparser, regex_dna, deltablue, pylint, pathlib, connected_components, tomli_loads, python_startup_no_site, shortest_path, fannkuch, richards_super, thrift, sqlglot_v2_normalize, mako, sympy_sum, regex_compile, pyflate, logging_format, nqueens, scimark_monte_carlo, sympy_expand, sympy_str, sympy_integrate, k_core, sqlglot_v2_optimize, create_gc_cycles, comprehensions, sqlglot_v2_parse, typing_runtime_protocols, sqlglot_v2_transpile, sqlite_synth, chaos

- Geometric mean (including insignificant results): 1.007x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.99x