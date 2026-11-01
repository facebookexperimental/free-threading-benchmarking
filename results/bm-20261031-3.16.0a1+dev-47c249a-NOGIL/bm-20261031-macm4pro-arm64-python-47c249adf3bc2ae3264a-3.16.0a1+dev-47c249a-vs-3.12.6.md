# Results vs. 3.12.6

- fork: python
- ref: 47c249adf3bc2ae3264a
- machine: darwin-arm64
- commit hash: 47c249a
- commit date: 2026-10-31
- overall geometric mean: 1.089x faster
- HPT reliability: 98.93%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 124 ms: 1.09x slower                                                        |
| html5lib       | 23.0 ms                                                  | 22.5 ms: 1.02x faster                                                       |
| Geometric mean | (ref)                                                    | 1.02x slower                                                                |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_generators                 | 206 ms                                                   | 110 ms: 1.87x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 290 ms: 1.71x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 290 ms: 1.65x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 286 ms: 1.56x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 296 ms: 1.55x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 178 ms: 1.30x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 138 ms: 1.29x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 136 ms: 1.26x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 182 ms: 1.23x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 287 ms: 1.18x faster                                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 293 ms: 1.14x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 11.9 ms: 1.14x faster                                                       |
| async_tree_eager_memoization     | 132 ms                                                   | 124 ms: 1.06x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 182 ms: 1.05x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 227 ms: 1.02x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 48.6 ms: 1.07x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 262 ms: 1.23x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 161 ms: 1.43x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 108 ms: 3.37x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.12x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 32.5 ms: 1.17x faster                                                       |
| pidigits       | 161 ms                                                   | 157 ms: 1.03x faster                                                        |
| nbody          | 54.2 ms                                                  | 58.0 ms: 1.07x slower                                                       |
| Geometric mean | (ref)                                                    | 1.04x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.30 ms: 1.28x faster                                                       |
| regex_dna      | 99.6 ms                                                  | 88.3 ms: 1.13x faster                                                       |
| regex_v8       | 9.59 ms                                                  | 8.93 ms: 1.07x faster                                                       |
| regex_compile  | 54.6 ms                                                  | 62.6 ms: 1.15x slower                                                       |
| Geometric mean | (ref)                                                    | 1.08x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.1 ms: 1.29x faster                                                       |
| xml_etree_parse      | 67.9 ms                                                  | 57.3 ms: 1.19x faster                                                       |
| json_dumps           | 4.26 ms                                                  | 3.74 ms: 1.14x faster                                                       |
| tomli_loads          | 957 ms                                                   | 873 ms: 1.10x faster                                                        |
| json_loads           | 10.9 us                                                  | 10.5 us: 1.04x faster                                                       |
| xml_etree_generate   | 38.9 ms                                                  | 37.7 ms: 1.03x faster                                                       |
| unpickle_pure_python | 103 us                                                   | 108 us: 1.05x slower                                                        |
| xml_etree_process    | 26.7 ms                                                  | 28.9 ms: 1.08x slower                                                       |
| pickle_pure_python   | 139 us                                                   | 155 us: 1.11x slower                                                        |
| Geometric mean       | (ref)                                                    | 1.05x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.77 ms: 1.09x slower                                                       |
| python_startup_no_site | 5.71 ms                                                  | 6.80 ms: 1.19x slower                                                       |
| Geometric mean         | (ref)                                                    | 1.14x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 5.42 ms: 1.14x slower                                                       |
| django_template | 13.6 ms                                                  | 16.8 ms: 1.23x slower                                                       |
| Geometric mean  | (ref)                                                    | 1.18x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.21 ms: 4.93x faster                                                       |
| gc_traversal                     | 2.01 ms                                                  | 763 us: 2.63x faster                                                        |
| pylint                           | 128 ms                                                   | 50.5 ms: 2.54x faster                                                       |
| mdp                              | 1.09 sec                                                 | 578 ms: 1.89x faster                                                        |
| async_generators                 | 206 ms                                                   | 110 ms: 1.87x faster                                                        |
| create_gc_cycles                 | 830 us                                                   | 457 us: 1.82x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 290 ms: 1.71x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 290 ms: 1.65x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 286 ms: 1.56x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 296 ms: 1.55x faster                                                        |
| deepcopy                         | 161 us                                                   | 108 us: 1.50x faster                                                        |
| typing_runtime_protocols         | 71.0 us                                                  | 53.2 us: 1.33x faster                                                       |
| deepcopy_memo                    | 18.3 us                                                  | 14.0 us: 1.31x faster                                                       |
| async_tree_memoization_tg        | 231 ms                                                   | 178 ms: 1.30x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 138 ms: 1.29x faster                                                        |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.1 ms: 1.29x faster                                                       |
| regex_effbot                     | 1.67 ms                                                  | 1.30 ms: 1.28x faster                                                       |
| async_tree_none_tg               | 172 ms                                                   | 136 ms: 1.26x faster                                                        |
| deepcopy_reduce                  | 1.46 us                                                  | 1.17 us: 1.24x faster                                                       |
| comprehensions                   | 9.84 us                                                  | 8.00 us: 1.23x faster                                                       |
| async_tree_memoization           | 223 ms                                                   | 182 ms: 1.23x faster                                                        |
| sqlite_synth                     | 967 ns                                                   | 805 ns: 1.20x faster                                                        |
| xml_etree_parse                  | 67.9 ms                                                  | 57.3 ms: 1.19x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 287 ms: 1.18x faster                                                        |
| go                               | 70.0 ms                                                  | 59.4 ms: 1.18x faster                                                       |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.17x faster                                                       |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.92 sec: 1.17x faster                                                      |
| float                            | 37.9 ms                                                  | 32.5 ms: 1.17x faster                                                       |
| json_dumps                       | 4.26 ms                                                  | 3.74 ms: 1.14x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 293 ms: 1.14x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 11.9 ms: 1.14x faster                                                       |
| k_core                           | 1.12 sec                                                 | 985 ms: 1.14x faster                                                        |
| dulwich_log                      | 21.3 ms                                                  | 18.8 ms: 1.13x faster                                                       |
| regex_dna                        | 99.6 ms                                                  | 88.3 ms: 1.13x faster                                                       |
| spectral_norm                    | 54.4 ms                                                  | 48.5 ms: 1.12x faster                                                       |
| pyflate                          | 216 ms                                                   | 193 ms: 1.12x faster                                                        |
| tomli_loads                      | 957 ms                                                   | 873 ms: 1.10x faster                                                        |
| scimark_fft                      | 142 ms                                                   | 130 ms: 1.09x faster                                                        |
| regex_v8                         | 9.59 ms                                                  | 8.93 ms: 1.07x faster                                                       |
| raytrace                         | 145 ms                                                   | 135 ms: 1.07x faster                                                        |
| logging_simple                   | 2.57 us                                                  | 2.40 us: 1.07x faster                                                       |
| pycparser                        | 497 ms                                                   | 467 ms: 1.06x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 124 ms: 1.06x faster                                                        |
| scimark_sor                      | 61.0 ms                                                  | 57.4 ms: 1.06x faster                                                       |
| logging_format                   | 2.80 us                                                  | 2.64 us: 1.06x faster                                                       |
| asyncio_websockets               | 190 ms                                                   | 182 ms: 1.05x faster                                                        |
| logging_silent                   | 50.9 ns                                                  | 48.9 ns: 1.04x faster                                                       |
| json_loads                       | 10.9 us                                                  | 10.5 us: 1.04x faster                                                       |
| nqueens                          | 43.5 ms                                                  | 42.1 ms: 1.03x faster                                                       |
| json                             | 1.93 ms                                                  | 1.87 ms: 1.03x faster                                                       |
| xml_etree_generate               | 38.9 ms                                                  | 37.7 ms: 1.03x faster                                                       |
| pidigits                         | 161 ms                                                   | 157 ms: 1.03x faster                                                        |
| html5lib                         | 23.0 ms                                                  | 22.5 ms: 1.02x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 227 ms: 1.02x faster                                                        |
| chaos                            | 28.9 ms                                                  | 28.4 ms: 1.02x faster                                                       |
| sympy_integrate                  | 8.02 ms                                                  | 7.93 ms: 1.01x faster                                                       |
| deltablue                        | 1.73 ms                                                  | 1.76 ms: 1.02x slower                                                       |
| fannkuch                         | 176 ms                                                   | 180 ms: 1.03x slower                                                        |
| hexiom                           | 3.04 ms                                                  | 3.12 ms: 1.03x slower                                                       |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.2 ms: 1.03x slower                                                       |
| sympy_sum                        | 57.6 ms                                                  | 59.7 ms: 1.04x slower                                                       |
| generators                       | 21.9 ms                                                  | 22.8 ms: 1.04x slower                                                       |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.16 ms: 1.04x slower                                                       |
| bench_mp_pool                    | 39.7 ms                                                  | 41.5 ms: 1.05x slower                                                       |
| pprint_safe_repr                 | 328 ms                                                   | 343 ms: 1.05x slower                                                        |
| unpickle_pure_python             | 103 us                                                   | 108 us: 1.05x slower                                                        |
| sympy_str                        | 104 ms                                                   | 109 ms: 1.05x slower                                                        |
| crypto_pyaes                     | 38.8 ms                                                  | 41.0 ms: 1.05x slower                                                       |
| thrift                           | 322 us                                                   | 341 us: 1.06x slower                                                        |
| pprint_pformat                   | 665 ms                                                   | 706 ms: 1.06x slower                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 48.6 ms: 1.07x slower                                                       |
| richards                         | 22.4 ms                                                  | 23.9 ms: 1.07x slower                                                       |
| nbody                            | 54.2 ms                                                  | 58.0 ms: 1.07x slower                                                       |
| richards_super                   | 25.4 ms                                                  | 27.2 ms: 1.07x slower                                                       |
| xml_etree_process                | 26.7 ms                                                  | 28.9 ms: 1.08x slower                                                       |
| meteor_contest                   | 47.7 ms                                                  | 51.7 ms: 1.08x slower                                                       |
| 2to3                             | 114 ms                                                   | 124 ms: 1.09x slower                                                        |
| python_startup                   | 8.01 ms                                                  | 8.77 ms: 1.09x slower                                                       |
| sympy_expand                     | 167 ms                                                   | 186 ms: 1.11x slower                                                        |
| pickle_pure_python               | 139 us                                                   | 155 us: 1.11x slower                                                        |
| bench_thread_pool                | 419 us                                                   | 467 us: 1.12x slower                                                        |
| shortest_path                    | 219 ms                                                   | 246 ms: 1.13x slower                                                        |
| mako                             | 4.77 ms                                                  | 5.42 ms: 1.14x slower                                                       |
| regex_compile                    | 54.6 ms                                                  | 62.6 ms: 1.15x slower                                                       |
| telco                            | 2.61 ms                                                  | 3.00 ms: 1.15x slower                                                       |
| connected_components             | 201 ms                                                   | 238 ms: 1.19x slower                                                        |
| python_startup_no_site           | 5.71 ms                                                  | 6.80 ms: 1.19x slower                                                       |
| django_template                  | 13.6 ms                                                  | 16.8 ms: 1.23x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 262 ms: 1.23x slower                                                        |
| many_optionals                   | 195 us                                                   | 247 us: 1.27x slower                                                        |
| scimark_lu                       | 51.3 ms                                                  | 66.0 ms: 1.29x slower                                                       |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 161 ms: 1.43x slower                                                        |
| coverage                         | 26.9 ms                                                  | 40.2 ms: 1.49x slower                                                       |
| async_tree_eager_tg              | 32.1 ms                                                  | 108 ms: 3.37x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                                |

Benchmark hidden because not significant (2): docutils, sphinx
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20261031-3.16.0a1+dev-47c249a-NOGIL/bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.089x faster

# HPT report

- Reliability score: 98.93% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.27x