# Results vs. 3.13.0rc2

- fork: python
- ref: ec7fad79d24e79961b86
- machine: darwin-arm64
- commit hash: ec7fad7
- commit date: 2025-07-23
- overall geometric mean: 1.011x faster
- HPT reliability: 65.16%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 121 ms: 1.08x slower                                                    |
| docutils       | 1.05 sec                                                       | 986 ms: 1.06x faster                                                    |
| html5lib       | 23.1 ms                                                        | 23.3 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 196 ms: 2.65x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.58x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 197 ms: 2.05x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 209 ms: 1.85x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 85.6 ms: 1.55x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 99.0 ms: 1.44x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 234 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 241 ms: 1.22x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 227 ms: 1.09x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.6 ms: 1.12x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.0 ms: 2.66x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.25x faster                                                            |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.4 ms: 1.11x faster                                                   |
| pidigits       | 166 ms                                                         | 162 ms: 1.03x faster                                                    |
| nbody          | 42.5 ms                                                        | 58.7 ms: 1.38x slower                                                   |
| Geometric mean | (ref)                                                          | 1.07x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.17 ms: 1.17x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 96.6 ms: 1.02x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 52.3 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 37.6 ms: 1.22x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 59.3 ms: 1.05x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 4.49 ms: 1.04x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 973 ms: 1.03x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.9 ms: 1.03x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.3 us: 1.05x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 109 us: 1.09x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 149 us: 1.15x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.00x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.57 ms: 1.11x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.96 ms: 1.17x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.9 ms: 1.12x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.7 ms: 1.17x slower                                                   |
| mako            | 4.41 ms                                                        | 5.64 ms: 1.28x slower                                                   |
| django_template | 12.5 ms                                                        | 16.4 ms: 1.31x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.22x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 763 us: 2.68x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 196 ms: 2.65x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.58x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 481 us: 2.07x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 197 ms: 2.05x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 209 ms: 1.85x faster                                                    |
| mdp                              | 1.06 sec                                                       | 603 ms: 1.76x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 85.6 ms: 1.55x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                    |
| k_core                           | 1.46 sec                                                       | 988 ms: 1.48x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 99.0 ms: 1.44x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 234 ms: 1.29x faster                                                    |
| deepcopy                         | 145 us                                                         | 117 us: 1.24x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.6 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 241 ms: 1.22x faster                                                    |
| go                               | 72.6 ms                                                        | 59.7 ms: 1.22x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 13.6 us: 1.21x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.17 ms: 1.17x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 817 ns: 1.16x faster                                                    |
| pyflate                          | 222 ms                                                         | 195 ms: 1.14x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 56.6 ms: 1.13x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| float                            | 31.4 ms                                                        | 28.4 ms: 1.11x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.07x faster                                                  |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                    |
| docutils                         | 1.05 sec                                                       | 986 ms: 1.06x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.23 us: 1.06x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 59.3 ms: 1.05x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.8 ms: 1.05x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.49 ms: 1.04x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 973 ms: 1.03x faster                                                    |
| pidigits                         | 166 ms                                                         | 162 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| fannkuch                         | 179 ms                                                         | 177 ms: 1.01x faster                                                    |
| pycparser                        | 470 ms                                                         | 467 ms: 1.01x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 23.3 ms: 1.01x slower                                                   |
| json                             | 1.94 ms                                                        | 1.96 ms: 1.01x slower                                                   |
| dask                             | 525 ms                                                         | 532 ms: 1.01x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 96.6 ms: 1.02x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 36.9 ms: 1.03x slower                                                   |
| shortest_path                    | 225 ms                                                         | 233 ms: 1.03x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.0 ms: 1.04x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.3 us: 1.05x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.21 ms: 1.05x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                   |
| connected_components             | 208 ms                                                         | 220 ms: 1.06x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.02 ms: 1.07x slower                                                   |
| thrift                           | 309 us                                                         | 332 us: 1.07x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.5 ms: 1.07x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 346 ms: 1.07x slower                                                    |
| 2to3                             | 112 ms                                                         | 121 ms: 1.08x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 227 ms: 1.09x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 52.3 ms: 1.09x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 709 ms: 1.09x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 109 us: 1.09x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 44.5 ns: 1.10x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.15 ms: 1.11x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 9.57 ms: 1.11x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.61 ms: 1.11x slower                                                   |
| pylint                           | 106 ms                                                         | 117 ms: 1.11x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.9 ms: 1.12x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 48.6 ms: 1.12x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.52 us: 1.13x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 73.1 us: 1.13x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.9 ms: 1.14x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 141 ms: 1.14x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.80 us: 1.14x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 149 us: 1.15x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 43.5 ms: 1.17x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.96 ms: 1.17x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.7 ms: 1.17x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 56.4 ms: 1.18x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 61.6 ms: 1.18x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 51.5 ms: 1.18x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.8 ms: 1.18x slower                                                   |
| chaos                            | 24.3 ms                                                        | 28.9 ms: 1.19x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 190 ms: 1.19x slower                                                    |
| raytrace                         | 109 ms                                                         | 131 ms: 1.20x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.2 ms: 1.22x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.31 us: 1.22x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.7 ms: 1.27x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.64 ms: 1.28x slower                                                   |
| coverage                         | 31.2 ms                                                        | 39.9 ms: 1.28x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.31 ms: 1.30x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.4 ms: 1.31x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 57.4 ms: 1.34x slower                                                   |
| nbody                            | 42.5 ms                                                        | 58.7 ms: 1.38x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 581 us: 1.41x slower                                                    |
| many_optionals                   | 200 us                                                         | 327 us: 1.63x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.0 ms: 2.66x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 18.1 ms: 2.89x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.00x faster                                                            |

Benchmark hidden because not significant (3): pathlib, coroutines, sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250723-3.15.0a0-ec7fad7-NOGIL/bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.011x faster

# HPT report

- Reliability score: 65.16% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.21x