# Results vs. 3.12.6

- fork: python
- ref: 6ea3f8cd7ff4ff9769ae
- machine: darwin-arm64
- commit hash: 6ea3f8c
- commit date: 2026-01-27
- overall geometric mean: 1.123x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260127-macm4pro-arm64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 116 ms: 1.02x slower                                                     |
| docutils       | 1.02 sec                                                 | 967 ms: 1.06x faster                                                     |
| html5lib       | 23.0 ms                                                  | 22.5 ms: 1.02x faster                                                    |
| sphinx         | 434 ms                                                   | 404 ms: 1.07x faster                                                     |
| Geometric mean | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260127-macm4pro-arm64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 238 ms: 2.08x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 240 ms: 2.00x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 238 ms: 1.93x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 235 ms: 1.90x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 141 ms: 1.63x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.60x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.51x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 249 ms: 1.36x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 256 ms: 1.30x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.19x faster                                                     |
| async_generators                 | 206 ms                                                   | 176 ms: 1.17x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 182 ms: 1.04x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 45.1 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 237 ms: 1.12x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 126 ms: 1.12x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.9 ms: 2.80x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.28x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260127-macm4pro-arm64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.6 ms: 1.33x faster                                                    |
| pidigits       | 161 ms                                                   | 156 ms: 1.03x faster                                                     |
| nbody          | 54.2 ms                                                  | 56.1 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260127-macm4pro-arm64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 49.3 ms: 1.11x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 91.6 ms: 1.09x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.07 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260127-macm4pro-arm64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.1 ms: 1.35x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 57.8 ms: 1.18x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.84 ms: 1.11x faster                                                    |
| tomli_loads          | 957 ms                                                   | 871 ms: 1.10x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 36.6 ms: 1.06x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 26.3 ms: 1.02x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 142 us: 1.02x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.1 us: 1.03x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 106 us: 1.03x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260127-macm4pro-arm64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.62 ms: 1.20x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.01 ms: 1.23x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260127-macm4pro-arm64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 21.8 ms: 1.00x slower                                                    |
| django_template | 13.6 ms                                                  | 15.0 ms: 1.10x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.6 ms: 1.11x slower                                                    |
| mako            | 4.77 ms                                                  | 5.43 ms: 1.14x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.09x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260127-macm4pro-arm64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.95 ms: 5.25x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 773 us: 2.60x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 238 ms: 2.08x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 240 ms: 2.00x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 238 ms: 1.93x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 235 ms: 1.90x faster                                                     |
| mdp                              | 1.09 sec                                                 | 595 ms: 1.83x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 503 us: 1.65x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 141 ms: 1.63x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.60x faster                                                     |
| deepcopy                         | 161 us                                                   | 103 us: 1.57x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.51x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.2 us: 1.49x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 249 ms: 1.36x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.1 ms: 1.35x faster                                                    |
| float                            | 37.9 ms                                                  | 28.6 ms: 1.33x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 256 ms: 1.30x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.13 us: 1.30x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.10 us: 1.21x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 808 ns: 1.20x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 17.8 ms: 1.19x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.19x faster                                                     |
| go                               | 70.0 ms                                                  | 58.9 ms: 1.19x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.5 ms: 1.18x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 57.8 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 176 ms: 1.17x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 43.6 ns: 1.17x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.93 sec: 1.16x faster                                                   |
| raytrace                         | 145 ms                                                   | 126 ms: 1.15x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 53.3 ms: 1.14x faster                                                    |
| pyflate                          | 216 ms                                                   | 190 ms: 1.14x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 126 ms: 1.12x faster                                                     |
| k_core                           | 1.12 sec                                                 | 994 ms: 1.12x faster                                                     |
| pylint                           | 128 ms                                                   | 114 ms: 1.12x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.84 ms: 1.11x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 49.3 ms: 1.11x faster                                                    |
| pycparser                        | 497 ms                                                   | 452 ms: 1.10x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.57 ms: 1.10x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.34 us: 1.10x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 871 ms: 1.10x faster                                                     |
| generators                       | 21.9 ms                                                  | 20.0 ms: 1.10x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 91.6 ms: 1.09x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.2 ms: 1.08x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.59 us: 1.08x faster                                                    |
| sphinx                           | 434 ms                                                   | 404 ms: 1.07x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                     |
| chaos                            | 28.9 ms                                                  | 27.1 ms: 1.07x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.6 ms: 1.06x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.07 ms: 1.06x faster                                                    |
| docutils                         | 1.02 sec                                                 | 967 ms: 1.06x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 41.6 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 182 ms: 1.04x faster                                                     |
| fannkuch                         | 176 ms                                                   | 169 ms: 1.04x faster                                                     |
| pidigits                         | 161 ms                                                   | 156 ms: 1.03x faster                                                     |
| json                             | 1.93 ms                                                  | 1.88 ms: 1.03x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 69.2 us: 1.03x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.85 ms: 1.02x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 22.5 ms: 1.02x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.3 ms: 1.02x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 45.1 ms: 1.01x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 327 ms: 1.00x faster                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.1 ms: 1.00x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.8 ms: 1.00x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 667 ms: 1.00x slower                                                     |
| hexiom                           | 3.04 ms                                                  | 3.06 ms: 1.01x slower                                                    |
| 2to3                             | 114 ms                                                   | 116 ms: 1.02x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 142 us: 1.02x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 58.8 ms: 1.02x slower                                                    |
| sympy_str                        | 104 ms                                                   | 107 ms: 1.03x slower                                                     |
| thrift                           | 322 us                                                   | 330 us: 1.03x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.1 us: 1.03x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.14 ms: 1.03x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 106 us: 1.03x slower                                                     |
| nbody                            | 54.2 ms                                                  | 56.1 ms: 1.03x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 41.1 ms: 1.06x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 182 ms: 1.09x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.0 ms: 1.10x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.6 ms: 1.11x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 237 ms: 1.12x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 126 ms: 1.12x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 53.4 ms: 1.12x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 44.5 ms: 1.12x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.43 ms: 1.14x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.97 ms: 1.14x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 58.5 ms: 1.14x slower                                                    |
| shortest_path                    | 219 ms                                                   | 252 ms: 1.15x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 9.62 ms: 1.20x slower                                                    |
| connected_components             | 201 ms                                                   | 245 ms: 1.22x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 7.01 ms: 1.23x slower                                                    |
| many_optionals                   | 195 us                                                   | 253 us: 1.29x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 563 us: 1.35x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.0 ms: 1.41x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.9 ms: 2.80x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.12x faster                                                             |

Benchmark hidden because not significant (3): richards, dask, richards_super
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260127-3.15.0a5+-6ea3f8c-NOGIL/bm-20260127-macm4pro-arm64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.123x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.35x