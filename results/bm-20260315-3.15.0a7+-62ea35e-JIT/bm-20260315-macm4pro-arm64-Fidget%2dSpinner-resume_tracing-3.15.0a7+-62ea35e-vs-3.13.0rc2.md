# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: darwin-arm64
- commit hash: 62ea35e
- commit date: 2026-03-15
- overall geometric mean: 1.206x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 110 ms: 1.01x faster                                                         |
| docutils       | 1.05 sec                                                       | 953 ms: 1.10x faster                                                         |
| html5lib       | 23.1 ms                                                        | 18.7 ms: 1.24x faster                                                        |
| sphinx         | 409 ms                                                         | 383 ms: 1.07x faster                                                         |
| Geometric mean | (ref)                                                          | 1.10x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 202 ms: 2.58x faster                                                         |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.57x faster                                                         |
| async_tree_io_tg                 | 405 ms                                                         | 207 ms: 1.96x faster                                                         |
| async_tree_io                    | 386 ms                                                         | 204 ms: 1.89x faster                                                         |
| async_tree_none                  | 142 ms                                                         | 87.9 ms: 1.62x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 89.0 ms: 1.49x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 126 ms: 1.47x faster                                                         |
| async_tree_memoization_tg        | 186 ms                                                         | 127 ms: 1.47x faster                                                         |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 236 ms: 1.28x faster                                                         |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 235 ms: 1.25x faster                                                         |
| async_tree_eager                 | 43.2 ms                                                        | 35.9 ms: 1.20x faster                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 102 ms: 1.19x faster                                                         |
| coroutines                       | 10.8 ms                                                        | 9.20 ms: 1.17x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 210 ms: 1.07x faster                                                         |
| async_generators                 | 193 ms                                                         | 181 ms: 1.07x faster                                                         |
| asyncio_websockets               | 194 ms                                                         | 183 ms: 1.06x faster                                                         |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 232 ms: 1.11x slower                                                         |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 116 ms: 1.13x slower                                                         |
| async_tree_eager_tg              | 28.9 ms                                                        | 76.7 ms: 2.65x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.29x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 23.3 ms: 1.35x faster                                                        |
| nbody          | 42.5 ms                                                        | 39.9 ms: 1.06x faster                                                        |
| pidigits       | 166 ms                                                         | 157 ms: 1.05x faster                                                         |
| Geometric mean | (ref)                                                          | 1.15x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 39.2 ms: 1.22x faster                                                        |
| regex_v8       | 10.7 ms                                                        | 9.54 ms: 1.12x faster                                                        |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                        |
| regex_dna      | 94.6 ms                                                        | 92.7 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                          | 1.11x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 617 ms: 1.62x faster                                                         |
| json_dumps           | 4.65 ms                                                        | 3.48 ms: 1.34x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 37.6 ms: 1.23x faster                                                        |
| xml_etree_process    | 25.4 ms                                                        | 21.2 ms: 1.20x faster                                                        |
| unpickle_pure_python | 99.5 us                                                        | 83.9 us: 1.19x faster                                                        |
| xml_etree_generate   | 35.8 ms                                                        | 31.7 ms: 1.13x faster                                                        |
| json_loads           | 10.8 us                                                        | 10.2 us: 1.06x faster                                                        |
| pickle_pure_python   | 130 us                                                         | 124 us: 1.05x faster                                                         |
| Geometric mean       | (ref)                                                          | 1.19x faster                                                                 |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.64 ms: 1.00x slower                                                        |
| python_startup_no_site | 5.95 ms                                                        | 6.22 ms: 1.04x slower                                                        |
| Geometric mean         | (ref)                                                          | 1.02x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|-----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 3.97 ms: 1.11x faster                                                        |
| django_template | 12.5 ms                                                        | 12.3 ms: 1.01x faster                                                        |
| Geometric mean  | (ref)                                                          | 1.06x faster                                                                 |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 202 ms: 2.58x faster                                                         |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.57x faster                                                         |
| richards                         | 22.1 ms                                                        | 9.66 ms: 2.28x faster                                                        |
| richards_super                   | 24.7 ms                                                        | 11.4 ms: 2.17x faster                                                        |
| mdp                              | 1.06 sec                                                       | 520 ms: 2.03x faster                                                         |
| async_tree_io_tg                 | 405 ms                                                         | 207 ms: 1.96x faster                                                         |
| async_tree_io                    | 386 ms                                                         | 204 ms: 1.89x faster                                                         |
| subparsers                       | 6.26 ms                                                        | 3.46 ms: 1.81x faster                                                        |
| scimark_sor                      | 64.0 ms                                                        | 36.6 ms: 1.75x faster                                                        |
| k_core                           | 1.46 sec                                                       | 854 ms: 1.71x faster                                                         |
| deepcopy_memo                    | 16.5 us                                                        | 9.98 us: 1.65x faster                                                        |
| tomli_loads                      | 1000 ms                                                        | 617 ms: 1.62x faster                                                         |
| async_tree_none                  | 142 ms                                                         | 87.9 ms: 1.62x faster                                                        |
| go                               | 72.6 ms                                                        | 45.4 ms: 1.60x faster                                                        |
| deepcopy                         | 145 us                                                         | 92.4 us: 1.57x faster                                                        |
| pyflate                          | 222 ms                                                         | 144 ms: 1.54x faster                                                         |
| scimark_lu                       | 42.8 ms                                                        | 28.6 ms: 1.50x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 89.0 ms: 1.49x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 126 ms: 1.47x faster                                                         |
| async_tree_memoization_tg        | 186 ms                                                         | 127 ms: 1.47x faster                                                         |
| float                            | 31.4 ms                                                        | 23.3 ms: 1.35x faster                                                        |
| json_dumps                       | 4.65 ms                                                        | 3.48 ms: 1.34x faster                                                        |
| scimark_monte_carlo              | 29.9 ms                                                        | 22.7 ms: 1.32x faster                                                        |
| deltablue                        | 1.45 ms                                                        | 1.11 ms: 1.31x faster                                                        |
| deepcopy_reduce                  | 1.30 us                                                        | 998 ns: 1.30x faster                                                         |
| pprint_safe_repr                 | 322 ms                                                         | 249 ms: 1.29x faster                                                         |
| logging_format                   | 2.45 us                                                        | 1.90 us: 1.28x faster                                                        |
| pprint_pformat                   | 650 ms                                                         | 507 ms: 1.28x faster                                                         |
| logging_simple                   | 2.24 us                                                        | 1.74 us: 1.28x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 236 ms: 1.28x faster                                                         |
| scimark_fft                      | 124 ms                                                         | 98.4 ms: 1.26x faster                                                        |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 235 ms: 1.25x faster                                                         |
| html5lib                         | 23.1 ms                                                        | 18.7 ms: 1.24x faster                                                        |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.6 ms: 1.23x faster                                                        |
| regex_compile                    | 47.9 ms                                                        | 39.2 ms: 1.22x faster                                                        |
| fannkuch                         | 179 ms                                                         | 148 ms: 1.20x faster                                                         |
| async_tree_eager                 | 43.2 ms                                                        | 35.9 ms: 1.20x faster                                                        |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.77 sec: 1.20x faster                                                       |
| xml_etree_process                | 25.4 ms                                                        | 21.2 ms: 1.20x faster                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 102 ms: 1.19x faster                                                         |
| unpickle_pure_python             | 99.5 us                                                        | 83.9 us: 1.19x faster                                                        |
| hexiom                           | 2.85 ms                                                        | 2.40 ms: 1.19x faster                                                        |
| telco                            | 3.07 ms                                                        | 2.60 ms: 1.18x faster                                                        |
| chaos                            | 24.3 ms                                                        | 20.7 ms: 1.17x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 9.20 ms: 1.17x faster                                                        |
| comprehensions                   | 6.80 us                                                        | 5.82 us: 1.17x faster                                                        |
| logging_silent                   | 40.6 ns                                                        | 35.0 ns: 1.16x faster                                                        |
| nqueens                          | 37.2 ms                                                        | 32.1 ms: 1.16x faster                                                        |
| spectral_norm                    | 43.7 ms                                                        | 37.8 ms: 1.16x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 878 us: 1.13x faster                                                         |
| xml_etree_generate               | 35.8 ms                                                        | 31.7 ms: 1.13x faster                                                        |
| dulwich_log                      | 19.8 ms                                                        | 17.6 ms: 1.13x faster                                                        |
| regex_v8                         | 10.7 ms                                                        | 9.54 ms: 1.12x faster                                                        |
| mako                             | 4.41 ms                                                        | 3.97 ms: 1.11x faster                                                        |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                        |
| docutils                         | 1.05 sec                                                       | 953 ms: 1.10x faster                                                         |
| meteor_contest                   | 47.9 ms                                                        | 44.2 ms: 1.08x faster                                                        |
| json                             | 1.94 ms                                                        | 1.80 ms: 1.08x faster                                                        |
| crypto_pyaes                     | 33.6 ms                                                        | 31.3 ms: 1.07x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 210 ms: 1.07x faster                                                         |
| async_generators                 | 193 ms                                                         | 181 ms: 1.07x faster                                                         |
| sphinx                           | 409 ms                                                         | 383 ms: 1.07x faster                                                         |
| pycparser                        | 470 ms                                                         | 440 ms: 1.07x faster                                                         |
| connected_components             | 208 ms                                                         | 195 ms: 1.06x faster                                                         |
| nbody                            | 42.5 ms                                                        | 39.9 ms: 1.06x faster                                                        |
| pathlib                          | 11.1 ms                                                        | 10.5 ms: 1.06x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 183 ms: 1.06x faster                                                         |
| json_loads                       | 10.8 us                                                        | 10.2 us: 1.06x faster                                                        |
| pidigits                         | 166 ms                                                         | 157 ms: 1.05x faster                                                         |
| pickle_pure_python               | 130 us                                                         | 124 us: 1.05x faster                                                         |
| shortest_path                    | 225 ms                                                         | 215 ms: 1.05x faster                                                         |
| typing_runtime_protocols         | 64.6 us                                                        | 62.1 us: 1.04x faster                                                        |
| thrift                           | 309 us                                                         | 298 us: 1.04x faster                                                         |
| gc_traversal                     | 2.04 ms                                                        | 1.98 ms: 1.03x faster                                                        |
| regex_dna                        | 94.6 ms                                                        | 92.7 ms: 1.02x faster                                                        |
| sqlite_synth                     | 948 ns                                                         | 933 ns: 1.02x faster                                                         |
| 2to3                             | 112 ms                                                         | 110 ms: 1.01x faster                                                         |
| django_template                  | 12.5 ms                                                        | 12.3 ms: 1.01x faster                                                        |
| dask                             | 525 ms                                                         | 521 ms: 1.01x faster                                                         |
| sympy_integrate                  | 7.53 ms                                                        | 7.47 ms: 1.01x faster                                                        |
| python_startup                   | 8.63 ms                                                        | 8.64 ms: 1.00x slower                                                        |
| raytrace                         | 109 ms                                                         | 110 ms: 1.01x slower                                                         |
| sympy_expand                     | 159 ms                                                         | 162 ms: 1.02x slower                                                         |
| sympy_sum                        | 52.3 ms                                                        | 53.4 ms: 1.02x slower                                                        |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.83 ms: 1.03x slower                                                        |
| sympy_str                        | 95.5 ms                                                        | 99.4 ms: 1.04x slower                                                        |
| coverage                         | 31.2 ms                                                        | 32.5 ms: 1.04x slower                                                        |
| python_startup_no_site           | 5.95 ms                                                        | 6.22 ms: 1.04x slower                                                        |
| bench_thread_pool                | 412 us                                                         | 433 us: 1.05x slower                                                         |
| pylint                           | 106 ms                                                         | 116 ms: 1.10x slower                                                         |
| many_optionals                   | 200 us                                                         | 222 us: 1.11x slower                                                         |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 232 ms: 1.11x slower                                                         |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 116 ms: 1.13x slower                                                         |
| bench_mp_pool                    | 37.8 ms                                                        | 43.8 ms: 1.16x slower                                                        |
| generators                       | 15.7 ms                                                        | 18.2 ms: 1.16x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 76.7 ms: 2.65x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.20x faster                                                                 |

Benchmark hidden because not significant (1): xml_etree_parse
Ignored benchmarks (12) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260315-3.15.0a7+-62ea35e-JIT/bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.206x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.12x
- 95% likely to have a speedup of 1.11x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: 1.23x