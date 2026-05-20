# Results vs. 3.12.6

- fork: python
- ref: de9c32fc34fe2e000de1
- machine: darwin-arm64
- commit hash: de9c32f
- commit date: 2026-05-20
- overall geometric mean: 1.101x faster
- HPT reliability: 99.62%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260520-macm4pro-arm64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| docutils       | 1.02 sec                                                 | 1.06 sec: 1.04x slower                                                  |
| html5lib       | 23.0 ms                                                  | 23.2 ms: 1.01x slower                                                   |
| sphinx         | 434 ms                                                   | 442 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260520-macm4pro-arm64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 284 ms: 1.75x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 275 ms: 1.67x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 293 ms: 1.64x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 279 ms: 1.60x faster                                                    |
| async_generators                 | 206 ms                                                   | 152 ms: 1.36x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 173 ms: 1.33x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 135 ms: 1.32x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 134 ms: 1.29x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 181 ms: 1.23x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 282 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 287 ms: 1.16x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 120 ms: 1.10x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 184 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 227 ms: 1.02x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 45.9 ms: 1.01x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 269 ms: 1.27x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 150 ms: 1.34x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 106 ms: 3.30x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.13x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260520-macm4pro-arm64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 32.6 ms: 1.16x faster                                                   |
| nbody          | 54.2 ms                                                  | 56.6 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                    | 1.04x faster                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260520-macm4pro-arm64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 94.0 ms: 1.06x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 51.8 ms: 1.05x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.17 ms: 1.05x faster                                                   |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260520-macm4pro-arm64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.3 ms: 1.28x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 57.4 ms: 1.18x faster                                                   |
| tomli_loads          | 957 ms                                                   | 853 ms: 1.12x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.86 ms: 1.10x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 37.5 ms: 1.04x faster                                                   |
| json_loads           | 10.9 us                                                  | 11.0 us: 1.02x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 108 us: 1.05x slower                                                    |
| xml_etree_process    | 26.7 ms                                                  | 28.3 ms: 1.06x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 148 us: 1.06x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260520-macm4pro-arm64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| django_template | 13.6 ms                                                  | 15.7 ms: 1.15x slower                                                   |
| mako            | 4.77 ms                                                  | 5.68 ms: 1.19x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.17x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260520-macm4pro-arm64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.28 ms: 4.85x faster                                                   |
| gc_traversal                     | 2.01 ms                                                  | 787 us: 2.55x faster                                                    |
| pylint                           | 128 ms                                                   | 53.6 ms: 2.39x faster                                                   |
| mdp                              | 1.09 sec                                                 | 585 ms: 1.87x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 284 ms: 1.75x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 275 ms: 1.67x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 293 ms: 1.64x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 506 us: 1.64x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 279 ms: 1.60x faster                                                    |
| deepcopy                         | 161 us                                                   | 105 us: 1.53x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.8 us: 1.43x faster                                                   |
| async_generators                 | 206 ms                                                   | 152 ms: 1.36x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 173 ms: 1.33x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 135 ms: 1.32x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 54.7 us: 1.30x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 134 ms: 1.29x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.3 ms: 1.28x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.17 us: 1.25x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 181 ms: 1.23x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 796 ns: 1.22x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.14 us: 1.21x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 282 ms: 1.20x faster                                                    |
| go                               | 70.0 ms                                                  | 59.0 ms: 1.19x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.89 sec: 1.18x faster                                                  |
| logging_silent                   | 50.9 ns                                                  | 43.0 ns: 1.18x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 57.4 ms: 1.18x faster                                                   |
| float                            | 37.9 ms                                                  | 32.6 ms: 1.16x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.16x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 287 ms: 1.16x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.5 ms: 1.15x faster                                                   |
| raytrace                         | 145 ms                                                   | 128 ms: 1.14x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 125 ms: 1.13x faster                                                    |
| pyflate                          | 216 ms                                                   | 191 ms: 1.13x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 54.3 ms: 1.12x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 853 ms: 1.12x faster                                                    |
| k_core                           | 1.12 sec                                                 | 1.00 sec: 1.12x faster                                                  |
| json_dumps                       | 4.26 ms                                                  | 3.86 ms: 1.10x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 120 ms: 1.10x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.35 us: 1.09x faster                                                   |
| pycparser                        | 497 ms                                                   | 462 ms: 1.08x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 40.4 ms: 1.08x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.61 us: 1.07x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 50.8 ms: 1.07x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 94.0 ms: 1.06x faster                                                   |
| chaos                            | 28.9 ms                                                  | 27.3 ms: 1.06x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 51.8 ms: 1.05x faster                                                   |
| generators                       | 21.9 ms                                                  | 20.9 ms: 1.05x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.17 ms: 1.05x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 37.5 ms: 1.04x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 184 ms: 1.04x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.68 ms: 1.03x faster                                                   |
| fannkuch                         | 176 ms                                                   | 172 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 227 ms: 1.02x faster                                                    |
| json                             | 1.93 ms                                                  | 1.91 ms: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 529 ms: 1.00x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.05 ms: 1.00x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 45.9 ms: 1.01x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 23.2 ms: 1.01x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.0 us: 1.02x slower                                                   |
| sphinx                           | 434 ms                                                   | 442 ms: 1.02x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.8 ms: 1.02x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 335 ms: 1.02x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 683 ms: 1.03x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.14 ms: 1.03x slower                                                   |
| hexiom                           | 3.04 ms                                                  | 3.14 ms: 1.03x slower                                                   |
| richards                         | 22.4 ms                                                  | 23.2 ms: 1.04x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.06 sec: 1.04x slower                                                  |
| richards_super                   | 25.4 ms                                                  | 26.5 ms: 1.04x slower                                                   |
| nbody                            | 54.2 ms                                                  | 56.6 ms: 1.04x slower                                                   |
| sympy_str                        | 104 ms                                                   | 109 ms: 1.05x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 60.3 ms: 1.05x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 108 us: 1.05x slower                                                    |
| thrift                           | 322 us                                                   | 339 us: 1.05x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 28.3 ms: 1.06x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 148 us: 1.06x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 186 ms: 1.11x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 43.6 ms: 1.12x slower                                                   |
| shortest_path                    | 219 ms                                                   | 249 ms: 1.14x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 45.5 ms: 1.15x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.7 ms: 1.15x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 55.1 ms: 1.15x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 59.7 ms: 1.16x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.04 ms: 1.17x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.68 ms: 1.19x slower                                                   |
| connected_components             | 201 ms                                                   | 242 ms: 1.20x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 269 ms: 1.27x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 150 ms: 1.34x slower                                                    |
| many_optionals                   | 195 us                                                   | 261 us: 1.34x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 565 us: 1.35x slower                                                    |
| coverage                         | 26.9 ms                                                  | 38.8 ms: 1.45x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 106 ms: 3.30x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                            |

Benchmark hidden because not significant (1): pidigits
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260520-3.16.0a0-de9c32f-NOGIL/bm-20260520-macm4pro-arm64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.101x faster

# HPT report

- Reliability score: 99.62% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.33x