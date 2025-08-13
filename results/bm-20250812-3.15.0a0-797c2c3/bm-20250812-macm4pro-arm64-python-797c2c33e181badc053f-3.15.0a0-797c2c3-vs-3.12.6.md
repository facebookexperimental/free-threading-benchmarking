# Results vs. 3.12.6

- fork: python
- ref: 797c2c33e181badc053f
- machine: darwin-arm64
- commit hash: 797c2c3
- commit date: 2025-08-12
- overall geometric mean: 1.090x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250812-macm4pro-arm64-python-797c2c33e181badc053f-3.15.0a0-797c2c3 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 115 ms: 1.01x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.06 sec: 1.04x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.6 ms: 1.07x slower                                                   |
| sphinx         | 434 ms                                                   | 414 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250812-macm4pro-arm64-python-797c2c33e181badc053f-3.15.0a0-797c2c3 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 247 ms: 2.00x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 250 ms: 1.92x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 256 ms: 1.80x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 254 ms: 1.75x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.61x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.58x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.52x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 264 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.2 ms: 1.08x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.18x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.2 ms: 2.74x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250812-macm4pro-arm64-python-797c2c33e181badc053f-3.15.0a0-797c2c3 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 31.0 ms: 1.22x faster                                                   |
| nbody          | 54.2 ms                                                  | 49.0 ms: 1.11x faster                                                   |
| pidigits       | 161 ms                                                   | 170 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250812-macm4pro-arm64-python-797c2c33e181badc053f-3.15.0a0-797c2c3 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 49.3 ms: 1.11x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 98.5 ms: 1.01x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.65 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250812-macm4pro-arm64-python-797c2c33e181badc053f-3.15.0a0-797c2c3 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 45.3 ms: 1.14x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.88 ms: 1.10x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.4 ms: 1.10x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 63.4 ms: 1.07x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.3 ms: 1.06x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 101 us: 1.02x faster                                                    |
| json_loads           | 10.9 us                                                  | 11.1 us: 1.03x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 143 us: 1.03x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.05x faster                                                            |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250812-macm4pro-arm64-python-797c2c33e181badc053f-3.15.0a0-797c2c3 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.85 ms: 1.10x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.33 ms: 1.11x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.11x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250812-macm4pro-arm64-python-797c2c33e181badc053f-3.15.0a0-797c2c3 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.0 ms: 1.04x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 22.0 ms: 1.01x slower                                                   |
| mako            | 4.77 ms                                                  | 4.94 ms: 1.03x slower                                                   |
| django_template | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.03x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250812-macm4pro-arm64-python-797c2c33e181badc053f-3.15.0a0-797c2c3 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.09 sec                                                 | 540 ms: 2.02x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 247 ms: 2.00x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 250 ms: 1.92x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 256 ms: 1.80x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 254 ms: 1.75x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.61x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.58x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.52x faster                                                    |
| deepcopy                         | 161 us                                                   | 112 us: 1.45x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.8 us: 1.43x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.61 us: 1.29x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 264 ms: 1.28x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.16 us: 1.26x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 40.8 ns: 1.25x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.7 ms: 1.24x faster                                                   |
| go                               | 70.0 ms                                                  | 56.7 ms: 1.24x faster                                                   |
| float                            | 37.9 ms                                                  | 31.0 ms: 1.22x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 44.6 ms: 1.22x faster                                                   |
| raytrace                         | 145 ms                                                   | 119 ms: 1.22x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 50.8 ms: 1.20x faster                                                   |
| subparsers                       | 20.8 ms                                                  | 17.4 ms: 1.19x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| k_core                           | 1.12 sec                                                 | 960 ms: 1.16x faster                                                    |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.4 ms: 1.16x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 45.3 ms: 1.14x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.99 sec: 1.12x faster                                                  |
| deltablue                        | 1.73 ms                                                  | 1.54 ms: 1.12x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.12x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 39.1 ms: 1.11x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 63.9 us: 1.11x faster                                                   |
| nbody                            | 54.2 ms                                                  | 49.0 ms: 1.11x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 49.3 ms: 1.11x faster                                                   |
| pylint                           | 128 ms                                                   | 116 ms: 1.10x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.3 ms: 1.10x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.88 ms: 1.10x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 35.4 ms: 1.10x faster                                                   |
| pyflate                          | 216 ms                                                   | 197 ms: 1.10x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.80 ms: 1.08x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 42.2 ms: 1.08x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.93 ms: 1.08x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.61 us: 1.07x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 63.4 ms: 1.07x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.41 us: 1.07x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 30.1 ms: 1.07x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 133 ms: 1.07x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.3 ms: 1.06x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.60 ms: 1.06x faster                                                   |
| richards                         | 22.4 ms                                                  | 21.3 ms: 1.05x faster                                                   |
| sphinx                           | 434 ms                                                   | 414 ms: 1.05x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 49.0 ms: 1.05x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 24.3 ms: 1.05x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 10.0 ms: 1.04x faster                                                   |
| thrift                           | 322 us                                                   | 310 us: 1.04x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.4 ms: 1.04x faster                                                   |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 101 us: 1.02x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 953 ns: 1.01x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 98.5 ms: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 57.2 ms: 1.01x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.65 ms: 1.01x slower                                                   |
| connected_components             | 201 ms                                                   | 202 ms: 1.01x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 671 ms: 1.01x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.0 ms: 1.01x slower                                                   |
| 2to3                             | 114 ms                                                   | 115 ms: 1.01x slower                                                    |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.01x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 170 ms: 1.02x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.1 us: 1.03x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 143 us: 1.03x slower                                                    |
| mako                             | 4.77 ms                                                  | 4.94 ms: 1.03x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 434 us: 1.04x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.06 sec: 1.04x slower                                                  |
| fannkuch                         | 176 ms                                                   | 183 ms: 1.04x slower                                                    |
| pidigits                         | 161 ms                                                   | 170 ms: 1.05x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.12 ms: 1.06x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 50.7 ms: 1.06x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 24.6 ms: 1.07x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.85 ms: 1.10x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.33 ms: 1.11x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.7 ms: 1.12x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 968 us: 1.17x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.06 ms: 1.17x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.18x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.9 ms: 1.22x slower                                                   |
| many_optionals                   | 195 us                                                   | 323 us: 1.65x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.2 ms: 2.74x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                            |

Benchmark hidden because not significant (5): tomli_loads, pprint_safe_repr, shortest_path, json, pycparser
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250812-3.15.0a0-797c2c3/bm-20250812-macm4pro-arm64-python-797c2c33e181badc053f-3.15.0a0-797c2c3.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.090x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.14x