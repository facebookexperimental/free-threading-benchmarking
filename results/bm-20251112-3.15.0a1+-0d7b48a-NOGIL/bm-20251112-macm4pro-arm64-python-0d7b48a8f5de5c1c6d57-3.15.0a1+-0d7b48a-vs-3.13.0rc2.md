# Results vs. 3.13.0rc2

- fork: python
- ref: 0d7b48a8f5de5c1c6d57
- machine: darwin-arm64
- commit hash: 0d7b48a
- commit date: 2025-11-12
- overall geometric mean: 1.002x slower
- HPT reliability: 76.19%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251112-macm4pro-arm64-python-0d7b48a8f5de5c1c6d57-3.15.0a1+-0d7b48a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 125 ms: 1.12x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.00 sec: 1.05x faster                                                   |
| html5lib       | 23.1 ms                                                        | 23.5 ms: 1.02x slower                                                    |
| sphinx         | 409 ms                                                         | 417 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251112-macm4pro-arm64-python-0d7b48a8f5de5c1c6d57-3.15.0a1+-0d7b48a |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 197 ms: 2.64x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 206 ms: 2.55x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 201 ms: 2.02x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 211 ms: 1.83x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 88.5 ms: 1.50x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 239 ms: 1.26x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 246 ms: 1.19x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                     |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.7 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.10x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 230 ms: 1.10x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 49.2 ms: 1.14x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.7 ms: 2.72x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.23x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251112-macm4pro-arm64-python-0d7b48a8f5de5c1c6d57-3.15.0a1+-0d7b48a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.7 ms: 1.06x faster                                                    |
| pidigits       | 166 ms                                                         | 162 ms: 1.02x faster                                                     |
| nbody          | 42.5 ms                                                        | 57.2 ms: 1.35x slower                                                    |
| Geometric mean | (ref)                                                          | 1.08x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251112-macm4pro-arm64-python-0d7b48a8f5de5c1c6d57-3.15.0a1+-0d7b48a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.53 ms: 1.12x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 97.9 ms: 1.03x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 53.0 ms: 1.11x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251112-macm4pro-arm64-python-0d7b48a8f5de5c1c6d57-3.15.0a1+-0d7b48a |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 37.8 ms: 1.22x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.12 ms: 1.13x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 59.0 ms: 1.06x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 958 ms: 1.04x faster                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 36.9 ms: 1.03x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.3 us: 1.05x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.0 ms: 1.07x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 112 us: 1.12x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 153 us: 1.18x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.00x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251112-macm4pro-arm64-python-0d7b48a8f5de5c1c6d57-3.15.0a1+-0d7b48a |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.69 ms: 1.12x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.04 ms: 1.18x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.15x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251112-macm4pro-arm64-python-0d7b48a8f5de5c1c6d57-3.15.0a1+-0d7b48a |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 24.6 ms: 1.15x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.9 ms: 1.19x slower                                                    |
| mako            | 4.41 ms                                                        | 5.75 ms: 1.30x slower                                                    |
| django_template | 12.5 ms                                                        | 16.4 ms: 1.32x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.24x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251112-macm4pro-arm64-python-0d7b48a8f5de5c1c6d57-3.15.0a1+-0d7b48a |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 197 ms: 2.64x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 775 us: 2.64x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 206 ms: 2.55x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 483 us: 2.06x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 201 ms: 2.02x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 211 ms: 1.83x faster                                                     |
| mdp                              | 1.06 sec                                                       | 612 ms: 1.73x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 88.5 ms: 1.50x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 239 ms: 1.26x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 13.2 us: 1.24x faster                                                    |
| deepcopy                         | 145 us                                                         | 118 us: 1.23x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.8 ms: 1.22x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 246 ms: 1.19x faster                                                     |
| go                               | 72.6 ms                                                        | 61.8 ms: 1.17x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 822 ns: 1.15x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 55.9 ms: 1.14x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.12 ms: 1.13x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.53 ms: 1.12x faster                                                    |
| pyflate                          | 222 ms                                                         | 198 ms: 1.12x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                     |
| float                            | 31.4 ms                                                        | 29.7 ms: 1.06x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 59.0 ms: 1.06x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.02 sec: 1.06x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.00 sec: 1.05x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 958 ms: 1.04x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 19.1 ms: 1.04x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.04x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.26 us: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| pidigits                         | 166 ms                                                         | 162 ms: 1.02x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.7 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 532 ms: 1.01x slower                                                     |
| pycparser                        | 470 ms                                                         | 476 ms: 1.01x slower                                                     |
| json                             | 1.94 ms                                                        | 1.97 ms: 1.02x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.5 ms: 1.02x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.13 ms: 1.02x slower                                                    |
| sphinx                           | 409 ms                                                         | 417 ms: 1.02x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 36.9 ms: 1.03x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 97.9 ms: 1.03x slower                                                    |
| fannkuch                         | 179 ms                                                         | 186 ms: 1.04x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.3 us: 1.05x slower                                                    |
| pylint                           | 106 ms                                                         | 112 ms: 1.06x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 8.01 ms: 1.06x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.0 ms: 1.07x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 133 ms: 1.08x slower                                                     |
| richards                         | 22.1 ms                                                        | 24.0 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.10x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 353 ms: 1.10x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 230 ms: 1.10x slower                                                     |
| regex_compile                    | 47.9 ms                                                        | 53.0 ms: 1.11x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 720 ms: 1.11x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.16 ms: 1.11x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 27.5 ms: 1.11x slower                                                    |
| thrift                           | 309 us                                                         | 344 us: 1.11x slower                                                     |
| 2to3                             | 112 ms                                                         | 125 ms: 1.12x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.63 ms: 1.12x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 112 us: 1.12x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 45.6 ns: 1.12x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.69 ms: 1.12x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.51 us: 1.12x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.2 ms: 1.14x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 73.7 us: 1.14x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.80 us: 1.14x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 34.3 ms: 1.15x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 24.6 ms: 1.15x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 60.5 ms: 1.16x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 44.0 ms: 1.16x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.17x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 51.1 ms: 1.17x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 56.3 ms: 1.18x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 153 us: 1.18x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 7.04 ms: 1.18x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 44.1 ms: 1.18x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.9 ms: 1.19x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 192 ms: 1.21x slower                                                     |
| chaos                            | 24.3 ms                                                        | 29.4 ms: 1.21x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.1 ms: 1.22x slower                                                    |
| raytrace                         | 109 ms                                                         | 133 ms: 1.22x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 8.51 us: 1.25x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.23 ms: 1.25x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 42.6 ms: 1.27x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 534 us: 1.30x slower                                                     |
| mako                             | 4.41 ms                                                        | 5.75 ms: 1.30x slower                                                    |
| coverage                         | 31.2 ms                                                        | 40.7 ms: 1.30x slower                                                    |
| django_template                  | 12.5 ms                                                        | 16.4 ms: 1.32x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 57.5 ms: 1.34x slower                                                    |
| nbody                            | 42.5 ms                                                        | 57.2 ms: 1.35x slower                                                    |
| many_optionals                   | 200 us                                                         | 387 us: 1.93x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.7 ms: 2.72x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 19.2 ms: 3.07x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                             |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251112-3.15.0a1+-0d7b48a-NOGIL/bm-20251112-macm4pro-arm64-python-0d7b48a8f5de5c1c6d57-3.15.0a1+-0d7b48a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.002x slower

# HPT report

- Reliability score: 76.19% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.31x