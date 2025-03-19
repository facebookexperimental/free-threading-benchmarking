# Results vs. 3.12.6

- fork: python
- ref: d783d7b51d31db568de6
- machine: darwin-arm64
- commit hash: d783d7b
- commit date: 2025-03-18
- overall geometric mean: 1.013x slower
- HPT reliability: 99.33%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6+-d783d7b |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 131 ms: 1.15x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                   |
| html5lib       | 23.0 ms                                                  | 24.2 ms: 1.05x slower                                                    |
| sphinx         | 434 ms                                                   | 435 ms: 1.00x slower                                                     |
| Geometric mean | (ref)                                                    | 1.05x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6+-d783d7b |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 231 ms: 2.14x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 224 ms: 2.14x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 221 ms: 2.02x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 240 ms: 1.91x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 99.6 ms: 1.73x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 139 ms: 1.66x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.54x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.51x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 246 ms: 1.38x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 255 ms: 1.31x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 12.3 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 123 ms: 1.07x faster                                                     |
| async_generators                 | 206 ms                                                   | 201 ms: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 234 ms: 1.10x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 126 ms: 1.12x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 55.7 ms: 1.22x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.1 ms: 2.74x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6+-d783d7b |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 35.5 ms: 1.07x faster                                                    |
| pidigits       | 161 ms                                                   | 159 ms: 1.01x faster                                                     |
| nbody          | 54.2 ms                                                  | 77.5 ms: 1.43x slower                                                    |
| Geometric mean | (ref)                                                    | 1.10x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6+-d783d7b |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.41 ms: 1.18x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 91.4 ms: 1.09x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.47 ms: 1.01x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 58.5 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6+-d783d7b |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.1 ms: 1.29x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 57.3 ms: 1.18x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 40.8 ms: 1.05x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.6 us: 1.07x slower                                                    |
| tomli_loads          | 957 ms                                                   | 1.06 sec: 1.11x slower                                                   |
| xml_etree_process    | 26.7 ms                                                  | 30.2 ms: 1.13x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 170 us: 1.22x slower                                                     |
| json_dumps           | 4.26 ms                                                  | 5.23 ms: 1.23x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 128 us: 1.24x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.06x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6+-d783d7b |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.14 ms: 1.14x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.21 ms: 1.26x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.20x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6+-d783d7b |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 25.9 ms: 1.19x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 13.0 ms: 1.24x slower                                                    |
| mako            | 4.77 ms                                                  | 6.12 ms: 1.28x slower                                                    |
| django_template | 13.6 ms                                                  | 18.2 ms: 1.34x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.26x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6+-d783d7b |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.36 ms: 2.22x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 925 us: 2.17x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 231 ms: 2.14x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 224 ms: 2.14x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 221 ms: 2.02x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 240 ms: 1.91x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 99.6 ms: 1.73x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 139 ms: 1.66x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 503 us: 1.65x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.54x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.51x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 246 ms: 1.38x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 255 ms: 1.31x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.1 ms: 1.29x faster                                                    |
| deepcopy                         | 161 us                                                   | 128 us: 1.26x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 57.3 ms: 1.18x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.41 ms: 1.18x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 838 ns: 1.15x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 12.3 ms: 1.11x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 19.5 ms: 1.09x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 91.4 ms: 1.09x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 123 ms: 1.07x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 11.5 ms: 1.07x faster                                                    |
| float                            | 37.9 ms                                                  | 35.5 ms: 1.07x faster                                                    |
| k_core                           | 1.12 sec                                                 | 1.06 sec: 1.06x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 17.4 us: 1.05x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.39 us: 1.05x faster                                                    |
| async_generators                 | 206 ms                                                   | 201 ms: 1.03x faster                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.47 ms: 1.01x faster                                                    |
| pidigits                         | 161 ms                                                   | 159 ms: 1.01x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| generators                       | 21.9 ms                                                  | 21.9 ms: 1.00x faster                                                    |
| sphinx                           | 434 ms                                                   | 435 ms: 1.00x slower                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.26 sec: 1.01x slower                                                   |
| pycparser                        | 497 ms                                                   | 504 ms: 1.01x slower                                                     |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                   |
| json                             | 1.93 ms                                                  | 1.97 ms: 1.02x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 40.5 ms: 1.02x slower                                                    |
| comprehensions                   | 9.84 us                                                  | 10.1 us: 1.03x slower                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 40.8 ms: 1.05x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 24.2 ms: 1.05x slower                                                    |
| go                               | 70.0 ms                                                  | 74.4 ms: 1.06x slower                                                    |
| thrift                           | 322 us                                                   | 344 us: 1.07x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.6 us: 1.07x slower                                                    |
| regex_compile                    | 54.6 ms                                                  | 58.5 ms: 1.07x slower                                                    |
| pyflate                          | 216 ms                                                   | 234 ms: 1.08x slower                                                     |
| spectral_norm                    | 54.4 ms                                                  | 59.0 ms: 1.08x slower                                                    |
| sqlalchemy_declarative           | 46.8 ms                                                  | 50.8 ms: 1.09x slower                                                    |
| logging_silent                   | 50.9 ns                                                  | 55.3 ns: 1.09x slower                                                    |
| raytrace                         | 145 ms                                                   | 158 ms: 1.09x slower                                                     |
| mdp                              | 1.09 sec                                                 | 1.19 sec: 1.09x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 63.1 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 234 ms: 1.10x slower                                                     |
| logging_simple                   | 2.57 us                                                  | 2.83 us: 1.10x slower                                                    |
| logging_format                   | 2.80 us                                                  | 3.10 us: 1.11x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 1.06 sec: 1.11x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 126 ms: 1.12x slower                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 79.9 us: 1.13x slower                                                    |
| shortest_path                    | 219 ms                                                   | 247 ms: 1.13x slower                                                     |
| xml_etree_process                | 26.7 ms                                                  | 30.2 ms: 1.13x slower                                                    |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.85 ms: 1.13x slower                                                    |
| nqueens                          | 43.5 ms                                                  | 49.4 ms: 1.14x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.14 ms: 1.14x slower                                                    |
| sympy_str                        | 104 ms                                                   | 120 ms: 1.15x slower                                                     |
| 2to3                             | 114 ms                                                   | 131 ms: 1.15x slower                                                     |
| scimark_sor                      | 61.0 ms                                                  | 70.1 ms: 1.15x slower                                                    |
| scimark_fft                      | 142 ms                                                   | 164 ms: 1.16x slower                                                     |
| chaos                            | 28.9 ms                                                  | 33.5 ms: 1.16x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 9.30 ms: 1.16x slower                                                    |
| deltablue                        | 1.73 ms                                                  | 2.01 ms: 1.16x slower                                                    |
| connected_components             | 201 ms                                                   | 235 ms: 1.17x slower                                                     |
| genshi_xml                       | 21.8 ms                                                  | 25.9 ms: 1.19x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 46.5 ms: 1.20x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 200 ms: 1.20x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 170 us: 1.22x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 55.7 ms: 1.22x slower                                                    |
| richards                         | 22.4 ms                                                  | 27.4 ms: 1.22x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.55 ms: 1.23x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 5.23 ms: 1.23x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 13.0 ms: 1.24x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 128 us: 1.24x slower                                                     |
| richards_super                   | 25.4 ms                                                  | 31.5 ms: 1.24x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 59.5 ms: 1.25x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 40.2 ms: 1.25x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 410 ms: 1.25x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 836 ms: 1.26x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 7.21 ms: 1.26x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 65.0 ms: 1.27x slower                                                    |
| fannkuch                         | 176 ms                                                   | 223 ms: 1.27x slower                                                     |
| mako                             | 4.77 ms                                                  | 6.12 ms: 1.28x slower                                                    |
| many_optionals                   | 195 us                                                   | 251 us: 1.28x slower                                                     |
| hexiom                           | 3.04 ms                                                  | 3.95 ms: 1.30x slower                                                    |
| django_template                  | 13.6 ms                                                  | 18.2 ms: 1.34x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.64 ms: 1.40x slower                                                    |
| coverage                         | 26.9 ms                                                  | 38.2 ms: 1.42x slower                                                    |
| nbody                            | 54.2 ms                                                  | 77.5 ms: 1.43x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 612 us: 1.46x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.1 ms: 2.74x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.02x slower                                                             |

Benchmark hidden because not significant (2): pylint, async_tree_eager_cpu_io_mixed
Ignored benchmarks (9) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250318-3.14.0a6+-d783d7b-NOGIL/bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6+-d783d7b.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.013x slower

# HPT report

- Reliability score: 99.33% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.22x