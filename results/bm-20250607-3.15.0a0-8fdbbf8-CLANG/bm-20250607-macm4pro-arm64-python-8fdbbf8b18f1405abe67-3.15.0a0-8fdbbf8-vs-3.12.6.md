# Results vs. 3.12.6

- fork: python
- ref: 8fdbbf8b18f1405abe67
- machine: darwin-arm64
- commit hash: 8fdbbf8
- commit date: 2025-06-07
- overall geometric mean: 1.156x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 107 ms: 1.06x faster                                                    |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                  |
| html5lib       | 23.0 ms                                                  | 22.2 ms: 1.04x faster                                                   |
| sphinx         | 434 ms                                                   | 390 ms: 1.11x faster                                                    |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 238 ms: 2.08x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 243 ms: 1.97x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 242 ms: 1.90x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 243 ms: 1.83x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 102 ms: 1.69x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 106 ms: 1.69x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 145 ms: 1.59x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 143 ms: 1.56x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 260 ms: 1.30x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 261 ms: 1.28x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                    |
| async_generators                 | 206 ms                                                   | 169 ms: 1.23x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 39.3 ms: 1.16x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.05x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 191 ms: 1.00x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 246 ms: 1.16x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 84.2 ms: 2.62x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.29x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.4 ms: 1.33x faster                                                   |
| nbody          | 54.2 ms                                                  | 47.6 ms: 1.14x faster                                                   |
| Geometric mean | (ref)                                                    | 1.15x faster                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 43.2 ms: 1.26x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.55 ms: 1.08x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 100 ms: 1.01x slower                                                    |
| regex_v8       | 9.59 ms                                                  | 10.2 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 42.4 ms: 1.22x faster                                                   |
| tomli_loads          | 957 ms                                                   | 796 ms: 1.20x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 32.9 ms: 1.18x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 59.4 ms: 1.14x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 91.1 us: 1.13x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 23.7 ms: 1.13x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 134 us: 1.04x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.8 us: 1.01x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 4.33 ms: 1.02x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.11x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.47 ms: 1.06x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.08 ms: 1.07x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.06x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.01 ms: 1.16x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 19.1 ms: 1.14x faster                                                   |
| mako            | 4.77 ms                                                  | 4.54 ms: 1.05x faster                                                   |
| django_template | 13.6 ms                                                  | 14.0 ms: 1.03x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.08x faster                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.14 ms: 2.27x faster                                                   |
| mdp                              | 1.09 sec                                                 | 501 ms: 2.18x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 238 ms: 2.08x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 243 ms: 1.97x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 242 ms: 1.90x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 243 ms: 1.83x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 102 ms: 1.69x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 106 ms: 1.69x faster                                                    |
| deepcopy                         | 161 us                                                   | 97.8 us: 1.65x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 11.1 us: 1.64x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 145 ms: 1.59x faster                                                    |
| generators                       | 21.9 ms                                                  | 14.0 ms: 1.56x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 143 ms: 1.56x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.01 us: 1.40x faster                                                   |
| go                               | 70.0 ms                                                  | 50.3 ms: 1.39x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.08 us: 1.36x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                   |
| float                            | 37.9 ms                                                  | 28.4 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 260 ms: 1.30x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 261 ms: 1.28x faster                                                    |
| raytrace                         | 145 ms                                                   | 114 ms: 1.28x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 43.2 ms: 1.26x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 16.8 ms: 1.26x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                    |
| async_generators                 | 206 ms                                                   | 169 ms: 1.23x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.50 ms: 1.22x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 42.4 ms: 1.22x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 58.5 us: 1.21x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 796 ms: 1.20x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 50.9 ms: 1.20x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.45 ms: 1.19x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 32.9 ms: 1.18x faster                                                   |
| k_core                           | 1.12 sec                                                 | 948 ms: 1.18x faster                                                    |
| pylint                           | 128 ms                                                   | 109 ms: 1.18x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.92 sec: 1.17x faster                                                  |
| genshi_text                      | 10.5 ms                                                  | 9.01 ms: 1.16x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 39.3 ms: 1.16x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 22.1 ms: 1.15x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 59.4 ms: 1.14x faster                                                   |
| genshi_xml                       | 21.8 ms                                                  | 19.1 ms: 1.14x faster                                                   |
| pyflate                          | 216 ms                                                   | 190 ms: 1.14x faster                                                    |
| nbody                            | 54.2 ms                                                  | 47.6 ms: 1.14x faster                                                   |
| richards                         | 22.4 ms                                                  | 19.7 ms: 1.14x faster                                                   |
| thrift                           | 322 us                                                   | 283 us: 1.14x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.14x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 38.4 ms: 1.13x faster                                                   |
| chaos                            | 28.9 ms                                                  | 25.6 ms: 1.13x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 91.1 us: 1.13x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 23.7 ms: 1.13x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.15 ms: 1.12x faster                                                   |
| sympy_str                        | 104 ms                                                   | 93.1 ms: 1.12x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.9 ms: 1.11x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 48.8 ms: 1.11x faster                                                   |
| sphinx                           | 434 ms                                                   | 390 ms: 1.11x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.53 us: 1.11x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 52.2 ms: 1.10x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.34 us: 1.10x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 46.8 ms: 1.10x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 130 ms: 1.09x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.55 ms: 1.08x faster                                                   |
| sympy_expand                     | 167 ms                                                   | 156 ms: 1.07x faster                                                    |
| pycparser                        | 497 ms                                                   | 466 ms: 1.07x faster                                                    |
| 2to3                             | 114 ms                                                   | 107 ms: 1.06x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.96 ms: 1.06x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.05x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.54 ms: 1.05x faster                                                   |
| json                             | 1.93 ms                                                  | 1.86 ms: 1.04x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 37.4 ms: 1.04x faster                                                   |
| pickle_pure_python               | 139 us                                                   | 134 us: 1.04x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 22.2 ms: 1.04x faster                                                   |
| fannkuch                         | 176 ms                                                   | 171 ms: 1.03x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 945 ns: 1.02x faster                                                    |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                  |
| meteor_contest                   | 47.7 ms                                                  | 47.2 ms: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 325 ms: 1.01x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.8 us: 1.01x faster                                                   |
| pprint_pformat                   | 665 ms                                                   | 660 ms: 1.01x faster                                                    |
| bench_thread_pool                | 419 us                                                   | 416 us: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 191 ms: 1.00x slower                                                    |
| regex_dna                        | 99.6 ms                                                  | 100 ms: 1.01x slower                                                    |
| shortest_path                    | 219 ms                                                   | 221 ms: 1.01x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.33 ms: 1.02x slower                                                   |
| gc_traversal                     | 2.01 ms                                                  | 2.05 ms: 1.02x slower                                                   |
| connected_components             | 201 ms                                                   | 206 ms: 1.03x slower                                                    |
| django_template                  | 13.6 ms                                                  | 14.0 ms: 1.03x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.47 ms: 1.06x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.08 ms: 1.07x slower                                                   |
| regex_v8                         | 9.59 ms                                                  | 10.2 ms: 1.07x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 43.2 ms: 1.09x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 929 us: 1.12x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.14x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.98 ms: 1.14x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 246 ms: 1.16x slower                                                    |
| many_optionals                   | 195 us                                                   | 232 us: 1.19x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.2 ms: 1.20x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 84.2 ms: 2.62x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 193 ns: 3.79x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.14x faster                                                            |

Benchmark hidden because not significant (1): pidigits
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250607-3.15.0a0-8fdbbf8-CLANG/bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.156x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.10x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: 1.15x