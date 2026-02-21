# Results vs. 3.12.6

- fork: python
- ref: 06292614ff7cef0ba28d
- machine: darwin-arm64
- commit hash: 0629261
- commit date: 2026-02-20
- overall geometric mean: 1.098x faster
- HPT reliability: 99.88%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.38x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260220-macm4pro-arm64-python-06292614ff7cef0ba28d-3.15.0a6+-0629261 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 122 ms: 1.07x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.02x faster                                                   |
| sphinx         | 434 ms                                                   | 420 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                    | 1.00x slower                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260220-macm4pro-arm64-python-06292614ff7cef0ba28d-3.15.0a6+-0629261 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 236 ms: 2.03x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 250 ms: 1.98x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 250 ms: 1.83x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 245 ms: 1.82x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.65x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 144 ms: 1.60x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.55x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 153 ms: 1.46x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 259 ms: 1.31x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                     |
| async_generators                 | 206 ms                                                   | 184 ms: 1.12x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 184 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.02x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 46.6 ms: 1.02x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 128 ms: 1.14x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.3 ms: 2.90x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260220-macm4pro-arm64-python-06292614ff7cef0ba28d-3.15.0a6+-0629261 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.7 ms: 1.32x faster                                                    |
| pidigits       | 161 ms                                                   | 162 ms: 1.01x slower                                                     |
| nbody          | 54.2 ms                                                  | 57.2 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260220-macm4pro-arm64-python-06292614ff7cef0ba28d-3.15.0a6+-0629261 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 50.8 ms: 1.08x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 93.8 ms: 1.06x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.19 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260220-macm4pro-arm64-python-06292614ff7cef0ba28d-3.15.0a6+-0629261 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.4 ms: 1.31x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 58.2 ms: 1.17x faster                                                    |
| tomli_loads          | 957 ms                                                   | 870 ms: 1.10x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.91 ms: 1.09x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.0 ms: 1.05x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 26.8 ms: 1.00x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.2 us: 1.03x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 147 us: 1.05x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 109 us: 1.06x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260220-macm4pro-arm64-python-06292614ff7cef0ba28d-3.15.0a6+-0629261 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.87 ms: 1.23x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.19 ms: 1.26x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.25x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260220-macm4pro-arm64-python-06292614ff7cef0ba28d-3.15.0a6+-0629261 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 22.6 ms: 1.04x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.3 ms: 1.08x slower                                                    |
| django_template | 13.6 ms                                                  | 15.4 ms: 1.13x slower                                                    |
| mako            | 4.77 ms                                                  | 5.52 ms: 1.16x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.10x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260220-macm4pro-arm64-python-06292614ff7cef0ba28d-3.15.0a6+-0629261 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.17 ms: 4.98x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 810 us: 2.48x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 236 ms: 2.03x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 250 ms: 1.98x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 250 ms: 1.83x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 245 ms: 1.82x faster                                                     |
| mdp                              | 1.09 sec                                                 | 610 ms: 1.79x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.65x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 507 us: 1.64x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 144 ms: 1.60x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.55x faster                                                     |
| deepcopy                         | 161 us                                                   | 106 us: 1.52x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 153 ms: 1.46x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.9 us: 1.42x faster                                                    |
| float                            | 37.9 ms                                                  | 28.7 ms: 1.32x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.4 ms: 1.31x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 259 ms: 1.31x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.16 us: 1.26x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 785 ns: 1.23x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.20 us: 1.20x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 43.3 ns: 1.18x faster                                                    |
| go                               | 70.0 ms                                                  | 59.7 ms: 1.17x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 58.2 ms: 1.17x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.5 ms: 1.15x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.15x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 125 ms: 1.14x faster                                                     |
| raytrace                         | 145 ms                                                   | 128 ms: 1.14x faster                                                     |
| k_core                           | 1.12 sec                                                 | 987 ms: 1.13x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.99 sec: 1.12x faster                                                   |
| async_generators                 | 206 ms                                                   | 184 ms: 1.12x faster                                                     |
| pyflate                          | 216 ms                                                   | 194 ms: 1.11x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 55.1 ms: 1.11x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 870 ms: 1.10x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 49.7 ms: 1.09x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.91 ms: 1.09x faster                                                    |
| pylint                           | 128 ms                                                   | 118 ms: 1.09x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 50.8 ms: 1.08x faster                                                    |
| pycparser                        | 497 ms                                                   | 463 ms: 1.08x faster                                                     |
| chaos                            | 28.9 ms                                                  | 27.1 ms: 1.07x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.41 us: 1.07x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 93.8 ms: 1.06x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.64 ms: 1.05x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.0 ms: 1.05x faster                                                    |
| generators                       | 21.9 ms                                                  | 20.9 ms: 1.05x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.68 us: 1.05x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.19 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 184 ms: 1.03x faster                                                     |
| sphinx                           | 434 ms                                                   | 420 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.02x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 42.4 ms: 1.02x faster                                                    |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.02x faster                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 323 ms: 1.02x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 662 ms: 1.00x faster                                                     |
| xml_etree_process                | 26.7 ms                                                  | 26.8 ms: 1.00x slower                                                    |
| pidigits                         | 161 ms                                                   | 162 ms: 1.01x slower                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 8.11 ms: 1.01x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.6 ms: 1.01x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 72.6 us: 1.02x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 46.6 ms: 1.02x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.13 ms: 1.02x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.0 ms: 1.03x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 26.2 ms: 1.03x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.2 us: 1.03x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.6 ms: 1.04x slower                                                    |
| thrift                           | 322 us                                                   | 334 us: 1.04x slower                                                     |
| hexiom                           | 3.04 ms                                                  | 3.16 ms: 1.04x slower                                                    |
| nbody                            | 54.2 ms                                                  | 57.2 ms: 1.05x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 147 us: 1.05x slower                                                     |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.05x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 109 us: 1.06x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 60.9 ms: 1.06x slower                                                    |
| 2to3                             | 114 ms                                                   | 122 ms: 1.07x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 11.3 ms: 1.08x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 55.3 ms: 1.08x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 187 ms: 1.12x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 43.7 ms: 1.12x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.4 ms: 1.13x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 128 ms: 1.14x slower                                                     |
| shortest_path                    | 219 ms                                                   | 252 ms: 1.15x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 55.1 ms: 1.15x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.52 ms: 1.16x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.02 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 46.9 ms: 1.18x slower                                                    |
| connected_components             | 201 ms                                                   | 245 ms: 1.22x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 9.87 ms: 1.23x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.19 ms: 1.26x slower                                                    |
| many_optionals                   | 195 us                                                   | 268 us: 1.37x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 577 us: 1.38x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.9 ms: 1.45x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.3 ms: 2.90x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                             |

Benchmark hidden because not significant (4): fannkuch, html5lib, json, dask
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260220-3.15.0a6+-0629261-NOGIL/bm-20260220-macm4pro-arm64-python-06292614ff7cef0ba28d-3.15.0a6+-0629261.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.098x faster

# HPT report

- Reliability score: 99.88% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.38x