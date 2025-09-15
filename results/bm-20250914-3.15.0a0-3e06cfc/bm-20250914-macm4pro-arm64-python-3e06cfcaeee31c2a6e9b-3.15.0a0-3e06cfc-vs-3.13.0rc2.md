# Results vs. 3.13.0rc2

- fork: python
- ref: 3e06cfcaeee31c2a6e9b
- machine: darwin-arm64
- commit hash: 3e06cfc
- commit date: 2025-09-14
- overall geometric mean: 1.027x faster
- HPT reliability: 97.18%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250914-macm4pro-arm64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 113 ms: 1.01x slower                                                    |
| html5lib       | 23.1 ms                                                        | 23.8 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250914-macm4pro-arm64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 250 ms: 2.10x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 252 ms: 2.07x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 250 ms: 1.62x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 251 ms: 1.54x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.27x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 260 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 262 ms: 1.12x faster                                                    |
| async_generators                 | 193 ms                                                         | 173 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.11x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.93 ms: 1.08x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.6 ms: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.8 ms: 3.00x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250914-macm4pro-arm64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.4 ms: 1.03x faster                                                   |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| nbody          | 42.5 ms                                                        | 49.8 ms: 1.17x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250914-macm4pro-arm64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.97 ms: 1.07x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 95.7 ms: 1.01x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 48.7 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250914-macm4pro-arm64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.79 ms: 1.23x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 901 ms: 1.11x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 43.5 ms: 1.06x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 61.2 ms: 1.02x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.6 ms: 1.01x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 99.8 us: 1.00x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.0 us: 1.02x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 146 us: 1.12x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.03x faster                                                            |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250914-macm4pro-arm64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.67 ms: 1.00x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.22 ms: 1.04x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250914-macm4pro-arm64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.91 ms: 1.01x faster                                                   |
| genshi_xml      | 21.4 ms                                                        | 21.6 ms: 1.01x slower                                                   |
| mako            | 4.41 ms                                                        | 4.93 ms: 1.12x slower                                                   |
| django_template | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.09x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250914-macm4pro-arm64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 250 ms: 2.10x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 252 ms: 2.07x faster                                                    |
| mdp                              | 1.06 sec                                                       | 537 ms: 1.97x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 250 ms: 1.62x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 251 ms: 1.54x faster                                                    |
| k_core                           | 1.46 sec                                                       | 956 ms: 1.53x faster                                                    |
| deepcopy                         | 145 us                                                         | 108 us: 1.35x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.4 us: 1.33x faster                                                   |
| go                               | 72.6 ms                                                        | 55.9 ms: 1.30x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 49.6 ms: 1.29x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.27x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.79 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 260 ms: 1.16x faster                                                    |
| pyflate                          | 222 ms                                                         | 195 ms: 1.14x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.14 us: 1.13x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 262 ms: 1.12x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                   |
| async_generators                 | 193 ms                                                         | 173 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.11x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 901 ms: 1.11x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 17.9 ms: 1.11x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.78 ms: 1.10x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                  |
| coroutines                       | 10.8 ms                                                        | 9.93 ms: 1.08x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 918 us: 1.08x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.97 ms: 1.07x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.5 ms: 1.06x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                   |
| connected_components             | 208 ms                                                         | 200 ms: 1.04x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.6 ms: 1.04x faster                                                   |
| float                            | 31.4 ms                                                        | 30.4 ms: 1.03x faster                                                   |
| richards                         | 22.1 ms                                                        | 21.4 ms: 1.03x faster                                                   |
| shortest_path                    | 225 ms                                                         | 219 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 63.1 us: 1.02x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 24.2 ms: 1.02x faster                                                   |
| json                             | 1.94 ms                                                        | 1.90 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 61.2 ms: 1.02x faster                                                   |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.80 ms: 1.02x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.41 ms: 1.02x faster                                                   |
| fannkuch                         | 179 ms                                                         | 177 ms: 1.01x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.6 ms: 1.01x faster                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.03 ms: 1.01x faster                                                   |
| genshi_text                      | 9.97 ms                                                        | 9.91 ms: 1.01x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 35.6 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 99.8 us: 1.00x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 8.67 ms: 1.00x slower                                                   |
| 2to3                             | 112 ms                                                         | 113 ms: 1.01x slower                                                    |
| thrift                           | 309 us                                                         | 312 us: 1.01x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.6 ms: 1.01x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 95.7 ms: 1.01x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.0 us: 1.02x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 48.7 ms: 1.02x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 38.0 ms: 1.02x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 328 ms: 1.02x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 665 ms: 1.02x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.8 ms: 1.03x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.30 us: 1.03x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.52 us: 1.03x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 49.7 ms: 1.04x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 428 us: 1.04x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 99.7 ms: 1.04x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.22 ms: 1.04x slower                                                   |
| pycparser                        | 470 ms                                                         | 493 ms: 1.05x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.53 ms: 1.05x slower                                                   |
| coverage                         | 31.2 ms                                                        | 33.1 ms: 1.06x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 132 ms: 1.06x slower                                                    |
| pylint                           | 106 ms                                                         | 112 ms: 1.06x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 170 ms: 1.07x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 56.0 ms: 1.07x slower                                                   |
| chaos                            | 24.3 ms                                                        | 26.0 ms: 1.07x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.92 ms: 1.08x slower                                                   |
| raytrace                         | 109 ms                                                         | 119 ms: 1.09x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.46 us: 1.10x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 36.9 ms: 1.10x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 41.6 ms: 1.10x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.4 ms: 1.11x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.93 ms: 1.12x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 146 us: 1.12x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 48.7 ms: 1.14x slower                                                   |
| nbody                            | 42.5 ms                                                        | 49.8 ms: 1.17x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                    |
| many_optionals                   | 200 us                                                         | 315 us: 1.57x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 17.2 ms: 2.74x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.8 ms: 3.00x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                            |

Benchmark hidden because not significant (6): sphinx, docutils, xml_etree_process, sqlite_synth, spectral_norm, logging_silent
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250914-3.15.0a0-3e06cfc/bm-20250914-macm4pro-arm64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.027x faster

# HPT report

- Reliability score: 97.18% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x