# Results vs. 3.12.6

- fork: python
- ref: ec7fad79d24e79961b86
- machine: darwin-arm64
- commit hash: ec7fad7
- commit date: 2025-07-23
- overall geometric mean: 1.090x faster
- HPT reliability: 97.65%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.26x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 121 ms: 1.06x slower                                                    |
| docutils       | 1.02 sec                                                 | 986 ms: 1.04x faster                                                    |
| html5lib       | 23.0 ms                                                  | 23.3 ms: 1.01x slower                                                   |
| sphinx         | 434 ms                                                   | 413 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.00x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.43x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 197 ms: 2.43x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 196 ms: 2.27x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.20x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 85.6 ms: 2.01x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 99.0 ms: 1.80x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 129 ms: 1.72x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 234 ms: 1.45x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 241 ms: 1.38x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.8 ms: 1.26x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 182 ms: 1.13x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 48.6 ms: 1.07x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 227 ms: 1.07x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.0 ms: 2.40x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.38x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.4 ms: 1.34x faster                                                   |
| nbody          | 54.2 ms                                                  | 58.7 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.17 ms: 1.05x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 52.3 ms: 1.04x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 96.6 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 37.6 ms: 1.37x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 59.3 ms: 1.15x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.9 ms: 1.05x faster                                                   |
| tomli_loads          | 957 ms                                                   | 973 ms: 1.02x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.3 us: 1.04x slower                                                   |
| json_dumps           | 4.26 ms                                                  | 4.49 ms: 1.05x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 109 us: 1.06x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 149 us: 1.07x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                            |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.57 ms: 1.19x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.96 ms: 1.22x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.9 ms: 1.10x slower                                                   |
| genshi_text     | 10.5 ms                                                  | 11.7 ms: 1.11x slower                                                   |
| mako            | 4.77 ms                                                  | 5.64 ms: 1.18x slower                                                   |
| django_template | 13.6 ms                                                  | 16.4 ms: 1.20x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.15x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 763 us: 2.63x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.43x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 197 ms: 2.43x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 196 ms: 2.27x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.20x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 85.6 ms: 2.01x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                    |
| mdp                              | 1.09 sec                                                 | 603 ms: 1.81x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 99.0 ms: 1.80x faster                                                   |
| create_gc_cycles                 | 830 us                                                   | 481 us: 1.73x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 129 ms: 1.72x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 234 ms: 1.45x faster                                                    |
| deepcopy                         | 161 us                                                   | 117 us: 1.38x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 241 ms: 1.38x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.6 ms: 1.37x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 13.6 us: 1.34x faster                                                   |
| float                            | 37.9 ms                                                  | 28.4 ms: 1.34x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.8 ms: 1.26x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.23 us: 1.19x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 8.31 us: 1.18x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 817 ns: 1.18x faster                                                    |
| go                               | 70.0 ms                                                  | 59.7 ms: 1.17x faster                                                   |
| subparsers                       | 20.8 ms                                                  | 18.1 ms: 1.15x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 59.3 ms: 1.15x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.2 ms: 1.15x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 44.5 ns: 1.14x faster                                                   |
| async_generators                 | 206 ms                                                   | 182 ms: 1.13x faster                                                    |
| k_core                           | 1.12 sec                                                 | 988 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                  |
| dulwich_log                      | 21.3 ms                                                  | 18.8 ms: 1.13x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.11x faster                                                   |
| raytrace                         | 145 ms                                                   | 131 ms: 1.11x faster                                                    |
| pyflate                          | 216 ms                                                   | 195 ms: 1.11x faster                                                    |
| pylint                           | 128 ms                                                   | 117 ms: 1.09x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 56.6 ms: 1.08x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.61 ms: 1.07x faster                                                   |
| pycparser                        | 497 ms                                                   | 467 ms: 1.06x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 51.5 ms: 1.06x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 36.9 ms: 1.05x faster                                                   |
| sphinx                           | 434 ms                                                   | 413 ms: 1.05x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.17 ms: 1.05x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 52.3 ms: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                    |
| docutils                         | 1.02 sec                                                 | 986 ms: 1.04x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.6 ms: 1.03x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.52 us: 1.02x faster                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 141 ms: 1.00x faster                                                    |
| dask                             | 528 ms                                                   | 532 ms: 1.01x slower                                                    |
| fannkuch                         | 176 ms                                                   | 177 ms: 1.01x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.3 ms: 1.01x slower                                                   |
| json                             | 1.93 ms                                                  | 1.96 ms: 1.01x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 973 ms: 1.02x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.0 ms: 1.03x slower                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 73.1 us: 1.03x slower                                                   |
| thrift                           | 322 us                                                   | 332 us: 1.03x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.15 ms: 1.04x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.3 us: 1.04x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 26.5 ms: 1.04x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.9 ms: 1.05x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.49 ms: 1.05x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 346 ms: 1.05x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 109 us: 1.06x slower                                                    |
| 2to3                             | 114 ms                                                   | 121 ms: 1.06x slower                                                    |
| shortest_path                    | 219 ms                                                   | 233 ms: 1.06x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 48.6 ms: 1.07x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 227 ms: 1.07x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 709 ms: 1.07x slower                                                    |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.07x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 61.6 ms: 1.07x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 149 us: 1.07x slower                                                    |
| nbody                            | 54.2 ms                                                  | 58.7 ms: 1.08x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 23.9 ms: 1.10x slower                                                   |
| connected_components             | 201 ms                                                   | 220 ms: 1.10x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 42.7 ms: 1.10x slower                                                   |
| genshi_text                      | 10.5 ms                                                  | 11.7 ms: 1.11x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.31 ms: 1.11x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 57.4 ms: 1.12x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.8 ms: 1.13x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 190 ms: 1.14x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 56.4 ms: 1.18x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.64 ms: 1.18x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.57 ms: 1.19x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.4 ms: 1.20x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.96 ms: 1.22x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.21 ms: 1.23x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 581 us: 1.39x slower                                                    |
| coverage                         | 26.9 ms                                                  | 39.9 ms: 1.49x slower                                                   |
| many_optionals                   | 195 us                                                   | 327 us: 1.68x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.0 ms: 2.40x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (6): xml_etree_process, chaos, logging_format, sympy_integrate, nqueens, pidigits
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250723-3.15.0a0-ec7fad7-NOGIL/bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.090x faster

# HPT report

- Reliability score: 97.65% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.26x