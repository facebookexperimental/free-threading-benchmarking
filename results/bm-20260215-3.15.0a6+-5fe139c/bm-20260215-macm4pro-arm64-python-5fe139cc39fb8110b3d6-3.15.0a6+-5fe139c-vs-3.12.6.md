# Results vs. 3.12.6

- fork: python
- ref: 5fe139cc39fb8110b3d6
- machine: darwin-arm64
- commit hash: 5fe139c
- commit date: 2026-02-15
- overall geometric mean: 1.160x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260215-macm4pro-arm64-python-5fe139cc39fb8110b3d6-3.15.0a6+-5fe139c |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 112 ms: 1.02x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| html5lib       | 23.0 ms                                                  | 21.5 ms: 1.07x faster                                                    |
| sphinx         | 434 ms                                                   | 394 ms: 1.10x faster                                                     |
| Geometric mean | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260215-macm4pro-arm64-python-5fe139cc39fb8110b3d6-3.15.0a6+-5fe139c |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 219 ms: 2.27x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 227 ms: 2.12x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 225 ms: 2.04x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 220 ms: 2.02x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 100 ms: 1.78x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 97.3 ms: 1.77x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 134 ms: 1.73x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 137 ms: 1.63x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 249 ms: 1.36x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 255 ms: 1.31x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                     |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.1 ms: 1.14x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 118 ms: 1.05x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 234 ms: 1.10x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.5 ms: 2.47x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.34x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260215-macm4pro-arm64-python-5fe139cc39fb8110b3d6-3.15.0a6+-5fe139c |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.1 ms: 1.35x faster                                                    |
| nbody          | 54.2 ms                                                  | 45.0 ms: 1.20x faster                                                    |
| pidigits       | 161 ms                                                   | 165 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                    | 1.17x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260215-macm4pro-arm64-python-5fe139cc39fb8110b3d6-3.15.0a6+-5fe139c |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 45.5 ms: 1.20x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 96.1 ms: 1.04x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.71 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260215-macm4pro-arm64-python-5fe139cc39fb8110b3d6-3.15.0a6+-5fe139c |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.7 ms: 1.27x faster                                                    |
| tomli_loads          | 957 ms                                                   | 847 ms: 1.13x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 34.5 ms: 1.13x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.81 ms: 1.12x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.5 ms: 1.09x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 62.6 ms: 1.08x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 97.6 us: 1.05x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.01x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 140 us: 1.01x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.10x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260215-macm4pro-arm64-python-5fe139cc39fb8110b3d6-3.15.0a6+-5fe139c |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.91 ms: 1.11x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.43 ms: 1.13x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.12x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260215-macm4pro-arm64-python-5fe139cc39fb8110b3d6-3.15.0a6+-5fe139c |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.64 ms: 1.09x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.1 ms: 1.03x faster                                                    |
| mako            | 4.77 ms                                                  | 4.69 ms: 1.02x faster                                                    |
| django_template | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.02x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260215-macm4pro-arm64-python-5fe139cc39fb8110b3d6-3.15.0a6+-5fe139c |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.96 ms: 5.25x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 219 ms: 2.27x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 227 ms: 2.12x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 225 ms: 2.04x faster                                                     |
| mdp                              | 1.09 sec                                                 | 537 ms: 2.03x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 220 ms: 2.02x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 100 ms: 1.78x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 97.3 ms: 1.77x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 134 ms: 1.73x faster                                                     |
| deepcopy                         | 161 us                                                   | 98.2 us: 1.65x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 137 ms: 1.63x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.5 us: 1.60x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.00 us: 1.41x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.07 us: 1.37x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 249 ms: 1.36x faster                                                     |
| float                            | 37.9 ms                                                  | 28.1 ms: 1.35x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                    |
| go                               | 70.0 ms                                                  | 53.0 ms: 1.32x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 255 ms: 1.31x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.7 ms: 1.27x faster                                                    |
| raytrace                         | 145 ms                                                   | 116 ms: 1.25x faster                                                     |
| k_core                           | 1.12 sec                                                 | 900 ms: 1.24x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 41.3 ns: 1.23x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 50.0 ms: 1.22x faster                                                    |
| nbody                            | 54.2 ms                                                  | 45.0 ms: 1.20x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 45.2 ms: 1.20x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 45.5 ms: 1.20x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.4 ms: 1.19x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.46 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 121 ms: 1.17x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.23 us: 1.15x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.44 us: 1.15x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.1 ms: 1.15x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.14x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.7 ms: 1.14x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.1 ms: 1.14x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 22.4 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 847 ms: 1.13x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 34.5 ms: 1.13x faster                                                    |
| pyflate                          | 216 ms                                                   | 192 ms: 1.12x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.81 ms: 1.12x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.1 ms: 1.12x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.0 ms: 1.11x faster                                                    |
| pylint                           | 128 ms                                                   | 115 ms: 1.11x faster                                                     |
| scimark_lu                       | 51.3 ms                                                  | 46.1 ms: 1.11x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 39.2 ms: 1.11x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 64.0 us: 1.11x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.75 ms: 1.11x faster                                                    |
| sphinx                           | 434 ms                                                   | 394 ms: 1.10x faster                                                     |
| xml_etree_process                | 26.7 ms                                                  | 24.5 ms: 1.09x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.64 ms: 1.09x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 62.6 ms: 1.08x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.92 ms: 1.08x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 21.5 ms: 1.07x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.51 ms: 1.07x faster                                                    |
| pycparser                        | 497 ms                                                   | 467 ms: 1.07x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 628 ms: 1.06x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 311 ms: 1.06x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 97.6 us: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| fannkuch                         | 176 ms                                                   | 168 ms: 1.04x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 96.1 ms: 1.04x faster                                                    |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.03x faster                                                     |
| thrift                           | 322 us                                                   | 311 us: 1.03x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 21.1 ms: 1.03x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 55.7 ms: 1.03x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.8 ms: 1.03x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 944 ns: 1.02x faster                                                     |
| 2to3                             | 114 ms                                                   | 112 ms: 1.02x faster                                                     |
| mako                             | 4.77 ms                                                  | 4.69 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| json                             | 1.93 ms                                                  | 1.90 ms: 1.02x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| shortest_path                    | 219 ms                                                   | 220 ms: 1.00x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 140 us: 1.01x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.71 ms: 1.01x slower                                                    |
| connected_components             | 201 ms                                                   | 205 ms: 1.02x slower                                                     |
| pidigits                         | 161 ms                                                   | 165 ms: 1.02x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.06 ms: 1.02x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 171 ms: 1.03x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 430 us: 1.03x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 118 ms: 1.05x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 50.5 ms: 1.06x slower                                                    |
| django_template                  | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.83 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 234 ms: 1.10x slower                                                     |
| create_gc_cycles                 | 830 us                                                   | 914 us: 1.10x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 8.91 ms: 1.11x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.43 ms: 1.13x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 45.4 ms: 1.14x slower                                                    |
| coverage                         | 26.9 ms                                                  | 31.9 ms: 1.19x slower                                                    |
| many_optionals                   | 195 us                                                   | 249 us: 1.28x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.5 ms: 2.47x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.16x faster                                                             |
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260215-3.15.0a6+-5fe139c/bm-20260215-macm4pro-arm64-python-5fe139cc39fb8110b3d6-3.15.0a6+-5fe139c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.160x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.23x