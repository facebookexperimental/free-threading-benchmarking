# Results vs. 3.13.0rc2

- fork: python
- ref: 246be21de1e2a51d757c
- machine: darwin-arm64
- commit hash: 246be21
- commit date: 2025-07-20
- overall geometric mean: 1.011x faster
- HPT reliability: 70.86%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250720-macm4pro-arm64-python-246be21de1e2a51d757c-3.15.0a0-246be21 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 121 ms: 1.09x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                  |
| html5lib       | 23.1 ms                                                        | 23.6 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250720-macm4pro-arm64-python-246be21de1e2a51d757c-3.15.0a0-246be21 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 193 ms: 2.69x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 202 ms: 2.60x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 197 ms: 2.05x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 208 ms: 1.86x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.3 ms: 1.54x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 99.4 ms: 1.43x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 236 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 243 ms: 1.21x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                    |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.00x faster                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 228 ms: 1.10x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.0 ms: 1.11x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.6 ms: 2.68x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.25x faster                                                            |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250720-macm4pro-arm64-python-246be21de1e2a51d757c-3.15.0a0-246be21 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.6 ms: 1.10x faster                                                   |
| pidigits       | 166 ms                                                         | 166 ms: 1.00x slower                                                    |
| nbody          | 42.5 ms                                                        | 54.4 ms: 1.28x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250720-macm4pro-arm64-python-246be21de1e2a51d757c-3.15.0a0-246be21 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.42 ms: 1.14x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 98.5 ms: 1.04x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 51.9 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250720-macm4pro-arm64-python-246be21de1e2a51d757c-3.15.0a0-246be21 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.2 ms: 1.21x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 57.1 ms: 1.09x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 956 ms: 1.05x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.57 ms: 1.02x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 36.5 ms: 1.02x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 26.5 ms: 1.05x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.06x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 110 us: 1.11x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 152 us: 1.17x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.00x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250720-macm4pro-arm64-python-246be21de1e2a51d757c-3.15.0a0-246be21 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.71 ms: 1.12x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 7.03 ms: 1.18x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.15x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250720-macm4pro-arm64-python-246be21de1e2a51d757c-3.15.0a0-246be21 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.4 ms: 1.10x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.3 ms: 1.13x slower                                                   |
| mako            | 4.41 ms                                                        | 5.60 ms: 1.27x slower                                                   |
| django_template | 12.5 ms                                                        | 16.2 ms: 1.30x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.20x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250720-macm4pro-arm64-python-246be21de1e2a51d757c-3.15.0a0-246be21 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 193 ms: 2.69x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 202 ms: 2.60x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 787 us: 2.59x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 197 ms: 2.05x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 494 us: 2.01x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 208 ms: 1.86x faster                                                    |
| mdp                              | 1.06 sec                                                       | 573 ms: 1.84x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.3 ms: 1.54x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 989 ms: 1.48x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 99.4 ms: 1.43x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 236 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 243 ms: 1.21x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.2 ms: 1.21x faster                                                   |
| deepcopy                         | 145 us                                                         | 121 us: 1.20x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.7 us: 1.20x faster                                                   |
| go                               | 72.6 ms                                                        | 60.8 ms: 1.19x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 815 ns: 1.16x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 55.1 ms: 1.16x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.42 ms: 1.14x faster                                                   |
| pyflate                          | 222 ms                                                         | 197 ms: 1.13x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                    |
| float                            | 31.4 ms                                                        | 28.6 ms: 1.10x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                  |
| xml_etree_parse                  | 62.4 ms                                                        | 57.1 ms: 1.09x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                   |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.8 ms: 1.06x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.23 us: 1.05x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 956 ms: 1.05x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                  |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.57 ms: 1.02x faster                                                   |
| fannkuch                         | 179 ms                                                         | 177 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.00x faster                                                    |
| pidigits                         | 166 ms                                                         | 166 ms: 1.00x slower                                                    |
| pathlib                          | 11.1 ms                                                        | 11.2 ms: 1.00x slower                                                   |
| dask                             | 525 ms                                                         | 532 ms: 1.01x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.5 ms: 1.02x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 23.6 ms: 1.02x slower                                                   |
| json                             | 1.94 ms                                                        | 2.01 ms: 1.04x slower                                                   |
| shortest_path                    | 225 ms                                                         | 233 ms: 1.04x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 98.5 ms: 1.04x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 26.5 ms: 1.05x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.23 ms: 1.05x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.06x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.02 ms: 1.06x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 343 ms: 1.07x slower                                                    |
| connected_components             | 208 ms                                                         | 222 ms: 1.07x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.03 ms: 1.07x slower                                                   |
| thrift                           | 309 us                                                         | 331 us: 1.07x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 696 ms: 1.07x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.8 ms: 1.08x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 51.9 ms: 1.08x slower                                                   |
| 2to3                             | 112 ms                                                         | 121 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.4 ms: 1.10x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 228 ms: 1.10x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 27.1 ms: 1.10x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 110 us: 1.11x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 45.0 ns: 1.11x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 48.0 ms: 1.11x slower                                                   |
| pylint                           | 106 ms                                                         | 118 ms: 1.12x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.5 ms: 1.12x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 139 ms: 1.12x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.71 ms: 1.12x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 72.9 us: 1.13x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 42.1 ms: 1.13x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.3 ms: 1.13x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.65 ms: 1.14x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.15x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.57 us: 1.15x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 55.2 ms: 1.15x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 61.1 ms: 1.17x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.95 us: 1.17x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 51.2 ms: 1.17x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 152 us: 1.17x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 187 ms: 1.18x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.88 us: 1.18x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 7.03 ms: 1.18x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 45.1 ms: 1.19x slower                                                   |
| raytrace                         | 109 ms                                                         | 131 ms: 1.20x slower                                                    |
| chaos                            | 24.3 ms                                                        | 29.3 ms: 1.21x slower                                                   |
| generators                       | 15.7 ms                                                        | 19.4 ms: 1.24x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.20 ms: 1.24x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.2 ms: 1.26x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.60 ms: 1.27x slower                                                   |
| nbody                            | 42.5 ms                                                        | 54.4 ms: 1.28x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.2 ms: 1.30x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.8 ms: 1.31x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 56.3 ms: 1.32x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 599 us: 1.45x slower                                                    |
| many_optionals                   | 200 us                                                         | 331 us: 1.65x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.6 ms: 2.68x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 18.1 ms: 2.89x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.00x faster                                                            |

Benchmark hidden because not significant (3): pycparser, coroutines, sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250720-3.15.0a0-246be21-NOGIL/bm-20250720-macm4pro-arm64-python-246be21de1e2a51d757c-3.15.0a0-246be21.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.011x faster

# HPT report

- Reliability score: 70.86% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.20x