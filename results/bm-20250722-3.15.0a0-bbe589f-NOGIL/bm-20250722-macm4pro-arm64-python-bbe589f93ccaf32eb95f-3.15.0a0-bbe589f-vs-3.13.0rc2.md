# Results vs. 3.13.0rc2

- fork: python
- ref: bbe589f93ccaf32eb95f
- machine: darwin-arm64
- commit hash: bbe589f
- commit date: 2025-07-22
- overall geometric mean: 1.003x faster
- HPT reliability: 76.20%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 124 ms: 1.11x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                  |
| html5lib       | 23.1 ms                                                        | 23.8 ms: 1.03x slower                                                   |
| sphinx         | 409 ms                                                         | 417 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 198 ms: 2.63x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 206 ms: 2.56x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 199 ms: 2.04x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.5 ms: 1.53x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 236 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 243 ms: 1.21x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 186 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 11.3 ms: 1.05x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 227 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.10x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.4 ms: 1.12x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.1 ms: 2.70x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.3 ms: 1.11x faster                                                   |
| pidigits       | 166 ms                                                         | 165 ms: 1.01x faster                                                    |
| nbody          | 42.5 ms                                                        | 58.3 ms: 1.37x slower                                                   |
| Geometric mean | (ref)                                                          | 1.07x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.35 ms: 1.14x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 96.6 ms: 1.02x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 52.5 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.7 ms: 1.19x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 58.4 ms: 1.07x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 975 ms: 1.03x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.57 ms: 1.02x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 36.9 ms: 1.03x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.7 us: 1.08x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 110 us: 1.11x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 150 us: 1.15x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.69 ms: 1.12x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 7.03 ms: 1.18x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.15x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.7 ms: 1.11x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.4 ms: 1.15x slower                                                   |
| mako            | 4.41 ms                                                        | 5.71 ms: 1.29x slower                                                   |
| django_template | 12.5 ms                                                        | 16.5 ms: 1.32x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.22x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 198 ms: 2.63x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 778 us: 2.62x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 206 ms: 2.56x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 487 us: 2.04x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 199 ms: 2.04x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                    |
| mdp                              | 1.06 sec                                                       | 601 ms: 1.76x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.5 ms: 1.53x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 997 ms: 1.47x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 236 ms: 1.28x faster                                                    |
| deepcopy                         | 145 us                                                         | 118 us: 1.23x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 243 ms: 1.21x faster                                                    |
| go                               | 72.6 ms                                                        | 60.2 ms: 1.21x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 13.7 us: 1.20x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.7 ms: 1.19x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 821 ns: 1.15x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 55.8 ms: 1.15x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.35 ms: 1.14x faster                                                   |
| pyflate                          | 222 ms                                                         | 196 ms: 1.13x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.11x faster                                                    |
| float                            | 31.4 ms                                                        | 28.3 ms: 1.11x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.08x faster                                                  |
| xml_etree_parse                  | 62.4 ms                                                        | 58.4 ms: 1.07x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 19.0 ms: 1.05x faster                                                   |
| async_generators                 | 193 ms                                                         | 186 ms: 1.04x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.25 us: 1.04x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                  |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 975 ms: 1.03x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.57 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 165 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 531 ms: 1.01x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 96.6 ms: 1.02x slower                                                   |
| sphinx                           | 409 ms                                                         | 417 ms: 1.02x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.8 ms: 1.03x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 36.9 ms: 1.03x slower                                                   |
| shortest_path                    | 225 ms                                                         | 233 ms: 1.04x slower                                                    |
| json                             | 1.94 ms                                                        | 2.03 ms: 1.05x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.21 ms: 1.05x slower                                                   |
| coroutines                       | 10.8 ms                                                        | 11.3 ms: 1.05x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                   |
| connected_components             | 208 ms                                                         | 222 ms: 1.07x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.6 ms: 1.07x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 8.08 ms: 1.07x slower                                                   |
| thrift                           | 309 us                                                         | 333 us: 1.08x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.7 us: 1.08x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 349 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 227 ms: 1.09x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 27.0 ms: 1.09x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 712 ms: 1.10x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.12 ms: 1.10x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 52.5 ms: 1.10x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.10x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 44.7 ns: 1.10x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 23.7 ms: 1.11x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 110 us: 1.11x slower                                                    |
| 2to3                             | 112 ms                                                         | 124 ms: 1.11x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.4 ms: 1.12x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 9.69 ms: 1.12x slower                                                   |
| pylint                           | 106 ms                                                         | 119 ms: 1.12x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.63 ms: 1.13x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 73.1 us: 1.13x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.9 ms: 1.13x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.55 us: 1.14x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.4 ms: 1.15x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 42.8 ms: 1.15x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 150 us: 1.15x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.83 us: 1.16x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 143 ms: 1.16x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 51.1 ms: 1.17x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 61.2 ms: 1.17x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 56.3 ms: 1.18x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 7.03 ms: 1.18x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 189 ms: 1.18x slower                                                    |
| raytrace                         | 109 ms                                                         | 130 ms: 1.20x slower                                                    |
| chaos                            | 24.3 ms                                                        | 29.1 ms: 1.20x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.25 us: 1.21x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 46.0 ms: 1.22x slower                                                   |
| generators                       | 15.7 ms                                                        | 19.4 ms: 1.24x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.9 ms: 1.28x slower                                                   |
| coverage                         | 31.2 ms                                                        | 39.9 ms: 1.28x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.71 ms: 1.29x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.35 ms: 1.32x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.5 ms: 1.32x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 57.9 ms: 1.35x slower                                                   |
| nbody                            | 42.5 ms                                                        | 58.3 ms: 1.37x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 598 us: 1.45x slower                                                    |
| many_optionals                   | 200 us                                                         | 338 us: 1.68x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.1 ms: 2.70x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 18.5 ms: 2.96x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.00x slower                                                            |

Benchmark hidden because not significant (3): pathlib, fannkuch, pycparser
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250722-3.15.0a0-bbe589f-NOGIL/bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.003x faster

# HPT report

- Reliability score: 76.20% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.20x