# Results vs. 3.12.6

- fork: python
- ref: 5197ecb5e4df30ba0f67
- machine: darwin-arm64
- commit hash: 5197ecb
- commit date: 2026-03-10
- overall geometric mean: 1.104x faster
- HPT reliability: 99.83%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7+-5197ecb |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 120 ms: 1.06x slower                                                     |
| docutils       | 1.02 sec                                                 | 998 ms: 1.02x faster                                                     |
| html5lib       | 23.0 ms                                                  | 22.7 ms: 1.01x faster                                                    |
| sphinx         | 434 ms                                                   | 419 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                    | 1.00x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7+-5197ecb |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 243 ms: 2.04x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 235 ms: 2.04x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 238 ms: 1.87x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 246 ms: 1.86x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 143 ms: 1.61x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.58x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.50x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 256 ms: 1.32x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 262 ms: 1.27x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.17x faster                                                     |
| async_generators                 | 206 ms                                                   | 184 ms: 1.12x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 184 ms: 1.03x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 46.5 ms: 1.02x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 128 ms: 1.13x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 92.6 ms: 2.88x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7+-5197ecb |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.7 ms: 1.32x faster                                                    |
| pidigits       | 161 ms                                                   | 164 ms: 1.02x slower                                                     |
| nbody          | 54.2 ms                                                  | 56.5 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7+-5197ecb |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 50.1 ms: 1.09x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 95.3 ms: 1.05x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.23 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7+-5197ecb |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.4 ms: 1.31x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 59.8 ms: 1.14x faster                                                    |
| tomli_loads          | 957 ms                                                   | 844 ms: 1.13x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.95 ms: 1.08x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 36.9 ms: 1.05x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 26.5 ms: 1.01x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 107 us: 1.04x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.3 us: 1.04x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 146 us: 1.05x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7+-5197ecb |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.96 ms: 1.24x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.27 ms: 1.27x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.26x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7+-5197ecb |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 22.8 ms: 1.05x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                    |
| django_template | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                    |
| mako            | 4.77 ms                                                  | 5.63 ms: 1.18x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.10x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7+-5197ecb |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.07 ms: 5.10x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 813 us: 2.47x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 243 ms: 2.04x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 235 ms: 2.04x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 238 ms: 1.87x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 246 ms: 1.86x faster                                                     |
| mdp                              | 1.09 sec                                                 | 603 ms: 1.81x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 507 us: 1.64x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 143 ms: 1.61x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.58x faster                                                     |
| deepcopy                         | 161 us                                                   | 105 us: 1.54x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.50x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.7 us: 1.44x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 256 ms: 1.32x faster                                                     |
| float                            | 37.9 ms                                                  | 28.7 ms: 1.32x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.4 ms: 1.31x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.13 us: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 262 ms: 1.27x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 802 ns: 1.21x faster                                                     |
| go                               | 70.0 ms                                                  | 59.1 ms: 1.19x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 43.2 ns: 1.18x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.37 us: 1.18x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.17x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.93 sec: 1.16x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.4 ms: 1.15x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.15x faster                                                    |
| raytrace                         | 145 ms                                                   | 126 ms: 1.15x faster                                                     |
| pyflate                          | 216 ms                                                   | 190 ms: 1.14x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 59.8 ms: 1.14x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 844 ms: 1.13x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 125 ms: 1.13x faster                                                     |
| k_core                           | 1.12 sec                                                 | 993 ms: 1.13x faster                                                     |
| async_generators                 | 206 ms                                                   | 184 ms: 1.12x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.31 us: 1.11x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 49.2 ms: 1.11x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.56 us: 1.10x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 55.7 ms: 1.10x faster                                                    |
| pycparser                        | 497 ms                                                   | 455 ms: 1.09x faster                                                     |
| pylint                           | 128 ms                                                   | 118 ms: 1.09x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 50.1 ms: 1.09x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.95 ms: 1.08x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 40.4 ms: 1.08x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.9 ms: 1.07x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.9 ms: 1.05x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.64 ms: 1.05x faster                                                    |
| generators                       | 21.9 ms                                                  | 21.0 ms: 1.05x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 95.3 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.23 ms: 1.04x faster                                                    |
| sphinx                           | 434 ms                                                   | 419 ms: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 184 ms: 1.03x faster                                                     |
| docutils                         | 1.02 sec                                                 | 998 ms: 1.02x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.7 ms: 1.01x faster                                                    |
| fannkuch                         | 176 ms                                                   | 173 ms: 1.01x faster                                                     |
| xml_etree_process                | 26.7 ms                                                  | 26.5 ms: 1.01x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 329 ms: 1.00x slower                                                     |
| richards                         | 22.4 ms                                                  | 22.6 ms: 1.01x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.5 ms: 1.01x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 672 ms: 1.01x slower                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 8.13 ms: 1.01x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 25.8 ms: 1.02x slower                                                    |
| pidigits                         | 161 ms                                                   | 164 ms: 1.02x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 46.5 ms: 1.02x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 73.2 us: 1.03x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.14 ms: 1.03x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.15 ms: 1.04x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 107 us: 1.04x slower                                                     |
| nbody                            | 54.2 ms                                                  | 56.5 ms: 1.04x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.3 us: 1.04x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.8 ms: 1.05x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 146 us: 1.05x slower                                                     |
| sympy_str                        | 104 ms                                                   | 109 ms: 1.05x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 60.6 ms: 1.05x slower                                                    |
| 2to3                             | 114 ms                                                   | 120 ms: 1.06x slower                                                     |
| thrift                           | 322 us                                                   | 341 us: 1.06x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 55.0 ms: 1.07x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 42.9 ms: 1.10x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 187 ms: 1.12x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 128 ms: 1.13x slower                                                     |
| shortest_path                    | 219 ms                                                   | 251 ms: 1.15x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 55.0 ms: 1.15x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.01 ms: 1.15x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 46.8 ms: 1.18x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.63 ms: 1.18x slower                                                    |
| connected_components             | 201 ms                                                   | 245 ms: 1.22x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 9.96 ms: 1.24x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.27 ms: 1.27x slower                                                    |
| many_optionals                   | 195 us                                                   | 263 us: 1.34x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 583 us: 1.39x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.7 ms: 1.44x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 92.6 ms: 2.88x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (2): dask, json
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260310-3.15.0a7+-5197ecb-NOGIL/bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7+-5197ecb.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.104x faster

# HPT report

- Reliability score: 99.83% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.37x