# Results vs. 3.12.6

- fork: python
- ref: e56f86fb6cc7cf14c255
- machine: darwin-arm64
- commit hash: e56f86f
- commit date: 2026-09-04
- overall geometric mean: 1.150x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 118 ms: 1.04x slower                                                    |
| docutils       | 1.02 sec                                                 | 954 ms: 1.07x faster                                                    |
| html5lib       | 23.0 ms                                                  | 21.2 ms: 1.08x faster                                                   |
| sphinx         | 434 ms                                                   | 400 ms: 1.08x faster                                                    |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 306 ms: 1.62x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 120 ms: 1.48x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 310 ms: 1.48x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 327 ms: 1.47x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.43 ms: 1.44x faster                                                   |
| async_generators                 | 206 ms                                                   | 144 ms: 1.43x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 125 ms: 1.38x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 331 ms: 1.35x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 173 ms: 1.34x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 177 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 282 ms: 1.18x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 291 ms: 1.16x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 115 ms: 1.14x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.2 ms: 1.13x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 263 ms: 1.24x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 153 ms: 1.36x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 103 ms: 3.19x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.14x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.4 ms: 1.33x faster                                                   |
| nbody          | 54.2 ms                                                  | 43.2 ms: 1.26x faster                                                   |
| pidigits       | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.17x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.32 ms: 1.26x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 92.9 ms: 1.07x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.33 ms: 1.03x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 54.1 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 42.4 ms: 1.22x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.54 ms: 1.20x faster                                                   |
| tomli_loads          | 957 ms                                                   | 796 ms: 1.20x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 35.6 ms: 1.09x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 24.9 ms: 1.07x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 97.8 us: 1.05x faster                                                   |
| json_loads           | 10.9 us                                                  | 10.6 us: 1.02x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 66.5 ms: 1.02x faster                                                   |
| Geometric mean       | (ref)                                                    | 1.10x faster                                                            |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.30 ms: 1.16x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.76 ms: 1.18x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.17x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.56 ms: 1.05x faster                                                   |
| django_template | 13.6 ms                                                  | 15.0 ms: 1.10x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.02x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.08 ms: 5.09x faster                                                   |
| pylint                           | 128 ms                                                   | 56.9 ms: 2.25x faster                                                   |
| mdp                              | 1.09 sec                                                 | 511 ms: 2.14x faster                                                    |
| deepcopy                         | 161 us                                                   | 96.8 us: 1.67x faster                                                   |
| async_tree_eager_io              | 496 ms                                                   | 306 ms: 1.62x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 11.7 us: 1.56x faster                                                   |
| async_tree_none                  | 178 ms                                                   | 120 ms: 1.48x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 310 ms: 1.48x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 6.67 us: 1.47x faster                                                   |
| async_tree_io_tg                 | 480 ms                                                   | 327 ms: 1.47x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 49.3 us: 1.44x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 9.43 ms: 1.44x faster                                                   |
| async_generators                 | 206 ms                                                   | 144 ms: 1.43x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.04 us: 1.40x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 125 ms: 1.38x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 331 ms: 1.35x faster                                                    |
| go                               | 70.0 ms                                                  | 52.1 ms: 1.34x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 173 ms: 1.34x faster                                                    |
| float                            | 37.9 ms                                                  | 28.4 ms: 1.33x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.0 ms: 1.29x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 42.8 ms: 1.27x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 177 ms: 1.26x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.32 ms: 1.26x faster                                                   |
| nbody                            | 54.2 ms                                                  | 43.2 ms: 1.26x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 40.7 ns: 1.25x faster                                                   |
| raytrace                         | 145 ms                                                   | 116 ms: 1.25x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 35.0 ms: 1.24x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 49.8 ms: 1.23x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 42.4 ms: 1.22x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.54 ms: 1.20x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 796 ms: 1.20x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 118 ms: 1.20x faster                                                    |
| pyflate                          | 216 ms                                                   | 182 ms: 1.19x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.17 us: 1.18x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.37 us: 1.18x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 282 ms: 1.18x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.46 ms: 1.18x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 291 ms: 1.16x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.8 ms: 1.16x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.16x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.80 ms: 1.15x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                  |
| hexiom                           | 3.04 ms                                                  | 2.65 ms: 1.15x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 115 ms: 1.14x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.6 ms: 1.14x faster                                                   |
| chaos                            | 28.9 ms                                                  | 25.4 ms: 1.14x faster                                                   |
| k_core                           | 1.12 sec                                                 | 982 ms: 1.14x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.2 ms: 1.13x faster                                                   |
| richards                         | 22.4 ms                                                  | 20.0 ms: 1.12x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 22.9 ms: 1.11x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 35.6 ms: 1.09x faster                                                   |
| fannkuch                         | 176 ms                                                   | 161 ms: 1.09x faster                                                    |
| sphinx                           | 434 ms                                                   | 400 ms: 1.08x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 21.2 ms: 1.08x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.44 ms: 1.08x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 24.9 ms: 1.07x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 92.9 ms: 1.07x faster                                                   |
| docutils                         | 1.02 sec                                                 | 954 ms: 1.07x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 310 ms: 1.06x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 97.8 us: 1.05x faster                                                   |
| sympy_str                        | 104 ms                                                   | 99.3 ms: 1.05x faster                                                   |
| pprint_pformat                   | 665 ms                                                   | 635 ms: 1.05x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.56 ms: 1.05x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 926 ns: 1.04x faster                                                    |
| thrift                           | 322 us                                                   | 309 us: 1.04x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.4 ms: 1.04x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 55.5 ms: 1.04x faster                                                   |
| gc_traversal                     | 2.01 ms                                                  | 1.95 ms: 1.03x faster                                                   |
| bench_thread_pool                | 419 us                                                   | 407 us: 1.03x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.33 ms: 1.03x faster                                                   |
| json                             | 1.93 ms                                                  | 1.88 ms: 1.03x faster                                                   |
| json_loads                       | 10.9 us                                                  | 10.6 us: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 66.5 ms: 1.02x faster                                                   |
| pycparser                        | 497 ms                                                   | 490 ms: 1.02x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 54.1 ms: 1.01x faster                                                   |
| create_gc_cycles                 | 830 us                                                   | 822 us: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                                    |
| shortest_path                    | 219 ms                                                   | 221 ms: 1.01x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 169 ms: 1.01x slower                                                    |
| connected_components             | 201 ms                                                   | 204 ms: 1.02x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 48.8 ms: 1.02x slower                                                   |
| 2to3                             | 114 ms                                                   | 118 ms: 1.04x slower                                                    |
| pidigits                         | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.0 ms: 1.10x slower                                                   |
| telco                            | 2.61 ms                                                  | 2.88 ms: 1.10x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.30 ms: 1.16x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.76 ms: 1.18x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 47.4 ms: 1.19x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 263 ms: 1.24x slower                                                    |
| many_optionals                   | 195 us                                                   | 243 us: 1.24x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 153 ms: 1.36x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 103 ms: 3.19x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.15x faster                                                            |

Benchmark hidden because not significant (2): pickle_pure_python, scimark_lu
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260904-3.16.0a0-e56f86f/bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.150x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.19x