# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: darwin-arm64
- commit hash: af09d44
- commit date: 2026-03-13
- overall geometric mean: 1.193x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260313-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-af09d44 |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 111 ms: 1.01x faster                                                         |
| docutils       | 1.05 sec                                                       | 963 ms: 1.09x faster                                                         |
| html5lib       | 23.1 ms                                                        | 19.2 ms: 1.21x faster                                                        |
| sphinx         | 409 ms                                                         | 388 ms: 1.05x faster                                                         |
| Geometric mean | (ref)                                                          | 1.09x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260313-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-af09d44 |
|----------------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 203 ms: 2.56x faster                                                         |
| async_tree_eager_io              | 525 ms                                                         | 205 ms: 2.56x faster                                                         |
| async_tree_io_tg                 | 405 ms                                                         | 208 ms: 1.94x faster                                                         |
| async_tree_io                    | 386 ms                                                         | 207 ms: 1.86x faster                                                         |
| async_tree_none                  | 142 ms                                                         | 89.5 ms: 1.59x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 90.9 ms: 1.46x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 127 ms: 1.45x faster                                                         |
| async_tree_memoization_tg        | 186 ms                                                         | 129 ms: 1.44x faster                                                         |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 241 ms: 1.25x faster                                                         |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 240 ms: 1.23x faster                                                         |
| async_tree_eager_memoization     | 122 ms                                                         | 101 ms: 1.21x faster                                                         |
| async_tree_eager                 | 43.2 ms                                                        | 36.3 ms: 1.19x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 9.15 ms: 1.18x faster                                                        |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                         |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 212 ms: 1.06x faster                                                         |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.04x faster                                                         |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 116 ms: 1.13x slower                                                         |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 235 ms: 1.13x slower                                                         |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.2 ms: 2.67x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.28x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260313-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-af09d44 |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 23.6 ms: 1.33x faster                                                        |
| nbody          | 42.5 ms                                                        | 40.1 ms: 1.06x faster                                                        |
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                         |
| Geometric mean | (ref)                                                          | 1.13x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260313-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-af09d44 |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 39.5 ms: 1.21x faster                                                        |
| regex_v8       | 10.7 ms                                                        | 9.57 ms: 1.12x faster                                                        |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                        |
| Geometric mean | (ref)                                                          | 1.11x faster                                                                 |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260313-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-af09d44 |
|----------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 630 ms: 1.59x faster                                                         |
| json_dumps           | 4.65 ms                                                        | 3.51 ms: 1.33x faster                                                        |
| xml_etree_process    | 25.4 ms                                                        | 21.3 ms: 1.19x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.0 ms: 1.18x faster                                                        |
| unpickle_pure_python | 99.5 us                                                        | 84.2 us: 1.18x faster                                                        |
| xml_etree_generate   | 35.8 ms                                                        | 31.5 ms: 1.14x faster                                                        |
| json_loads           | 10.8 us                                                        | 10.4 us: 1.04x faster                                                        |
| pickle_pure_python   | 130 us                                                         | 125 us: 1.04x faster                                                         |
| xml_etree_parse      | 62.4 ms                                                        | 63.0 ms: 1.01x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.17x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260313-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-af09d44 |
|------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.71 ms: 1.01x slower                                                        |
| python_startup_no_site | 5.95 ms                                                        | 6.26 ms: 1.05x slower                                                        |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260313-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-af09d44 |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako           | 4.41 ms                                                        | 3.97 ms: 1.11x faster                                                        |
| Geometric mean | (ref)                                                          | 1.06x faster                                                                 |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260313-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-af09d44 |
|----------------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 203 ms: 2.56x faster                                                         |
| async_tree_eager_io              | 525 ms                                                         | 205 ms: 2.56x faster                                                         |
| richards                         | 22.1 ms                                                        | 9.83 ms: 2.24x faster                                                        |
| richards_super                   | 24.7 ms                                                        | 11.5 ms: 2.14x faster                                                        |
| mdp                              | 1.06 sec                                                       | 511 ms: 2.07x faster                                                         |
| async_tree_io_tg                 | 405 ms                                                         | 208 ms: 1.94x faster                                                         |
| async_tree_io                    | 386 ms                                                         | 207 ms: 1.86x faster                                                         |
| subparsers                       | 6.26 ms                                                        | 3.52 ms: 1.78x faster                                                        |
| scimark_sor                      | 64.0 ms                                                        | 37.1 ms: 1.72x faster                                                        |
| k_core                           | 1.46 sec                                                       | 857 ms: 1.71x faster                                                         |
| deepcopy_memo                    | 16.5 us                                                        | 10.0 us: 1.64x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 89.5 ms: 1.59x faster                                                        |
| tomli_loads                      | 1000 ms                                                        | 630 ms: 1.59x faster                                                         |
| go                               | 72.6 ms                                                        | 46.3 ms: 1.57x faster                                                        |
| deepcopy                         | 145 us                                                         | 93.4 us: 1.55x faster                                                        |
| scimark_lu                       | 42.8 ms                                                        | 28.2 ms: 1.52x faster                                                        |
| pyflate                          | 222 ms                                                         | 147 ms: 1.51x faster                                                         |
| async_tree_none_tg               | 133 ms                                                         | 90.9 ms: 1.46x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 127 ms: 1.45x faster                                                         |
| async_tree_memoization_tg        | 186 ms                                                         | 129 ms: 1.44x faster                                                         |
| float                            | 31.4 ms                                                        | 23.6 ms: 1.33x faster                                                        |
| json_dumps                       | 4.65 ms                                                        | 3.51 ms: 1.33x faster                                                        |
| scimark_monte_carlo              | 29.9 ms                                                        | 22.7 ms: 1.32x faster                                                        |
| deltablue                        | 1.45 ms                                                        | 1.11 ms: 1.31x faster                                                        |
| deepcopy_reduce                  | 1.30 us                                                        | 994 ns: 1.30x faster                                                         |
| logging_format                   | 2.45 us                                                        | 1.90 us: 1.29x faster                                                        |
| pprint_safe_repr                 | 322 ms                                                         | 251 ms: 1.28x faster                                                         |
| pprint_pformat                   | 650 ms                                                         | 509 ms: 1.28x faster                                                         |
| scimark_fft                      | 124 ms                                                         | 97.0 ms: 1.27x faster                                                        |
| logging_simple                   | 2.24 us                                                        | 1.76 us: 1.27x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 241 ms: 1.25x faster                                                         |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 240 ms: 1.23x faster                                                         |
| regex_compile                    | 47.9 ms                                                        | 39.5 ms: 1.21x faster                                                        |
| html5lib                         | 23.1 ms                                                        | 19.2 ms: 1.21x faster                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 101 ms: 1.21x faster                                                         |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.77 sec: 1.20x faster                                                       |
| telco                            | 3.07 ms                                                        | 2.56 ms: 1.20x faster                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 36.3 ms: 1.19x faster                                                        |
| hexiom                           | 2.85 ms                                                        | 2.39 ms: 1.19x faster                                                        |
| xml_etree_process                | 25.4 ms                                                        | 21.3 ms: 1.19x faster                                                        |
| fannkuch                         | 179 ms                                                         | 151 ms: 1.18x faster                                                         |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.0 ms: 1.18x faster                                                        |
| unpickle_pure_python             | 99.5 us                                                        | 84.2 us: 1.18x faster                                                        |
| logging_silent                   | 40.6 ns                                                        | 34.4 ns: 1.18x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 9.15 ms: 1.18x faster                                                        |
| spectral_norm                    | 43.7 ms                                                        | 37.7 ms: 1.16x faster                                                        |
| nqueens                          | 37.2 ms                                                        | 32.4 ms: 1.15x faster                                                        |
| chaos                            | 24.3 ms                                                        | 21.3 ms: 1.14x faster                                                        |
| xml_etree_generate               | 35.8 ms                                                        | 31.5 ms: 1.14x faster                                                        |
| regex_v8                         | 10.7 ms                                                        | 9.57 ms: 1.12x faster                                                        |
| mako                             | 4.41 ms                                                        | 3.97 ms: 1.11x faster                                                        |
| dulwich_log                      | 19.8 ms                                                        | 17.9 ms: 1.11x faster                                                        |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 904 us: 1.10x faster                                                         |
| docutils                         | 1.05 sec                                                       | 963 ms: 1.09x faster                                                         |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                         |
| json                             | 1.94 ms                                                        | 1.82 ms: 1.07x faster                                                        |
| pycparser                        | 470 ms                                                         | 442 ms: 1.06x faster                                                         |
| connected_components             | 208 ms                                                         | 196 ms: 1.06x faster                                                         |
| nbody                            | 42.5 ms                                                        | 40.1 ms: 1.06x faster                                                        |
| crypto_pyaes                     | 33.6 ms                                                        | 31.7 ms: 1.06x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 212 ms: 1.06x faster                                                         |
| meteor_contest                   | 47.9 ms                                                        | 45.4 ms: 1.05x faster                                                        |
| sphinx                           | 409 ms                                                         | 388 ms: 1.05x faster                                                         |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                        |
| shortest_path                    | 225 ms                                                         | 215 ms: 1.04x faster                                                         |
| json_loads                       | 10.8 us                                                        | 10.4 us: 1.04x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.04x faster                                                         |
| typing_runtime_protocols         | 64.6 us                                                        | 62.1 us: 1.04x faster                                                        |
| pickle_pure_python               | 130 us                                                         | 125 us: 1.04x faster                                                         |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                         |
| thrift                           | 309 us                                                         | 300 us: 1.03x faster                                                         |
| gc_traversal                     | 2.04 ms                                                        | 2.02 ms: 1.01x faster                                                        |
| sqlite_synth                     | 948 ns                                                         | 939 ns: 1.01x faster                                                         |
| 2to3                             | 112 ms                                                         | 111 ms: 1.01x faster                                                         |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                         |
| xml_etree_parse                  | 62.4 ms                                                        | 63.0 ms: 1.01x slower                                                        |
| python_startup                   | 8.63 ms                                                        | 8.71 ms: 1.01x slower                                                        |
| raytrace                         | 109 ms                                                         | 111 ms: 1.01x slower                                                         |
| sympy_integrate                  | 7.53 ms                                                        | 7.66 ms: 1.02x slower                                                        |
| sympy_expand                     | 159 ms                                                         | 164 ms: 1.03x slower                                                         |
| bench_thread_pool                | 412 us                                                         | 429 us: 1.04x slower                                                         |
| coverage                         | 31.2 ms                                                        | 32.7 ms: 1.05x slower                                                        |
| python_startup_no_site           | 5.95 ms                                                        | 6.26 ms: 1.05x slower                                                        |
| sympy_sum                        | 52.3 ms                                                        | 55.6 ms: 1.06x slower                                                        |
| sympy_str                        | 95.5 ms                                                        | 103 ms: 1.08x slower                                                         |
| comprehensions                   | 6.80 us                                                        | 7.33 us: 1.08x slower                                                        |
| pylint                           | 106 ms                                                         | 117 ms: 1.11x slower                                                         |
| generators                       | 15.7 ms                                                        | 17.5 ms: 1.12x slower                                                        |
| many_optionals                   | 200 us                                                         | 225 us: 1.12x slower                                                         |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 116 ms: 1.13x slower                                                         |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 235 ms: 1.13x slower                                                         |
| bench_mp_pool                    | 37.8 ms                                                        | 44.3 ms: 1.17x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.2 ms: 2.67x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.19x faster                                                                 |

Benchmark hidden because not significant (3): regex_dna, django_template, scimark_sparse_mat_mult
Ignored benchmarks (12) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260313-3.15.0a7+-af09d44-JIT/bm-20260313-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-af09d44.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.193x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.11x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: 1.23x