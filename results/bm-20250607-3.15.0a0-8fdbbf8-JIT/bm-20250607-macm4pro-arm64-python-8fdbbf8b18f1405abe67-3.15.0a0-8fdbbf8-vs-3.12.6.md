# Results vs. 3.12.6

- fork: python
- ref: 8fdbbf8b18f1405abe67
- machine: darwin-arm64
- commit hash: 8fdbbf8
- commit date: 2025-06-07
- overall geometric mean: 1.114x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 113 ms: 1.01x faster                                                    |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.01x slower                                                  |
| html5lib       | 23.0 ms                                                  | 23.7 ms: 1.03x slower                                                   |
| sphinx         | 434 ms                                                   | 404 ms: 1.07x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 242 ms: 2.05x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 248 ms: 1.94x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 247 ms: 1.86x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 252 ms: 1.77x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 104 ms: 1.66x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 108 ms: 1.66x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 145 ms: 1.53x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 259 ms: 1.30x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 261 ms: 1.28x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 180 ms: 1.15x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.5 ms: 1.10x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 86.1 ms: 2.68x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.26x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.7 ms: 1.23x faster                                                   |
| nbody          | 54.2 ms                                                  | 48.8 ms: 1.11x faster                                                   |
| pidigits       | 161 ms                                                   | 161 ms: 1.00x faster                                                    |
| Geometric mean | (ref)                                                    | 1.11x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 47.9 ms: 1.14x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 96.8 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_generate   | 38.9 ms                                                  | 33.7 ms: 1.15x faster                                                   |
| xml_etree_iterparse  | 51.6 ms                                                  | 44.7 ms: 1.15x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 23.2 ms: 1.15x faster                                                   |
| tomli_loads          | 957 ms                                                   | 846 ms: 1.13x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 93.4 us: 1.10x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 63.4 ms: 1.07x faster                                                   |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.02x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 141 us: 1.01x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.38 ms: 1.03x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.54 ms: 1.07x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.12 ms: 1.07x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.07x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.35 ms: 1.10x faster                                                   |
| genshi_text     | 10.5 ms                                                  | 9.81 ms: 1.07x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 21.6 ms: 1.01x faster                                                   |
| django_template | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.01x faster                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.43 ms: 2.20x faster                                                   |
| mdp                              | 1.09 sec                                                 | 513 ms: 2.13x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 242 ms: 2.05x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 248 ms: 1.94x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 247 ms: 1.86x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 252 ms: 1.77x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 104 ms: 1.66x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 108 ms: 1.66x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 145 ms: 1.53x faster                                                    |
| deepcopy                         | 161 us                                                   | 109 us: 1.48x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 13.2 us: 1.39x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.32 us: 1.34x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 259 ms: 1.30x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.14 us: 1.28x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 261 ms: 1.28x faster                                                    |
| generators                       | 21.9 ms                                                  | 17.4 ms: 1.26x faster                                                   |
| float                            | 37.9 ms                                                  | 30.7 ms: 1.23x faster                                                   |
| raytrace                         | 145 ms                                                   | 118 ms: 1.23x faster                                                    |
| go                               | 70.0 ms                                                  | 57.4 ms: 1.22x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 50.7 ms: 1.20x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 17.7 ms: 1.20x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 46.2 ms: 1.18x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 33.7 ms: 1.15x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.7 ms: 1.15x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 23.2 ms: 1.15x faster                                                   |
| async_generators                 | 206 ms                                                   | 180 ms: 1.15x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 47.9 ms: 1.14x faster                                                   |
| pyflate                          | 216 ms                                                   | 190 ms: 1.14x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 62.5 us: 1.14x faster                                                   |
| k_core                           | 1.12 sec                                                 | 986 ms: 1.13x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 846 ms: 1.13x faster                                                    |
| pylint                           | 128 ms                                                   | 113 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                  |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.12x faster                                                   |
| nbody                            | 54.2 ms                                                  | 48.8 ms: 1.11x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 39.2 ms: 1.11x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 93.4 us: 1.10x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.2 ms: 1.10x faster                                                   |
| mako                             | 4.77 ms                                                  | 4.35 ms: 1.10x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 41.5 ms: 1.10x faster                                                   |
| chaos                            | 28.9 ms                                                  | 26.7 ms: 1.08x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.82 ms: 1.08x faster                                                   |
| sphinx                           | 434 ms                                                   | 404 ms: 1.07x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 63.4 ms: 1.07x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.48 ms: 1.07x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 9.81 ms: 1.07x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 48.1 ms: 1.07x faster                                                   |
| thrift                           | 322 us                                                   | 302 us: 1.07x faster                                                    |
| sympy_str                        | 104 ms                                                   | 99.0 ms: 1.05x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.65 ms: 1.05x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 55.1 ms: 1.04x faster                                                   |
| json                             | 1.93 ms                                                  | 1.87 ms: 1.04x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 24.6 ms: 1.03x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 938 ns: 1.03x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.8 ms: 1.03x faster                                                   |
| richards                         | 22.4 ms                                                  | 21.8 ms: 1.03x faster                                                   |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.02x faster                                                   |
| fannkuch                         | 176 ms                                                   | 173 ms: 1.02x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.6 ms: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                    |
| 2to3                             | 114 ms                                                   | 113 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 38.7 ms: 1.00x faster                                                   |
| pidigits                         | 161 ms                                                   | 161 ms: 1.00x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.82 us: 1.01x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.09 ms: 1.01x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 169 ms: 1.01x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 141 us: 1.01x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.01x slower                                                  |
| gc_traversal                     | 2.01 ms                                                  | 2.03 ms: 1.01x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 48.4 ms: 1.01x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.38 ms: 1.03x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 23.7 ms: 1.03x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 434 us: 1.04x slower                                                    |
| shortest_path                    | 219 ms                                                   | 233 ms: 1.06x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.54 ms: 1.07x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.12 ms: 1.07x slower                                                   |
| connected_components             | 201 ms                                                   | 215 ms: 1.07x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 43.3 ms: 1.09x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 910 us: 1.10x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                   |
| telco                            | 2.61 ms                                                  | 2.94 ms: 1.13x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.7 ms: 1.22x slower                                                   |
| many_optionals                   | 195 us                                                   | 241 us: 1.24x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 86.1 ms: 2.68x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 195 ns: 3.83x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                            |

Benchmark hidden because not significant (6): scimark_fft, regex_v8, pprint_safe_repr, logging_simple, pycparser, pprint_pformat
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250607-3.15.0a0-8fdbbf8-JIT/bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.114x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.16x