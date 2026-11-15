# Results vs. 3.12.6

- fork: python
- ref: edd6f7692ad1bb30ba48
- machine: darwin-arm64
- commit hash: edd6f76
- commit date: 2026-11-14
- overall geometric mean: 1.338x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.20x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 112 ms: 1.02x faster                                                        |
| docutils       | 1.02 sec                                                 | 865 ms: 1.18x faster                                                        |
| html5lib       | 23.0 ms                                                  | 17.9 ms: 1.29x faster                                                       |
| sphinx         | 434 ms                                                   | 379 ms: 1.14x faster                                                        |
| Geometric mean | (ref)                                                    | 1.15x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_generators                 | 206 ms                                                   | 105 ms: 1.97x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 252 ms: 1.97x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 261 ms: 1.84x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 255 ms: 1.80x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.67x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 268 ms: 1.66x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 151 ms: 1.53x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 153 ms: 1.45x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 9.93 ms: 1.37x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 258 ms: 1.29x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 266 ms: 1.27x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 36.7 ms: 1.24x faster                                                       |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 217 ms: 1.06x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 139 ms: 1.24x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.3 ms: 2.78x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.29x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 54.2 ms                                                  | 30.8 ms: 1.76x faster                                                       |
| float          | 37.9 ms                                                  | 22.2 ms: 1.71x faster                                                       |
| pidigits       | 161 ms                                                   | 144 ms: 1.12x faster                                                        |
| Geometric mean | (ref)                                                    | 1.50x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.31 ms: 1.27x faster                                                       |
| regex_compile  | 54.6 ms                                                  | 45.6 ms: 1.20x faster                                                       |
| regex_dna      | 99.6 ms                                                  | 89.6 ms: 1.11x faster                                                       |
| regex_v8       | 9.59 ms                                                  | 8.94 ms: 1.07x faster                                                       |
| Geometric mean | (ref)                                                    | 1.16x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| tomli_loads          | 957 ms                                                   | 625 ms: 1.53x faster                                                        |
| unpickle_pure_python | 103 us                                                   | 72.5 us: 1.42x faster                                                       |
| xml_etree_iterparse  | 51.6 ms                                                  | 40.1 ms: 1.29x faster                                                       |
| json_dumps           | 4.26 ms                                                  | 3.32 ms: 1.28x faster                                                       |
| pickle_pure_python   | 139 us                                                   | 109 us: 1.28x faster                                                        |
| xml_etree_process    | 26.7 ms                                                  | 21.6 ms: 1.24x faster                                                       |
| xml_etree_generate   | 38.9 ms                                                  | 31.9 ms: 1.22x faster                                                       |
| xml_etree_parse      | 67.9 ms                                                  | 64.2 ms: 1.06x faster                                                       |
| json_loads           | 10.9 us                                                  | 10.4 us: 1.05x faster                                                       |
| Geometric mean       | (ref)                                                    | 1.25x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.00 ms: 1.00x faster                                                       |
| python_startup_no_site | 5.71 ms                                                  | 6.29 ms: 1.10x slower                                                       |
| Geometric mean         | (ref)                                                    | 1.05x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 3.67 ms: 1.30x faster                                                       |
| django_template | 13.6 ms                                                  | 12.2 ms: 1.12x faster                                                       |
| Geometric mean  | (ref)                                                    | 1.21x faster                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.46 ms: 6.01x faster                                                       |
| pylint                           | 128 ms                                                   | 49.7 ms: 2.58x faster                                                       |
| richards_super                   | 25.4 ms                                                  | 10.9 ms: 2.33x faster                                                       |
| richards                         | 22.4 ms                                                  | 9.65 ms: 2.32x faster                                                       |
| mdp                              | 1.09 sec                                                 | 498 ms: 2.19x faster                                                        |
| async_generators                 | 206 ms                                                   | 105 ms: 1.97x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 252 ms: 1.97x faster                                                        |
| scimark_sor                      | 61.0 ms                                                  | 31.7 ms: 1.92x faster                                                       |
| deepcopy_memo                    | 18.3 us                                                  | 9.74 us: 1.88x faster                                                       |
| comprehensions                   | 9.84 us                                                  | 5.35 us: 1.84x faster                                                       |
| deepcopy                         | 161 us                                                   | 87.9 us: 1.84x faster                                                       |
| async_tree_io_tg                 | 480 ms                                                   | 261 ms: 1.84x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 255 ms: 1.80x faster                                                        |
| typing_runtime_protocols         | 71.0 us                                                  | 40.3 us: 1.76x faster                                                       |
| nbody                            | 54.2 ms                                                  | 30.8 ms: 1.76x faster                                                       |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                        |
| spectral_norm                    | 54.4 ms                                                  | 31.5 ms: 1.73x faster                                                       |
| float                            | 37.9 ms                                                  | 22.2 ms: 1.71x faster                                                       |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.67x faster                                                        |
| scimark_lu                       | 51.3 ms                                                  | 30.8 ms: 1.67x faster                                                       |
| async_tree_eager_io_tg           | 446 ms                                                   | 268 ms: 1.66x faster                                                        |
| scimark_fft                      | 142 ms                                                   | 91.6 ms: 1.55x faster                                                       |
| deepcopy_reduce                  | 1.46 us                                                  | 946 ns: 1.54x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 151 ms: 1.53x faster                                                        |
| tomli_loads                      | 957 ms                                                   | 625 ms: 1.53x faster                                                        |
| logging_silent                   | 50.9 ns                                                  | 33.8 ns: 1.51x faster                                                       |
| deltablue                        | 1.73 ms                                                  | 1.15 ms: 1.50x faster                                                       |
| logging_simple                   | 2.57 us                                                  | 1.74 us: 1.48x faster                                                       |
| logging_format                   | 2.80 us                                                  | 1.90 us: 1.48x faster                                                       |
| go                               | 70.0 ms                                                  | 47.9 ms: 1.46x faster                                                       |
| raytrace                         | 145 ms                                                   | 99.8 ms: 1.45x faster                                                       |
| pyflate                          | 216 ms                                                   | 149 ms: 1.45x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 153 ms: 1.45x faster                                                        |
| nqueens                          | 43.5 ms                                                  | 30.1 ms: 1.44x faster                                                       |
| chaos                            | 28.9 ms                                                  | 20.2 ms: 1.43x faster                                                       |
| unpickle_pure_python             | 103 us                                                   | 72.5 us: 1.42x faster                                                       |
| scimark_monte_carlo              | 32.2 ms                                                  | 22.9 ms: 1.41x faster                                                       |
| coroutines                       | 13.6 ms                                                  | 9.93 ms: 1.37x faster                                                       |
| pprint_safe_repr                 | 328 ms                                                   | 249 ms: 1.32x faster                                                        |
| create_gc_cycles                 | 830 us                                                   | 632 us: 1.31x faster                                                        |
| mako                             | 4.77 ms                                                  | 3.67 ms: 1.30x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 258 ms: 1.29x faster                                                        |
| pprint_pformat                   | 665 ms                                                   | 515 ms: 1.29x faster                                                        |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.1 ms: 1.29x faster                                                       |
| html5lib                         | 23.0 ms                                                  | 17.9 ms: 1.29x faster                                                       |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.75 sec: 1.28x faster                                                      |
| json_dumps                       | 4.26 ms                                                  | 3.32 ms: 1.28x faster                                                       |
| crypto_pyaes                     | 38.8 ms                                                  | 30.4 ms: 1.28x faster                                                       |
| pickle_pure_python               | 139 us                                                   | 109 us: 1.28x faster                                                        |
| dulwich_log                      | 21.3 ms                                                  | 16.7 ms: 1.28x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 266 ms: 1.27x faster                                                        |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.63 ms: 1.27x faster                                                       |
| regex_effbot                     | 1.67 ms                                                  | 1.31 ms: 1.27x faster                                                       |
| hexiom                           | 3.04 ms                                                  | 2.40 ms: 1.27x faster                                                       |
| generators                       | 21.9 ms                                                  | 17.5 ms: 1.25x faster                                                       |
| async_tree_eager                 | 45.6 ms                                                  | 36.7 ms: 1.24x faster                                                       |
| xml_etree_process                | 26.7 ms                                                  | 21.6 ms: 1.24x faster                                                       |
| xml_etree_generate               | 38.9 ms                                                  | 31.9 ms: 1.22x faster                                                       |
| k_core                           | 1.12 sec                                                 | 921 ms: 1.21x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                        |
| regex_compile                    | 54.6 ms                                                  | 45.6 ms: 1.20x faster                                                       |
| pathlib                          | 12.4 ms                                                  | 10.4 ms: 1.19x faster                                                       |
| fannkuch                         | 176 ms                                                   | 147 ms: 1.19x faster                                                        |
| docutils                         | 1.02 sec                                                 | 865 ms: 1.18x faster                                                        |
| sphinx                           | 434 ms                                                   | 379 ms: 1.14x faster                                                        |
| gc_traversal                     | 2.01 ms                                                  | 1.77 ms: 1.14x faster                                                       |
| pidigits                         | 161 ms                                                   | 144 ms: 1.12x faster                                                        |
| django_template                  | 13.6 ms                                                  | 12.2 ms: 1.12x faster                                                       |
| regex_dna                        | 99.6 ms                                                  | 89.6 ms: 1.11x faster                                                       |
| thrift                           | 322 us                                                   | 290 us: 1.11x faster                                                        |
| pycparser                        | 497 ms                                                   | 449 ms: 1.11x faster                                                        |
| sympy_sum                        | 57.6 ms                                                  | 51.9 ms: 1.11x faster                                                       |
| sympy_integrate                  | 8.02 ms                                                  | 7.28 ms: 1.10x faster                                                       |
| sympy_str                        | 104 ms                                                   | 94.8 ms: 1.10x faster                                                       |
| regex_v8                         | 9.59 ms                                                  | 8.94 ms: 1.07x faster                                                       |
| json                             | 1.93 ms                                                  | 1.80 ms: 1.07x faster                                                       |
| meteor_contest                   | 47.7 ms                                                  | 44.7 ms: 1.07x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 217 ms: 1.06x faster                                                        |
| sqlite_synth                     | 967 ns                                                   | 913 ns: 1.06x faster                                                        |
| xml_etree_parse                  | 67.9 ms                                                  | 64.2 ms: 1.06x faster                                                       |
| sympy_expand                     | 167 ms                                                   | 159 ms: 1.05x faster                                                        |
| many_optionals                   | 195 us                                                   | 186 us: 1.05x faster                                                        |
| json_loads                       | 10.9 us                                                  | 10.4 us: 1.05x faster                                                       |
| bench_thread_pool                | 419 us                                                   | 406 us: 1.03x faster                                                        |
| 2to3                             | 114 ms                                                   | 112 ms: 1.02x faster                                                        |
| telco                            | 2.61 ms                                                  | 2.58 ms: 1.01x faster                                                       |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                        |
| connected_components             | 201 ms                                                   | 200 ms: 1.01x faster                                                        |
| shortest_path                    | 219 ms                                                   | 218 ms: 1.00x faster                                                        |
| python_startup                   | 8.01 ms                                                  | 8.00 ms: 1.00x faster                                                       |
| bench_mp_pool                    | 39.7 ms                                                  | 42.0 ms: 1.06x slower                                                       |
| python_startup_no_site           | 5.71 ms                                                  | 6.29 ms: 1.10x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 139 ms: 1.24x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.3 ms: 2.78x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.33x faster                                                                |
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20261114-3.16.0a2+dev-edd6f76-JIT/bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.338x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.25x
- 95% likely to have a speedup of 1.24x
- 99% likely to have a speedup of 1.20x

# Memory
- memory change: 1.18x