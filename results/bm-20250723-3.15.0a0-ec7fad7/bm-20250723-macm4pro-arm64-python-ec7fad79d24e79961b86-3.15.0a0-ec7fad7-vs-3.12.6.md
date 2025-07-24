# Results vs. 3.12.6

- fork: python
- ref: ec7fad79d24e79961b86
- machine: darwin-arm64
- commit hash: ec7fad7
- commit date: 2025-07-23
- overall geometric mean: 1.090x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 116 ms: 1.02x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.06 sec: 1.04x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.3 ms: 1.06x slower                                                   |
| sphinx         | 434 ms                                                   | 410 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 249 ms: 1.99x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 251 ms: 1.91x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 258 ms: 1.78x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 256 ms: 1.74x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 108 ms: 1.60x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.56x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.51x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 264 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 177 ms: 1.17x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.3 ms: 1.08x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 249 ms: 1.17x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.6 ms: 2.76x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.9 ms: 1.23x faster                                                   |
| nbody          | 54.2 ms                                                  | 49.5 ms: 1.09x faster                                                   |
| pidigits       | 161 ms                                                   | 165 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 49.3 ms: 1.11x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 97.4 ms: 1.02x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.65 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 43.7 ms: 1.18x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.1 ms: 1.11x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 61.5 ms: 1.10x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.5 ms: 1.05x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 101 us: 1.02x faster                                                    |
| tomli_loads          | 957 ms                                                   | 950 ms: 1.01x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 4.49 ms: 1.05x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 147 us: 1.06x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.66 ms: 1.08x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.20 ms: 1.09x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.08x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.2 ms: 1.03x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 22.0 ms: 1.01x slower                                                   |
| mako            | 4.77 ms                                                  | 5.07 ms: 1.06x slower                                                   |
| django_template | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.04x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.09 sec                                                 | 542 ms: 2.02x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 249 ms: 1.99x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 251 ms: 1.91x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 258 ms: 1.78x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 256 ms: 1.74x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 108 ms: 1.60x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.56x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.51x faster                                                    |
| deepcopy                         | 161 us                                                   | 113 us: 1.43x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 13.0 us: 1.40x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.57 us: 1.30x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 264 ms: 1.28x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.17 us: 1.25x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                                    |
| generators                       | 21.9 ms                                                  | 17.5 ms: 1.25x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 43.6 ms: 1.25x faster                                                   |
| go                               | 70.0 ms                                                  | 56.6 ms: 1.24x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 41.3 ns: 1.23x faster                                                   |
| float                            | 37.9 ms                                                  | 30.9 ms: 1.23x faster                                                   |
| raytrace                         | 145 ms                                                   | 119 ms: 1.22x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 51.1 ms: 1.19x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.19x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 17.5 ms: 1.19x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.7 ms: 1.18x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.2 ms: 1.17x faster                                                   |
| async_generators                 | 206 ms                                                   | 177 ms: 1.17x faster                                                    |
| k_core                           | 1.12 sec                                                 | 960 ms: 1.16x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 38.2 ms: 1.14x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.53 ms: 1.13x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.00 sec: 1.12x faster                                                  |
| pylint                           | 128 ms                                                   | 115 ms: 1.12x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.2 ms: 1.11x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 49.3 ms: 1.11x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 35.1 ms: 1.11x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 61.5 ms: 1.10x faster                                                   |
| chaos                            | 28.9 ms                                                  | 26.2 ms: 1.10x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 64.7 us: 1.10x faster                                                   |
| nbody                            | 54.2 ms                                                  | 49.5 ms: 1.09x faster                                                   |
| pyflate                          | 216 ms                                                   | 199 ms: 1.08x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.92 ms: 1.08x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 42.3 ms: 1.08x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.60 us: 1.08x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.40 us: 1.07x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.50 ms: 1.07x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 30.1 ms: 1.07x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.86 ms: 1.06x faster                                                   |
| sphinx                           | 434 ms                                                   | 410 ms: 1.06x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 135 ms: 1.05x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.5 ms: 1.05x faster                                                   |
| thrift                           | 322 us                                                   | 310 us: 1.04x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 49.5 ms: 1.04x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 37.5 ms: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 24.6 ms: 1.03x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 10.2 ms: 1.03x faster                                                   |
| richards                         | 22.4 ms                                                  | 21.7 ms: 1.03x faster                                                   |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.03x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 97.4 ms: 1.02x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 101 us: 1.02x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 56.6 ms: 1.02x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 953 ns: 1.01x faster                                                    |
| json                             | 1.93 ms                                                  | 1.91 ms: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 950 ms: 1.01x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 660 ms: 1.01x faster                                                    |
| shortest_path                    | 219 ms                                                   | 218 ms: 1.00x faster                                                    |
| connected_components             | 201 ms                                                   | 201 ms: 1.00x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.65 ms: 1.01x slower                                                   |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.0 ms: 1.01x slower                                                   |
| 2to3                             | 114 ms                                                   | 116 ms: 1.02x slower                                                    |
| pidigits                         | 161 ms                                                   | 165 ms: 1.02x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 171 ms: 1.03x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.06 sec: 1.04x slower                                                  |
| meteor_contest                   | 47.7 ms                                                  | 49.8 ms: 1.04x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 438 us: 1.05x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.10 ms: 1.05x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.49 ms: 1.05x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 24.3 ms: 1.06x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 147 us: 1.06x slower                                                    |
| fannkuch                         | 176 ms                                                   | 186 ms: 1.06x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.07 ms: 1.06x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.66 ms: 1.08x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.20 ms: 1.09x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 43.8 ms: 1.10x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 946 us: 1.14x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.05 ms: 1.17x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 249 ms: 1.17x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.9 ms: 1.22x slower                                                   |
| many_optionals                   | 195 us                                                   | 324 us: 1.66x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.6 ms: 2.76x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                            |

Benchmark hidden because not significant (3): pprint_safe_repr, json_loads, pycparser
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250723-3.15.0a0-ec7fad7/bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.090x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.14x