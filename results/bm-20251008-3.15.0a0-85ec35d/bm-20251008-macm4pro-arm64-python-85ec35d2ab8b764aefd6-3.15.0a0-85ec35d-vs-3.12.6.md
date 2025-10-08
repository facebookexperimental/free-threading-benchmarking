# Results vs. 3.12.6

- fork: python
- ref: 85ec35d2ab8b764aefd6
- machine: darwin-arm64
- commit hash: 85ec35d
- commit date: 2025-10-08
- overall geometric mean: 1.104x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 113 ms: 1.01x faster                                                    |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.4 ms: 1.06x slower                                                   |
| sphinx         | 434 ms                                                   | 411 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.00x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 249 ms: 1.99x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 252 ms: 1.90x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 253 ms: 1.82x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 253 ms: 1.76x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.64x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.58x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.50x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 262 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 263 ms: 1.27x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.1 ms: 1.11x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 191 ms: 1.00x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.5 ms: 2.72x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.0 ms: 1.26x faster                                                   |
| nbody          | 54.2 ms                                                  | 47.7 ms: 1.14x faster                                                   |
| pidigits       | 161 ms                                                   | 167 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.11x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 49.1 ms: 1.11x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 97.9 ms: 1.02x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.86 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 43.9 ms: 1.17x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 61.5 ms: 1.10x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.4 ms: 1.10x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.89 ms: 1.09x faster                                                   |
| tomli_loads          | 957 ms                                                   | 883 ms: 1.08x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 25.3 ms: 1.06x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 98.2 us: 1.05x faster                                                   |
| json_loads           | 10.9 us                                                  | 11.0 us: 1.01x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 146 us: 1.05x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.70 ms: 1.09x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.23 ms: 1.09x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.95 ms: 1.05x faster                                                   |
| mako            | 4.77 ms                                                  | 4.94 ms: 1.04x slower                                                   |
| django_template | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.02x slower                                                            |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.09 sec                                                 | 549 ms: 1.99x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 249 ms: 1.99x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 252 ms: 1.90x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 253 ms: 1.82x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 253 ms: 1.76x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.64x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.58x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 11.9 us: 1.53x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.50x faster                                                    |
| deepcopy                         | 161 us                                                   | 109 us: 1.48x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.35x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.49 us: 1.31x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 262 ms: 1.29x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.15 us: 1.27x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 263 ms: 1.27x faster                                                    |
| float                            | 37.9 ms                                                  | 30.0 ms: 1.26x faster                                                   |
| go                               | 70.0 ms                                                  | 55.7 ms: 1.26x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 43.7 ms: 1.24x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 41.1 ns: 1.24x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.8 ms: 1.23x faster                                                   |
| raytrace                         | 145 ms                                                   | 118 ms: 1.23x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 50.5 ms: 1.21x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.9 ms: 1.17x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.1 ms: 1.17x faster                                                   |
| k_core                           | 1.12 sec                                                 | 958 ms: 1.17x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.17x faster                                                   |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 123 ms: 1.15x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 18.0 ms: 1.15x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                  |
| deltablue                        | 1.73 ms                                                  | 1.51 ms: 1.14x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| nbody                            | 54.2 ms                                                  | 47.7 ms: 1.14x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.83 ms: 1.13x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 38.8 ms: 1.12x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 63.3 us: 1.12x faster                                                   |
| pylint                           | 128 ms                                                   | 115 ms: 1.12x faster                                                    |
| pyflate                          | 216 ms                                                   | 194 ms: 1.11x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 49.1 ms: 1.11x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 41.1 ms: 1.11x faster                                                   |
| chaos                            | 28.9 ms                                                  | 26.2 ms: 1.11x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 61.5 ms: 1.10x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 35.4 ms: 1.10x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.35 us: 1.10x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.89 ms: 1.09x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.79 ms: 1.09x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.58 us: 1.09x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 883 ms: 1.08x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.7 ms: 1.08x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 47.6 ms: 1.08x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.52 ms: 1.07x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 25.3 ms: 1.06x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 24.0 ms: 1.06x faster                                                   |
| sphinx                           | 434 ms                                                   | 411 ms: 1.05x faster                                                    |
| richards                         | 22.4 ms                                                  | 21.3 ms: 1.05x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 9.95 ms: 1.05x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 98.2 us: 1.05x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                    |
| sympy_str                        | 104 ms                                                   | 100 ms: 1.04x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.4 ms: 1.04x faster                                                   |
| thrift                           | 322 us                                                   | 312 us: 1.03x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 322 ms: 1.02x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 652 ms: 1.02x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 97.9 ms: 1.02x faster                                                   |
| 2to3                             | 114 ms                                                   | 113 ms: 1.01x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 56.9 ms: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 960 ns: 1.01x faster                                                    |
| shortest_path                    | 219 ms                                                   | 218 ms: 1.01x faster                                                    |
| connected_components             | 201 ms                                                   | 201 ms: 1.00x slower                                                    |
| asyncio_websockets               | 190 ms                                                   | 191 ms: 1.00x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 421 us: 1.01x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.0 us: 1.01x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 169 ms: 1.01x slower                                                    |
| fannkuch                         | 176 ms                                                   | 178 ms: 1.02x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.86 ms: 1.03x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| gc_traversal                     | 2.01 ms                                                  | 2.07 ms: 1.03x slower                                                   |
| mako                             | 4.77 ms                                                  | 4.94 ms: 1.04x slower                                                   |
| pidigits                         | 161 ms                                                   | 167 ms: 1.04x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.6 ms: 1.04x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 146 us: 1.05x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 41.9 ms: 1.06x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 24.4 ms: 1.06x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.70 ms: 1.09x slower                                                   |
| telco                            | 2.61 ms                                                  | 2.85 ms: 1.09x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.23 ms: 1.09x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 938 us: 1.13x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.4 ms: 1.21x slower                                                   |
| many_optionals                   | 195 us                                                   | 329 us: 1.69x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.5 ms: 2.72x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                            |

Benchmark hidden because not significant (3): genshi_xml, json, pycparser
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251008-3.15.0a0-85ec35d/bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.104x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.14x