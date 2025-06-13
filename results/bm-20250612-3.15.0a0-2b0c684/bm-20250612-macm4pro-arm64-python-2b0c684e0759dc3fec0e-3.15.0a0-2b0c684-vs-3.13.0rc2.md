# Results vs. 3.13.0rc2

- fork: python
- ref: 2b0c684e0759dc3fec0e
- machine: darwin-arm64
- commit hash: 2b0c684
- commit date: 2025-06-12
- overall geometric mean: 1.030x faster
- HPT reliability: 89.38%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 113 ms: 1.01x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.05 sec: 1.00x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.0 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 246 ms: 2.14x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 254 ms: 2.05x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 249 ms: 1.63x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 252 ms: 1.53x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.26x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 264 ms: 1.14x faster                                                    |
| async_generators                 | 193 ms                                                         | 171 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.10x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.9 ms: 1.03x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 250 ms: 1.20x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.27x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.5 ms: 3.03x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.8 ms: 1.05x faster                                                   |
| pidigits       | 166 ms                                                         | 167 ms: 1.01x slower                                                    |
| nbody          | 42.5 ms                                                        | 47.3 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.71 ms: 1.10x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 47.8 ms: 1.00x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 97.6 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 918 ms: 1.09x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.43 ms: 1.05x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 43.9 ms: 1.05x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 24.8 ms: 1.02x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.1 ms: 1.02x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 61.4 ms: 1.02x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 98.2 us: 1.01x faster                                                   |
| pickle_pure_python   | 130 us                                                         | 145 us: 1.12x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.71 ms: 1.01x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.23 ms: 1.05x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.79 ms: 1.02x faster                                                   |
| mako            | 4.41 ms                                                        | 4.81 ms: 1.09x slower                                                   |
| django_template | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.07x slower                                                            |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 246 ms: 2.14x faster                                                    |
| mdp                              | 1.06 sec                                                       | 513 ms: 2.06x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 254 ms: 2.05x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 249 ms: 1.63x faster                                                    |
| k_core                           | 1.46 sec                                                       | 950 ms: 1.54x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 252 ms: 1.53x faster                                                    |
| deepcopy                         | 145 us                                                         | 110 us: 1.32x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.5 us: 1.32x faster                                                   |
| go                               | 72.6 ms                                                        | 55.7 ms: 1.30x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.26x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 50.8 ms: 1.26x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 264 ms: 1.14x faster                                                    |
| pyflate                          | 222 ms                                                         | 196 ms: 1.13x faster                                                    |
| async_generators                 | 193 ms                                                         | 171 ms: 1.13x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.16 us: 1.11x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 17.9 ms: 1.11x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.10x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.71 ms: 1.10x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 918 ms: 1.09x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                  |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| float                            | 31.4 ms                                                        | 29.8 ms: 1.05x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.43 ms: 1.05x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.9 ms: 1.05x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 946 us: 1.05x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 61.7 us: 1.05x faster                                                   |
| connected_components             | 208 ms                                                         | 200 ms: 1.04x faster                                                    |
| shortest_path                    | 225 ms                                                         | 217 ms: 1.04x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.9 ms: 1.04x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.75 ms: 1.04x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.9 ms: 1.03x faster                                                   |
| telco                            | 3.07 ms                                                        | 3.00 ms: 1.02x faster                                                   |
| thrift                           | 309 us                                                         | 302 us: 1.02x faster                                                    |
| json                             | 1.94 ms                                                        | 1.90 ms: 1.02x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 24.8 ms: 1.02x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 35.1 ms: 1.02x faster                                                   |
| genshi_text                      | 9.97 ms                                                        | 9.79 ms: 1.02x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 61.4 ms: 1.02x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 98.2 us: 1.01x faster                                                   |
| fannkuch                         | 179 ms                                                         | 176 ms: 1.01x faster                                                    |
| richards                         | 22.1 ms                                                        | 21.9 ms: 1.01x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 24.6 ms: 1.01x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.51 ms: 1.00x faster                                                   |
| regex_compile                    | 47.9 ms                                                        | 47.8 ms: 1.00x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.05 sec: 1.00x slower                                                  |
| pathlib                          | 11.1 ms                                                        | 11.2 ms: 1.01x slower                                                   |
| pidigits                         | 166 ms                                                         | 167 ms: 1.01x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.71 ms: 1.01x slower                                                   |
| sqlite_synth                     | 948 ns                                                         | 958 ns: 1.01x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 48.4 ms: 1.01x slower                                                   |
| 2to3                             | 112 ms                                                         | 113 ms: 1.01x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.10 ms: 1.03x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 97.6 ms: 1.03x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 38.6 ms: 1.04x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 24.0 ms: 1.04x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.51 ms: 1.04x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 99.5 ms: 1.04x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.86 ms: 1.04x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 430 us: 1.04x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.23 ms: 1.05x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 45.8 ms: 1.05x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 130 ms: 1.05x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 167 ms: 1.05x slower                                                    |
| pycparser                        | 470 ms                                                         | 496 ms: 1.05x slower                                                    |
| coverage                         | 31.2 ms                                                        | 33.0 ms: 1.06x slower                                                   |
| chaos                            | 24.3 ms                                                        | 26.1 ms: 1.07x slower                                                   |
| raytrace                         | 109 ms                                                         | 117 ms: 1.08x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 56.4 ms: 1.08x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 350 ms: 1.09x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 707 ms: 1.09x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.81 ms: 1.09x slower                                                   |
| pylint                           | 106 ms                                                         | 115 ms: 1.09x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.42 us: 1.09x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.3 ms: 1.10x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 47.5 ms: 1.11x slower                                                   |
| nbody                            | 42.5 ms                                                        | 47.3 ms: 1.11x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 145 us: 1.12x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.9 ms: 1.13x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.76 us: 1.13x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.55 us: 1.14x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.4 ms: 1.17x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 250 ms: 1.20x slower                                                    |
| many_optionals                   | 200 us                                                         | 244 us: 1.22x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.27x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.57 ms: 1.53x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.5 ms: 3.03x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 197 ns: 4.85x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (5): json_loads, dask, genshi_xml, async_tree_eager_cpu_io_mixed, sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250612-3.15.0a0-2b0c684/bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.030x faster

# HPT report

- Reliability score: 89.38% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.09x