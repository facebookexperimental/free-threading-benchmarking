# Results vs. 3.12.6

- fork: python
- ref: 47c249adf3bc2ae3264a
- machine: darwin-arm64
- commit hash: 47c249a
- commit date: 2026-10-31
- overall geometric mean: 1.208x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 109 ms: 1.04x faster                                                        |
| docutils       | 1.02 sec                                                 | 875 ms: 1.17x faster                                                        |
| html5lib       | 23.0 ms                                                  | 19.9 ms: 1.15x faster                                                       |
| sphinx         | 434 ms                                                   | 380 ms: 1.14x faster                                                        |
| Geometric mean | (ref)                                                    | 1.13x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 259 ms: 1.91x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 273 ms: 1.76x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 266 ms: 1.73x faster                                                        |
| async_generators                 | 206 ms                                                   | 122 ms: 1.69x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 107 ms: 1.66x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 276 ms: 1.62x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 109 ms: 1.58x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 155 ms: 1.49x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 158 ms: 1.40x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.34x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 256 ms: 1.30x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 262 ms: 1.29x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 39.8 ms: 1.14x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 212 ms: 1.09x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 184 ms: 1.03x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.13x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 139 ms: 1.23x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.8 ms: 2.86x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.26x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.1 ms: 1.35x faster                                                       |
| nbody          | 54.2 ms                                                  | 45.6 ms: 1.19x faster                                                       |
| pidigits       | 161 ms                                                   | 157 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                    | 1.18x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.33 ms: 1.25x faster                                                       |
| regex_dna      | 99.6 ms                                                  | 85.6 ms: 1.16x faster                                                       |
| regex_v8       | 9.59 ms                                                  | 8.68 ms: 1.10x faster                                                       |
| regex_compile  | 54.6 ms                                                  | 53.4 ms: 1.02x faster                                                       |
| Geometric mean | (ref)                                                    | 1.13x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.6 ms: 1.27x faster                                                       |
| tomli_loads          | 957 ms                                                   | 799 ms: 1.20x faster                                                        |
| json_dumps           | 4.26 ms                                                  | 3.58 ms: 1.19x faster                                                       |
| xml_etree_generate   | 38.9 ms                                                  | 33.4 ms: 1.16x faster                                                       |
| unpickle_pure_python | 103 us                                                   | 91.3 us: 1.13x faster                                                       |
| xml_etree_process    | 26.7 ms                                                  | 24.1 ms: 1.11x faster                                                       |
| xml_etree_parse      | 67.9 ms                                                  | 63.1 ms: 1.08x faster                                                       |
| json_loads           | 10.9 us                                                  | 10.1 us: 1.07x faster                                                       |
| pickle_pure_python   | 139 us                                                   | 137 us: 1.02x faster                                                        |
| Geometric mean       | (ref)                                                    | 1.13x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.11 ms: 1.01x slower                                                       |
| python_startup_no_site | 5.71 ms                                                  | 6.31 ms: 1.11x slower                                                       |
| Geometric mean         | (ref)                                                    | 1.06x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.60 ms: 1.04x faster                                                       |
| django_template | 13.6 ms                                                  | 14.2 ms: 1.04x slower                                                       |
| Geometric mean  | (ref)                                                    | 1.00x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.81 ms: 5.45x faster                                                       |
| pylint                           | 128 ms                                                   | 49.3 ms: 2.60x faster                                                       |
| mdp                              | 1.09 sec                                                 | 506 ms: 2.16x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 259 ms: 1.91x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 273 ms: 1.76x faster                                                        |
| deepcopy                         | 161 us                                                   | 93.3 us: 1.73x faster                                                       |
| async_tree_io                    | 459 ms                                                   | 266 ms: 1.73x faster                                                        |
| async_generators                 | 206 ms                                                   | 122 ms: 1.69x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 107 ms: 1.66x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 276 ms: 1.62x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 109 ms: 1.58x faster                                                        |
| deepcopy_memo                    | 18.3 us                                                  | 11.7 us: 1.56x faster                                                       |
| typing_runtime_protocols         | 71.0 us                                                  | 46.3 us: 1.53x faster                                                       |
| comprehensions                   | 9.84 us                                                  | 6.58 us: 1.50x faster                                                       |
| async_tree_memoization_tg        | 231 ms                                                   | 155 ms: 1.49x faster                                                        |
| deepcopy_reduce                  | 1.46 us                                                  | 1.03 us: 1.42x faster                                                       |
| generators                       | 21.9 ms                                                  | 15.6 ms: 1.41x faster                                                       |
| async_tree_memoization           | 223 ms                                                   | 158 ms: 1.40x faster                                                        |
| create_gc_cycles                 | 830 us                                                   | 597 us: 1.39x faster                                                        |
| go                               | 70.0 ms                                                  | 51.0 ms: 1.37x faster                                                       |
| float                            | 37.9 ms                                                  | 28.1 ms: 1.35x faster                                                       |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.34x faster                                                       |
| spectral_norm                    | 54.4 ms                                                  | 41.6 ms: 1.31x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 256 ms: 1.30x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 262 ms: 1.29x faster                                                        |
| raytrace                         | 145 ms                                                   | 113 ms: 1.29x faster                                                        |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.6 ms: 1.27x faster                                                       |
| scimark_sor                      | 61.0 ms                                                  | 48.2 ms: 1.26x faster                                                       |
| regex_effbot                     | 1.67 ms                                                  | 1.33 ms: 1.25x faster                                                       |
| dulwich_log                      | 21.3 ms                                                  | 17.3 ms: 1.23x faster                                                       |
| nqueens                          | 43.5 ms                                                  | 35.4 ms: 1.23x faster                                                       |
| deltablue                        | 1.73 ms                                                  | 1.42 ms: 1.21x faster                                                       |
| logging_silent                   | 50.9 ns                                                  | 42.0 ns: 1.21x faster                                                       |
| pathlib                          | 12.4 ms                                                  | 10.3 ms: 1.20x faster                                                       |
| tomli_loads                      | 957 ms                                                   | 799 ms: 1.20x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                        |
| json_dumps                       | 4.26 ms                                                  | 3.58 ms: 1.19x faster                                                       |
| scimark_fft                      | 142 ms                                                   | 119 ms: 1.19x faster                                                        |
| nbody                            | 54.2 ms                                                  | 45.6 ms: 1.19x faster                                                       |
| pyflate                          | 216 ms                                                   | 183 ms: 1.18x faster                                                        |
| logging_simple                   | 2.57 us                                                  | 2.19 us: 1.17x faster                                                       |
| gc_traversal                     | 2.01 ms                                                  | 1.71 ms: 1.17x faster                                                       |
| docutils                         | 1.02 sec                                                 | 875 ms: 1.17x faster                                                        |
| chaos                            | 28.9 ms                                                  | 24.8 ms: 1.17x faster                                                       |
| regex_dna                        | 99.6 ms                                                  | 85.6 ms: 1.16x faster                                                       |
| logging_format                   | 2.80 us                                                  | 2.41 us: 1.16x faster                                                       |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.93 sec: 1.16x faster                                                      |
| xml_etree_generate               | 38.9 ms                                                  | 33.4 ms: 1.16x faster                                                       |
| hexiom                           | 3.04 ms                                                  | 2.62 ms: 1.16x faster                                                       |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.8 ms: 1.16x faster                                                       |
| k_core                           | 1.12 sec                                                 | 965 ms: 1.16x faster                                                        |
| html5lib                         | 23.0 ms                                                  | 19.9 ms: 1.15x faster                                                       |
| async_tree_eager                 | 45.6 ms                                                  | 39.8 ms: 1.14x faster                                                       |
| sphinx                           | 434 ms                                                   | 380 ms: 1.14x faster                                                        |
| sympy_integrate                  | 8.02 ms                                                  | 7.06 ms: 1.14x faster                                                       |
| unpickle_pure_python             | 103 us                                                   | 91.3 us: 1.13x faster                                                       |
| xml_etree_process                | 26.7 ms                                                  | 24.1 ms: 1.11x faster                                                       |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.88 ms: 1.11x faster                                                       |
| regex_v8                         | 9.59 ms                                                  | 8.68 ms: 1.10x faster                                                       |
| richards_super                   | 25.4 ms                                                  | 23.1 ms: 1.10x faster                                                       |
| richards                         | 22.4 ms                                                  | 20.4 ms: 1.10x faster                                                       |
| scimark_lu                       | 51.3 ms                                                  | 46.9 ms: 1.09x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 212 ms: 1.09x faster                                                        |
| sympy_str                        | 104 ms                                                   | 95.9 ms: 1.09x faster                                                       |
| sympy_sum                        | 57.6 ms                                                  | 53.1 ms: 1.08x faster                                                       |
| pycparser                        | 497 ms                                                   | 459 ms: 1.08x faster                                                        |
| thrift                           | 322 us                                                   | 298 us: 1.08x faster                                                        |
| crypto_pyaes                     | 38.8 ms                                                  | 36.0 ms: 1.08x faster                                                       |
| xml_etree_parse                  | 67.9 ms                                                  | 63.1 ms: 1.08x faster                                                       |
| json_loads                       | 10.9 us                                                  | 10.1 us: 1.07x faster                                                       |
| sqlite_synth                     | 967 ns                                                   | 905 ns: 1.07x faster                                                        |
| json                             | 1.93 ms                                                  | 1.81 ms: 1.07x faster                                                       |
| pprint_safe_repr                 | 328 ms                                                   | 309 ms: 1.06x faster                                                        |
| pprint_pformat                   | 665 ms                                                   | 631 ms: 1.05x faster                                                        |
| bench_thread_pool                | 419 us                                                   | 400 us: 1.05x faster                                                        |
| 2to3                             | 114 ms                                                   | 109 ms: 1.04x faster                                                        |
| mako                             | 4.77 ms                                                  | 4.60 ms: 1.04x faster                                                       |
| asyncio_websockets               | 190 ms                                                   | 184 ms: 1.03x faster                                                        |
| sympy_expand                     | 167 ms                                                   | 163 ms: 1.03x faster                                                        |
| pidigits                         | 161 ms                                                   | 157 ms: 1.02x faster                                                        |
| regex_compile                    | 54.6 ms                                                  | 53.4 ms: 1.02x faster                                                       |
| pickle_pure_python               | 139 us                                                   | 137 us: 1.02x faster                                                        |
| fannkuch                         | 176 ms                                                   | 173 ms: 1.02x faster                                                        |
| meteor_contest                   | 47.7 ms                                                  | 47.5 ms: 1.01x faster                                                       |
| python_startup                   | 8.01 ms                                                  | 8.11 ms: 1.01x slower                                                       |
| shortest_path                    | 219 ms                                                   | 225 ms: 1.03x slower                                                        |
| connected_components             | 201 ms                                                   | 208 ms: 1.04x slower                                                        |
| django_template                  | 13.6 ms                                                  | 14.2 ms: 1.04x slower                                                       |
| bench_mp_pool                    | 39.7 ms                                                  | 41.7 ms: 1.05x slower                                                       |
| telco                            | 2.61 ms                                                  | 2.75 ms: 1.05x slower                                                       |
| many_optionals                   | 195 us                                                   | 215 us: 1.10x slower                                                        |
| python_startup_no_site           | 5.71 ms                                                  | 6.31 ms: 1.11x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.13x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 139 ms: 1.23x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.8 ms: 2.86x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.20x faster                                                                |
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20261031-3.16.0a1+dev-47c249a-CLANG/bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.208x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.14x
- 95% likely to have a speedup of 1.13x
- 99% likely to have a speedup of 1.11x

# Memory
- memory change: 1.14x