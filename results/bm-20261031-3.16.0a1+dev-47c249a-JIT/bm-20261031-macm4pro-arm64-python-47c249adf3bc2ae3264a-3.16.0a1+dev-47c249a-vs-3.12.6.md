# Results vs. 3.12.6

- fork: python
- ref: 47c249adf3bc2ae3264a
- machine: darwin-arm64
- commit hash: 47c249a
- commit date: 2026-10-31
- overall geometric mean: 1.356x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.22x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 111 ms: 1.02x faster                                                        |
| docutils       | 1.02 sec                                                 | 854 ms: 1.20x faster                                                        |
| html5lib       | 23.0 ms                                                  | 17.5 ms: 1.32x faster                                                       |
| sphinx         | 434 ms                                                   | 373 ms: 1.16x faster                                                        |
| Geometric mean | (ref)                                                    | 1.17x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 242 ms: 2.05x faster                                                        |
| async_generators                 | 206 ms                                                   | 105 ms: 1.97x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 256 ms: 1.88x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 246 ms: 1.87x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 97.7 ms: 1.82x faster                                                       |
| async_tree_eager_io_tg           | 446 ms                                                   | 258 ms: 1.73x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 100 ms: 1.72x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 149 ms: 1.55x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 150 ms: 1.49x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 9.67 ms: 1.40x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 252 ms: 1.32x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 260 ms: 1.30x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 35.7 ms: 1.28x faster                                                       |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 211 ms: 1.09x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 242 ms: 1.14x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 137 ms: 1.22x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.0 ms: 2.71x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.32x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 54.2 ms                                                  | 30.8 ms: 1.76x faster                                                       |
| float          | 37.9 ms                                                  | 21.7 ms: 1.75x faster                                                       |
| pidigits       | 161 ms                                                   | 158 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                    | 1.47x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.29 ms: 1.29x faster                                                       |
| regex_compile  | 54.6 ms                                                  | 44.9 ms: 1.22x faster                                                       |
| regex_dna      | 99.6 ms                                                  | 88.3 ms: 1.13x faster                                                       |
| regex_v8       | 9.59 ms                                                  | 8.91 ms: 1.08x faster                                                       |
| Geometric mean | (ref)                                                    | 1.18x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| tomli_loads          | 957 ms                                                   | 610 ms: 1.57x faster                                                        |
| unpickle_pure_python | 103 us                                                   | 72.6 us: 1.42x faster                                                       |
| xml_etree_iterparse  | 51.6 ms                                                  | 39.1 ms: 1.32x faster                                                       |
| pickle_pure_python   | 139 us                                                   | 108 us: 1.29x faster                                                        |
| json_dumps           | 4.26 ms                                                  | 3.31 ms: 1.29x faster                                                       |
| xml_etree_process    | 26.7 ms                                                  | 21.5 ms: 1.24x faster                                                       |
| xml_etree_generate   | 38.9 ms                                                  | 32.0 ms: 1.21x faster                                                       |
| xml_etree_parse      | 67.9 ms                                                  | 61.8 ms: 1.10x faster                                                       |
| json_loads           | 10.9 us                                                  | 10.1 us: 1.08x faster                                                       |
| Geometric mean       | (ref)                                                    | 1.27x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.18 ms: 1.02x slower                                                       |
| python_startup_no_site | 5.71 ms                                                  | 6.36 ms: 1.12x slower                                                       |
| Geometric mean         | (ref)                                                    | 1.07x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 3.70 ms: 1.29x faster                                                       |
| django_template | 13.6 ms                                                  | 12.1 ms: 1.13x faster                                                       |
| Geometric mean  | (ref)                                                    | 1.21x faster                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.44 ms: 6.04x faster                                                       |
| pylint                           | 128 ms                                                   | 49.1 ms: 2.61x faster                                                       |
| richards                         | 22.4 ms                                                  | 9.46 ms: 2.37x faster                                                       |
| richards_super                   | 25.4 ms                                                  | 10.8 ms: 2.35x faster                                                       |
| mdp                              | 1.09 sec                                                 | 494 ms: 2.21x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 242 ms: 2.05x faster                                                        |
| async_generators                 | 206 ms                                                   | 105 ms: 1.97x faster                                                        |
| scimark_sor                      | 61.0 ms                                                  | 31.3 ms: 1.95x faster                                                       |
| deepcopy_memo                    | 18.3 us                                                  | 9.60 us: 1.91x faster                                                       |
| async_tree_io_tg                 | 480 ms                                                   | 256 ms: 1.88x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 246 ms: 1.87x faster                                                        |
| comprehensions                   | 9.84 us                                                  | 5.31 us: 1.85x faster                                                       |
| async_tree_none                  | 178 ms                                                   | 97.7 ms: 1.82x faster                                                       |
| deepcopy                         | 161 us                                                   | 89.3 us: 1.81x faster                                                       |
| nbody                            | 54.2 ms                                                  | 30.8 ms: 1.76x faster                                                       |
| float                            | 37.9 ms                                                  | 21.7 ms: 1.75x faster                                                       |
| typing_runtime_protocols         | 71.0 us                                                  | 40.6 us: 1.75x faster                                                       |
| spectral_norm                    | 54.4 ms                                                  | 31.3 ms: 1.74x faster                                                       |
| async_tree_eager_io_tg           | 446 ms                                                   | 258 ms: 1.73x faster                                                        |
| scimark_lu                       | 51.3 ms                                                  | 29.8 ms: 1.72x faster                                                       |
| async_tree_none_tg               | 172 ms                                                   | 100 ms: 1.72x faster                                                        |
| tomli_loads                      | 957 ms                                                   | 610 ms: 1.57x faster                                                        |
| scimark_fft                      | 142 ms                                                   | 90.9 ms: 1.56x faster                                                       |
| async_tree_memoization_tg        | 231 ms                                                   | 149 ms: 1.55x faster                                                        |
| deltablue                        | 1.73 ms                                                  | 1.13 ms: 1.53x faster                                                       |
| logging_simple                   | 2.57 us                                                  | 1.68 us: 1.53x faster                                                       |
| logging_silent                   | 50.9 ns                                                  | 33.4 ns: 1.52x faster                                                       |
| deepcopy_reduce                  | 1.46 us                                                  | 960 ns: 1.52x faster                                                        |
| logging_format                   | 2.80 us                                                  | 1.86 us: 1.51x faster                                                       |
| go                               | 70.0 ms                                                  | 46.6 ms: 1.50x faster                                                       |
| async_tree_memoization           | 223 ms                                                   | 150 ms: 1.49x faster                                                        |
| raytrace                         | 145 ms                                                   | 97.6 ms: 1.49x faster                                                       |
| nqueens                          | 43.5 ms                                                  | 29.8 ms: 1.46x faster                                                       |
| pyflate                          | 216 ms                                                   | 148 ms: 1.46x faster                                                        |
| chaos                            | 28.9 ms                                                  | 19.8 ms: 1.46x faster                                                       |
| unpickle_pure_python             | 103 us                                                   | 72.6 us: 1.42x faster                                                       |
| coroutines                       | 13.6 ms                                                  | 9.67 ms: 1.40x faster                                                       |
| scimark_monte_carlo              | 32.2 ms                                                  | 23.1 ms: 1.39x faster                                                       |
| create_gc_cycles                 | 830 us                                                   | 611 us: 1.36x faster                                                        |
| pprint_safe_repr                 | 328 ms                                                   | 243 ms: 1.35x faster                                                        |
| pprint_pformat                   | 665 ms                                                   | 501 ms: 1.33x faster                                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 252 ms: 1.32x faster                                                        |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.1 ms: 1.32x faster                                                       |
| html5lib                         | 23.0 ms                                                  | 17.5 ms: 1.32x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 260 ms: 1.30x faster                                                        |
| hexiom                           | 3.04 ms                                                  | 2.35 ms: 1.29x faster                                                       |
| regex_effbot                     | 1.67 ms                                                  | 1.29 ms: 1.29x faster                                                       |
| mako                             | 4.77 ms                                                  | 3.70 ms: 1.29x faster                                                       |
| pickle_pure_python               | 139 us                                                   | 108 us: 1.29x faster                                                        |
| json_dumps                       | 4.26 ms                                                  | 3.31 ms: 1.29x faster                                                       |
| crypto_pyaes                     | 38.8 ms                                                  | 30.2 ms: 1.28x faster                                                       |
| generators                       | 21.9 ms                                                  | 17.2 ms: 1.28x faster                                                       |
| async_tree_eager                 | 45.6 ms                                                  | 35.7 ms: 1.28x faster                                                       |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.63 ms: 1.28x faster                                                       |
| dulwich_log                      | 21.3 ms                                                  | 16.8 ms: 1.27x faster                                                       |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.77 sec: 1.26x faster                                                      |
| xml_etree_process                | 26.7 ms                                                  | 21.5 ms: 1.24x faster                                                       |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                        |
| fannkuch                         | 176 ms                                                   | 144 ms: 1.22x faster                                                        |
| k_core                           | 1.12 sec                                                 | 917 ms: 1.22x faster                                                        |
| regex_compile                    | 54.6 ms                                                  | 44.9 ms: 1.22x faster                                                       |
| xml_etree_generate               | 38.9 ms                                                  | 32.0 ms: 1.21x faster                                                       |
| pathlib                          | 12.4 ms                                                  | 10.2 ms: 1.21x faster                                                       |
| docutils                         | 1.02 sec                                                 | 854 ms: 1.20x faster                                                        |
| sympy_sum                        | 57.6 ms                                                  | 48.9 ms: 1.18x faster                                                       |
| sphinx                           | 434 ms                                                   | 373 ms: 1.16x faster                                                        |
| gc_traversal                     | 2.01 ms                                                  | 1.74 ms: 1.16x faster                                                       |
| thrift                           | 322 us                                                   | 282 us: 1.14x faster                                                        |
| sympy_integrate                  | 8.02 ms                                                  | 7.10 ms: 1.13x faster                                                       |
| regex_dna                        | 99.6 ms                                                  | 88.3 ms: 1.13x faster                                                       |
| django_template                  | 13.6 ms                                                  | 12.1 ms: 1.13x faster                                                       |
| pycparser                        | 497 ms                                                   | 442 ms: 1.12x faster                                                        |
| sympy_str                        | 104 ms                                                   | 92.9 ms: 1.12x faster                                                       |
| xml_etree_parse                  | 67.9 ms                                                  | 61.8 ms: 1.10x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 211 ms: 1.09x faster                                                        |
| json                             | 1.93 ms                                                  | 1.77 ms: 1.09x faster                                                       |
| meteor_contest                   | 47.7 ms                                                  | 43.9 ms: 1.09x faster                                                       |
| regex_v8                         | 9.59 ms                                                  | 8.91 ms: 1.08x faster                                                       |
| json_loads                       | 10.9 us                                                  | 10.1 us: 1.08x faster                                                       |
| sympy_expand                     | 167 ms                                                   | 155 ms: 1.07x faster                                                        |
| sqlite_synth                     | 967 ns                                                   | 902 ns: 1.07x faster                                                        |
| many_optionals                   | 195 us                                                   | 185 us: 1.05x faster                                                        |
| telco                            | 2.61 ms                                                  | 2.52 ms: 1.04x faster                                                       |
| bench_thread_pool                | 419 us                                                   | 408 us: 1.03x faster                                                        |
| 2to3                             | 114 ms                                                   | 111 ms: 1.02x faster                                                        |
| pidigits                         | 161 ms                                                   | 158 ms: 1.02x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                        |
| shortest_path                    | 219 ms                                                   | 218 ms: 1.01x faster                                                        |
| connected_components             | 201 ms                                                   | 200 ms: 1.00x faster                                                        |
| python_startup                   | 8.01 ms                                                  | 8.18 ms: 1.02x slower                                                       |
| bench_mp_pool                    | 39.7 ms                                                  | 42.6 ms: 1.07x slower                                                       |
| python_startup_no_site           | 5.71 ms                                                  | 6.36 ms: 1.12x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 242 ms: 1.14x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 137 ms: 1.22x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.0 ms: 2.71x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.35x faster                                                                |
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20261031-3.16.0a1+dev-47c249a-JIT/bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.356x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.26x
- 95% likely to have a speedup of 1.25x
- 99% likely to have a speedup of 1.22x

# Memory
- memory change: 1.19x