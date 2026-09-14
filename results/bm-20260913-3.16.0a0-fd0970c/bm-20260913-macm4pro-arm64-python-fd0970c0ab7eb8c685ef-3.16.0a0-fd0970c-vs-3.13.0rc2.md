# Results vs. 3.13.0rc2

- fork: python
- ref: fd0970c0ab7eb8c685ef
- machine: darwin-arm64
- commit hash: fd0970c
- commit date: 2026-09-13
- overall geometric mean: 1.051x faster
- HPT reliability: 99.37%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260913-macm4pro-arm64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 119 ms: 1.07x slower                                                    |
| docutils       | 1.05 sec                                                       | 945 ms: 1.11x faster                                                    |
| html5lib       | 23.1 ms                                                        | 21.4 ms: 1.08x faster                                                   |
| sphinx         | 409 ms                                                         | 399 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260913-macm4pro-arm64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 335 ms: 1.56x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 340 ms: 1.55x faster                                                    |
| async_generators                 | 193 ms                                                         | 145 ms: 1.33x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 328 ms: 1.24x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.35 ms: 1.15x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 341 ms: 1.13x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 173 ms: 1.07x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 125 ms: 1.06x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 137 ms: 1.04x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 293 ms: 1.03x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 286 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 135 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 250 ms: 1.11x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 266 ms: 1.28x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 154 ms: 1.51x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 65.2 ms: 1.51x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 103 ms: 3.58x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x slower                                                            |

Benchmark hidden because not significant (1): async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260913-macm4pro-arm64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.6 ms: 1.10x faster                                                   |
| pidigits       | 166 ms                                                         | 168 ms: 1.01x slower                                                    |
| nbody          | 42.5 ms                                                        | 43.9 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260913-macm4pro-arm64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.32 ms: 1.22x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.34 ms: 1.15x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 92.4 ms: 1.02x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 53.6 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                          | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260913-macm4pro-arm64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.54 ms: 1.31x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 794 ms: 1.26x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 43.7 ms: 1.05x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 94.4 us: 1.05x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.1 ms: 1.01x faster                                                   |
| pickle_pure_python   | 130 us                                                         | 140 us: 1.07x slower                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 68.3 ms: 1.10x slower                                                   |
| Geometric mean       | (ref)                                                          | 1.05x faster                                                            |

Benchmark hidden because not significant (2): xml_etree_generate, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260913-macm4pro-arm64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.29 ms: 1.08x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.76 ms: 1.14x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.11x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260913-macm4pro-arm64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.55 ms: 1.03x slower                                                   |
| django_template | 12.5 ms                                                        | 14.9 ms: 1.20x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.11x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260913-macm4pro-arm64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 509 ms: 2.08x faster                                                    |
| pylint                           | 106 ms                                                         | 56.7 ms: 1.86x faster                                                   |
| async_tree_eager_io_tg           | 521 ms                                                         | 335 ms: 1.56x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 340 ms: 1.55x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.09 ms: 1.53x faster                                                   |
| deepcopy                         | 145 us                                                         | 96.6 us: 1.50x faster                                                   |
| k_core                           | 1.46 sec                                                       | 983 ms: 1.49x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.7 us: 1.41x faster                                                   |
| go                               | 72.6 ms                                                        | 52.2 ms: 1.39x faster                                                   |
| async_generators                 | 193 ms                                                         | 145 ms: 1.33x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 49.0 us: 1.32x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.54 ms: 1.31x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 48.8 ms: 1.31x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 794 ms: 1.26x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.03 us: 1.25x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 328 ms: 1.24x faster                                                    |
| pyflate                          | 222 ms                                                         | 181 ms: 1.23x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.32 ms: 1.22x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 819 us: 1.21x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.35 ms: 1.15x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.34 ms: 1.15x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 341 ms: 1.13x faster                                                    |
| fannkuch                         | 179 ms                                                         | 161 ms: 1.11x faster                                                    |
| docutils                         | 1.05 sec                                                       | 945 ms: 1.11x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.0 ms: 1.10x faster                                                   |
| float                            | 31.4 ms                                                        | 28.6 ms: 1.10x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                  |
| richards_super                   | 24.7 ms                                                        | 22.8 ms: 1.08x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.3 ms: 1.08x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.6 ms: 1.08x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 21.4 ms: 1.08x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.64 ms: 1.08x faster                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 298 ms: 1.08x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 115 ms: 1.08x faster                                                    |
| nqueens                          | 37.2 ms                                                        | 34.6 ms: 1.08x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.85 ms: 1.07x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 173 ms: 1.07x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 613 ms: 1.06x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 125 ms: 1.06x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.7 ms: 1.05x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 94.4 us: 1.05x faster                                                   |
| gc_traversal                     | 2.04 ms                                                        | 1.96 ms: 1.04x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 137 ms: 1.04x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.15 us: 1.04x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                   |
| logging_format                   | 2.45 us                                                        | 2.36 us: 1.04x faster                                                   |
| comprehensions                   | 6.80 us                                                        | 6.60 us: 1.03x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 293 ms: 1.03x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 286 ms: 1.03x faster                                                    |
| sphinx                           | 409 ms                                                         | 399 ms: 1.03x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 92.4 ms: 1.02x faster                                                   |
| spectral_norm                    | 43.7 ms                                                        | 42.8 ms: 1.02x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 928 ns: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| json                             | 1.94 ms                                                        | 1.91 ms: 1.02x faster                                                   |
| connected_components             | 208 ms                                                         | 205 ms: 1.01x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.43 ms: 1.01x faster                                                   |
| shortest_path                    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 25.1 ms: 1.01x faster                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.77 ms: 1.01x faster                                                   |
| deltablue                        | 1.45 ms                                                        | 1.45 ms: 1.00x faster                                                   |
| thrift                           | 309 us                                                         | 312 us: 1.01x slower                                                    |
| pidigits                         | 166 ms                                                         | 168 ms: 1.01x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 418 us: 1.01x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 48.8 ms: 1.02x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.55 ms: 1.03x slower                                                   |
| nbody                            | 42.5 ms                                                        | 43.9 ms: 1.03x slower                                                   |
| chaos                            | 24.3 ms                                                        | 25.1 ms: 1.03x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 98.9 ms: 1.04x slower                                                   |
| pycparser                        | 470 ms                                                         | 490 ms: 1.04x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 168 ms: 1.05x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.2 ms: 1.05x slower                                                   |
| raytrace                         | 109 ms                                                         | 115 ms: 1.06x slower                                                    |
| 2to3                             | 112 ms                                                         | 119 ms: 1.07x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 140 us: 1.07x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.29 ms: 1.08x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.1 ms: 1.09x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 68.3 ms: 1.10x slower                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 135 ms: 1.10x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.1 ms: 1.10x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 250 ms: 1.11x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 53.6 ms: 1.12x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 48.5 ms: 1.13x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.76 ms: 1.14x slower                                                   |
| django_template                  | 12.5 ms                                                        | 14.9 ms: 1.20x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 45.7 ms: 1.21x slower                                                   |
| many_optionals                   | 200 us                                                         | 244 us: 1.22x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 266 ms: 1.28x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 154 ms: 1.51x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 65.2 ms: 1.51x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 103 ms: 3.58x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.05x faster                                                            |

Benchmark hidden because not significant (4): async_tree_memoization, logging_silent, xml_etree_generate, json_loads
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260913-3.16.0a0-fd0970c/bm-20260913-macm4pro-arm64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.051x faster

# HPT report

- Reliability score: 99.37% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.17x