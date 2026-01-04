# Results vs. 3.12.6

- fork: python
- ref: 9609574e7fd36edfaa8b
- machine: darwin-arm64
- commit hash: 9609574
- commit date: 2026-01-03
- overall geometric mean: 1.163x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 112 ms: 1.01x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.02 sec: 1.00x faster                                                   |
| html5lib       | 23.0 ms                                                  | 21.6 ms: 1.06x faster                                                    |
| sphinx         | 434 ms                                                   | 391 ms: 1.11x faster                                                     |
| Geometric mean | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 228 ms: 2.17x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 225 ms: 2.13x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 220 ms: 2.02x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 234 ms: 1.97x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.74x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 99.7 ms: 1.73x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 136 ms: 1.70x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 139 ms: 1.60x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 253 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 250 ms: 1.33x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 106 ms: 1.24x faster                                                     |
| async_generators                 | 206 ms                                                   | 174 ms: 1.18x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.7 ms: 1.12x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 119 ms: 1.06x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 240 ms: 1.13x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.8 ms: 2.48x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.33x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.1 ms: 1.40x faster                                                    |
| nbody          | 54.2 ms                                                  | 45.7 ms: 1.19x faster                                                    |
| pidigits       | 161 ms                                                   | 162 ms: 1.00x slower                                                     |
| Geometric mean | (ref)                                                    | 1.18x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 45.1 ms: 1.21x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.50 ms: 1.11x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 97.6 ms: 1.02x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.72 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.0 ms: 1.29x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 34.5 ms: 1.13x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.89 ms: 1.09x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.5 ms: 1.09x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 63.2 ms: 1.07x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 96.8 us: 1.06x faster                                                    |
| tomli_loads          | 957 ms                                                   | 915 ms: 1.05x faster                                                     |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.01x faster                                                    |
| Geometric mean       | (ref)                                                    | 1.09x faster                                                             |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.67 ms: 1.08x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.24 ms: 1.09x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.68 ms: 1.08x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.1 ms: 1.03x faster                                                    |
| mako            | 4.77 ms                                                  | 4.65 ms: 1.03x faster                                                    |
| django_template | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.02x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.03 ms: 5.16x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 228 ms: 2.17x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 225 ms: 2.13x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 220 ms: 2.02x faster                                                     |
| mdp                              | 1.09 sec                                                 | 541 ms: 2.02x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 234 ms: 1.97x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.74x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 99.7 ms: 1.73x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 136 ms: 1.70x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.2 us: 1.63x faster                                                    |
| deepcopy                         | 161 us                                                   | 101 us: 1.61x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 139 ms: 1.60x faster                                                     |
| float                            | 37.9 ms                                                  | 27.1 ms: 1.40x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.04 us: 1.40x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.07 us: 1.37x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.35x faster                                                    |
| go                               | 70.0 ms                                                  | 52.2 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 253 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 250 ms: 1.33x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.0 ms: 1.29x faster                                                    |
| raytrace                         | 145 ms                                                   | 114 ms: 1.27x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 40.5 ns: 1.26x faster                                                    |
| k_core                           | 1.12 sec                                                 | 900 ms: 1.24x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 106 ms: 1.24x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 43.8 ms: 1.24x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 49.6 ms: 1.23x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 45.1 ms: 1.21x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.3 ms: 1.20x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.45 ms: 1.19x faster                                                    |
| nbody                            | 54.2 ms                                                  | 45.7 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 174 ms: 1.18x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 120 ms: 1.18x faster                                                     |
| scimark_lu                       | 51.3 ms                                                  | 44.0 ms: 1.17x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.7 ms: 1.16x faster                                                    |
| pyflate                          | 216 ms                                                   | 187 ms: 1.16x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.16x faster                                                    |
| chaos                            | 28.9 ms                                                  | 25.0 ms: 1.16x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.23 us: 1.15x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.80 ms: 1.15x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.46 us: 1.14x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                   |
| pylint                           | 128 ms                                                   | 113 ms: 1.13x faster                                                     |
| richards                         | 22.4 ms                                                  | 19.8 ms: 1.13x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.8 ms: 1.13x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 34.5 ms: 1.13x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 63.1 us: 1.12x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 22.6 ms: 1.12x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.7 ms: 1.12x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.50 ms: 1.11x faster                                                    |
| sphinx                           | 434 ms                                                   | 391 ms: 1.11x faster                                                     |
| hexiom                           | 3.04 ms                                                  | 2.75 ms: 1.10x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.89 ms: 1.09x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.34 ms: 1.09x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 39.9 ms: 1.09x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 301 ms: 1.09x faster                                                     |
| xml_etree_process                | 26.7 ms                                                  | 24.5 ms: 1.09x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 611 ms: 1.09x faster                                                     |
| genshi_text                      | 10.5 ms                                                  | 9.68 ms: 1.08x faster                                                    |
| pycparser                        | 497 ms                                                   | 462 ms: 1.08x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 63.2 ms: 1.07x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 21.6 ms: 1.06x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 96.8 us: 1.06x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 36.7 ms: 1.06x faster                                                    |
| thrift                           | 322 us                                                   | 304 us: 1.06x faster                                                     |
| sympy_sum                        | 57.6 ms                                                  | 54.5 ms: 1.06x faster                                                    |
| sympy_str                        | 104 ms                                                   | 98.8 ms: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 915 ms: 1.05x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 21.1 ms: 1.03x faster                                                    |
| fannkuch                         | 176 ms                                                   | 170 ms: 1.03x faster                                                     |
| mako                             | 4.77 ms                                                  | 4.65 ms: 1.03x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 97.6 ms: 1.02x faster                                                    |
| json                             | 1.93 ms                                                  | 1.90 ms: 1.02x faster                                                    |
| 2to3                             | 114 ms                                                   | 112 ms: 1.01x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                     |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.01x faster                                                    |
| docutils                         | 1.02 sec                                                 | 1.02 sec: 1.00x faster                                                   |
| pidigits                         | 161 ms                                                   | 162 ms: 1.00x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 168 ms: 1.00x slower                                                     |
| shortest_path                    | 219 ms                                                   | 221 ms: 1.01x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.72 ms: 1.01x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 428 us: 1.02x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.05 ms: 1.02x slower                                                    |
| connected_components             | 201 ms                                                   | 205 ms: 1.02x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 49.3 ms: 1.03x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 119 ms: 1.06x slower                                                     |
| telco                            | 2.61 ms                                                  | 2.81 ms: 1.07x slower                                                    |
| django_template                  | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.67 ms: 1.08x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.24 ms: 1.09x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 917 us: 1.11x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 44.5 ms: 1.12x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 240 ms: 1.13x slower                                                     |
| coverage                         | 26.9 ms                                                  | 31.9 ms: 1.19x slower                                                    |
| many_optionals                   | 195 us                                                   | 252 us: 1.29x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.8 ms: 2.48x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.16x faster                                                             |

Benchmark hidden because not significant (2): sqlite_synth, pickle_pure_python
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260103-3.15.0a3+-9609574/bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.163x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.22x