# Results vs. 3.13.0rc2

- fork: python
- ref: 4e40f2bea7edfa5ba7e2
- machine: darwin-arm64
- commit hash: 4e40f2b
- commit date: 2025-07-27
- overall geometric mean: 1.012x faster
- HPT reliability: 59.53%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250727-macm4pro-arm64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 121 ms: 1.09x slower                                                    |
| docutils       | 1.05 sec                                                       | 995 ms: 1.05x faster                                                    |
| html5lib       | 23.1 ms                                                        | 23.3 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250727-macm4pro-arm64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 197 ms: 2.65x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.58x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.05x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 208 ms: 1.86x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.5 ms: 1.53x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 99.4 ms: 1.43x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 235 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 242 ms: 1.21x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                    |
| async_generators                 | 193 ms                                                         | 184 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 11.0 ms: 1.02x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 226 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.2 ms: 1.12x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.0 ms: 2.66x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.25x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250727-macm4pro-arm64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.8 ms: 1.13x faster                                                   |
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                    |
| nbody          | 42.5 ms                                                        | 59.1 ms: 1.39x slower                                                   |
| Geometric mean | (ref)                                                          | 1.06x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250727-macm4pro-arm64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.12 ms: 1.17x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 96.0 ms: 1.01x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 52.4 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250727-macm4pro-arm64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 36.4 ms: 1.27x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 56.3 ms: 1.11x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 965 ms: 1.04x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.51 ms: 1.03x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 36.7 ms: 1.03x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.05x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 109 us: 1.10x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 149 us: 1.15x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250727-macm4pro-arm64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.55 ms: 1.11x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.94 ms: 1.17x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250727-macm4pro-arm64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.9 ms: 1.12x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.6 ms: 1.16x slower                                                   |
| mako            | 4.41 ms                                                        | 5.58 ms: 1.27x slower                                                   |
| django_template | 12.5 ms                                                        | 16.3 ms: 1.31x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.21x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250727-macm4pro-arm64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 764 us: 2.67x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 197 ms: 2.65x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.58x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 484 us: 2.05x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.05x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 208 ms: 1.86x faster                                                    |
| mdp                              | 1.06 sec                                                       | 599 ms: 1.76x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.5 ms: 1.53x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 988 ms: 1.48x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 99.4 ms: 1.43x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 235 ms: 1.28x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 36.4 ms: 1.27x faster                                                   |
| deepcopy                         | 145 us                                                         | 116 us: 1.25x faster                                                    |
| go                               | 72.6 ms                                                        | 59.7 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 242 ms: 1.21x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.6 us: 1.21x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.12 ms: 1.17x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 814 ns: 1.16x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 55.3 ms: 1.16x faster                                                   |
| pyflate                          | 222 ms                                                         | 195 ms: 1.14x faster                                                    |
| float                            | 31.4 ms                                                        | 27.8 ms: 1.13x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 56.3 ms: 1.11x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.08x faster                                                  |
| deepcopy_reduce                  | 1.30 us                                                        | 1.22 us: 1.06x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.7 ms: 1.06x faster                                                   |
| async_generators                 | 193 ms                                                         | 184 ms: 1.05x faster                                                    |
| docutils                         | 1.05 sec                                                       | 995 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 965 ms: 1.04x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.51 ms: 1.03x faster                                                   |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                   |
| fannkuch                         | 179 ms                                                         | 178 ms: 1.01x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 23.3 ms: 1.01x slower                                                   |
| dask                             | 525 ms                                                         | 531 ms: 1.01x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 96.0 ms: 1.01x slower                                                   |
| json                             | 1.94 ms                                                        | 1.97 ms: 1.02x slower                                                   |
| coroutines                       | 10.8 ms                                                        | 11.0 ms: 1.02x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 36.7 ms: 1.03x slower                                                   |
| shortest_path                    | 225 ms                                                         | 232 ms: 1.03x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.0 ms: 1.04x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.22 ms: 1.05x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.05x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                   |
| connected_components             | 208 ms                                                         | 220 ms: 1.06x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.98 ms: 1.06x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 26.4 ms: 1.07x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 348 ms: 1.08x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 43.9 ns: 1.08x slower                                                   |
| thrift                           | 309 us                                                         | 334 us: 1.08x slower                                                    |
| 2to3                             | 112 ms                                                         | 121 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 226 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 708 ms: 1.09x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 52.4 ms: 1.09x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.12 ms: 1.10x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 109 us: 1.10x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.55 ms: 1.11x slower                                                   |
| pylint                           | 106 ms                                                         | 117 ms: 1.11x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.2 ms: 1.12x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.62 ms: 1.12x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 23.9 ms: 1.12x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.7 ms: 1.13x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.52 us: 1.13x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 73.2 us: 1.13x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 142 ms: 1.15x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 149 us: 1.15x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.81 us: 1.15x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.6 ms: 1.16x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 55.7 ms: 1.16x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 43.4 ms: 1.17x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.94 ms: 1.17x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 61.2 ms: 1.17x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 51.4 ms: 1.18x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.8 ms: 1.18x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 190 ms: 1.19x slower                                                    |
| chaos                            | 24.3 ms                                                        | 29.1 ms: 1.20x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.22 us: 1.21x slower                                                   |
| generators                       | 15.7 ms                                                        | 19.1 ms: 1.22x slower                                                   |
| raytrace                         | 109 ms                                                         | 133 ms: 1.22x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.58 ms: 1.27x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.9 ms: 1.28x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.1 ms: 1.29x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.3 ms: 1.31x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.34 ms: 1.32x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 56.6 ms: 1.32x slower                                                   |
| nbody                            | 42.5 ms                                                        | 59.1 ms: 1.39x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 581 us: 1.41x slower                                                    |
| many_optionals                   | 200 us                                                         | 330 us: 1.65x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.0 ms: 2.66x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 18.1 ms: 2.89x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (2): pycparser, sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250727-3.15.0a0-4e40f2b-NOGIL/bm-20250727-macm4pro-arm64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.012x faster

# HPT report

- Reliability score: 59.53% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.21x