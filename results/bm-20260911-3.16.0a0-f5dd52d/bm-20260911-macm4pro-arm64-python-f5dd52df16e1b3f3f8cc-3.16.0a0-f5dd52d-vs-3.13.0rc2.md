# Results vs. 3.13.0rc2

- fork: python
- ref: f5dd52df16e1b3f3f8cc
- machine: darwin-arm64
- commit hash: f5dd52d
- commit date: 2026-09-11
- overall geometric mean: 1.053x faster
- HPT reliability: 99.67%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 117 ms: 1.05x slower                                                    |
| docutils       | 1.05 sec                                                       | 948 ms: 1.10x faster                                                    |
| html5lib       | 23.1 ms                                                        | 21.1 ms: 1.10x faster                                                   |
| sphinx         | 409 ms                                                         | 397 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 332 ms: 1.57x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 336 ms: 1.56x faster                                                    |
| async_generators                 | 193 ms                                                         | 144 ms: 1.34x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 327 ms: 1.24x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 340 ms: 1.14x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.63 ms: 1.12x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 173 ms: 1.08x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 125 ms: 1.06x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 136 ms: 1.05x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 290 ms: 1.04x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 283 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 133 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 247 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 263 ms: 1.26x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 153 ms: 1.49x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 64.6 ms: 1.50x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 103 ms: 3.56x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x slower                                                            |

Benchmark hidden because not significant (1): async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.9 ms: 1.09x faster                                                   |
| pidigits       | 166 ms                                                         | 166 ms: 1.00x faster                                                    |
| nbody          | 42.5 ms                                                        | 45.6 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.33 ms: 1.21x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.28 ms: 1.15x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 91.9 ms: 1.03x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 53.4 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                          | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.53 ms: 1.32x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 789 ms: 1.27x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 42.3 ms: 1.09x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 95.3 us: 1.04x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.0 ms: 1.01x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 66.1 ms: 1.06x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 140 us: 1.07x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.06x faster                                                            |

Benchmark hidden because not significant (2): xml_etree_generate, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.21 ms: 1.07x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.70 ms: 1.13x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.10x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.55 ms: 1.03x slower                                                   |
| django_template | 12.5 ms                                                        | 14.9 ms: 1.20x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.11x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 510 ms: 2.07x faster                                                    |
| pylint                           | 106 ms                                                         | 56.6 ms: 1.87x faster                                                   |
| async_tree_eager_io_tg           | 521 ms                                                         | 332 ms: 1.57x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 336 ms: 1.56x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.08 ms: 1.54x faster                                                   |
| deepcopy                         | 145 us                                                         | 97.0 us: 1.50x faster                                                   |
| k_core                           | 1.46 sec                                                       | 978 ms: 1.50x faster                                                    |
| go                               | 72.6 ms                                                        | 52.2 ms: 1.39x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 11.9 us: 1.39x faster                                                   |
| async_generators                 | 193 ms                                                         | 144 ms: 1.34x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 49.0 us: 1.32x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.53 ms: 1.32x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 49.6 ms: 1.29x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 789 ms: 1.27x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 327 ms: 1.24x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.07 us: 1.22x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.33 ms: 1.21x faster                                                   |
| pyflate                          | 222 ms                                                         | 184 ms: 1.21x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 823 us: 1.21x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.28 ms: 1.15x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 340 ms: 1.14x faster                                                    |
| fannkuch                         | 179 ms                                                         | 159 ms: 1.13x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.63 ms: 1.12x faster                                                   |
| docutils                         | 1.05 sec                                                       | 948 ms: 1.10x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.0 ms: 1.10x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.94 sec: 1.10x faster                                                  |
| html5lib                         | 23.1 ms                                                        | 21.1 ms: 1.10x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 42.3 ms: 1.09x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.5 ms: 1.09x faster                                                   |
| float                            | 31.4 ms                                                        | 28.9 ms: 1.09x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.3 ms: 1.08x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 22.9 ms: 1.08x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.64 ms: 1.08x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 173 ms: 1.08x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 300 ms: 1.07x faster                                                    |
| nqueens                          | 37.2 ms                                                        | 34.8 ms: 1.07x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 125 ms: 1.06x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 117 ms: 1.06x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 615 ms: 1.06x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.91 ms: 1.05x faster                                                   |
| gc_traversal                     | 2.04 ms                                                        | 1.94 ms: 1.05x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 136 ms: 1.05x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 95.3 us: 1.04x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 290 ms: 1.04x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.15 us: 1.04x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 283 ms: 1.04x faster                                                    |
| comprehensions                   | 6.80 us                                                        | 6.56 us: 1.04x faster                                                   |
| spectral_norm                    | 43.7 ms                                                        | 42.2 ms: 1.04x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                   |
| logging_format                   | 2.45 us                                                        | 2.37 us: 1.03x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 91.9 ms: 1.03x faster                                                   |
| sphinx                           | 409 ms                                                         | 397 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                    |
| json                             | 1.94 ms                                                        | 1.90 ms: 1.02x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 926 ns: 1.02x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.39 ms: 1.02x faster                                                   |
| connected_components             | 208 ms                                                         | 205 ms: 1.02x faster                                                    |
| shortest_path                    | 225 ms                                                         | 222 ms: 1.01x faster                                                    |
| bench_thread_pool                | 412 us                                                         | 406 us: 1.01x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 25.0 ms: 1.01x faster                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.77 ms: 1.01x faster                                                   |
| pidigits                         | 166 ms                                                         | 166 ms: 1.00x faster                                                    |
| deltablue                        | 1.45 ms                                                        | 1.47 ms: 1.01x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 48.6 ms: 1.01x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.55 ms: 1.03x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 98.5 ms: 1.03x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 42.1 ns: 1.04x slower                                                   |
| chaos                            | 24.3 ms                                                        | 25.2 ms: 1.04x slower                                                   |
| pycparser                        | 470 ms                                                         | 491 ms: 1.04x slower                                                    |
| 2to3                             | 112 ms                                                         | 117 ms: 1.05x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 168 ms: 1.05x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.1 ms: 1.05x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 66.1 ms: 1.06x slower                                                   |
| raytrace                         | 109 ms                                                         | 116 ms: 1.06x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.21 ms: 1.07x slower                                                   |
| nbody                            | 42.5 ms                                                        | 45.6 ms: 1.07x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 140 us: 1.07x slower                                                    |
| generators                       | 15.7 ms                                                        | 17.0 ms: 1.08x slower                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 133 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 247 ms: 1.10x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.3 ms: 1.11x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 53.4 ms: 1.12x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.70 ms: 1.13x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 48.6 ms: 1.14x slower                                                   |
| many_optionals                   | 200 us                                                         | 239 us: 1.19x slower                                                    |
| django_template                  | 12.5 ms                                                        | 14.9 ms: 1.20x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 46.8 ms: 1.24x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 263 ms: 1.26x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 153 ms: 1.49x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 64.6 ms: 1.50x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 103 ms: 3.56x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.05x faster                                                            |

Benchmark hidden because not significant (4): async_tree_memoization, xml_etree_generate, json_loads, thrift
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260911-3.16.0a0-f5dd52d/bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.053x faster

# HPT report

- Reliability score: 99.67% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.18x