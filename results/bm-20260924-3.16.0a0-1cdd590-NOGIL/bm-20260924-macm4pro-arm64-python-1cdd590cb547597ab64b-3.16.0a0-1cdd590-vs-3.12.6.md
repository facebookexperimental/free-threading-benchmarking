# Results vs. 3.12.6

- fork: python
- ref: 1cdd590cb547597ab64b
- machine: darwin-arm64
- commit hash: 1cdd590
- commit date: 2026-09-24
- overall geometric mean: 1.082x faster
- HPT reliability: 97.16%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 127 ms: 1.12x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.06 sec: 1.03x slower                                                  |
| html5lib       | 23.0 ms                                                  | 22.6 ms: 1.02x faster                                                   |
| sphinx         | 434 ms                                                   | 440 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.04x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 296 ms: 1.68x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 288 ms: 1.66x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 297 ms: 1.55x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 288 ms: 1.55x faster                                                    |
| async_generators                 | 206 ms                                                   | 155 ms: 1.34x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 177 ms: 1.30x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 136 ms: 1.26x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.8 ms: 1.26x faster                                                   |
| async_tree_none                  | 178 ms                                                   | 151 ms: 1.18x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 190 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 294 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 304 ms: 1.10x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 144 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 257 ms: 1.11x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 276 ms: 1.30x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 64.2 ms: 1.41x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 161 ms: 1.43x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 111 ms: 3.46x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.9 ms: 1.23x faster                                                   |
| nbody          | 54.2 ms                                                  | 50.9 ms: 1.06x faster                                                   |
| pidigits       | 161 ms                                                   | 170 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.35 ms: 1.23x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 94.5 ms: 1.05x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.18 ms: 1.04x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 60.3 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.8 ms: 1.26x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.74 ms: 1.14x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 60.3 ms: 1.13x faster                                                   |
| tomli_loads          | 957 ms                                                   | 877 ms: 1.09x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 36.9 ms: 1.05x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 104 us: 1.01x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.2 us: 1.04x slower                                                   |
| xml_etree_process    | 26.7 ms                                                  | 27.9 ms: 1.04x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 148 us: 1.06x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 10.4 ms: 1.30x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 7.58 ms: 1.33x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.32x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 5.54 ms: 1.16x slower                                                   |
| django_template | 13.6 ms                                                  | 16.3 ms: 1.20x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.18x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.16 ms: 5.00x faster                                                   |
| gc_traversal                     | 2.01 ms                                                  | 791 us: 2.54x faster                                                    |
| pylint                           | 128 ms                                                   | 52.7 ms: 2.43x faster                                                   |
| mdp                              | 1.09 sec                                                 | 580 ms: 1.88x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 494 us: 1.68x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 296 ms: 1.68x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 288 ms: 1.66x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 297 ms: 1.55x faster                                                    |
| deepcopy                         | 161 us                                                   | 104 us: 1.55x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 288 ms: 1.55x faster                                                    |
| async_generators                 | 206 ms                                                   | 155 ms: 1.34x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 13.8 us: 1.33x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 54.0 us: 1.31x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.53 us: 1.31x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 177 ms: 1.30x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.14 us: 1.28x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.8 ms: 1.26x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 136 ms: 1.26x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.8 ms: 1.26x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.35 ms: 1.23x faster                                                   |
| float                            | 37.9 ms                                                  | 30.9 ms: 1.23x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 789 ns: 1.23x faster                                                    |
| go                               | 70.0 ms                                                  | 57.5 ms: 1.22x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.87 sec: 1.20x faster                                                  |
| spectral_norm                    | 54.4 ms                                                  | 45.5 ms: 1.20x faster                                                   |
| async_tree_none                  | 178 ms                                                   | 151 ms: 1.18x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 190 ms: 1.17x faster                                                    |
| raytrace                         | 145 ms                                                   | 125 ms: 1.16x faster                                                    |
| pyflate                          | 216 ms                                                   | 188 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 294 ms: 1.15x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.15x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 38.1 ms: 1.14x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.74 ms: 1.14x faster                                                   |
| k_core                           | 1.12 sec                                                 | 986 ms: 1.13x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 125 ms: 1.13x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 60.3 ms: 1.13x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 19.1 ms: 1.11x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 55.2 ms: 1.11x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 46.3 ns: 1.10x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 304 ms: 1.10x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 877 ms: 1.09x faster                                                    |
| generators                       | 21.9 ms                                                  | 20.1 ms: 1.09x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.37 us: 1.08x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.61 us: 1.07x faster                                                   |
| nbody                            | 54.2 ms                                                  | 50.9 ms: 1.06x faster                                                   |
| chaos                            | 28.9 ms                                                  | 27.3 ms: 1.06x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 94.5 ms: 1.05x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 36.9 ms: 1.05x faster                                                   |
| pycparser                        | 497 ms                                                   | 473 ms: 1.05x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.18 ms: 1.04x faster                                                   |
| fannkuch                         | 176 ms                                                   | 169 ms: 1.04x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.67 ms: 1.03x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.02 ms: 1.03x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 22.6 ms: 1.02x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.99 ms: 1.01x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.96 ms: 1.01x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.5 ms: 1.01x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 104 us: 1.01x slower                                                    |
| sphinx                           | 434 ms                                                   | 440 ms: 1.02x slower                                                    |
| json                             | 1.93 ms                                                  | 1.98 ms: 1.02x slower                                                   |
| richards                         | 22.4 ms                                                  | 23.0 ms: 1.03x slower                                                   |
| sympy_str                        | 104 ms                                                   | 107 ms: 1.03x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.06 sec: 1.03x slower                                                  |
| json_loads                       | 10.9 us                                                  | 11.2 us: 1.04x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 26.3 ms: 1.04x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 340 ms: 1.04x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 59.8 ms: 1.04x slower                                                   |
| xml_etree_process                | 26.7 ms                                                  | 27.9 ms: 1.04x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 40.7 ms: 1.05x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 696 ms: 1.05x slower                                                    |
| pidigits                         | 161 ms                                                   | 170 ms: 1.06x slower                                                    |
| thrift                           | 322 us                                                   | 340 us: 1.06x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 148 us: 1.06x slower                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 144 ms: 1.10x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 184 ms: 1.10x slower                                                    |
| regex_compile                    | 54.6 ms                                                  | 60.3 ms: 1.10x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 52.9 ms: 1.11x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 257 ms: 1.11x slower                                                    |
| 2to3                             | 114 ms                                                   | 127 ms: 1.12x slower                                                    |
| shortest_path                    | 219 ms                                                   | 248 ms: 1.13x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.54 ms: 1.16x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 46.2 ms: 1.16x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.07 ms: 1.18x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.3 ms: 1.20x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 61.5 ms: 1.20x slower                                                   |
| connected_components             | 201 ms                                                   | 241 ms: 1.20x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 276 ms: 1.30x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 10.4 ms: 1.30x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 7.58 ms: 1.33x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 564 us: 1.35x slower                                                    |
| many_optionals                   | 195 us                                                   | 263 us: 1.35x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 64.2 ms: 1.41x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 161 ms: 1.43x slower                                                    |
| coverage                         | 26.9 ms                                                  | 39.7 ms: 1.48x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 111 ms: 3.46x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                            |
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260924-3.16.0a0-1cdd590-NOGIL/bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.082x faster

# HPT report

- Reliability score: 97.16% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.34x