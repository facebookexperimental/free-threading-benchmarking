# Results vs. 3.12.6

- fork: python
- ref: f57be7b2b3dc61ed18c5
- machine: darwin-arm64
- commit hash: f57be7b
- commit date: 2025-08-24
- overall geometric mean: 1.091x faster
- HPT reliability: 98.67%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.25x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250824-macm4pro-arm64-python-f57be7b2b3dc61ed18c5-3.15.0a0-f57be7b |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 123 ms: 1.08x slower                                                    |
| docutils       | 1.02 sec                                                 | 983 ms: 1.04x faster                                                    |
| html5lib       | 23.0 ms                                                  | 23.1 ms: 1.01x slower                                                   |
| sphinx         | 434 ms                                                   | 403 ms: 1.07x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250824-macm4pro-arm64-python-f57be7b2b3dc61ed18c5-3.15.0a0-f57be7b |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 205 ms: 2.42x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.42x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 196 ms: 2.28x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.9 ms: 1.98x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 234 ms: 1.45x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 242 ms: 1.38x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.9 ms: 1.25x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 182 ms: 1.14x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 225 ms: 1.06x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 48.8 ms: 1.07x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.1 ms: 2.43x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.38x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250824-macm4pro-arm64-python-f57be7b2b3dc61ed18c5-3.15.0a0-f57be7b |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.6 ms: 1.28x faster                                                   |
| pidigits       | 161 ms                                                   | 160 ms: 1.01x faster                                                    |
| nbody          | 54.2 ms                                                  | 56.4 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250824-macm4pro-arm64-python-f57be7b2b3dc61ed18c5-3.15.0a0-f57be7b |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.10 ms: 1.05x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 94.7 ms: 1.05x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 53.0 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250824-macm4pro-arm64-python-f57be7b2b3dc61ed18c5-3.15.0a0-f57be7b |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.2 ms: 1.35x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 59.8 ms: 1.14x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.86 ms: 1.10x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.5 ms: 1.07x faster                                                   |
| tomli_loads          | 957 ms                                                   | 982 ms: 1.03x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.3 us: 1.04x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 110 us: 1.07x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 152 us: 1.09x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                            |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250824-macm4pro-arm64-python-f57be7b2b3dc61ed18c5-3.15.0a0-f57be7b |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.45 ms: 1.18x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.88 ms: 1.21x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.19x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250824-macm4pro-arm64-python-f57be7b2b3dc61ed18c5-3.15.0a0-f57be7b |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 24.0 ms: 1.10x slower                                                   |
| genshi_text     | 10.5 ms                                                  | 11.5 ms: 1.10x slower                                                   |
| mako            | 4.77 ms                                                  | 5.69 ms: 1.19x slower                                                   |
| django_template | 13.6 ms                                                  | 16.6 ms: 1.22x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.15x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250824-macm4pro-arm64-python-f57be7b2b3dc61ed18c5-3.15.0a0-f57be7b |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 770 us: 2.61x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 205 ms: 2.42x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.42x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 196 ms: 2.28x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.9 ms: 1.98x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| mdp                              | 1.09 sec                                                 | 602 ms: 1.81x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 482 us: 1.72x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 234 ms: 1.45x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 242 ms: 1.38x faster                                                    |
| deepcopy                         | 161 us                                                   | 118 us: 1.36x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.2 ms: 1.35x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 14.2 us: 1.29x faster                                                   |
| float                            | 37.9 ms                                                  | 29.6 ms: 1.28x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.9 ms: 1.25x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.20x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.30 us: 1.18x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 824 ns: 1.17x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.26 us: 1.16x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.1 ms: 1.15x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.6 ms: 1.14x faster                                                   |
| go                               | 70.0 ms                                                  | 61.3 ms: 1.14x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 44.6 ns: 1.14x faster                                                   |
| async_generators                 | 206 ms                                                   | 182 ms: 1.14x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 59.8 ms: 1.14x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                   |
| k_core                           | 1.12 sec                                                 | 992 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.99 sec: 1.13x faster                                                  |
| subparsers                       | 20.8 ms                                                  | 18.5 ms: 1.12x faster                                                   |
| raytrace                         | 145 ms                                                   | 131 ms: 1.11x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 55.2 ms: 1.11x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.86 ms: 1.10x faster                                                   |
| pylint                           | 128 ms                                                   | 116 ms: 1.10x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.3 ms: 1.08x faster                                                   |
| pyflate                          | 216 ms                                                   | 200 ms: 1.08x faster                                                    |
| sphinx                           | 434 ms                                                   | 403 ms: 1.07x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.61 ms: 1.07x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 36.5 ms: 1.07x faster                                                   |
| pycparser                        | 497 ms                                                   | 471 ms: 1.06x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.10 ms: 1.05x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 94.7 ms: 1.05x faster                                                   |
| docutils                         | 1.02 sec                                                 | 983 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 53.0 ms: 1.03x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.50 us: 1.03x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.76 us: 1.01x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.94 ms: 1.01x faster                                                   |
| pidigits                         | 161 ms                                                   | 160 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 23.1 ms: 1.01x slower                                                   |
| dask                             | 528 ms                                                   | 533 ms: 1.01x slower                                                    |
| chaos                            | 28.9 ms                                                  | 29.2 ms: 1.01x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 982 ms: 1.03x slower                                                    |
| thrift                           | 322 us                                                   | 331 us: 1.03x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 337 ms: 1.03x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 73.3 us: 1.03x slower                                                   |
| hexiom                           | 3.04 ms                                                  | 3.15 ms: 1.04x slower                                                   |
| richards                         | 22.4 ms                                                  | 23.3 ms: 1.04x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 690 ms: 1.04x slower                                                    |
| nbody                            | 54.2 ms                                                  | 56.4 ms: 1.04x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.3 us: 1.04x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 26.5 ms: 1.05x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.8 ms: 1.05x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 60.5 ms: 1.05x slower                                                   |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.06x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 225 ms: 1.06x slower                                                    |
| fannkuch                         | 176 ms                                                   | 187 ms: 1.07x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 48.8 ms: 1.07x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 110 us: 1.07x slower                                                    |
| shortest_path                    | 219 ms                                                   | 236 ms: 1.08x slower                                                    |
| 2to3                             | 114 ms                                                   | 123 ms: 1.08x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 152 us: 1.09x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 42.6 ms: 1.10x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 24.0 ms: 1.10x slower                                                   |
| genshi_text                      | 10.5 ms                                                  | 11.5 ms: 1.10x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.29 ms: 1.10x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.0 ms: 1.11x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 57.0 ms: 1.11x slower                                                   |
| connected_components             | 201 ms                                                   | 223 ms: 1.11x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.95 ms: 1.13x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 189 ms: 1.13x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.45 ms: 1.18x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 56.7 ms: 1.19x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.69 ms: 1.19x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.88 ms: 1.21x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.6 ms: 1.22x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 594 us: 1.42x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.1 ms: 1.49x slower                                                   |
| many_optionals                   | 195 us                                                   | 334 us: 1.71x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.1 ms: 2.43x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (4): json, nqueens, xml_etree_process, scimark_fft
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250824-3.15.0a0-f57be7b-NOGIL/bm-20250824-macm4pro-arm64-python-f57be7b2b3dc61ed18c5-3.15.0a0-f57be7b.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.091x faster

# HPT report

- Reliability score: 98.67% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.25x