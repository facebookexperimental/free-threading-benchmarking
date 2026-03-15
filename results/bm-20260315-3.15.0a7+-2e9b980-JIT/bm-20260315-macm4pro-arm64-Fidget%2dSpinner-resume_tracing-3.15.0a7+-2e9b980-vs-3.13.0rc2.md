# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: darwin-arm64
- commit hash: 2e9b980
- commit date: 2026-03-15
- overall geometric mean: 1.195x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 111 ms: 1.01x faster                                                         |
| docutils       | 1.05 sec                                                       | 962 ms: 1.09x faster                                                         |
| html5lib       | 23.1 ms                                                        | 18.8 ms: 1.23x faster                                                        |
| sphinx         | 409 ms                                                         | 386 ms: 1.06x faster                                                         |
| Geometric mean | (ref)                                                          | 1.09x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|----------------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 203 ms: 2.56x faster                                                         |
| async_tree_eager_io              | 525 ms                                                         | 207 ms: 2.53x faster                                                         |
| async_tree_io_tg                 | 405 ms                                                         | 207 ms: 1.95x faster                                                         |
| async_tree_io                    | 386 ms                                                         | 207 ms: 1.87x faster                                                         |
| async_tree_none                  | 142 ms                                                         | 88.2 ms: 1.61x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 89.4 ms: 1.48x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 126 ms: 1.47x faster                                                         |
| async_tree_memoization_tg        | 186 ms                                                         | 127 ms: 1.46x faster                                                         |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 238 ms: 1.27x faster                                                         |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 237 ms: 1.24x faster                                                         |
| async_tree_eager_memoization     | 122 ms                                                         | 102 ms: 1.19x faster                                                         |
| async_tree_eager                 | 43.2 ms                                                        | 36.5 ms: 1.18x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 9.35 ms: 1.15x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 212 ms: 1.06x faster                                                         |
| async_generators                 | 193 ms                                                         | 183 ms: 1.06x faster                                                         |
| asyncio_websockets               | 194 ms                                                         | 184 ms: 1.05x faster                                                         |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 234 ms: 1.12x slower                                                         |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 115 ms: 1.13x slower                                                         |
| async_tree_eager_tg              | 28.9 ms                                                        | 76.7 ms: 2.65x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.28x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 23.6 ms: 1.33x faster                                                        |
| nbody          | 42.5 ms                                                        | 39.8 ms: 1.07x faster                                                        |
| pidigits       | 166 ms                                                         | 159 ms: 1.04x faster                                                         |
| Geometric mean | (ref)                                                          | 1.14x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 39.5 ms: 1.21x faster                                                        |
| regex_v8       | 10.7 ms                                                        | 9.53 ms: 1.12x faster                                                        |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                        |
| regex_dna      | 94.6 ms                                                        | 93.2 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                          | 1.11x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|----------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 628 ms: 1.59x faster                                                         |
| json_dumps           | 4.65 ms                                                        | 3.51 ms: 1.33x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 38.5 ms: 1.20x faster                                                        |
| xml_etree_process    | 25.4 ms                                                        | 21.5 ms: 1.18x faster                                                        |
| unpickle_pure_python | 99.5 us                                                        | 84.9 us: 1.17x faster                                                        |
| xml_etree_generate   | 35.8 ms                                                        | 32.1 ms: 1.12x faster                                                        |
| pickle_pure_python   | 130 us                                                         | 126 us: 1.03x faster                                                         |
| json_loads           | 10.8 us                                                        | 10.6 us: 1.03x faster                                                        |
| xml_etree_parse      | 62.4 ms                                                        | 64.2 ms: 1.03x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.17x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.68 ms: 1.01x slower                                                        |
| python_startup_no_site | 5.95 ms                                                        | 6.24 ms: 1.05x slower                                                        |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|-----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.00 ms: 1.10x faster                                                        |
| django_template | 12.5 ms                                                        | 12.4 ms: 1.01x faster                                                        |
| Geometric mean  | (ref)                                                          | 1.05x faster                                                                 |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|----------------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 203 ms: 2.56x faster                                                         |
| async_tree_eager_io              | 525 ms                                                         | 207 ms: 2.53x faster                                                         |
| richards                         | 22.1 ms                                                        | 9.63 ms: 2.29x faster                                                        |
| richards_super                   | 24.7 ms                                                        | 11.4 ms: 2.17x faster                                                        |
| mdp                              | 1.06 sec                                                       | 523 ms: 2.02x faster                                                         |
| async_tree_io_tg                 | 405 ms                                                         | 207 ms: 1.95x faster                                                         |
| async_tree_io                    | 386 ms                                                         | 207 ms: 1.87x faster                                                         |
| subparsers                       | 6.26 ms                                                        | 3.50 ms: 1.79x faster                                                        |
| scimark_sor                      | 64.0 ms                                                        | 36.8 ms: 1.74x faster                                                        |
| k_core                           | 1.46 sec                                                       | 858 ms: 1.70x faster                                                         |
| deepcopy_memo                    | 16.5 us                                                        | 10.0 us: 1.64x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 88.2 ms: 1.61x faster                                                        |
| tomli_loads                      | 1000 ms                                                        | 628 ms: 1.59x faster                                                         |
| go                               | 72.6 ms                                                        | 45.9 ms: 1.58x faster                                                        |
| deepcopy                         | 145 us                                                         | 94.3 us: 1.54x faster                                                        |
| pyflate                          | 222 ms                                                         | 145 ms: 1.53x faster                                                         |
| async_tree_none_tg               | 133 ms                                                         | 89.4 ms: 1.48x faster                                                        |
| scimark_lu                       | 42.8 ms                                                        | 28.9 ms: 1.48x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 126 ms: 1.47x faster                                                         |
| async_tree_memoization_tg        | 186 ms                                                         | 127 ms: 1.46x faster                                                         |
| float                            | 31.4 ms                                                        | 23.6 ms: 1.33x faster                                                        |
| json_dumps                       | 4.65 ms                                                        | 3.51 ms: 1.33x faster                                                        |
| scimark_monte_carlo              | 29.9 ms                                                        | 22.9 ms: 1.31x faster                                                        |
| deltablue                        | 1.45 ms                                                        | 1.11 ms: 1.31x faster                                                        |
| deepcopy_reduce                  | 1.30 us                                                        | 1.00 us: 1.29x faster                                                        |
| logging_format                   | 2.45 us                                                        | 1.91 us: 1.28x faster                                                        |
| pprint_safe_repr                 | 322 ms                                                         | 252 ms: 1.28x faster                                                         |
| pprint_pformat                   | 650 ms                                                         | 510 ms: 1.27x faster                                                         |
| logging_simple                   | 2.24 us                                                        | 1.76 us: 1.27x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 238 ms: 1.27x faster                                                         |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 237 ms: 1.24x faster                                                         |
| html5lib                         | 23.1 ms                                                        | 18.8 ms: 1.23x faster                                                        |
| scimark_fft                      | 124 ms                                                         | 101 ms: 1.22x faster                                                         |
| regex_compile                    | 47.9 ms                                                        | 39.5 ms: 1.21x faster                                                        |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.5 ms: 1.20x faster                                                        |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.78 sec: 1.19x faster                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 102 ms: 1.19x faster                                                         |
| fannkuch                         | 179 ms                                                         | 150 ms: 1.19x faster                                                         |
| async_tree_eager                 | 43.2 ms                                                        | 36.5 ms: 1.18x faster                                                        |
| xml_etree_process                | 25.4 ms                                                        | 21.5 ms: 1.18x faster                                                        |
| hexiom                           | 2.85 ms                                                        | 2.42 ms: 1.17x faster                                                        |
| unpickle_pure_python             | 99.5 us                                                        | 84.9 us: 1.17x faster                                                        |
| telco                            | 3.07 ms                                                        | 2.62 ms: 1.17x faster                                                        |
| logging_silent                   | 40.6 ns                                                        | 35.1 ns: 1.16x faster                                                        |
| chaos                            | 24.3 ms                                                        | 21.0 ms: 1.15x faster                                                        |
| nqueens                          | 37.2 ms                                                        | 32.3 ms: 1.15x faster                                                        |
| comprehensions                   | 6.80 us                                                        | 5.90 us: 1.15x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 9.35 ms: 1.15x faster                                                        |
| spectral_norm                    | 43.7 ms                                                        | 38.1 ms: 1.15x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 881 us: 1.13x faster                                                         |
| regex_v8                         | 10.7 ms                                                        | 9.53 ms: 1.12x faster                                                        |
| xml_etree_generate               | 35.8 ms                                                        | 32.1 ms: 1.12x faster                                                        |
| dulwich_log                      | 19.8 ms                                                        | 17.9 ms: 1.11x faster                                                        |
| mako                             | 4.41 ms                                                        | 4.00 ms: 1.10x faster                                                        |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                        |
| docutils                         | 1.05 sec                                                       | 962 ms: 1.09x faster                                                         |
| meteor_contest                   | 47.9 ms                                                        | 44.8 ms: 1.07x faster                                                        |
| nbody                            | 42.5 ms                                                        | 39.8 ms: 1.07x faster                                                        |
| crypto_pyaes                     | 33.6 ms                                                        | 31.6 ms: 1.06x faster                                                        |
| connected_components             | 208 ms                                                         | 196 ms: 1.06x faster                                                         |
| pathlib                          | 11.1 ms                                                        | 10.5 ms: 1.06x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 212 ms: 1.06x faster                                                         |
| pycparser                        | 470 ms                                                         | 444 ms: 1.06x faster                                                         |
| sphinx                           | 409 ms                                                         | 386 ms: 1.06x faster                                                         |
| async_generators                 | 193 ms                                                         | 183 ms: 1.06x faster                                                         |
| json                             | 1.94 ms                                                        | 1.84 ms: 1.06x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 184 ms: 1.05x faster                                                         |
| pidigits                         | 166 ms                                                         | 159 ms: 1.04x faster                                                         |
| shortest_path                    | 225 ms                                                         | 216 ms: 1.04x faster                                                         |
| typing_runtime_protocols         | 64.6 us                                                        | 62.2 us: 1.04x faster                                                        |
| pickle_pure_python               | 130 us                                                         | 126 us: 1.03x faster                                                         |
| gc_traversal                     | 2.04 ms                                                        | 1.99 ms: 1.03x faster                                                        |
| json_loads                       | 10.8 us                                                        | 10.6 us: 1.03x faster                                                        |
| thrift                           | 309 us                                                         | 303 us: 1.02x faster                                                         |
| regex_dna                        | 94.6 ms                                                        | 93.2 ms: 1.02x faster                                                        |
| 2to3                             | 112 ms                                                         | 111 ms: 1.01x faster                                                         |
| dask                             | 525 ms                                                         | 521 ms: 1.01x faster                                                         |
| django_template                  | 12.5 ms                                                        | 12.4 ms: 1.01x faster                                                        |
| python_startup                   | 8.63 ms                                                        | 8.68 ms: 1.01x slower                                                        |
| sympy_integrate                  | 7.53 ms                                                        | 7.60 ms: 1.01x slower                                                        |
| raytrace                         | 109 ms                                                         | 111 ms: 1.02x slower                                                         |
| xml_etree_parse                  | 62.4 ms                                                        | 64.2 ms: 1.03x slower                                                        |
| sympy_sum                        | 52.3 ms                                                        | 54.2 ms: 1.04x slower                                                        |
| sympy_expand                     | 159 ms                                                         | 166 ms: 1.04x slower                                                         |
| sympy_str                        | 95.5 ms                                                        | 99.5 ms: 1.04x slower                                                        |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.86 ms: 1.05x slower                                                        |
| python_startup_no_site           | 5.95 ms                                                        | 6.24 ms: 1.05x slower                                                        |
| bench_thread_pool                | 412 us                                                         | 433 us: 1.05x slower                                                         |
| coverage                         | 31.2 ms                                                        | 32.8 ms: 1.05x slower                                                        |
| pylint                           | 106 ms                                                         | 116 ms: 1.10x slower                                                         |
| many_optionals                   | 200 us                                                         | 224 us: 1.12x slower                                                         |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 234 ms: 1.12x slower                                                         |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 115 ms: 1.13x slower                                                         |
| bench_mp_pool                    | 37.8 ms                                                        | 44.0 ms: 1.16x slower                                                        |
| generators                       | 15.7 ms                                                        | 18.3 ms: 1.17x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 76.7 ms: 2.65x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.19x faster                                                                 |

Benchmark hidden because not significant (1): sqlite_synth
Ignored benchmarks (12) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260315-3.15.0a7+-2e9b980-JIT/bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.195x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.11x
- 95% likely to have a speedup of 1.10x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.23x