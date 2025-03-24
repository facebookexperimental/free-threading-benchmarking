# Results vs. 3.12.6

- fork: python
- ref: af29d5cfd19bf2656955
- machine: darwin-arm64
- commit hash: af29d5c
- commit date: 2025-03-24
- overall geometric mean: 1.020x slower
- HPT reliability: 99.74%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 133 ms: 1.16x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                   |
| html5lib       | 23.0 ms                                                  | 24.3 ms: 1.06x slower                                                    |
| sphinx         | 434 ms                                                   | 441 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                    | 1.07x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 233 ms: 2.13x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 226 ms: 2.12x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 224 ms: 1.99x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 241 ms: 1.91x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 100 ms: 1.72x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 137 ms: 1.69x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.54x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 145 ms: 1.53x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 244 ms: 1.38x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 255 ms: 1.31x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 12.1 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 120 ms: 1.09x faster                                                     |
| async_generators                 | 206 ms                                                   | 193 ms: 1.07x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 232 ms: 1.00x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 122 ms: 1.08x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 234 ms: 1.10x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 56.5 ms: 1.24x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.0 ms: 2.77x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 36.1 ms: 1.05x faster                                                    |
| pidigits       | 161 ms                                                   | 162 ms: 1.00x slower                                                     |
| nbody          | 54.2 ms                                                  | 78.5 ms: 1.45x slower                                                    |
| Geometric mean | (ref)                                                    | 1.11x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 93.3 ms: 1.07x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.68 ms: 1.01x slower                                                    |
| regex_compile  | 54.6 ms                                                  | 59.4 ms: 1.09x slower                                                    |
| Geometric mean | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.5 ms: 1.30x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 55.8 ms: 1.22x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 41.2 ms: 1.06x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.9 us: 1.10x slower                                                    |
| tomli_loads          | 957 ms                                                   | 1.09 sec: 1.14x slower                                                   |
| xml_etree_process    | 26.7 ms                                                  | 30.6 ms: 1.15x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 5.19 ms: 1.22x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 170 us: 1.22x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 128 us: 1.24x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.07x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.26 ms: 1.16x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.30 ms: 1.28x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.22x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 26.3 ms: 1.21x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 13.2 ms: 1.26x slower                                                    |
| mako            | 4.77 ms                                                  | 6.20 ms: 1.30x slower                                                    |
| django_template | 13.6 ms                                                  | 18.3 ms: 1.34x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.28x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.46 ms: 2.20x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 931 us: 2.16x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 233 ms: 2.13x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 226 ms: 2.12x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 224 ms: 1.99x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 241 ms: 1.91x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 100 ms: 1.72x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 137 ms: 1.69x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 501 us: 1.66x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.54x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 145 ms: 1.53x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 244 ms: 1.38x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 255 ms: 1.31x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.5 ms: 1.30x faster                                                    |
| deepcopy                         | 161 us                                                   | 129 us: 1.25x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 55.8 ms: 1.22x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 846 ns: 1.14x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 12.1 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 120 ms: 1.09x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 19.8 ms: 1.07x faster                                                    |
| async_generators                 | 206 ms                                                   | 193 ms: 1.07x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 93.3 ms: 1.07x faster                                                    |
| k_core                           | 1.12 sec                                                 | 1.06 sec: 1.06x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.7 ms: 1.05x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.39 us: 1.05x faster                                                    |
| float                            | 37.9 ms                                                  | 36.1 ms: 1.05x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 17.5 us: 1.05x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                                     |
| pidigits                         | 161 ms                                                   | 162 ms: 1.00x slower                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 232 ms: 1.00x slower                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.26 sec: 1.01x slower                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.68 ms: 1.01x slower                                                    |
| generators                       | 21.9 ms                                                  | 22.2 ms: 1.01x slower                                                    |
| sphinx                           | 434 ms                                                   | 441 ms: 1.02x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 40.4 ms: 1.02x slower                                                    |
| pycparser                        | 497 ms                                                   | 509 ms: 1.02x slower                                                     |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                   |
| comprehensions                   | 9.84 us                                                  | 10.2 us: 1.04x slower                                                    |
| json                             | 1.93 ms                                                  | 2.02 ms: 1.05x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 24.3 ms: 1.06x slower                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 41.2 ms: 1.06x slower                                                    |
| go                               | 70.0 ms                                                  | 74.8 ms: 1.07x slower                                                    |
| pyflate                          | 216 ms                                                   | 234 ms: 1.08x slower                                                     |
| thrift                           | 322 us                                                   | 349 us: 1.08x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 122 ms: 1.08x slower                                                     |
| logging_silent                   | 50.9 ns                                                  | 55.4 ns: 1.09x slower                                                    |
| regex_compile                    | 54.6 ms                                                  | 59.4 ms: 1.09x slower                                                    |
| mdp                              | 1.09 sec                                                 | 1.20 sec: 1.10x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.9 us: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 234 ms: 1.10x slower                                                     |
| sqlalchemy_declarative           | 46.8 ms                                                  | 51.7 ms: 1.10x slower                                                    |
| spectral_norm                    | 54.4 ms                                                  | 60.2 ms: 1.11x slower                                                    |
| raytrace                         | 145 ms                                                   | 162 ms: 1.11x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 64.3 ms: 1.12x slower                                                    |
| logging_simple                   | 2.57 us                                                  | 2.88 us: 1.12x slower                                                    |
| logging_format                   | 2.80 us                                                  | 3.15 us: 1.12x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 9.15 ms: 1.14x slower                                                    |
| shortest_path                    | 219 ms                                                   | 250 ms: 1.14x slower                                                     |
| tomli_loads                      | 957 ms                                                   | 1.09 sec: 1.14x slower                                                   |
| nqueens                          | 43.5 ms                                                  | 49.7 ms: 1.14x slower                                                    |
| scimark_fft                      | 142 ms                                                   | 162 ms: 1.14x slower                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 81.3 us: 1.15x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 30.6 ms: 1.15x slower                                                    |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.93 ms: 1.15x slower                                                    |
| sympy_str                        | 104 ms                                                   | 120 ms: 1.15x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 9.26 ms: 1.16x slower                                                    |
| scimark_sor                      | 61.0 ms                                                  | 70.7 ms: 1.16x slower                                                    |
| chaos                            | 28.9 ms                                                  | 33.5 ms: 1.16x slower                                                    |
| 2to3                             | 114 ms                                                   | 133 ms: 1.16x slower                                                     |
| deltablue                        | 1.73 ms                                                  | 2.02 ms: 1.17x slower                                                    |
| connected_components             | 201 ms                                                   | 235 ms: 1.17x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 46.8 ms: 1.20x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.50 ms: 1.20x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 26.3 ms: 1.21x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 5.19 ms: 1.22x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 170 us: 1.22x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 204 ms: 1.22x slower                                                     |
| richards_super                   | 25.4 ms                                                  | 31.2 ms: 1.23x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 56.5 ms: 1.24x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 128 us: 1.24x slower                                                     |
| richards                         | 22.4 ms                                                  | 27.9 ms: 1.24x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 13.2 ms: 1.26x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 40.6 ms: 1.26x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 60.3 ms: 1.26x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 417 ms: 1.27x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 849 ms: 1.28x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 7.30 ms: 1.28x slower                                                    |
| fannkuch                         | 176 ms                                                   | 226 ms: 1.29x slower                                                     |
| mako                             | 4.77 ms                                                  | 6.20 ms: 1.30x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.95 ms: 1.30x slower                                                    |
| many_optionals                   | 195 us                                                   | 256 us: 1.31x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 67.7 ms: 1.32x slower                                                    |
| django_template                  | 13.6 ms                                                  | 18.3 ms: 1.34x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.64 ms: 1.40x slower                                                    |
| nbody                            | 54.2 ms                                                  | 78.5 ms: 1.45x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 615 us: 1.47x slower                                                     |
| coverage                         | 26.9 ms                                                  | 40.2 ms: 1.49x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.0 ms: 2.77x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.02x slower                                                             |

Benchmark hidden because not significant (1): pylint
Ignored benchmarks (9) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250324-3.14.0a6+-af29d5c-NOGIL/bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.020x slower

# HPT report

- Reliability score: 99.74% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.22x