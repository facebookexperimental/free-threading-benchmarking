# Results vs. default_base_vs_NOGIL

- fork: python
- ref: 410fdda081ba1ca95be0
- machine: darwin-arm64
- commit hash: 410fdda
- commit date: 2026-10-31
- overall geometric mean: 1.100x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                                      | 124 ms: 1.11x slower                                                        |
| docutils       | 887 ms                                                                      | 1.02 sec: 1.15x slower                                                      |
| html5lib       | 19.9 ms                                                                     | 22.5 ms: 1.13x slower                                                       |
| sphinx         | 380 ms                                                                      | 436 ms: 1.15x slower                                                        |
| Geometric mean | (ref)                                                                       | 1.13x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------------------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| asyncio_websockets               | 187 ms                                                                      | 181 ms: 1.03x faster                                                        |
| async_tree_eager_io_tg           | 277 ms                                                                      | 285 ms: 1.03x slower                                                        |
| async_tree_io_tg                 | 275 ms                                                                      | 289 ms: 1.05x slower                                                        |
| async_tree_eager_cpu_io_mixed    | 216 ms                                                                      | 227 ms: 1.05x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 245 ms                                                                      | 263 ms: 1.07x slower                                                        |
| async_tree_cpu_io_mixed_tg       | 267 ms                                                                      | 287 ms: 1.08x slower                                                        |
| async_tree_eager_io              | 262 ms                                                                      | 289 ms: 1.10x slower                                                        |
| async_tree_io                    | 268 ms                                                                      | 297 ms: 1.11x slower                                                        |
| async_tree_eager_memoization     | 111 ms                                                                      | 124 ms: 1.12x slower                                                        |
| async_tree_cpu_io_mixed          | 262 ms                                                                      | 293 ms: 1.12x slower                                                        |
| async_generators                 | 97.6 ms                                                                     | 110 ms: 1.13x slower                                                        |
| async_tree_memoization_tg        | 156 ms                                                                      | 178 ms: 1.14x slower                                                        |
| async_tree_memoization           | 159 ms                                                                      | 182 ms: 1.14x slower                                                        |
| async_tree_eager_memoization_tg  | 140 ms                                                                      | 161 ms: 1.15x slower                                                        |
| async_tree_eager_tg              | 91.8 ms                                                                     | 108 ms: 1.18x slower                                                        |
| async_tree_eager                 | 40.3 ms                                                                     | 48.8 ms: 1.21x slower                                                       |
| coroutines                       | 9.64 ms                                                                     | 11.8 ms: 1.23x slower                                                       |
| async_tree_none_tg               | 109 ms                                                                      | 136 ms: 1.25x slower                                                        |
| async_tree_none                  | 109 ms                                                                      | 139 ms: 1.28x slower                                                        |
| Geometric mean                   | (ref)                                                                       | 1.12x slower                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 158 ms                                                                      | 157 ms: 1.01x faster                                                        |
| float          | 26.8 ms                                                                     | 32.7 ms: 1.22x slower                                                       |
| nbody          | 44.2 ms                                                                     | 58.3 ms: 1.32x slower                                                       |
| Geometric mean | (ref)                                                                       | 1.17x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_v8       | 8.97 ms                                                                     | 8.92 ms: 1.01x faster                                                       |
| regex_dna      | 88.4 ms                                                                     | 88.1 ms: 1.00x faster                                                       |
| regex_effbot   | 1.29 ms                                                                     | 1.31 ms: 1.02x slower                                                       |
| regex_compile  | 52.4 ms                                                                     | 62.5 ms: 1.19x slower                                                       |
| Geometric mean | (ref)                                                                       | 1.05x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_parse      | 61.6 ms                                                                     | 57.6 ms: 1.07x faster                                                       |
| xml_etree_iterparse  | 40.3 ms                                                                     | 40.2 ms: 1.00x faster                                                       |
| json_loads           | 10.3 us                                                                     | 10.6 us: 1.03x slower                                                       |
| json_dumps           | 3.52 ms                                                                     | 3.65 ms: 1.04x slower                                                       |
| tomli_loads          | 797 ms                                                                      | 865 ms: 1.09x slower                                                        |
| xml_etree_generate   | 34.2 ms                                                                     | 37.8 ms: 1.10x slower                                                       |
| pickle_pure_python   | 137 us                                                                      | 155 us: 1.13x slower                                                        |
| unpickle_pure_python | 92.6 us                                                                     | 108 us: 1.16x slower                                                        |
| xml_etree_process    | 24.4 ms                                                                     | 28.8 ms: 1.18x slower                                                       |
| Geometric mean       | (ref)                                                                       | 1.07x slower                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|------------------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 6.33 ms                                                                     | 6.80 ms: 1.07x slower                                                       |
| python_startup         | 8.12 ms                                                                     | 8.78 ms: 1.08x slower                                                       |
| Geometric mean         | (ref)                                                                       | 1.08x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|-----------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| django_template | 14.4 ms                                                                     | 16.6 ms: 1.15x slower                                                       |
| mako            | 4.32 ms                                                                     | 5.40 ms: 1.25x slower                                                       |
| Geometric mean  | (ref)                                                                       | 1.20x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------------------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| gc_traversal                     | 1.73 ms                                                                     | 771 us: 2.24x faster                                                        |
| create_gc_cycles                 | 617 us                                                                      | 455 us: 1.36x faster                                                        |
| sqlite_synth                     | 912 ns                                                                      | 804 ns: 1.14x faster                                                        |
| xml_etree_parse                  | 61.6 ms                                                                     | 57.6 ms: 1.07x faster                                                       |
| asyncio_websockets               | 187 ms                                                                      | 181 ms: 1.03x faster                                                        |
| bench_mp_pool                    | 42.3 ms                                                                     | 41.6 ms: 1.02x faster                                                       |
| pidigits                         | 158 ms                                                                      | 157 ms: 1.01x faster                                                        |
| regex_v8                         | 8.97 ms                                                                     | 8.92 ms: 1.01x faster                                                       |
| xml_etree_iterparse              | 40.3 ms                                                                     | 40.2 ms: 1.00x faster                                                       |
| regex_dna                        | 88.4 ms                                                                     | 88.1 ms: 1.00x faster                                                       |
| bpe_tokeniser                    | 1.89 sec                                                                    | 1.91 sec: 1.01x slower                                                      |
| pathlib                          | 10.4 ms                                                                     | 10.6 ms: 1.01x slower                                                       |
| regex_effbot                     | 1.29 ms                                                                     | 1.31 ms: 1.02x slower                                                       |
| pycparser                        | 456 ms                                                                      | 467 ms: 1.02x slower                                                        |
| json                             | 1.82 ms                                                                     | 1.88 ms: 1.03x slower                                                       |
| k_core                           | 966 ms                                                                      | 994 ms: 1.03x slower                                                        |
| async_tree_eager_io_tg           | 277 ms                                                                      | 285 ms: 1.03x slower                                                        |
| json_loads                       | 10.3 us                                                                     | 10.6 us: 1.03x slower                                                       |
| json_dumps                       | 3.52 ms                                                                     | 3.65 ms: 1.04x slower                                                       |
| async_tree_io_tg                 | 275 ms                                                                      | 289 ms: 1.05x slower                                                        |
| async_tree_eager_cpu_io_mixed    | 216 ms                                                                      | 227 ms: 1.05x slower                                                        |
| dulwich_log                      | 17.6 ms                                                                     | 18.7 ms: 1.06x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 245 ms                                                                      | 263 ms: 1.07x slower                                                        |
| python_startup_no_site           | 6.33 ms                                                                     | 6.80 ms: 1.07x slower                                                       |
| async_tree_cpu_io_mixed_tg       | 267 ms                                                                      | 287 ms: 1.08x slower                                                        |
| python_startup                   | 8.12 ms                                                                     | 8.78 ms: 1.08x slower                                                       |
| telco                            | 2.79 ms                                                                     | 3.02 ms: 1.08x slower                                                       |
| tomli_loads                      | 797 ms                                                                      | 865 ms: 1.09x slower                                                        |
| pyflate                          | 178 ms                                                                      | 193 ms: 1.09x slower                                                        |
| subparsers                       | 3.88 ms                                                                     | 4.22 ms: 1.09x slower                                                       |
| meteor_contest                   | 47.5 ms                                                                     | 51.8 ms: 1.09x slower                                                       |
| shortest_path                    | 224 ms                                                                      | 245 ms: 1.09x slower                                                        |
| xml_etree_generate               | 34.2 ms                                                                     | 37.8 ms: 1.10x slower                                                       |
| async_tree_eager_io              | 262 ms                                                                      | 289 ms: 1.10x slower                                                        |
| 2to3                             | 112 ms                                                                      | 124 ms: 1.11x slower                                                        |
| async_tree_io                    | 268 ms                                                                      | 297 ms: 1.11x slower                                                        |
| sympy_integrate                  | 7.16 ms                                                                     | 7.97 ms: 1.11x slower                                                       |
| sympy_sum                        | 53.5 ms                                                                     | 59.7 ms: 1.12x slower                                                       |
| many_optionals                   | 220 us                                                                      | 246 us: 1.12x slower                                                        |
| async_tree_eager_memoization     | 111 ms                                                                      | 124 ms: 1.12x slower                                                        |
| async_tree_cpu_io_mixed          | 262 ms                                                                      | 293 ms: 1.12x slower                                                        |
| sympy_str                        | 97.0 ms                                                                     | 109 ms: 1.12x slower                                                        |
| sqlglot_v2_normalize             | 42.8 ms                                                                     | 48.1 ms: 1.12x slower                                                       |
| logging_format                   | 2.34 us                                                                     | 2.63 us: 1.13x slower                                                       |
| pprint_safe_repr                 | 305 ms                                                                      | 343 ms: 1.13x slower                                                        |
| sympy_expand                     | 165 ms                                                                      | 186 ms: 1.13x slower                                                        |
| async_generators                 | 97.6 ms                                                                     | 110 ms: 1.13x slower                                                        |
| crypto_pyaes                     | 36.0 ms                                                                     | 40.7 ms: 1.13x slower                                                       |
| html5lib                         | 19.9 ms                                                                     | 22.5 ms: 1.13x slower                                                       |
| pickle_pure_python               | 137 us                                                                      | 155 us: 1.13x slower                                                        |
| deepcopy_reduce                  | 1.03 us                                                                     | 1.17 us: 1.13x slower                                                       |
| sqlglot_v2_optimize              | 20.8 ms                                                                     | 23.6 ms: 1.14x slower                                                       |
| logging_simple                   | 2.11 us                                                                     | 2.40 us: 1.14x slower                                                       |
| deepcopy                         | 95.0 us                                                                     | 108 us: 1.14x slower                                                        |
| thrift                           | 298 us                                                                      | 338 us: 1.14x slower                                                        |
| async_tree_memoization_tg        | 156 ms                                                                      | 178 ms: 1.14x slower                                                        |
| mdp                              | 498 ms                                                                      | 569 ms: 1.14x slower                                                        |
| pprint_pformat                   | 621 ms                                                                      | 709 ms: 1.14x slower                                                        |
| async_tree_memoization           | 159 ms                                                                      | 182 ms: 1.14x slower                                                        |
| fannkuch                         | 157 ms                                                                      | 179 ms: 1.14x slower                                                        |
| sphinx                           | 380 ms                                                                      | 436 ms: 1.15x slower                                                        |
| connected_components             | 207 ms                                                                      | 237 ms: 1.15x slower                                                        |
| docutils                         | 887 ms                                                                      | 1.02 sec: 1.15x slower                                                      |
| async_tree_eager_memoization_tg  | 140 ms                                                                      | 161 ms: 1.15x slower                                                        |
| bench_thread_pool                | 407 us                                                                      | 469 us: 1.15x slower                                                        |
| django_template                  | 14.4 ms                                                                     | 16.6 ms: 1.15x slower                                                       |
| go                               | 50.9 ms                                                                     | 59.3 ms: 1.16x slower                                                       |
| unpickle_pure_python             | 92.6 us                                                                     | 108 us: 1.16x slower                                                        |
| chaos                            | 24.2 ms                                                                     | 28.3 ms: 1.17x slower                                                       |
| sqlglot_v2_transpile             | 579 us                                                                      | 681 us: 1.18x slower                                                        |
| xml_etree_process                | 24.4 ms                                                                     | 28.8 ms: 1.18x slower                                                       |
| async_tree_eager_tg              | 91.8 ms                                                                     | 108 ms: 1.18x slower                                                        |
| logging_silent                   | 41.4 ns                                                                     | 48.9 ns: 1.18x slower                                                       |
| typing_runtime_protocols         | 45.3 us                                                                     | 53.6 us: 1.18x slower                                                       |
| scimark_sor                      | 48.6 ms                                                                     | 57.7 ms: 1.19x slower                                                       |
| sqlglot_v2_parse                 | 473 us                                                                      | 563 us: 1.19x slower                                                        |
| regex_compile                    | 52.4 ms                                                                     | 62.5 ms: 1.19x slower                                                       |
| richards                         | 19.7 ms                                                                     | 23.5 ms: 1.19x slower                                                       |
| spectral_norm                    | 40.5 ms                                                                     | 48.5 ms: 1.20x slower                                                       |
| raytrace                         | 112 ms                                                                      | 134 ms: 1.20x slower                                                        |
| richards_super                   | 22.4 ms                                                                     | 27.1 ms: 1.21x slower                                                       |
| async_tree_eager                 | 40.3 ms                                                                     | 48.8 ms: 1.21x slower                                                       |
| hexiom                           | 2.57 ms                                                                     | 3.12 ms: 1.21x slower                                                       |
| scimark_fft                      | 108 ms                                                                      | 132 ms: 1.21x slower                                                        |
| float                            | 26.8 ms                                                                     | 32.7 ms: 1.22x slower                                                       |
| deepcopy_memo                    | 11.4 us                                                                     | 13.9 us: 1.22x slower                                                       |
| coroutines                       | 9.64 ms                                                                     | 11.8 ms: 1.23x slower                                                       |
| nqueens                          | 34.1 ms                                                                     | 42.1 ms: 1.23x slower                                                       |
| comprehensions                   | 6.52 us                                                                     | 8.07 us: 1.24x slower                                                       |
| scimark_sparse_mat_mult          | 1.76 ms                                                                     | 2.18 ms: 1.24x slower                                                       |
| async_tree_none_tg               | 109 ms                                                                      | 136 ms: 1.25x slower                                                        |
| deltablue                        | 1.42 ms                                                                     | 1.77 ms: 1.25x slower                                                       |
| mako                             | 4.32 ms                                                                     | 5.40 ms: 1.25x slower                                                       |
| scimark_monte_carlo              | 26.3 ms                                                                     | 33.3 ms: 1.27x slower                                                       |
| async_tree_none                  | 109 ms                                                                      | 139 ms: 1.28x slower                                                        |
| nbody                            | 44.2 ms                                                                     | 58.3 ms: 1.32x slower                                                       |
| generators                       | 16.7 ms                                                                     | 22.7 ms: 1.35x slower                                                       |
| scimark_lu                       | 45.7 ms                                                                     | 63.4 ms: 1.39x slower                                                       |
| Geometric mean                   | (ref)                                                                       | 1.11x slower                                                                |

Benchmark hidden because not significant (1): pylint
Ignored benchmarks (8) of results/bm-20261031-3.16.0a1+dev-47c249a/bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (1) of results/bm-20261031-3.16.0a1+dev-410fdda-NOGIL/bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda.json: coverage

- Geometric mean (including insignificant results): 1.100x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.10x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.12x