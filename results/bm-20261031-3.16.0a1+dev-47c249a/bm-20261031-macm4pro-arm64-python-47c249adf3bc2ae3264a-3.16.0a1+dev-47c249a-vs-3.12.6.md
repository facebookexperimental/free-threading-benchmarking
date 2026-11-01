# Results vs. 3.12.6

- fork: python
- ref: 47c249adf3bc2ae3264a
- machine: darwin-arm64
- commit hash: 47c249a
- commit date: 2026-10-31
- overall geometric mean: 1.216x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 112 ms: 1.02x faster                                                        |
| docutils       | 1.02 sec                                                 | 887 ms: 1.15x faster                                                        |
| html5lib       | 23.0 ms                                                  | 19.9 ms: 1.16x faster                                                       |
| sphinx         | 434 ms                                                   | 380 ms: 1.14x faster                                                        |
| Geometric mean | (ref)                                                    | 1.11x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_generators                 | 206 ms                                                   | 97.6 ms: 2.12x faster                                                       |
| async_tree_eager_io              | 496 ms                                                   | 262 ms: 1.89x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 275 ms: 1.75x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 268 ms: 1.72x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 109 ms: 1.64x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 277 ms: 1.61x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 109 ms: 1.57x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 156 ms: 1.48x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 9.64 ms: 1.41x faster                                                       |
| async_tree_memoization           | 223 ms                                                   | 159 ms: 1.40x faster                                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 262 ms: 1.27x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 267 ms: 1.27x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 40.3 ms: 1.13x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 140 ms: 1.24x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.8 ms: 2.85x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.26x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 26.8 ms: 1.41x faster                                                       |
| nbody          | 54.2 ms                                                  | 44.2 ms: 1.23x faster                                                       |
| pidigits       | 161 ms                                                   | 158 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                    | 1.21x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.29 ms: 1.30x faster                                                       |
| regex_dna      | 99.6 ms                                                  | 88.4 ms: 1.13x faster                                                       |
| regex_v8       | 9.59 ms                                                  | 8.97 ms: 1.07x faster                                                       |
| regex_compile  | 54.6 ms                                                  | 52.4 ms: 1.04x faster                                                       |
| Geometric mean | (ref)                                                    | 1.13x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.3 ms: 1.28x faster                                                       |
| json_dumps           | 4.26 ms                                                  | 3.52 ms: 1.21x faster                                                       |
| tomli_loads          | 957 ms                                                   | 797 ms: 1.20x faster                                                        |
| xml_etree_generate   | 38.9 ms                                                  | 34.2 ms: 1.14x faster                                                       |
| unpickle_pure_python | 103 us                                                   | 92.6 us: 1.11x faster                                                       |
| xml_etree_parse      | 67.9 ms                                                  | 61.6 ms: 1.10x faster                                                       |
| xml_etree_process    | 26.7 ms                                                  | 24.4 ms: 1.09x faster                                                       |
| json_loads           | 10.9 us                                                  | 10.3 us: 1.06x faster                                                       |
| pickle_pure_python   | 139 us                                                   | 137 us: 1.02x faster                                                        |
| Geometric mean       | (ref)                                                    | 1.13x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.12 ms: 1.01x slower                                                       |
| python_startup_no_site | 5.71 ms                                                  | 6.33 ms: 1.11x slower                                                       |
| Geometric mean         | (ref)                                                    | 1.06x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.32 ms: 1.10x faster                                                       |
| django_template | 13.6 ms                                                  | 14.4 ms: 1.05x slower                                                       |
| Geometric mean  | (ref)                                                    | 1.02x faster                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.88 ms: 5.36x faster                                                       |
| pylint                           | 128 ms                                                   | 49.6 ms: 2.58x faster                                                       |
| mdp                              | 1.09 sec                                                 | 498 ms: 2.19x faster                                                        |
| async_generators                 | 206 ms                                                   | 97.6 ms: 2.12x faster                                                       |
| async_tree_eager_io              | 496 ms                                                   | 262 ms: 1.89x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 275 ms: 1.75x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 268 ms: 1.72x faster                                                        |
| deepcopy                         | 161 us                                                   | 95.0 us: 1.70x faster                                                       |
| async_tree_none                  | 178 ms                                                   | 109 ms: 1.64x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 277 ms: 1.61x faster                                                        |
| deepcopy_memo                    | 18.3 us                                                  | 11.4 us: 1.60x faster                                                       |
| async_tree_none_tg               | 172 ms                                                   | 109 ms: 1.57x faster                                                        |
| typing_runtime_protocols         | 71.0 us                                                  | 45.3 us: 1.57x faster                                                       |
| comprehensions                   | 9.84 us                                                  | 6.52 us: 1.51x faster                                                       |
| async_tree_memoization_tg        | 231 ms                                                   | 156 ms: 1.48x faster                                                        |
| deepcopy_reduce                  | 1.46 us                                                  | 1.03 us: 1.41x faster                                                       |
| float                            | 37.9 ms                                                  | 26.8 ms: 1.41x faster                                                       |
| coroutines                       | 13.6 ms                                                  | 9.64 ms: 1.41x faster                                                       |
| async_tree_memoization           | 223 ms                                                   | 159 ms: 1.40x faster                                                        |
| go                               | 70.0 ms                                                  | 50.9 ms: 1.37x faster                                                       |
| create_gc_cycles                 | 830 us                                                   | 617 us: 1.34x faster                                                        |
| spectral_norm                    | 54.4 ms                                                  | 40.5 ms: 1.34x faster                                                       |
| generators                       | 21.9 ms                                                  | 16.7 ms: 1.31x faster                                                       |
| scimark_fft                      | 142 ms                                                   | 108 ms: 1.31x faster                                                        |
| raytrace                         | 145 ms                                                   | 112 ms: 1.30x faster                                                        |
| regex_effbot                     | 1.67 ms                                                  | 1.29 ms: 1.30x faster                                                       |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.3 ms: 1.28x faster                                                       |
| nqueens                          | 43.5 ms                                                  | 34.1 ms: 1.27x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 262 ms: 1.27x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 267 ms: 1.27x faster                                                        |
| scimark_sor                      | 61.0 ms                                                  | 48.6 ms: 1.26x faster                                                       |
| logging_silent                   | 50.9 ns                                                  | 41.4 ns: 1.23x faster                                                       |
| nbody                            | 54.2 ms                                                  | 44.2 ms: 1.23x faster                                                       |
| scimark_monte_carlo              | 32.2 ms                                                  | 26.3 ms: 1.23x faster                                                       |
| deltablue                        | 1.73 ms                                                  | 1.42 ms: 1.22x faster                                                       |
| logging_simple                   | 2.57 us                                                  | 2.11 us: 1.22x faster                                                       |
| pyflate                          | 216 ms                                                   | 178 ms: 1.21x faster                                                        |
| json_dumps                       | 4.26 ms                                                  | 3.52 ms: 1.21x faster                                                       |
| dulwich_log                      | 21.3 ms                                                  | 17.6 ms: 1.21x faster                                                       |
| tomli_loads                      | 957 ms                                                   | 797 ms: 1.20x faster                                                        |
| logging_format                   | 2.80 us                                                  | 2.34 us: 1.20x faster                                                       |
| chaos                            | 28.9 ms                                                  | 24.2 ms: 1.20x faster                                                       |
| pathlib                          | 12.4 ms                                                  | 10.4 ms: 1.19x faster                                                       |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                        |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.89 sec: 1.18x faster                                                      |
| hexiom                           | 3.04 ms                                                  | 2.57 ms: 1.18x faster                                                       |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.76 ms: 1.18x faster                                                       |
| gc_traversal                     | 2.01 ms                                                  | 1.73 ms: 1.16x faster                                                       |
| html5lib                         | 23.0 ms                                                  | 19.9 ms: 1.16x faster                                                       |
| k_core                           | 1.12 sec                                                 | 966 ms: 1.16x faster                                                        |
| docutils                         | 1.02 sec                                                 | 887 ms: 1.15x faster                                                        |
| sphinx                           | 434 ms                                                   | 380 ms: 1.14x faster                                                        |
| richards                         | 22.4 ms                                                  | 19.7 ms: 1.14x faster                                                       |
| xml_etree_generate               | 38.9 ms                                                  | 34.2 ms: 1.14x faster                                                       |
| richards_super                   | 25.4 ms                                                  | 22.4 ms: 1.13x faster                                                       |
| async_tree_eager                 | 45.6 ms                                                  | 40.3 ms: 1.13x faster                                                       |
| regex_dna                        | 99.6 ms                                                  | 88.4 ms: 1.13x faster                                                       |
| scimark_lu                       | 51.3 ms                                                  | 45.7 ms: 1.12x faster                                                       |
| sympy_integrate                  | 8.02 ms                                                  | 7.16 ms: 1.12x faster                                                       |
| fannkuch                         | 176 ms                                                   | 157 ms: 1.12x faster                                                        |
| unpickle_pure_python             | 103 us                                                   | 92.6 us: 1.11x faster                                                       |
| mako                             | 4.77 ms                                                  | 4.32 ms: 1.10x faster                                                       |
| xml_etree_parse                  | 67.9 ms                                                  | 61.6 ms: 1.10x faster                                                       |
| xml_etree_process                | 26.7 ms                                                  | 24.4 ms: 1.09x faster                                                       |
| pycparser                        | 497 ms                                                   | 456 ms: 1.09x faster                                                        |
| thrift                           | 322 us                                                   | 298 us: 1.08x faster                                                        |
| crypto_pyaes                     | 38.8 ms                                                  | 36.0 ms: 1.08x faster                                                       |
| sympy_sum                        | 57.6 ms                                                  | 53.5 ms: 1.08x faster                                                       |
| pprint_safe_repr                 | 328 ms                                                   | 305 ms: 1.08x faster                                                        |
| sympy_str                        | 104 ms                                                   | 97.0 ms: 1.07x faster                                                       |
| pprint_pformat                   | 665 ms                                                   | 621 ms: 1.07x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                        |
| regex_v8                         | 9.59 ms                                                  | 8.97 ms: 1.07x faster                                                       |
| sqlite_synth                     | 967 ns                                                   | 912 ns: 1.06x faster                                                        |
| json                             | 1.93 ms                                                  | 1.82 ms: 1.06x faster                                                       |
| json_loads                       | 10.9 us                                                  | 10.3 us: 1.06x faster                                                       |
| regex_compile                    | 54.6 ms                                                  | 52.4 ms: 1.04x faster                                                       |
| bench_thread_pool                | 419 us                                                   | 407 us: 1.03x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                        |
| pidigits                         | 161 ms                                                   | 158 ms: 1.02x faster                                                        |
| pickle_pure_python               | 139 us                                                   | 137 us: 1.02x faster                                                        |
| 2to3                             | 114 ms                                                   | 112 ms: 1.02x faster                                                        |
| sympy_expand                     | 167 ms                                                   | 165 ms: 1.01x faster                                                        |
| meteor_contest                   | 47.7 ms                                                  | 47.5 ms: 1.00x faster                                                       |
| python_startup                   | 8.01 ms                                                  | 8.12 ms: 1.01x slower                                                       |
| shortest_path                    | 219 ms                                                   | 224 ms: 1.02x slower                                                        |
| connected_components             | 201 ms                                                   | 207 ms: 1.03x slower                                                        |
| django_template                  | 13.6 ms                                                  | 14.4 ms: 1.05x slower                                                       |
| bench_mp_pool                    | 39.7 ms                                                  | 42.3 ms: 1.07x slower                                                       |
| telco                            | 2.61 ms                                                  | 2.79 ms: 1.07x slower                                                       |
| python_startup_no_site           | 5.71 ms                                                  | 6.33 ms: 1.11x slower                                                       |
| many_optionals                   | 195 us                                                   | 220 us: 1.13x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 140 ms: 1.24x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.8 ms: 2.85x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.21x faster                                                                |
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20261031-3.16.0a1+dev-47c249a/bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.216x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.14x
- 95% likely to have a speedup of 1.13x
- 99% likely to have a speedup of 1.12x

# Memory
- memory change: 1.14x