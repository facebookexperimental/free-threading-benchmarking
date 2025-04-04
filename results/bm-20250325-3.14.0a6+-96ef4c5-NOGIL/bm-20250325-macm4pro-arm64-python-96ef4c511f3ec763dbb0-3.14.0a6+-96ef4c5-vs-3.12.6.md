# Results vs. 3.12.6

- fork: python
- ref: 96ef4c511f3ec763dbb0
- machine: darwin-arm64
- commit hash: 96ef4c5
- commit date: 2025-03-25
- overall geometric mean: 1.049x faster
- HPT reliability: 54.65%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 125 ms: 1.10x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| html5lib       | 23.0 ms                                                  | 25.3 ms: 1.10x slower                                                    |
| sphinx         | 434 ms                                                   | 426 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                    | 1.04x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 204 ms: 2.36x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 216 ms: 2.29x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 204 ms: 2.18x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 220 ms: 2.09x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 89.8 ms: 1.92x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 127 ms: 1.81x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 107 ms: 1.67x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 135 ms: 1.64x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 236 ms: 1.43x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 246 ms: 1.35x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                    |
| async_generators                 | 206 ms                                                   | 180 ms: 1.15x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 115 ms: 1.15x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 116 ms: 1.03x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 227 ms: 1.07x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 52.6 ms: 1.16x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.9 ms: 2.52x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.34x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 32.1 ms: 1.18x faster                                                    |
| pidigits       | 161 ms                                                   | 165 ms: 1.02x slower                                                     |
| nbody          | 54.2 ms                                                  | 62.1 ms: 1.15x slower                                                    |
| Geometric mean | (ref)                                                    | 1.00x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.59 ms: 1.05x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 55.6 ms: 1.02x slower                                                    |
| regex_dna      | 99.6 ms                                                  | 103 ms: 1.03x slower                                                     |
| regex_v8       | 9.59 ms                                                  | 9.93 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.01x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 37.3 ms: 1.38x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 58.8 ms: 1.15x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.8 ms: 1.03x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.6 ms: 1.03x slower                                                    |
| tomli_loads          | 957 ms                                                   | 1.00 sec: 1.05x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 112 us: 1.08x slower                                                     |
| json_loads           | 10.9 us                                                  | 12.2 us: 1.13x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 161 us: 1.15x slower                                                     |
| json_dumps           | 4.26 ms                                                  | 5.16 ms: 1.21x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.01x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.57 ms: 1.19x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.61 ms: 1.33x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.26x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 24.7 ms: 1.13x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 12.0 ms: 1.14x slower                                                    |
| mako            | 4.77 ms                                                  | 5.81 ms: 1.22x slower                                                    |
| django_template | 13.6 ms                                                  | 16.7 ms: 1.23x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.18x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 766 us: 2.62x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 204 ms: 2.36x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 216 ms: 2.29x faster                                                     |
| subparsers                       | 20.8 ms                                                  | 9.14 ms: 2.27x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 204 ms: 2.18x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 220 ms: 2.09x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 89.8 ms: 1.92x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 127 ms: 1.81x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 460 us: 1.80x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 107 ms: 1.67x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 135 ms: 1.64x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 236 ms: 1.43x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.3 ms: 1.38x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 246 ms: 1.35x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                    |
| deepcopy                         | 161 us                                                   | 128 us: 1.26x faster                                                     |
| float                            | 37.9 ms                                                  | 32.1 ms: 1.18x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 821 ns: 1.18x faster                                                     |
| generators                       | 21.9 ms                                                  | 18.8 ms: 1.17x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 15.8 us: 1.16x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 58.8 ms: 1.15x faster                                                    |
| async_generators                 | 206 ms                                                   | 180 ms: 1.15x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 115 ms: 1.15x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.82 us: 1.12x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.11x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 19.2 ms: 1.11x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.32 us: 1.11x faster                                                    |
| k_core                           | 1.12 sec                                                 | 1.02 sec: 1.10x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.05 sec: 1.09x faster                                                   |
| pylint                           | 128 ms                                                   | 119 ms: 1.07x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 57.4 ms: 1.06x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 51.8 ms: 1.05x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.59 ms: 1.05x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 49.4 ns: 1.03x faster                                                    |
| raytrace                         | 145 ms                                                   | 141 ms: 1.03x faster                                                     |
| go                               | 70.0 ms                                                  | 68.1 ms: 1.03x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.8 ms: 1.03x faster                                                    |
| pycparser                        | 497 ms                                                   | 485 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                     |
| sphinx                           | 434 ms                                                   | 426 ms: 1.02x faster                                                     |
| pyflate                          | 216 ms                                                   | 212 ms: 1.02x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 42.9 ms: 1.01x faster                                                    |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.73 ms: 1.01x slower                                                    |
| regex_compile                    | 54.6 ms                                                  | 55.6 ms: 1.02x slower                                                    |
| pidigits                         | 161 ms                                                   | 165 ms: 1.02x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 116 ms: 1.03x slower                                                     |
| xml_etree_process                | 26.7 ms                                                  | 27.6 ms: 1.03x slower                                                    |
| regex_dna                        | 99.6 ms                                                  | 103 ms: 1.03x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.93 ms: 1.04x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.33 ms: 1.04x slower                                                    |
| scimark_fft                      | 142 ms                                                   | 148 ms: 1.04x slower                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 74.4 us: 1.05x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 1.00 sec: 1.05x slower                                                   |
| json                             | 1.93 ms                                                  | 2.03 ms: 1.05x slower                                                    |
| logging_format                   | 2.80 us                                                  | 2.95 us: 1.05x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 40.9 ms: 1.05x slower                                                    |
| logging_simple                   | 2.57 us                                                  | 2.71 us: 1.05x slower                                                    |
| thrift                           | 322 us                                                   | 340 us: 1.06x slower                                                     |
| chaos                            | 28.9 ms                                                  | 30.6 ms: 1.06x slower                                                    |
| mdp                              | 1.09 sec                                                 | 1.16 sec: 1.06x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 61.4 ms: 1.07x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 227 ms: 1.07x slower                                                     |
| shortest_path                    | 219 ms                                                   | 234 ms: 1.07x slower                                                     |
| sympy_str                        | 104 ms                                                   | 112 ms: 1.08x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 42.8 ms: 1.08x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.25 ms: 1.08x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 112 us: 1.08x slower                                                     |
| hexiom                           | 3.04 ms                                                  | 3.31 ms: 1.09x slower                                                    |
| sqlalchemy_declarative           | 46.8 ms                                                  | 51.2 ms: 1.10x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 35.3 ms: 1.10x slower                                                    |
| 2to3                             | 114 ms                                                   | 125 ms: 1.10x slower                                                     |
| html5lib                         | 23.0 ms                                                  | 25.3 ms: 1.10x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 56.5 ms: 1.10x slower                                                    |
| connected_components             | 201 ms                                                   | 223 ms: 1.11x slower                                                     |
| json_loads                       | 10.9 us                                                  | 12.2 us: 1.13x slower                                                    |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.84 ms: 1.13x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 24.7 ms: 1.13x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 28.9 ms: 1.14x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 190 ms: 1.14x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 12.0 ms: 1.14x slower                                                    |
| nbody                            | 54.2 ms                                                  | 62.1 ms: 1.15x slower                                                    |
| richards                         | 22.4 ms                                                  | 25.8 ms: 1.15x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 161 us: 1.15x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 52.6 ms: 1.16x slower                                                    |
| fannkuch                         | 176 ms                                                   | 204 ms: 1.16x slower                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 390 ms: 1.19x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 791 ms: 1.19x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 9.57 ms: 1.19x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 57.3 ms: 1.20x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 5.16 ms: 1.21x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.81 ms: 1.22x slower                                                    |
| django_template                  | 13.6 ms                                                  | 16.7 ms: 1.23x slower                                                    |
| many_optionals                   | 195 us                                                   | 250 us: 1.28x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 7.61 ms: 1.33x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.52 ms: 1.35x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 588 us: 1.40x slower                                                     |
| coverage                         | 26.9 ms                                                  | 39.0 ms: 1.45x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.9 ms: 2.52x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.04x faster                                                             |
Ignored benchmarks (9) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250325-3.14.0a6+-96ef4c5-NOGIL/bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.049x faster

# HPT report

- Reliability score: 54.65% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.23x