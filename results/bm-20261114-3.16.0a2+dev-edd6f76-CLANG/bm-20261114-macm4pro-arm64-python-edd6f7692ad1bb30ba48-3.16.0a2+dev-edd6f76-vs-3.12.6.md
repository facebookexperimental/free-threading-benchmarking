# Results vs. 3.12.6

- fork: python
- ref: edd6f7692ad1bb30ba48
- machine: darwin-arm64
- commit hash: edd6f76
- commit date: 2026-11-14
- overall geometric mean: 1.185x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 114 ms: 1.00x faster                                                        |
| docutils       | 1.02 sec                                                 | 902 ms: 1.13x faster                                                        |
| html5lib       | 23.0 ms                                                  | 20.5 ms: 1.12x faster                                                       |
| sphinx         | 434 ms                                                   | 387 ms: 1.12x faster                                                        |
| Geometric mean | (ref)                                                    | 1.09x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 268 ms: 1.85x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 284 ms: 1.69x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 276 ms: 1.67x faster                                                        |
| async_generators                 | 206 ms                                                   | 128 ms: 1.62x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 281 ms: 1.59x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.58x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 113 ms: 1.53x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 158 ms: 1.46x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 163 ms: 1.37x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.35x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 271 ms: 1.25x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 41.2 ms: 1.11x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.18x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 142 ms: 1.26x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 94.1 ms: 2.93x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.22x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.1 ms: 1.30x faster                                                       |
| nbody          | 54.2 ms                                                  | 46.6 ms: 1.16x faster                                                       |
| pidigits       | 161 ms                                                   | 146 ms: 1.11x faster                                                        |
| Geometric mean | (ref)                                                    | 1.19x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.32 ms: 1.26x faster                                                       |
| regex_dna      | 99.6 ms                                                  | 87.6 ms: 1.14x faster                                                       |
| regex_v8       | 9.59 ms                                                  | 9.00 ms: 1.07x faster                                                       |
| regex_compile  | 54.6 ms                                                  | 54.2 ms: 1.01x faster                                                       |
| Geometric mean | (ref)                                                    | 1.11x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 41.0 ms: 1.26x faster                                                       |
| json_dumps           | 4.26 ms                                                  | 3.61 ms: 1.18x faster                                                       |
| tomli_loads          | 957 ms                                                   | 814 ms: 1.18x faster                                                        |
| xml_etree_generate   | 38.9 ms                                                  | 33.7 ms: 1.16x faster                                                       |
| unpickle_pure_python | 103 us                                                   | 93.2 us: 1.10x faster                                                       |
| xml_etree_process    | 26.7 ms                                                  | 24.5 ms: 1.09x faster                                                       |
| xml_etree_parse      | 67.9 ms                                                  | 64.2 ms: 1.06x faster                                                       |
| json_loads           | 10.9 us                                                  | 10.8 us: 1.01x faster                                                       |
| Geometric mean       | (ref)                                                    | 1.11x faster                                                                |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 7.99 ms: 1.00x faster                                                       |
| python_startup_no_site | 5.71 ms                                                  | 6.28 ms: 1.10x slower                                                       |
| Geometric mean         | (ref)                                                    | 1.05x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.65 ms: 1.03x faster                                                       |
| django_template | 13.6 ms                                                  | 14.5 ms: 1.07x slower                                                       |
| Geometric mean  | (ref)                                                    | 1.02x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.98 ms: 5.22x faster                                                       |
| pylint                           | 128 ms                                                   | 50.3 ms: 2.55x faster                                                       |
| mdp                              | 1.09 sec                                                 | 518 ms: 2.11x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 268 ms: 1.85x faster                                                        |
| deepcopy                         | 161 us                                                   | 93.6 us: 1.73x faster                                                       |
| async_tree_io_tg                 | 480 ms                                                   | 284 ms: 1.69x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 276 ms: 1.67x faster                                                        |
| async_generators                 | 206 ms                                                   | 128 ms: 1.62x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 281 ms: 1.59x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.58x faster                                                        |
| typing_runtime_protocols         | 71.0 us                                                  | 45.5 us: 1.56x faster                                                       |
| deepcopy_memo                    | 18.3 us                                                  | 11.9 us: 1.54x faster                                                       |
| async_tree_none_tg               | 172 ms                                                   | 113 ms: 1.53x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 158 ms: 1.46x faster                                                        |
| comprehensions                   | 9.84 us                                                  | 6.78 us: 1.45x faster                                                       |
| deepcopy_reduce                  | 1.46 us                                                  | 1.01 us: 1.45x faster                                                       |
| generators                       | 21.9 ms                                                  | 16.0 ms: 1.37x faster                                                       |
| async_tree_memoization           | 223 ms                                                   | 163 ms: 1.37x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.35x faster                                                       |
| go                               | 70.0 ms                                                  | 52.4 ms: 1.34x faster                                                       |
| create_gc_cycles                 | 830 us                                                   | 628 us: 1.32x faster                                                        |
| float                            | 37.9 ms                                                  | 29.1 ms: 1.30x faster                                                       |
| spectral_norm                    | 54.4 ms                                                  | 41.8 ms: 1.30x faster                                                       |
| raytrace                         | 145 ms                                                   | 114 ms: 1.27x faster                                                        |
| scimark_sor                      | 61.0 ms                                                  | 48.2 ms: 1.27x faster                                                       |
| regex_effbot                     | 1.67 ms                                                  | 1.32 ms: 1.26x faster                                                       |
| xml_etree_iterparse              | 51.6 ms                                                  | 41.0 ms: 1.26x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 271 ms: 1.25x faster                                                        |
| nqueens                          | 43.5 ms                                                  | 35.2 ms: 1.23x faster                                                       |
| dulwich_log                      | 21.3 ms                                                  | 17.5 ms: 1.21x faster                                                       |
| scimark_fft                      | 142 ms                                                   | 118 ms: 1.20x faster                                                        |
| logging_silent                   | 50.9 ns                                                  | 42.4 ns: 1.20x faster                                                       |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.74 ms: 1.19x faster                                                       |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.1 ms: 1.19x faster                                                       |
| deltablue                        | 1.73 ms                                                  | 1.46 ms: 1.18x faster                                                       |
| json_dumps                       | 4.26 ms                                                  | 3.61 ms: 1.18x faster                                                       |
| tomli_loads                      | 957 ms                                                   | 814 ms: 1.18x faster                                                        |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.17x faster                                                       |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.92 sec: 1.16x faster                                                      |
| nbody                            | 54.2 ms                                                  | 46.6 ms: 1.16x faster                                                       |
| logging_simple                   | 2.57 us                                                  | 2.21 us: 1.16x faster                                                       |
| pyflate                          | 216 ms                                                   | 186 ms: 1.16x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                        |
| xml_etree_generate               | 38.9 ms                                                  | 33.7 ms: 1.16x faster                                                       |
| k_core                           | 1.12 sec                                                 | 970 ms: 1.15x faster                                                        |
| logging_format                   | 2.80 us                                                  | 2.44 us: 1.15x faster                                                       |
| hexiom                           | 3.04 ms                                                  | 2.66 ms: 1.14x faster                                                       |
| chaos                            | 28.9 ms                                                  | 25.4 ms: 1.14x faster                                                       |
| regex_dna                        | 99.6 ms                                                  | 87.6 ms: 1.14x faster                                                       |
| gc_traversal                     | 2.01 ms                                                  | 1.77 ms: 1.14x faster                                                       |
| docutils                         | 1.02 sec                                                 | 902 ms: 1.13x faster                                                        |
| html5lib                         | 23.0 ms                                                  | 20.5 ms: 1.12x faster                                                       |
| sphinx                           | 434 ms                                                   | 387 ms: 1.12x faster                                                        |
| sympy_integrate                  | 8.02 ms                                                  | 7.22 ms: 1.11x faster                                                       |
| async_tree_eager                 | 45.6 ms                                                  | 41.2 ms: 1.11x faster                                                       |
| pidigits                         | 161 ms                                                   | 146 ms: 1.11x faster                                                        |
| unpickle_pure_python             | 103 us                                                   | 93.2 us: 1.10x faster                                                       |
| scimark_lu                       | 51.3 ms                                                  | 46.7 ms: 1.10x faster                                                       |
| xml_etree_process                | 26.7 ms                                                  | 24.5 ms: 1.09x faster                                                       |
| richards                         | 22.4 ms                                                  | 20.8 ms: 1.08x faster                                                       |
| richards_super                   | 25.4 ms                                                  | 23.6 ms: 1.08x faster                                                       |
| thrift                           | 322 us                                                   | 300 us: 1.07x faster                                                        |
| regex_v8                         | 9.59 ms                                                  | 9.00 ms: 1.07x faster                                                       |
| crypto_pyaes                     | 38.8 ms                                                  | 36.5 ms: 1.06x faster                                                       |
| sympy_str                        | 104 ms                                                   | 98.1 ms: 1.06x faster                                                       |
| pycparser                        | 497 ms                                                   | 469 ms: 1.06x faster                                                        |
| xml_etree_parse                  | 67.9 ms                                                  | 64.2 ms: 1.06x faster                                                       |
| sympy_sum                        | 57.6 ms                                                  | 54.5 ms: 1.06x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                        |
| pprint_safe_repr                 | 328 ms                                                   | 314 ms: 1.04x faster                                                        |
| sqlite_synth                     | 967 ns                                                   | 933 ns: 1.04x faster                                                        |
| pprint_pformat                   | 665 ms                                                   | 645 ms: 1.03x faster                                                        |
| bench_thread_pool                | 419 us                                                   | 407 us: 1.03x faster                                                        |
| mako                             | 4.77 ms                                                  | 4.65 ms: 1.03x faster                                                       |
| json_loads                       | 10.9 us                                                  | 10.8 us: 1.01x faster                                                       |
| regex_compile                    | 54.6 ms                                                  | 54.2 ms: 1.01x faster                                                       |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                                        |
| 2to3                             | 114 ms                                                   | 114 ms: 1.00x faster                                                        |
| python_startup                   | 8.01 ms                                                  | 7.99 ms: 1.00x faster                                                       |
| shortest_path                    | 219 ms                                                   | 224 ms: 1.03x slower                                                        |
| meteor_contest                   | 47.7 ms                                                  | 49.0 ms: 1.03x slower                                                       |
| connected_components             | 201 ms                                                   | 208 ms: 1.04x slower                                                        |
| bench_mp_pool                    | 39.7 ms                                                  | 41.9 ms: 1.06x slower                                                       |
| django_template                  | 13.6 ms                                                  | 14.5 ms: 1.07x slower                                                       |
| telco                            | 2.61 ms                                                  | 2.80 ms: 1.07x slower                                                       |
| python_startup_no_site           | 5.71 ms                                                  | 6.28 ms: 1.10x slower                                                       |
| many_optionals                   | 195 us                                                   | 229 us: 1.17x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.18x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 142 ms: 1.26x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 94.1 ms: 2.93x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.18x faster                                                                |

Benchmark hidden because not significant (4): json, fannkuch, sympy_expand, pickle_pure_python
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20261114-3.16.0a2+dev-edd6f76-CLANG/bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.185x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.12x
- 95% likely to have a speedup of 1.11x
- 99% likely to have a speedup of 1.10x

# Memory
- memory change: 1.15x