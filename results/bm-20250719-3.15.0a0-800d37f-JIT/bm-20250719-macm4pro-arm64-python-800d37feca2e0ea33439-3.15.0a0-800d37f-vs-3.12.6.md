# Results vs. 3.12.6

- fork: python
- ref: 800d37feca2e0ea33439
- machine: darwin-arm64
- commit hash: 800d37f
- commit date: 2025-07-19
- overall geometric mean: 1.087x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 120 ms: 1.05x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.09 sec: 1.07x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.9 ms: 1.08x slower                                                   |
| sphinx         | 434 ms                                                   | 419 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                    | 1.04x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 259 ms: 1.91x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 254 ms: 1.89x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 259 ms: 1.77x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 261 ms: 1.71x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 108 ms: 1.59x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.55x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 150 ms: 1.54x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.49x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 267 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 270 ms: 1.23x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 113 ms: 1.17x faster                                                    |
| async_generators                 | 206 ms                                                   | 188 ms: 1.10x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 43.1 ms: 1.06x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.02x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 133 ms: 1.18x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 253 ms: 1.19x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.7 ms: 2.79x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.22x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 32.4 ms: 1.17x faster                                                   |
| nbody          | 54.2 ms                                                  | 56.8 ms: 1.05x slower                                                   |
| pidigits       | 161 ms                                                   | 169 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.02x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 49.0 ms: 1.11x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 98.2 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 44.5 ms: 1.16x faster                                                   |
| tomli_loads          | 957 ms                                                   | 828 ms: 1.16x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 34.5 ms: 1.13x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 91.8 us: 1.12x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 24.1 ms: 1.11x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 62.7 ms: 1.08x faster                                                   |
| json_loads           | 10.9 us                                                  | 11.0 us: 1.02x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 144 us: 1.03x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.50 ms: 1.06x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.82 ms: 1.10x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.29 ms: 1.10x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.10x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.44 ms: 1.08x faster                                                   |
| genshi_text     | 10.5 ms                                                  | 10.2 ms: 1.03x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 22.3 ms: 1.02x slower                                                   |
| django_template | 13.6 ms                                                  | 15.9 ms: 1.17x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.02x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 10.0 ms: 2.07x faster                                                   |
| mdp                              | 1.09 sec                                                 | 535 ms: 2.04x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 259 ms: 1.91x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 254 ms: 1.89x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 259 ms: 1.77x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 261 ms: 1.71x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 108 ms: 1.59x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.55x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 150 ms: 1.54x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.49x faster                                                    |
| deepcopy                         | 161 us                                                   | 113 us: 1.43x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 13.0 us: 1.40x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.41 us: 1.33x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 267 ms: 1.27x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.17 us: 1.25x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 270 ms: 1.23x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 42.0 ns: 1.21x faster                                                   |
| go                               | 70.0 ms                                                  | 59.1 ms: 1.18x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 51.6 ms: 1.18x faster                                                   |
| raytrace                         | 145 ms                                                   | 123 ms: 1.18x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 113 ms: 1.17x faster                                                    |
| float                            | 37.9 ms                                                  | 32.4 ms: 1.17x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.5 ms: 1.16x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 828 ms: 1.16x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.5 ms: 1.15x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.1 ms: 1.15x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| k_core                           | 1.12 sec                                                 | 989 ms: 1.13x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 34.5 ms: 1.13x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 91.8 us: 1.12x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 127 ms: 1.12x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.01 sec: 1.12x faster                                                  |
| regex_compile                    | 54.6 ms                                                  | 49.0 ms: 1.11x faster                                                   |
| pprint_pformat                   | 665 ms                                                   | 598 ms: 1.11x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 49.0 ms: 1.11x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 24.1 ms: 1.11x faster                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 296 ms: 1.11x faster                                                    |
| pyflate                          | 216 ms                                                   | 196 ms: 1.10x faster                                                    |
| async_generators                 | 206 ms                                                   | 188 ms: 1.10x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.2 ms: 1.10x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 65.0 us: 1.09x faster                                                   |
| pylint                           | 128 ms                                                   | 118 ms: 1.09x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 62.7 ms: 1.08x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 40.3 ms: 1.08x faster                                                   |
| mako                             | 4.77 ms                                                  | 4.44 ms: 1.08x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 30.0 ms: 1.07x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.62 ms: 1.06x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 43.1 ms: 1.06x faster                                                   |
| chaos                            | 28.9 ms                                                  | 27.6 ms: 1.05x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.70 us: 1.04x faster                                                   |
| sphinx                           | 434 ms                                                   | 419 ms: 1.03x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 49.7 ms: 1.03x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.49 us: 1.03x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 10.2 ms: 1.03x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.79 ms: 1.03x faster                                                   |
| thrift                           | 322 us                                                   | 314 us: 1.03x faster                                                    |
| fannkuch                         | 176 ms                                                   | 172 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 98.2 ms: 1.01x faster                                                   |
| sympy_str                        | 104 ms                                                   | 103 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 38.5 ms: 1.01x faster                                                   |
| richards                         | 22.4 ms                                                  | 22.5 ms: 1.00x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 57.9 ms: 1.01x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.10 ms: 1.01x slower                                                   |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.02x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.0 us: 1.02x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 48.7 ms: 1.02x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 22.3 ms: 1.02x slower                                                   |
| pycparser                        | 497 ms                                                   | 512 ms: 1.03x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 144 us: 1.03x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 173 ms: 1.04x slower                                                    |
| nbody                            | 54.2 ms                                                  | 56.8 ms: 1.05x slower                                                   |
| pidigits                         | 161 ms                                                   | 169 ms: 1.05x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 440 us: 1.05x slower                                                    |
| 2to3                             | 114 ms                                                   | 120 ms: 1.05x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.12 ms: 1.05x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.50 ms: 1.06x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.09 sec: 1.07x slower                                                  |
| shortest_path                    | 219 ms                                                   | 234 ms: 1.07x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 24.9 ms: 1.08x slower                                                   |
| connected_components             | 201 ms                                                   | 218 ms: 1.08x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.82 ms: 1.10x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.29 ms: 1.10x slower                                                   |
| telco                            | 2.61 ms                                                  | 2.93 ms: 1.12x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 45.4 ms: 1.14x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 968 us: 1.17x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.9 ms: 1.17x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 133 ms: 1.18x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 253 ms: 1.19x slower                                                    |
| coverage                         | 26.9 ms                                                  | 33.6 ms: 1.25x slower                                                   |
| many_optionals                   | 195 us                                                   | 261 us: 1.33x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.7 ms: 2.79x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                            |

Benchmark hidden because not significant (5): sqlite_synth, hexiom, richards_super, regex_v8, json
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250719-3.15.0a0-800d37f-JIT/bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.087x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.17x