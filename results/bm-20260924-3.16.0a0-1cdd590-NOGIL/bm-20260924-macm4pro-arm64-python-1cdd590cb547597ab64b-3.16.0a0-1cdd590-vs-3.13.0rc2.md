# Results vs. 3.13.0rc2

- fork: python
- ref: 1cdd590cb547597ab64b
- machine: darwin-arm64
- commit hash: 1cdd590
- commit date: 2026-09-24
- overall geometric mean: 1.002x faster
- HPT reliability: 92.73%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.30x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 127 ms: 1.14x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| html5lib       | 23.1 ms                                                        | 22.6 ms: 1.02x faster                                                   |
| sphinx         | 409 ms                                                         | 440 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 288 ms: 1.81x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 296 ms: 1.78x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 288 ms: 1.41x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 297 ms: 1.30x faster                                                    |
| async_generators                 | 193 ms                                                         | 155 ms: 1.25x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 177 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 294 ms: 1.02x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 190 ms: 1.03x slower                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 304 ms: 1.03x slower                                                    |
| async_tree_none                  | 142 ms                                                         | 151 ms: 1.06x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 257 ms: 1.14x slower                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 144 ms: 1.18x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 276 ms: 1.33x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 64.2 ms: 1.49x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 161 ms: 1.57x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 111 ms: 3.85x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x slower                                                            |

Benchmark hidden because not significant (2): coroutines, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.9 ms: 1.02x faster                                                   |
| pidigits       | 166 ms                                                         | 170 ms: 1.03x slower                                                    |
| nbody          | 42.5 ms                                                        | 50.9 ms: 1.20x slower                                                   |
| Geometric mean | (ref)                                                          | 1.06x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.35 ms: 1.19x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.18 ms: 1.17x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 60.3 ms: 1.26x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.74 ms: 1.24x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 877 ms: 1.14x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.8 ms: 1.13x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 60.3 ms: 1.03x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 36.9 ms: 1.03x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.2 us: 1.04x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 104 us: 1.04x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.9 ms: 1.10x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 148 us: 1.14x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 10.4 ms: 1.21x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 7.58 ms: 1.27x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.24x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 5.54 ms: 1.26x slower                                                   |
| django_template | 12.5 ms                                                        | 16.3 ms: 1.31x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.28x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 791 us: 2.58x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 494 us: 2.01x faster                                                    |
| pylint                           | 106 ms                                                         | 52.7 ms: 2.00x faster                                                   |
| mdp                              | 1.06 sec                                                       | 580 ms: 1.82x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 288 ms: 1.81x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 296 ms: 1.78x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.16 ms: 1.51x faster                                                   |
| k_core                           | 1.46 sec                                                       | 986 ms: 1.48x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 288 ms: 1.41x faster                                                    |
| deepcopy                         | 145 us                                                         | 104 us: 1.39x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 297 ms: 1.30x faster                                                    |
| go                               | 72.6 ms                                                        | 57.5 ms: 1.26x faster                                                   |
| async_generators                 | 193 ms                                                         | 155 ms: 1.25x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.74 ms: 1.24x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 789 ns: 1.20x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 54.0 us: 1.20x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 13.8 us: 1.19x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.35 ms: 1.19x faster                                                   |
| pyflate                          | 222 ms                                                         | 188 ms: 1.18x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.18 ms: 1.17x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 55.2 ms: 1.16x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.87 sec: 1.14x faster                                                  |
| tomli_loads                      | 1000 ms                                                        | 877 ms: 1.14x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.14 us: 1.14x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.8 ms: 1.13x faster                                                   |
| fannkuch                         | 179 ms                                                         | 169 ms: 1.06x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 177 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 19.1 ms: 1.04x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 60.3 ms: 1.03x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 294 ms: 1.02x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 22.6 ms: 1.02x faster                                                   |
| float                            | 31.4 ms                                                        | 30.9 ms: 1.02x faster                                                   |
| pycparser                        | 470 ms                                                         | 473 ms: 1.01x slower                                                    |
| docutils                         | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| scimark_fft                      | 124 ms                                                         | 125 ms: 1.01x slower                                                    |
| json                             | 1.94 ms                                                        | 1.98 ms: 1.02x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 38.1 ms: 1.02x slower                                                   |
| pidigits                         | 166 ms                                                         | 170 ms: 1.03x slower                                                    |
| async_tree_memoization           | 184 ms                                                         | 190 ms: 1.03x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.9 ms: 1.03x slower                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 304 ms: 1.03x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.2 us: 1.04x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 45.5 ms: 1.04x slower                                                   |
| richards                         | 22.1 ms                                                        | 23.0 ms: 1.04x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 104 us: 1.04x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 2.99 ms: 1.05x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 340 ms: 1.06x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.96 ms: 1.06x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.37 us: 1.06x slower                                                   |
| async_tree_none                  | 142 ms                                                         | 151 ms: 1.06x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.3 ms: 1.07x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.61 us: 1.07x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 696 ms: 1.07x slower                                                    |
| sphinx                           | 409 ms                                                         | 440 ms: 1.08x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.5 ms: 1.09x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 27.9 ms: 1.10x slower                                                   |
| thrift                           | 309 us                                                         | 340 us: 1.10x slower                                                    |
| shortest_path                    | 225 ms                                                         | 248 ms: 1.11x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 52.9 ms: 1.11x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.53 us: 1.11x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 107 ms: 1.12x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.3 ms: 1.13x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.02 ms: 1.13x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 148 us: 1.14x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 46.3 ns: 1.14x slower                                                   |
| 2to3                             | 112 ms                                                         | 127 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 257 ms: 1.14x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 59.8 ms: 1.14x slower                                                   |
| raytrace                         | 109 ms                                                         | 125 ms: 1.15x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 184 ms: 1.15x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.67 ms: 1.15x slower                                                   |
| connected_components             | 208 ms                                                         | 241 ms: 1.16x slower                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 144 ms: 1.18x slower                                                    |
| nbody                            | 42.5 ms                                                        | 50.9 ms: 1.20x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 10.4 ms: 1.21x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 40.7 ms: 1.21x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 46.2 ms: 1.22x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.54 ms: 1.26x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 60.3 ms: 1.26x slower                                                   |
| coverage                         | 31.2 ms                                                        | 39.7 ms: 1.27x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 7.58 ms: 1.27x slower                                                   |
| generators                       | 15.7 ms                                                        | 20.1 ms: 1.28x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.3 ms: 1.31x slower                                                   |
| many_optionals                   | 200 us                                                         | 263 us: 1.31x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 276 ms: 1.33x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 564 us: 1.37x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 61.5 ms: 1.44x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 64.2 ms: 1.49x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 161 ms: 1.57x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 111 ms: 3.85x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x slower                                                            |

Benchmark hidden because not significant (4): regex_dna, telco, coroutines, async_tree_none_tg
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260924-3.16.0a0-1cdd590-NOGIL/bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.002x faster

# HPT report

- Reliability score: 92.73% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.30x