# Results vs. 3.12.6

- fork: python
- ref: d591b5effb8ec8177a95
- machine: darwin-arm64
- commit hash: d591b5e
- commit date: 2025-07-30
- overall geometric mean: 1.085x faster
- HPT reliability: 96.61%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.25x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 121 ms: 1.06x slower                                                    |
| docutils       | 1.02 sec                                                 | 989 ms: 1.03x faster                                                    |
| html5lib       | 23.0 ms                                                  | 23.6 ms: 1.02x slower                                                   |
| sphinx         | 434 ms                                                   | 407 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.00x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 203 ms: 2.44x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 197 ms: 2.44x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.30x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.20x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 85.5 ms: 2.01x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.88x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 99.1 ms: 1.80x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 233 ms: 1.45x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 241 ms: 1.38x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.8 ms: 1.26x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.21x faster                                                    |
| async_generators                 | 206 ms                                                   | 180 ms: 1.15x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 111 ms: 1.02x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 47.6 ms: 1.05x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 224 ms: 1.06x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 76.7 ms: 2.39x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.39x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.0 ms: 1.30x faster                                                   |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                    |
| nbody          | 54.2 ms                                                  | 60.7 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.13 ms: 1.05x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 96.5 ms: 1.03x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 52.9 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.7 ms: 1.33x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 58.0 ms: 1.17x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.7 ms: 1.06x faster                                                   |
| tomli_loads          | 957 ms                                                   | 1.01 sec: 1.05x slower                                                  |
| json_loads           | 10.9 us                                                  | 11.4 us: 1.05x slower                                                   |
| json_dumps           | 4.26 ms                                                  | 4.54 ms: 1.07x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 112 us: 1.08x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 152 us: 1.09x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.02x faster                                                            |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.61 ms: 1.20x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.96 ms: 1.22x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.7 ms: 1.09x slower                                                   |
| genshi_text     | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                   |
| mako            | 4.77 ms                                                  | 5.73 ms: 1.20x slower                                                   |
| django_template | 13.6 ms                                                  | 16.6 ms: 1.22x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.15x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 774 us: 2.60x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 203 ms: 2.44x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 197 ms: 2.44x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.30x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.20x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 85.5 ms: 2.01x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.88x faster                                                    |
| mdp                              | 1.09 sec                                                 | 604 ms: 1.81x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 99.1 ms: 1.80x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 487 us: 1.70x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 233 ms: 1.45x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 241 ms: 1.38x faster                                                    |
| deepcopy                         | 161 us                                                   | 120 us: 1.35x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.7 ms: 1.33x faster                                                   |
| float                            | 37.9 ms                                                  | 29.0 ms: 1.30x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 14.1 us: 1.30x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.8 ms: 1.26x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.21x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 817 ns: 1.18x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.34 us: 1.18x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.25 us: 1.17x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 58.0 ms: 1.17x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.0 ms: 1.16x faster                                                   |
| subparsers                       | 20.8 ms                                                  | 18.0 ms: 1.15x faster                                                   |
| async_generators                 | 206 ms                                                   | 180 ms: 1.15x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.8 ms: 1.13x faster                                                   |
| go                               | 70.0 ms                                                  | 61.9 ms: 1.13x faster                                                   |
| k_core                           | 1.12 sec                                                 | 988 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                  |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.13x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 45.2 ns: 1.13x faster                                                   |
| raytrace                         | 145 ms                                                   | 133 ms: 1.09x faster                                                    |
| pylint                           | 128 ms                                                   | 118 ms: 1.09x faster                                                    |
| pyflate                          | 216 ms                                                   | 200 ms: 1.08x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 56.8 ms: 1.07x faster                                                   |
| sphinx                           | 434 ms                                                   | 407 ms: 1.06x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.7 ms: 1.06x faster                                                   |
| pycparser                        | 497 ms                                                   | 472 ms: 1.05x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 51.6 ms: 1.05x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.64 ms: 1.05x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.13 ms: 1.05x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                    |
| docutils                         | 1.02 sec                                                 | 989 ms: 1.03x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.5 ms: 1.03x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 52.9 ms: 1.03x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 111 ms: 1.02x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 43.1 ms: 1.01x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 8.00 ms: 1.00x faster                                                   |
| dask                             | 528 ms                                                   | 531 ms: 1.01x slower                                                    |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                    |
| chaos                            | 28.9 ms                                                  | 29.3 ms: 1.01x slower                                                   |
| logging_format                   | 2.80 us                                                  | 2.84 us: 1.01x slower                                                   |
| hexiom                           | 3.04 ms                                                  | 3.11 ms: 1.02x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 23.6 ms: 1.02x slower                                                   |
| scimark_fft                      | 142 ms                                                   | 145 ms: 1.02x slower                                                    |
| fannkuch                         | 176 ms                                                   | 180 ms: 1.03x slower                                                    |
| json                             | 1.93 ms                                                  | 1.99 ms: 1.03x slower                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 73.4 us: 1.03x slower                                                   |
| thrift                           | 322 us                                                   | 334 us: 1.04x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 47.6 ms: 1.05x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 1.01 sec: 1.05x slower                                                  |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 224 ms: 1.06x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 61.0 ms: 1.06x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 34.1 ms: 1.06x slower                                                   |
| 2to3                             | 114 ms                                                   | 121 ms: 1.06x slower                                                    |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.06x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 349 ms: 1.07x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 27.1 ms: 1.07x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.54 ms: 1.07x slower                                                   |
| richards                         | 22.4 ms                                                  | 23.9 ms: 1.07x slower                                                   |
| shortest_path                    | 219 ms                                                   | 234 ms: 1.07x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 711 ms: 1.07x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 42.0 ms: 1.08x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 112 us: 1.08x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 23.7 ms: 1.09x slower                                                   |
| genshi_text                      | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 152 us: 1.09x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.28 ms: 1.10x slower                                                   |
| connected_components             | 201 ms                                                   | 221 ms: 1.10x slower                                                    |
| nbody                            | 54.2 ms                                                  | 60.7 ms: 1.12x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 57.6 ms: 1.12x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.9 ms: 1.13x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 190 ms: 1.14x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 56.1 ms: 1.18x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.61 ms: 1.20x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.73 ms: 1.20x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.6 ms: 1.22x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.96 ms: 1.22x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.24 ms: 1.24x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 601 us: 1.44x slower                                                    |
| coverage                         | 26.9 ms                                                  | 39.7 ms: 1.48x slower                                                   |
| many_optionals                   | 195 us                                                   | 325 us: 1.67x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 76.7 ms: 2.39x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (2): xml_etree_process, logging_simple
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250730-3.15.0a0-d591b5e-NOGIL/bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.085x faster

# HPT report

- Reliability score: 96.61% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.25x