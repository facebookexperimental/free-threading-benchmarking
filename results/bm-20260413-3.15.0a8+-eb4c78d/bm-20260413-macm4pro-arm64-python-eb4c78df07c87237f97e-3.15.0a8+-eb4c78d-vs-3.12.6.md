# Results vs. 3.12.6

- fork: python
- ref: eb4c78df07c87237f97e
- machine: darwin-arm64
- commit hash: eb4c78d
- commit date: 2026-04-13
- overall geometric mean: 1.150x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.25x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8+-eb4c78d |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 119 ms: 1.05x slower                                                     |
| html5lib       | 23.0 ms                                                  | 21.6 ms: 1.07x faster                                                    |
| sphinx         | 434 ms                                                   | 399 ms: 1.09x faster                                                     |
| Geometric mean | (ref)                                                    | 1.03x faster                                                             |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8+-eb4c78d |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 226 ms: 2.19x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 228 ms: 2.10x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 220 ms: 2.02x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 237 ms: 1.94x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 100 ms: 1.71x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 136 ms: 1.69x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 135 ms: 1.65x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 252 ms: 1.34x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 254 ms: 1.31x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 106 ms: 1.24x faster                                                     |
| async_generators                 | 206 ms                                                   | 180 ms: 1.15x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 41.7 ms: 1.09x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.07x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 240 ms: 1.13x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 83.2 ms: 2.59x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.32x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8+-eb4c78d |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.3 ms: 1.39x faster                                                    |
| nbody          | 54.2 ms                                                  | 44.6 ms: 1.22x faster                                                    |
| pidigits       | 161 ms                                                   | 164 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                    | 1.18x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8+-eb4c78d |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 46.0 ms: 1.19x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 97.1 ms: 1.03x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.69 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8+-eb4c78d |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.4 ms: 1.28x faster                                                    |
| tomli_loads          | 957 ms                                                   | 820 ms: 1.17x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.81 ms: 1.12x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 35.3 ms: 1.10x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 25.0 ms: 1.07x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 97.9 us: 1.05x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 65.3 ms: 1.04x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 141 us: 1.01x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.09x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8+-eb4c78d |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.81 ms: 1.10x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.33 ms: 1.11x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.10x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8+-eb4c78d |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.74 ms: 1.08x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.3 ms: 1.02x faster                                                    |
| mako            | 4.77 ms                                                  | 4.89 ms: 1.03x slower                                                    |
| django_template | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.01x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8+-eb4c78d |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.08 ms: 5.10x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 226 ms: 2.19x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 228 ms: 2.10x faster                                                     |
| mdp                              | 1.09 sec                                                 | 534 ms: 2.04x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 220 ms: 2.02x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 237 ms: 1.94x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 100 ms: 1.71x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 136 ms: 1.69x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 135 ms: 1.65x faster                                                     |
| deepcopy                         | 161 us                                                   | 99.4 us: 1.63x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 11.5 us: 1.58x faster                                                    |
| float                            | 37.9 ms                                                  | 27.3 ms: 1.39x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.10 us: 1.39x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 252 ms: 1.34x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.10 us: 1.33x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                    |
| go                               | 70.0 ms                                                  | 53.0 ms: 1.32x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 254 ms: 1.31x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 42.1 ms: 1.29x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.4 ms: 1.28x faster                                                    |
| raytrace                         | 145 ms                                                   | 114 ms: 1.27x faster                                                     |
| k_core                           | 1.12 sec                                                 | 897 ms: 1.25x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 106 ms: 1.24x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 41.1 ns: 1.24x faster                                                    |
| nbody                            | 54.2 ms                                                  | 44.6 ms: 1.22x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 50.8 ms: 1.20x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 118 ms: 1.20x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 36.4 ms: 1.19x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 46.0 ms: 1.19x faster                                                    |
| pyflate                          | 216 ms                                                   | 184 ms: 1.18x faster                                                     |
| chaos                            | 28.9 ms                                                  | 24.7 ms: 1.17x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.47 ms: 1.17x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 820 ms: 1.17x faster                                                     |
| generators                       | 21.9 ms                                                  | 18.9 ms: 1.16x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.22 us: 1.16x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.16x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.94 sec: 1.15x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.44 us: 1.15x faster                                                    |
| async_generators                 | 206 ms                                                   | 180 ms: 1.15x faster                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.3 ms: 1.14x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.8 ms: 1.13x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 45.4 ms: 1.13x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                    |
| pylint                           | 128 ms                                                   | 115 ms: 1.12x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.81 ms: 1.12x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 35.3 ms: 1.10x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 64.6 us: 1.10x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.89 ms: 1.10x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.7 ms: 1.09x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.79 ms: 1.09x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 23.3 ms: 1.09x faster                                                    |
| sphinx                           | 434 ms                                                   | 399 ms: 1.09x faster                                                     |
| richards                         | 22.4 ms                                                  | 20.6 ms: 1.09x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.74 ms: 1.08x faster                                                    |
| pycparser                        | 497 ms                                                   | 464 ms: 1.07x faster                                                     |
| xml_etree_process                | 26.7 ms                                                  | 25.0 ms: 1.07x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 21.6 ms: 1.07x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.55 ms: 1.06x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 97.9 us: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 65.3 ms: 1.04x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 316 ms: 1.04x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 642 ms: 1.03x faster                                                     |
| fannkuch                         | 176 ms                                                   | 170 ms: 1.03x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 941 ns: 1.03x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 97.1 ms: 1.03x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.3 ms: 1.02x faster                                                    |
| json                             | 1.93 ms                                                  | 1.90 ms: 1.02x faster                                                    |
| thrift                           | 322 us                                                   | 316 us: 1.02x faster                                                     |
| sympy_str                        | 104 ms                                                   | 102 ms: 1.02x faster                                                     |
| sympy_sum                        | 57.6 ms                                                  | 56.7 ms: 1.02x faster                                                    |
| dask                             | 528 ms                                                   | 521 ms: 1.01x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 39.0 ms: 1.00x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.69 ms: 1.01x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 141 us: 1.01x slower                                                     |
| pidigits                         | 161 ms                                                   | 164 ms: 1.02x slower                                                     |
| shortest_path                    | 219 ms                                                   | 223 ms: 1.02x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 428 us: 1.02x slower                                                     |
| connected_components             | 201 ms                                                   | 206 ms: 1.02x slower                                                     |
| mako                             | 4.77 ms                                                  | 4.89 ms: 1.03x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 174 ms: 1.04x slower                                                     |
| 2to3                             | 114 ms                                                   | 119 ms: 1.05x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 50.4 ms: 1.06x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.07x slower                                                     |
| telco                            | 2.61 ms                                                  | 2.86 ms: 1.10x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.81 ms: 1.10x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.33 ms: 1.11x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 240 ms: 1.13x slower                                                     |
| create_gc_cycles                 | 830 us                                                   | 966 us: 1.16x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 46.8 ms: 1.18x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.6 ms: 1.21x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.52 ms: 1.25x slower                                                    |
| many_optionals                   | 195 us                                                   | 257 us: 1.31x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 83.2 ms: 2.59x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.15x faster                                                             |

Benchmark hidden because not significant (2): json_loads, docutils
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260413-3.15.0a8+-eb4c78d/bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8+-eb4c78d.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.150x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.25x