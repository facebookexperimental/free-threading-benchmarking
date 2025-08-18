# Results vs. 3.12.6

- fork: python
- ref: bc2872445b2aee4bb4e0
- machine: darwin-arm64
- commit hash: bc28724
- commit date: 2025-08-18
- overall geometric mean: 1.090x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 117 ms: 1.02x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.5 ms: 1.06x slower                                                   |
| sphinx         | 434 ms                                                   | 411 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 249 ms: 1.99x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 252 ms: 1.91x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 258 ms: 1.78x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 258 ms: 1.73x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.61x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.56x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.51x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.95 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 265 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.0 ms: 1.08x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.18x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.5 ms: 2.75x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 31.8 ms: 1.19x faster                                                   |
| nbody          | 54.2 ms                                                  | 49.2 ms: 1.10x faster                                                   |
| pidigits       | 161 ms                                                   | 164 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 49.7 ms: 1.10x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 96.6 ms: 1.03x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.84 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 44.1 ms: 1.17x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.89 ms: 1.09x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 62.1 ms: 1.09x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.9 ms: 1.08x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.7 ms: 1.04x faster                                                   |
| tomli_loads          | 957 ms                                                   | 946 ms: 1.01x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 103 us: 1.00x faster                                                    |
| json_loads           | 10.9 us                                                  | 11.0 us: 1.01x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 148 us: 1.06x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.65 ms: 1.08x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.21 ms: 1.09x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.08x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.1 ms: 1.04x faster                                                   |
| mako            | 4.77 ms                                                  | 4.95 ms: 1.04x slower                                                   |
| django_template | 13.6 ms                                                  | 15.6 ms: 1.14x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.03x slower                                                            |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.09 sec                                                 | 539 ms: 2.02x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 249 ms: 1.99x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 252 ms: 1.91x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 258 ms: 1.78x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 258 ms: 1.73x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.61x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.56x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.51x faster                                                    |
| deepcopy                         | 161 us                                                   | 114 us: 1.42x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 13.2 us: 1.39x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 9.95 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 265 ms: 1.28x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.74 us: 1.27x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                    |
| generators                       | 21.9 ms                                                  | 17.6 ms: 1.24x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.18 us: 1.24x faster                                                   |
| go                               | 70.0 ms                                                  | 57.5 ms: 1.22x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 42.0 ns: 1.21x faster                                                   |
| raytrace                         | 145 ms                                                   | 121 ms: 1.20x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 45.5 ms: 1.19x faster                                                   |
| float                            | 37.9 ms                                                  | 31.8 ms: 1.19x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 51.4 ms: 1.19x faster                                                   |
| subparsers                       | 20.8 ms                                                  | 17.6 ms: 1.18x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.1 ms: 1.17x faster                                                   |
| k_core                           | 1.12 sec                                                 | 957 ms: 1.17x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.2 ms: 1.17x faster                                                   |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 38.3 ms: 1.14x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                   |
| pylint                           | 128 ms                                                   | 114 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.99 sec: 1.12x faster                                                  |
| nbody                            | 54.2 ms                                                  | 49.2 ms: 1.10x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 49.7 ms: 1.10x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.57 ms: 1.10x faster                                                   |
| pyflate                          | 216 ms                                                   | 197 ms: 1.10x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.89 ms: 1.09x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.35 us: 1.09x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 62.1 ms: 1.09x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.56 us: 1.09x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 65.3 us: 1.09x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 42.0 ms: 1.08x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 35.9 ms: 1.08x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.46 ms: 1.08x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 132 ms: 1.07x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.1 ms: 1.07x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.86 ms: 1.06x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 30.5 ms: 1.06x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.97 ms: 1.05x faster                                                   |
| sphinx                           | 434 ms                                                   | 411 ms: 1.05x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 48.9 ms: 1.05x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 10.1 ms: 1.04x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 25.7 ms: 1.04x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 37.5 ms: 1.04x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 936 ns: 1.03x faster                                                    |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.6 ms: 1.03x faster                                                   |
| richards                         | 22.4 ms                                                  | 21.8 ms: 1.03x faster                                                   |
| thrift                           | 322 us                                                   | 313 us: 1.03x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 24.7 ms: 1.03x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 56.5 ms: 1.02x faster                                                   |
| shortest_path                    | 219 ms                                                   | 215 ms: 1.02x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 946 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                    |
| connected_components             | 201 ms                                                   | 199 ms: 1.01x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 103 us: 1.00x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.0 us: 1.01x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 675 ms: 1.02x slower                                                    |
| pidigits                         | 161 ms                                                   | 164 ms: 1.02x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 334 ms: 1.02x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 170 ms: 1.02x slower                                                    |
| 2to3                             | 114 ms                                                   | 117 ms: 1.02x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 429 us: 1.03x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.84 ms: 1.03x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| meteor_contest                   | 47.7 ms                                                  | 49.4 ms: 1.03x slower                                                   |
| fannkuch                         | 176 ms                                                   | 182 ms: 1.04x slower                                                    |
| mako                             | 4.77 ms                                                  | 4.95 ms: 1.04x slower                                                   |
| gc_traversal                     | 2.01 ms                                                  | 2.10 ms: 1.04x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 148 us: 1.06x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 24.5 ms: 1.06x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.65 ms: 1.08x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.21 ms: 1.09x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.1 ms: 1.11x slower                                                   |
| telco                            | 2.61 ms                                                  | 2.91 ms: 1.12x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 947 us: 1.14x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.6 ms: 1.14x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.18x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.9 ms: 1.22x slower                                                   |
| many_optionals                   | 195 us                                                   | 325 us: 1.67x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.5 ms: 2.75x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                            |

Benchmark hidden because not significant (3): json, genshi_xml, pycparser
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250818-3.15.0a0-bc28724/bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.090x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.14x