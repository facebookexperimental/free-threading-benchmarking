# Results vs. 3.13.0rc2

- fork: python
- ref: 98e2c3af4794d6c6ebe4
- machine: darwin-arm64
- commit hash: 98e2c3a
- commit date: 2025-05-09
- overall geometric mean: 1.003x faster
- HPT reliability: 78.08%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 122 ms: 1.09x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.03x faster                                                  |
| html5lib       | 23.1 ms                                                        | 25.8 ms: 1.12x slower                                                   |
| sphinx         | 409 ms                                                         | 424 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 194 ms: 2.69x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.57x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 197 ms: 2.06x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.7 ms: 1.53x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 235 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 243 ms: 1.21x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 179 ms: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 228 ms: 1.09x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.9 ms: 1.16x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.9 ms: 2.69x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.25x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.3 ms: 1.11x faster                                                   |
| pidigits       | 166 ms                                                         | 162 ms: 1.02x faster                                                    |
| nbody          | 42.5 ms                                                        | 56.6 ms: 1.33x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.31 ms: 1.15x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.50 ms: 1.07x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 98.2 ms: 1.04x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 54.1 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 37.8 ms: 1.22x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 55.8 ms: 1.12x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 990 ms: 1.01x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 38.2 ms: 1.07x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 27.8 ms: 1.10x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 111 us: 1.11x slower                                                    |
| json_loads           | 10.8 us                                                        | 12.6 us: 1.16x slower                                                   |
| json_dumps           | 4.65 ms                                                        | 5.43 ms: 1.17x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 153 us: 1.18x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.45 ms: 1.09x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.87 ms: 1.15x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.12x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.7 ms: 1.11x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.6 ms: 1.16x slower                                                   |
| mako            | 4.41 ms                                                        | 5.64 ms: 1.28x slower                                                   |
| django_template | 12.5 ms                                                        | 17.1 ms: 1.37x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.23x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 194 ms: 2.69x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 780 us: 2.62x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.57x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 482 us: 2.06x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 197 ms: 2.06x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                    |
| mdp                              | 1.06 sec                                                       | 582 ms: 1.82x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.7 ms: 1.53x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 998 ms: 1.47x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 235 ms: 1.28x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.8 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 243 ms: 1.21x faster                                                    |
| go                               | 72.6 ms                                                        | 63.0 ms: 1.15x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 14.3 us: 1.15x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.31 ms: 1.15x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 825 ns: 1.15x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 55.8 ms: 1.15x faster                                                   |
| deepcopy                         | 145 us                                                         | 127 us: 1.14x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 55.8 ms: 1.12x faster                                                   |
| float                            | 31.4 ms                                                        | 28.3 ms: 1.11x faster                                                   |
| pyflate                          | 222 ms                                                         | 201 ms: 1.10x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 179 ms: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.99 sec: 1.07x faster                                                  |
| regex_effbot                     | 1.61 ms                                                        | 1.50 ms: 1.07x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 19.0 ms: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.03x faster                                                  |
| pidigits                         | 166 ms                                                         | 162 ms: 1.02x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 990 ms: 1.01x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.28 us: 1.01x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 11.3 ms: 1.01x slower                                                   |
| pycparser                        | 470 ms                                                         | 476 ms: 1.01x slower                                                    |
| shortest_path                    | 225 ms                                                         | 232 ms: 1.03x slower                                                    |
| fannkuch                         | 179 ms                                                         | 185 ms: 1.03x slower                                                    |
| sphinx                           | 409 ms                                                         | 424 ms: 1.04x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 98.2 ms: 1.04x slower                                                   |
| connected_components             | 208 ms                                                         | 219 ms: 1.05x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 38.2 ms: 1.07x slower                                                   |
| json                             | 1.94 ms                                                        | 2.08 ms: 1.07x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 8.14 ms: 1.08x slower                                                   |
| thrift                           | 309 us                                                         | 336 us: 1.09x slower                                                    |
| 2to3                             | 112 ms                                                         | 122 ms: 1.09x slower                                                    |
| richards                         | 22.1 ms                                                        | 24.1 ms: 1.09x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.45 ms: 1.09x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 228 ms: 1.09x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.8 ms: 1.10x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.37 ms: 1.10x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.15 ms: 1.11x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 23.7 ms: 1.11x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.61 ms: 1.11x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 111 us: 1.11x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 41.5 ms: 1.11x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 27.5 ms: 1.11x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 25.8 ms: 1.12x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 729 ms: 1.12x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 361 ms: 1.12x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 54.1 ms: 1.13x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.8 ms: 1.13x slower                                                   |
| pylint                           | 106 ms                                                         | 120 ms: 1.13x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.87 ms: 1.15x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 49.9 ms: 1.16x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 55.5 ms: 1.16x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.6 ms: 1.16x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 144 ms: 1.16x slower                                                    |
| json_loads                       | 10.8 us                                                        | 12.6 us: 1.16x slower                                                   |
| json_dumps                       | 4.65 ms                                                        | 5.43 ms: 1.17x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 61.5 ms: 1.18x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 112 ms: 1.18x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 153 us: 1.18x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 44.7 ms: 1.18x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 76.5 us: 1.18x slower                                                   |
| generators                       | 15.7 ms                                                        | 18.7 ms: 1.19x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 52.5 ms: 1.20x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 192 ms: 1.21x slower                                                    |
| chaos                            | 24.3 ms                                                        | 29.5 ms: 1.22x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.17 ms: 1.22x slower                                                   |
| raytrace                         | 109 ms                                                         | 133 ms: 1.22x slower                                                    |
| many_optionals                   | 200 us                                                         | 252 us: 1.26x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.85 us: 1.27x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.9 ms: 1.28x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.64 ms: 1.28x slower                                                   |
| logging_format                   | 2.45 us                                                        | 3.13 us: 1.28x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.6 ms: 1.30x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.90 us: 1.31x slower                                                   |
| nbody                            | 42.5 ms                                                        | 56.6 ms: 1.33x slower                                                   |
| django_template                  | 12.5 ms                                                        | 17.1 ms: 1.37x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 597 us: 1.45x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 64.7 ms: 1.51x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 9.56 ms: 1.53x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.9 ms: 2.69x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 215 ns: 5.29x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed
Ignored benchmarks (11) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250509-3.15.0a0-98e2c3a-NOGIL/bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.003x faster

# HPT report

- Reliability score: 78.08% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.22x