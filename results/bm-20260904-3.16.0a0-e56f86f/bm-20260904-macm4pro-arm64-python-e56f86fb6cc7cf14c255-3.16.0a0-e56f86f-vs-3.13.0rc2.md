# Results vs. 3.13.0rc2

- fork: python
- ref: e56f86fb6cc7cf14c255
- machine: darwin-arm64
- commit hash: e56f86f
- commit date: 2026-09-04
- overall geometric mean: 1.062x faster
- HPT reliability: 99.97%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 118 ms: 1.06x slower                                                    |
| docutils       | 1.05 sec                                                       | 954 ms: 1.10x faster                                                    |
| html5lib       | 23.1 ms                                                        | 21.2 ms: 1.09x faster                                                   |
| sphinx         | 409 ms                                                         | 400 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 306 ms: 1.72x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 331 ms: 1.57x faster                                                    |
| async_generators                 | 193 ms                                                         | 144 ms: 1.34x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 310 ms: 1.25x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 327 ms: 1.24x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 120 ms: 1.19x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.43 ms: 1.14x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 173 ms: 1.08x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.2 ms: 1.07x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 125 ms: 1.06x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 115 ms: 1.06x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 177 ms: 1.04x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 282 ms: 1.04x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 291 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 263 ms: 1.27x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 153 ms: 1.49x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 103 ms: 3.55x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.4 ms: 1.11x faster                                                   |
| pidigits       | 166 ms                                                         | 168 ms: 1.01x slower                                                    |
| nbody          | 42.5 ms                                                        | 43.2 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.32 ms: 1.22x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.33 ms: 1.15x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 92.9 ms: 1.02x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 54.1 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                          | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.54 ms: 1.31x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 796 ms: 1.26x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 42.4 ms: 1.09x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.6 us: 1.02x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 97.8 us: 1.02x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.6 ms: 1.01x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 66.5 ms: 1.06x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 139 us: 1.07x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.06x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.30 ms: 1.08x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.76 ms: 1.14x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.11x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.56 ms: 1.03x slower                                                   |
| django_template | 12.5 ms                                                        | 15.0 ms: 1.20x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.11x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 511 ms: 2.07x faster                                                    |
| pylint                           | 106 ms                                                         | 56.9 ms: 1.86x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 306 ms: 1.72x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 331 ms: 1.57x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.08 ms: 1.54x faster                                                   |
| deepcopy                         | 145 us                                                         | 96.8 us: 1.50x faster                                                   |
| k_core                           | 1.46 sec                                                       | 982 ms: 1.49x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.7 us: 1.40x faster                                                   |
| go                               | 72.6 ms                                                        | 52.1 ms: 1.39x faster                                                   |
| async_generators                 | 193 ms                                                         | 144 ms: 1.34x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.54 ms: 1.31x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 49.3 us: 1.31x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 49.8 ms: 1.29x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 796 ms: 1.26x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 310 ms: 1.25x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.04 us: 1.24x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 327 ms: 1.24x faster                                                    |
| pyflate                          | 222 ms                                                         | 182 ms: 1.22x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.32 ms: 1.22x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 822 us: 1.21x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 120 ms: 1.19x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.33 ms: 1.15x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 9.43 ms: 1.14x faster                                                   |
| fannkuch                         | 179 ms                                                         | 161 ms: 1.11x faster                                                    |
| float                            | 31.4 ms                                                        | 28.4 ms: 1.11x faster                                                   |
| richards                         | 22.1 ms                                                        | 20.0 ms: 1.10x faster                                                   |
| docutils                         | 1.05 sec                                                       | 954 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                  |
| html5lib                         | 23.1 ms                                                        | 21.2 ms: 1.09x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 42.4 ms: 1.09x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 22.9 ms: 1.08x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 173 ms: 1.08x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.8 ms: 1.08x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 40.2 ms: 1.07x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.65 ms: 1.07x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.6 ms: 1.06x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 125 ms: 1.06x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.88 ms: 1.06x faster                                                   |
| nqueens                          | 37.2 ms                                                        | 35.0 ms: 1.06x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 115 ms: 1.06x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 1.95 ms: 1.05x faster                                                   |
| scimark_fft                      | 124 ms                                                         | 118 ms: 1.04x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 177 ms: 1.04x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 282 ms: 1.04x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 310 ms: 1.04x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 291 ms: 1.04x faster                                                    |
| json                             | 1.94 ms                                                        | 1.88 ms: 1.03x faster                                                   |
| logging_format                   | 2.45 us                                                        | 2.37 us: 1.03x faster                                                   |
| logging_simple                   | 2.24 us                                                        | 2.17 us: 1.03x faster                                                   |
| pprint_pformat                   | 650 ms                                                         | 635 ms: 1.02x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 926 ns: 1.02x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 42.8 ms: 1.02x faster                                                   |
| sphinx                           | 409 ms                                                         | 400 ms: 1.02x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.6 us: 1.02x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| comprehensions                   | 6.80 us                                                        | 6.67 us: 1.02x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 92.9 ms: 1.02x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 97.8 us: 1.02x faster                                                   |
| connected_components             | 208 ms                                                         | 204 ms: 1.02x faster                                                    |
| shortest_path                    | 225 ms                                                         | 221 ms: 1.02x faster                                                    |
| bench_thread_pool                | 412 us                                                         | 407 us: 1.01x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.44 ms: 1.01x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 35.6 ms: 1.01x faster                                                   |
| deltablue                        | 1.45 ms                                                        | 1.46 ms: 1.01x slower                                                   |
| pidigits                         | 166 ms                                                         | 168 ms: 1.01x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.80 ms: 1.01x slower                                                   |
| nbody                            | 42.5 ms                                                        | 43.2 ms: 1.02x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 48.8 ms: 1.02x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.56 ms: 1.03x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 99.3 ms: 1.04x slower                                                   |
| pycparser                        | 470 ms                                                         | 490 ms: 1.04x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.4 ms: 1.05x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 169 ms: 1.06x slower                                                    |
| 2to3                             | 112 ms                                                         | 118 ms: 1.06x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.5 ms: 1.06x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 66.5 ms: 1.06x slower                                                   |
| raytrace                         | 109 ms                                                         | 116 ms: 1.07x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 139 us: 1.07x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.30 ms: 1.08x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.0 ms: 1.08x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.4 ms: 1.11x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 54.1 ms: 1.13x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.76 ms: 1.14x slower                                                   |
| django_template                  | 12.5 ms                                                        | 15.0 ms: 1.20x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 51.7 ms: 1.21x slower                                                   |
| many_optionals                   | 200 us                                                         | 243 us: 1.21x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 47.4 ms: 1.25x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 263 ms: 1.27x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 153 ms: 1.49x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 103 ms: 3.55x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.06x faster                                                            |

Benchmark hidden because not significant (3): thrift, logging_silent, async_tree_eager_cpu_io_mixed
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260904-3.16.0a0-e56f86f/bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.062x faster

# HPT report

- Reliability score: 99.97% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.15x