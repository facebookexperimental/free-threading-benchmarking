# Results vs. 3.12.6

- fork: python
- ref: e64395e8eb8d3a9e35e3
- machine: darwin-arm64
- commit hash: e64395e
- commit date: 2025-05-28
- overall geometric mean: 1.114x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250528-macm4pro-arm64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 112 ms: 1.02x faster                                                    |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                  |
| html5lib       | 23.0 ms                                                  | 23.6 ms: 1.02x slower                                                   |
| sphinx         | 434 ms                                                   | 405 ms: 1.07x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250528-macm4pro-arm64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 243 ms: 2.04x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 250 ms: 1.92x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 255 ms: 1.80x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 252 ms: 1.77x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.64x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.59x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.50x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 260 ms: 1.30x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 261 ms: 1.28x faster                                                    |
| async_generators                 | 206 ms                                                   | 170 ms: 1.22x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.4 ms: 1.10x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 246 ms: 1.16x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.3 ms: 2.72x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.26x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250528-macm4pro-arm64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.5 ms: 1.28x faster                                                   |
| nbody          | 54.2 ms                                                  | 47.3 ms: 1.15x faster                                                   |
| pidigits       | 161 ms                                                   | 162 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                    | 1.13x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250528-macm4pro-arm64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 48.1 ms: 1.14x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.67 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250528-macm4pro-arm64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 43.2 ms: 1.19x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 60.8 ms: 1.12x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.3 ms: 1.10x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 24.9 ms: 1.07x faster                                                   |
| tomli_loads          | 957 ms                                                   | 908 ms: 1.05x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 98.0 us: 1.05x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 4.46 ms: 1.05x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 146 us: 1.05x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.7 us: 1.08x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250528-macm4pro-arm64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.58 ms: 1.07x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.14 ms: 1.08x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.07x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250528-macm4pro-arm64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.72 ms: 1.08x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 21.4 ms: 1.02x faster                                                   |
| mako            | 4.77 ms                                                  | 4.94 ms: 1.04x slower                                                   |
| django_template | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.01x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250528-macm4pro-arm64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.56 ms: 2.17x faster                                                   |
| mdp                              | 1.09 sec                                                 | 509 ms: 2.14x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 243 ms: 2.04x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 250 ms: 1.92x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 255 ms: 1.80x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 252 ms: 1.77x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.64x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.59x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.50x faster                                                    |
| deepcopy                         | 161 us                                                   | 108 us: 1.49x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.4 us: 1.48x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.40 us: 1.33x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 260 ms: 1.30x faster                                                    |
| float                            | 37.9 ms                                                  | 29.5 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 261 ms: 1.28x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.15 us: 1.27x faster                                                   |
| go                               | 70.0 ms                                                  | 55.9 ms: 1.25x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.7 ms: 1.24x faster                                                   |
| raytrace                         | 145 ms                                                   | 118 ms: 1.23x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 49.9 ms: 1.22x faster                                                   |
| async_generators                 | 206 ms                                                   | 170 ms: 1.22x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 45.3 ms: 1.20x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 17.8 ms: 1.20x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.2 ms: 1.19x faster                                                   |
| k_core                           | 1.12 sec                                                 | 945 ms: 1.18x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.94 sec: 1.15x faster                                                  |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.50 ms: 1.15x faster                                                   |
| nbody                            | 54.2 ms                                                  | 47.3 ms: 1.15x faster                                                   |
| pylint                           | 128 ms                                                   | 113 ms: 1.14x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 48.1 ms: 1.14x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 62.6 us: 1.13x faster                                                   |
| chaos                            | 28.9 ms                                                  | 25.9 ms: 1.12x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 60.8 ms: 1.12x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.86 ms: 1.12x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 39.2 ms: 1.11x faster                                                   |
| pyflate                          | 216 ms                                                   | 195 ms: 1.11x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.2 ms: 1.11x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.75 ms: 1.11x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.1 ms: 1.11x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 35.3 ms: 1.10x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 46.6 ms: 1.10x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 41.4 ms: 1.10x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 130 ms: 1.09x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.38 ms: 1.09x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 9.72 ms: 1.08x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 24.9 ms: 1.07x faster                                                   |
| sphinx                           | 434 ms                                                   | 405 ms: 1.07x faster                                                    |
| thrift                           | 322 us                                                   | 303 us: 1.06x faster                                                    |
| sympy_str                        | 104 ms                                                   | 98.8 ms: 1.05x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 908 ms: 1.05x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 98.0 us: 1.05x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 24.4 ms: 1.04x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 37.3 ms: 1.04x faster                                                   |
| richards                         | 22.4 ms                                                  | 21.6 ms: 1.04x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 55.5 ms: 1.04x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.74 us: 1.02x faster                                                   |
| genshi_xml                       | 21.8 ms                                                  | 21.4 ms: 1.02x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 949 ns: 1.02x faster                                                    |
| 2to3                             | 114 ms                                                   | 112 ms: 1.02x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.53 us: 1.02x faster                                                   |
| pycparser                        | 497 ms                                                   | 491 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                    |
| shortest_path                    | 219 ms                                                   | 217 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                    |
| meteor_contest                   | 47.7 ms                                                  | 47.5 ms: 1.00x faster                                                   |
| sympy_expand                     | 167 ms                                                   | 166 ms: 1.00x faster                                                    |
| connected_components             | 201 ms                                                   | 201 ms: 1.00x slower                                                    |
| pidigits                         | 161 ms                                                   | 162 ms: 1.01x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                  |
| regex_v8                         | 9.59 ms                                                  | 9.67 ms: 1.01x slower                                                   |
| json                             | 1.93 ms                                                  | 1.96 ms: 1.01x slower                                                   |
| fannkuch                         | 176 ms                                                   | 178 ms: 1.02x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.6 ms: 1.02x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 431 us: 1.03x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.08 ms: 1.03x slower                                                   |
| mako                             | 4.77 ms                                                  | 4.94 ms: 1.04x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.46 ms: 1.05x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 146 us: 1.05x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.58 ms: 1.07x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 715 ms: 1.08x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.14 ms: 1.08x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 353 ms: 1.08x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.7 us: 1.08x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 43.6 ms: 1.10x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 939 us: 1.13x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 246 ms: 1.16x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.03 ms: 1.16x slower                                                   |
| coverage                         | 26.9 ms                                                  | 33.1 ms: 1.23x slower                                                   |
| many_optionals                   | 195 us                                                   | 241 us: 1.24x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.3 ms: 2.72x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 194 ns: 3.81x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                            |

Benchmark hidden because not significant (1): regex_dna
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250528-3.15.0a0-e64395e/bm-20250528-macm4pro-arm64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.114x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.15x