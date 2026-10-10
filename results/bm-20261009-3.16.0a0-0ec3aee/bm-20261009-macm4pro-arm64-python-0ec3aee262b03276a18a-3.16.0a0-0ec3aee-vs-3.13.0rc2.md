# Results vs. 3.13.0rc2

- fork: python
- ref: 0ec3aee262b03276a18a
- machine: darwin-arm64
- commit hash: 0ec3aee
- commit date: 2026-10-09
- overall geometric mean: 1.072x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 119 ms: 1.06x slower                                                    |
| docutils       | 1.05 sec                                                       | 950 ms: 1.10x faster                                                    |
| html5lib       | 23.1 ms                                                        | 21.2 ms: 1.09x faster                                                   |
| sphinx         | 409 ms                                                         | 397 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 305 ms: 1.72x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 330 ms: 1.58x faster                                                    |
| async_generators                 | 193 ms                                                         | 144 ms: 1.34x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 308 ms: 1.26x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 325 ms: 1.25x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 119 ms: 1.19x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.68 ms: 1.11x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 172 ms: 1.08x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 124 ms: 1.07x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.9 ms: 1.06x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 116 ms: 1.06x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 176 ms: 1.05x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 280 ms: 1.05x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 290 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 261 ms: 1.26x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 153 ms: 1.50x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 103 ms: 3.56x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.8 ms: 1.13x faster                                                   |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.32 ms: 1.22x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.22 ms: 1.16x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 91.5 ms: 1.03x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 54.0 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                          | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.58 ms: 1.30x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 809 ms: 1.24x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 42.8 ms: 1.08x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 93.7 us: 1.06x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.4 us: 1.04x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 34.5 ms: 1.04x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 65.3 ms: 1.05x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 137 us: 1.06x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.07x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.05 ms: 1.05x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.60 ms: 1.11x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.08x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.45 ms: 1.01x slower                                                   |
| django_template | 12.5 ms                                                        | 14.7 ms: 1.18x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.09x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 502 ms: 2.11x faster                                                    |
| pylint                           | 106 ms                                                         | 55.2 ms: 1.91x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 305 ms: 1.72x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 330 ms: 1.58x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.09 ms: 1.53x faster                                                   |
| k_core                           | 1.46 sec                                                       | 972 ms: 1.51x faster                                                    |
| deepcopy                         | 145 us                                                         | 96.8 us: 1.50x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 11.8 us: 1.40x faster                                                   |
| go                               | 72.6 ms                                                        | 52.0 ms: 1.40x faster                                                   |
| async_generators                 | 193 ms                                                         | 144 ms: 1.34x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 48.6 us: 1.33x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.58 ms: 1.30x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 49.5 ms: 1.29x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.03 us: 1.26x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 308 ms: 1.26x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 325 ms: 1.25x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 809 ms: 1.24x faster                                                    |
| pyflate                          | 222 ms                                                         | 181 ms: 1.23x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.32 ms: 1.22x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 833 us: 1.19x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 119 ms: 1.19x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.22 ms: 1.16x faster                                                   |
| fannkuch                         | 179 ms                                                         | 157 ms: 1.14x faster                                                    |
| float                            | 31.4 ms                                                        | 27.8 ms: 1.13x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 26.9 ms: 1.11x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 9.68 ms: 1.11x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.0 ms: 1.10x faster                                                   |
| docutils                         | 1.05 sec                                                       | 950 ms: 1.10x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.1 ms: 1.10x faster                                                   |
| scimark_fft                      | 124 ms                                                         | 113 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                  |
| html5lib                         | 23.1 ms                                                        | 21.2 ms: 1.09x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 22.9 ms: 1.08x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 172 ms: 1.08x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.64 ms: 1.08x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 42.8 ms: 1.08x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 124 ms: 1.07x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 41.2 ms: 1.06x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 93.7 us: 1.06x faster                                                   |
| nqueens                          | 37.2 ms                                                        | 35.1 ms: 1.06x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 40.9 ms: 1.06x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.90 ms: 1.06x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.5 ms: 1.06x faster                                                   |
| gc_traversal                     | 2.04 ms                                                        | 1.93 ms: 1.06x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 116 ms: 1.06x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.33 us: 1.05x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 176 ms: 1.05x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 280 ms: 1.05x faster                                                    |
| json                             | 1.94 ms                                                        | 1.85 ms: 1.05x faster                                                   |
| json_loads                       | 10.8 us                                                        | 10.4 us: 1.04x faster                                                   |
| comprehensions                   | 6.80 us                                                        | 6.52 us: 1.04x faster                                                   |
| logging_simple                   | 2.24 us                                                        | 2.14 us: 1.04x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 290 ms: 1.04x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 914 ns: 1.04x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 310 ms: 1.04x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 34.5 ms: 1.04x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 91.5 ms: 1.03x faster                                                   |
| sphinx                           | 409 ms                                                         | 397 ms: 1.03x faster                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.74 ms: 1.02x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.36 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| thrift                           | 309 us                                                         | 303 us: 1.02x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 639 ms: 1.02x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                   |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| bench_thread_pool                | 412 us                                                         | 408 us: 1.01x faster                                                    |
| connected_components             | 208 ms                                                         | 207 ms: 1.00x faster                                                    |
| shortest_path                    | 225 ms                                                         | 226 ms: 1.01x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.45 ms: 1.01x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.47 ms: 1.01x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 48.7 ms: 1.02x slower                                                   |
| chaos                            | 24.3 ms                                                        | 24.9 ms: 1.03x slower                                                   |
| pycparser                        | 470 ms                                                         | 484 ms: 1.03x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 41.9 ns: 1.03x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 99.0 ms: 1.04x slower                                                   |
| raytrace                         | 109 ms                                                         | 113 ms: 1.04x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 65.3 ms: 1.05x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 54.8 ms: 1.05x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 9.05 ms: 1.05x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 168 ms: 1.05x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 137 us: 1.06x slower                                                    |
| 2to3                             | 112 ms                                                         | 119 ms: 1.06x slower                                                    |
| generators                       | 15.7 ms                                                        | 16.9 ms: 1.08x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 46.6 ms: 1.09x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 36.8 ms: 1.09x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.60 ms: 1.11x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 54.0 ms: 1.13x slower                                                   |
| many_optionals                   | 200 us                                                         | 233 us: 1.16x slower                                                    |
| django_template                  | 12.5 ms                                                        | 14.7 ms: 1.18x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.8 ms: 1.18x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 261 ms: 1.26x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 153 ms: 1.50x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 103 ms: 3.56x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x faster                                                            |

Benchmark hidden because not significant (2): async_tree_eager_cpu_io_mixed, nbody
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261009-3.16.0a0-0ec3aee/bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.072x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.13x