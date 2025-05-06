# Results vs. 3.12.6

- fork: python
- ref: c4bcc6a77864b42574ec
- machine: darwin-arm64
- commit hash: c4bcc6a
- commit date: 2025-05-06
- overall geometric mean: 1.092x faster
- HPT reliability: 98.01%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250506-macm4pro-arm64-python-c4bcc6a77864b42574ec-3.14.0a7+-c4bcc6a |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 121 ms: 1.06x slower                                                     |
| docutils       | 1.02 sec                                                 | 995 ms: 1.03x faster                                                     |
| html5lib       | 23.0 ms                                                  | 25.4 ms: 1.10x slower                                                    |
| sphinx         | 434 ms                                                   | 411 ms: 1.06x faster                                                     |
| Geometric mean | (ref)                                                    | 1.02x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250506-macm4pro-arm64-python-c4bcc6a77864b42574ec-3.14.0a7+-c4bcc6a |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 197 ms: 2.44x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.43x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.29x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.20x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 87.3 ms: 1.97x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.87x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.76x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 234 ms: 1.45x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.35x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                     |
| async_generators                 | 206 ms                                                   | 177 ms: 1.16x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.03x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 226 ms: 1.06x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 50.6 ms: 1.11x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.5 ms: 2.41x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.38x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250506-macm4pro-arm64-python-c4bcc6a77864b42574ec-3.14.0a7+-c4bcc6a |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.4 ms: 1.33x faster                                                    |
| pidigits       | 161 ms                                                   | 158 ms: 1.02x faster                                                     |
| nbody          | 54.2 ms                                                  | 55.7 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250506-macm4pro-arm64-python-c4bcc6a77864b42574ec-3.14.0a7+-c4bcc6a |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 95.5 ms: 1.04x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 52.5 ms: 1.04x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.38 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250506-macm4pro-arm64-python-c4bcc6a77864b42574ec-3.14.0a7+-c4bcc6a |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.1 ms: 1.35x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 59.2 ms: 1.15x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 36.8 ms: 1.06x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 26.6 ms: 1.01x faster                                                    |
| tomli_loads          | 957 ms                                                   | 978 ms: 1.02x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 107 us: 1.04x slower                                                     |
| pickle_pure_python   | 139 us                                                   | 150 us: 1.08x slower                                                     |
| json_loads           | 10.9 us                                                  | 12.3 us: 1.13x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 5.18 ms: 1.22x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.01x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250506-macm4pro-arm64-python-c4bcc6a77864b42574ec-3.14.0a7+-c4bcc6a |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.35 ms: 1.17x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.81 ms: 1.19x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.18x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250506-macm4pro-arm64-python-c4bcc6a77864b42574ec-3.14.0a7+-c4bcc6a |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.4 ms: 1.08x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                    |
| mako            | 4.77 ms                                                  | 5.57 ms: 1.17x slower                                                    |
| django_template | 13.6 ms                                                  | 16.4 ms: 1.20x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.13x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250506-macm4pro-arm64-python-c4bcc6a77864b42574ec-3.14.0a7+-c4bcc6a |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 753 us: 2.67x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 197 ms: 2.44x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.43x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.29x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.20x faster                                                     |
| subparsers                       | 20.8 ms                                                  | 9.62 ms: 2.16x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 87.3 ms: 1.97x faster                                                    |
| mdp                              | 1.09 sec                                                 | 572 ms: 1.91x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.87x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 467 us: 1.78x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.76x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 234 ms: 1.45x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.1 ms: 1.35x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.35x faster                                                    |
| float                            | 37.9 ms                                                  | 28.4 ms: 1.33x faster                                                    |
| deepcopy                         | 161 us                                                   | 124 us: 1.30x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 14.1 us: 1.29x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.4 ms: 1.19x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 819 ns: 1.18x faster                                                     |
| async_generators                 | 206 ms                                                   | 177 ms: 1.16x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 18.5 ms: 1.15x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.27 us: 1.15x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 59.2 ms: 1.15x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.96 sec: 1.14x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 8.64 us: 1.14x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 44.7 ns: 1.14x faster                                                    |
| k_core                           | 1.12 sec                                                 | 986 ms: 1.13x faster                                                     |
| go                               | 70.0 ms                                                  | 61.8 ms: 1.13x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.12x faster                                                    |
| raytrace                         | 145 ms                                                   | 132 ms: 1.10x faster                                                     |
| pylint                           | 128 ms                                                   | 117 ms: 1.09x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 55.8 ms: 1.09x faster                                                    |
| pyflate                          | 216 ms                                                   | 201 ms: 1.08x faster                                                     |
| pycparser                        | 497 ms                                                   | 468 ms: 1.06x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.62 ms: 1.06x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 41.1 ms: 1.06x faster                                                    |
| sphinx                           | 434 ms                                                   | 411 ms: 1.06x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 36.8 ms: 1.06x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 51.9 ms: 1.05x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 95.5 ms: 1.04x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 52.5 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                     |
| docutils                         | 1.02 sec                                                 | 995 ms: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.03x faster                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.38 ms: 1.02x faster                                                    |
| pidigits                         | 161 ms                                                   | 158 ms: 1.02x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.94 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                     |
| xml_etree_process                | 26.7 ms                                                  | 26.6 ms: 1.01x faster                                                    |
| chaos                            | 28.9 ms                                                  | 29.1 ms: 1.00x slower                                                    |
| logging_simple                   | 2.57 us                                                  | 2.62 us: 1.02x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 978 ms: 1.02x slower                                                     |
| hexiom                           | 3.04 ms                                                  | 3.11 ms: 1.02x slower                                                    |
| nbody                            | 54.2 ms                                                  | 55.7 ms: 1.03x slower                                                    |
| fannkuch                         | 176 ms                                                   | 181 ms: 1.03x slower                                                     |
| logging_format                   | 2.80 us                                                  | 2.89 us: 1.03x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 107 us: 1.04x slower                                                     |
| sympy_str                        | 104 ms                                                   | 109 ms: 1.05x slower                                                     |
| json                             | 1.93 ms                                                  | 2.03 ms: 1.05x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 60.5 ms: 1.05x slower                                                    |
| shortest_path                    | 219 ms                                                   | 232 ms: 1.06x slower                                                     |
| 2to3                             | 114 ms                                                   | 121 ms: 1.06x slower                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 75.1 us: 1.06x slower                                                    |
| sqlalchemy_declarative           | 46.8 ms                                                  | 49.6 ms: 1.06x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 226 ms: 1.06x slower                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 34.2 ms: 1.06x slower                                                    |
| scimark_fft                      | 142 ms                                                   | 152 ms: 1.07x slower                                                     |
| genshi_xml                       | 21.8 ms                                                  | 23.4 ms: 1.08x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 716 ms: 1.08x slower                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 353 ms: 1.08x slower                                                     |
| richards_super                   | 25.4 ms                                                  | 27.4 ms: 1.08x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 150 us: 1.08x slower                                                     |
| richards                         | 22.4 ms                                                  | 24.2 ms: 1.08x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 42.0 ms: 1.08x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 42.9 ms: 1.08x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                    |
| connected_components             | 201 ms                                                   | 218 ms: 1.09x slower                                                     |
| html5lib                         | 23.0 ms                                                  | 25.4 ms: 1.10x slower                                                    |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.72 ms: 1.10x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 50.6 ms: 1.11x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 188 ms: 1.12x slower                                                     |
| json_loads                       | 10.9 us                                                  | 12.3 us: 1.13x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 54.3 ms: 1.14x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 58.6 ms: 1.14x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.35 ms: 1.17x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.57 ms: 1.17x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.81 ms: 1.19x slower                                                    |
| django_template                  | 13.6 ms                                                  | 16.4 ms: 1.20x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 5.18 ms: 1.22x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.25 ms: 1.24x slower                                                    |
| many_optionals                   | 195 us                                                   | 250 us: 1.28x slower                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.72 ms: 1.31x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 583 us: 1.39x slower                                                     |
| coverage                         | 26.9 ms                                                  | 40.0 ms: 1.49x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.5 ms: 2.41x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                             |
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250506-3.14.0a7+-c4bcc6a-NOGIL/bm-20250506-macm4pro-arm64-python-c4bcc6a77864b42574ec-3.14.0a7+-c4bcc6a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.092x faster

# HPT report

- Reliability score: 98.01% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.27x