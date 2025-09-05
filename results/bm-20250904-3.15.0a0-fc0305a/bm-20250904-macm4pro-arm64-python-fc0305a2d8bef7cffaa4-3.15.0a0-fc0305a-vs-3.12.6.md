# Results vs. 3.12.6

- fork: python
- ref: fc0305a2d8bef7cffaa4
- machine: darwin-arm64
- commit hash: fc0305a
- commit date: 2025-09-04
- overall geometric mean: 1.100x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 114 ms: 1.00x faster                                                    |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.1 ms: 1.05x slower                                                   |
| sphinx         | 434 ms                                                   | 410 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.00x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 247 ms: 2.01x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 250 ms: 1.92x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 251 ms: 1.83x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 253 ms: 1.76x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.64x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.59x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.50x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 261 ms: 1.30x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 263 ms: 1.27x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 173 ms: 1.19x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.5 ms: 1.10x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 246 ms: 1.16x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 86.8 ms: 2.70x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 31.3 ms: 1.21x faster                                                   |
| nbody          | 54.2 ms                                                  | 48.4 ms: 1.12x faster                                                   |
| pidigits       | 161 ms                                                   | 166 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 48.8 ms: 1.12x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 97.2 ms: 1.02x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.94 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 44.2 ms: 1.17x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.81 ms: 1.12x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 61.6 ms: 1.10x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.3 ms: 1.10x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.1 ms: 1.06x faster                                                   |
| tomli_loads          | 957 ms                                                   | 915 ms: 1.05x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 101 us: 1.02x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 147 us: 1.06x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.06x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.70 ms: 1.09x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.23 ms: 1.09x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.99 ms: 1.05x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 21.7 ms: 1.00x faster                                                   |
| mako            | 4.77 ms                                                  | 4.88 ms: 1.02x slower                                                   |
| django_template | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.02x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.09 sec                                                 | 541 ms: 2.02x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 247 ms: 2.01x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 250 ms: 1.92x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 251 ms: 1.83x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 253 ms: 1.76x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.64x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.59x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.50x faster                                                    |
| deepcopy                         | 161 us                                                   | 108 us: 1.50x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.5 us: 1.46x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.47 us: 1.32x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 261 ms: 1.30x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.13 us: 1.29x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 263 ms: 1.27x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 40.8 ns: 1.25x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 43.6 ms: 1.25x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.8 ms: 1.24x faster                                                   |
| go                               | 70.0 ms                                                  | 56.8 ms: 1.23x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 50.1 ms: 1.22x faster                                                   |
| float                            | 37.9 ms                                                  | 31.3 ms: 1.21x faster                                                   |
| subparsers                       | 20.8 ms                                                  | 17.2 ms: 1.21x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| raytrace                         | 145 ms                                                   | 121 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 173 ms: 1.19x faster                                                    |
| k_core                           | 1.12 sec                                                 | 948 ms: 1.18x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.1 ms: 1.17x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.2 ms: 1.17x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 38.3 ms: 1.14x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                  |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.13x faster                                                   |
| pylint                           | 128 ms                                                   | 114 ms: 1.13x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.53 ms: 1.13x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 48.8 ms: 1.12x faster                                                   |
| nbody                            | 54.2 ms                                                  | 48.4 ms: 1.12x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.81 ms: 1.12x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 63.6 us: 1.12x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.33 us: 1.10x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.54 us: 1.10x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 61.6 ms: 1.10x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 35.3 ms: 1.10x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 41.5 ms: 1.10x faster                                                   |
| pyflate                          | 216 ms                                                   | 198 ms: 1.09x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.5 ms: 1.09x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.79 ms: 1.09x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 131 ms: 1.08x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.9 ms: 1.08x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.49 ms: 1.07x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.95 ms: 1.07x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 25.1 ms: 1.06x faster                                                   |
| sphinx                           | 434 ms                                                   | 410 ms: 1.06x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.99 ms: 1.05x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 915 ms: 1.05x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 49.2 ms: 1.04x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 24.4 ms: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                    |
| thrift                           | 322 us                                                   | 309 us: 1.04x faster                                                    |
| richards                         | 22.4 ms                                                  | 21.6 ms: 1.04x faster                                                   |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.04x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.8 ms: 1.03x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 97.2 ms: 1.02x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 101 us: 1.02x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 56.2 ms: 1.02x faster                                                   |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 959 ns: 1.01x faster                                                    |
| 2to3                             | 114 ms                                                   | 114 ms: 1.00x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.7 ms: 1.00x faster                                                   |
| shortest_path                    | 219 ms                                                   | 220 ms: 1.01x slower                                                    |
| json                             | 1.93 ms                                                  | 1.95 ms: 1.01x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 671 ms: 1.01x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 332 ms: 1.01x slower                                                    |
| connected_components             | 201 ms                                                   | 204 ms: 1.01x slower                                                    |
| fannkuch                         | 176 ms                                                   | 178 ms: 1.02x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 426 us: 1.02x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 170 ms: 1.02x slower                                                    |
| mako                             | 4.77 ms                                                  | 4.88 ms: 1.02x slower                                                   |
| pidigits                         | 161 ms                                                   | 166 ms: 1.03x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| regex_v8                         | 9.59 ms                                                  | 9.94 ms: 1.04x slower                                                   |
| gc_traversal                     | 2.01 ms                                                  | 2.09 ms: 1.04x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 24.1 ms: 1.05x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 147 us: 1.06x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 42.0 ms: 1.06x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 50.6 ms: 1.06x slower                                                   |
| telco                            | 2.61 ms                                                  | 2.79 ms: 1.07x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.70 ms: 1.09x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.23 ms: 1.09x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 932 us: 1.12x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 246 ms: 1.16x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.9 ms: 1.23x slower                                                   |
| many_optionals                   | 195 us                                                   | 316 us: 1.62x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 86.8 ms: 2.70x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                            |

Benchmark hidden because not significant (3): pycparser, asyncio_websockets, json_loads
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250904-3.15.0a0-fc0305a/bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.100x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.14x