# Results vs. 3.12.6

- fork: python
- ref: 432ddd99e2b06a75a4f4
- machine: darwin-arm64
- commit hash: 432ddd9
- commit date: 2026-02-09
- overall geometric mean: 1.172x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260209-macm4pro-arm64-python-432ddd99e2b06a75a4f4-3.15.0a5+-432ddd9 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 112 ms: 1.01x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.00 sec: 1.02x faster                                                   |
| html5lib       | 23.0 ms                                                  | 21.2 ms: 1.09x faster                                                    |
| sphinx         | 434 ms                                                   | 387 ms: 1.12x faster                                                     |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260209-macm4pro-arm64-python-432ddd99e2b06a75a4f4-3.15.0a5+-432ddd9 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 220 ms: 2.25x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 227 ms: 2.11x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 225 ms: 2.04x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 222 ms: 2.00x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 96.5 ms: 1.78x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 135 ms: 1.71x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 138 ms: 1.61x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 250 ms: 1.35x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 257 ms: 1.30x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 104 ms: 1.26x faster                                                     |
| async_generators                 | 206 ms                                                   | 176 ms: 1.18x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.3 ms: 1.13x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 119 ms: 1.06x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 235 ms: 1.10x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.9 ms: 2.46x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.34x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260209-macm4pro-arm64-python-432ddd99e2b06a75a4f4-3.15.0a5+-432ddd9 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.6 ms: 1.37x faster                                                    |
| nbody          | 54.2 ms                                                  | 44.3 ms: 1.22x faster                                                    |
| pidigits       | 161 ms                                                   | 161 ms: 1.00x faster                                                     |
| Geometric mean | (ref)                                                    | 1.19x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260209-macm4pro-arm64-python-432ddd99e2b06a75a4f4-3.15.0a5+-432ddd9 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 46.0 ms: 1.19x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.1 ms: 1.06x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.49 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260209-macm4pro-arm64-python-432ddd99e2b06a75a4f4-3.15.0a5+-432ddd9 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.0 ms: 1.32x faster                                                    |
| tomli_loads          | 957 ms                                                   | 839 ms: 1.14x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 34.1 ms: 1.14x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.78 ms: 1.13x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 60.7 ms: 1.12x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.2 ms: 1.11x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 97.8 us: 1.05x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.6 us: 1.03x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 138 us: 1.01x faster                                                     |
| Geometric mean       | (ref)                                                    | 1.11x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260209-macm4pro-arm64-python-432ddd99e2b06a75a4f4-3.15.0a5+-432ddd9 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.70 ms: 1.09x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.28 ms: 1.10x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260209-macm4pro-arm64-python-432ddd99e2b06a75a4f4-3.15.0a5+-432ddd9 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.49 ms: 1.11x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.1 ms: 1.03x faster                                                    |
| mako            | 4.77 ms                                                  | 4.73 ms: 1.01x faster                                                    |
| django_template | 13.6 ms                                                  | 14.4 ms: 1.06x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.02x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260209-macm4pro-arm64-python-432ddd99e2b06a75a4f4-3.15.0a5+-432ddd9 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.01 ms: 5.18x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 220 ms: 2.25x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 227 ms: 2.11x faster                                                     |
| mdp                              | 1.09 sec                                                 | 528 ms: 2.07x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 225 ms: 2.04x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 222 ms: 2.00x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 96.5 ms: 1.78x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 135 ms: 1.71x faster                                                     |
| deepcopy                         | 161 us                                                   | 97.3 us: 1.66x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 138 ms: 1.61x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.6 us: 1.58x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 6.98 us: 1.41x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.06 us: 1.38x faster                                                    |
| float                            | 37.9 ms                                                  | 27.6 ms: 1.37x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 250 ms: 1.35x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                    |
| go                               | 70.0 ms                                                  | 52.7 ms: 1.33x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.0 ms: 1.32x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 257 ms: 1.30x faster                                                     |
| raytrace                         | 145 ms                                                   | 114 ms: 1.27x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 104 ms: 1.26x faster                                                     |
| k_core                           | 1.12 sec                                                 | 892 ms: 1.25x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 40.8 ns: 1.25x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 44.0 ms: 1.24x faster                                                    |
| nbody                            | 54.2 ms                                                  | 44.3 ms: 1.22x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 50.5 ms: 1.21x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 118 ms: 1.20x faster                                                     |
| generators                       | 21.9 ms                                                  | 18.4 ms: 1.20x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 43.0 ms: 1.19x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 46.0 ms: 1.19x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.18 us: 1.18x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.47 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 176 ms: 1.18x faster                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.6 ms: 1.17x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.41 us: 1.16x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.79 ms: 1.16x faster                                                    |
| pyflate                          | 216 ms                                                   | 187 ms: 1.16x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.15x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 61.5 us: 1.15x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.4 ms: 1.15x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 839 ms: 1.14x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 34.1 ms: 1.14x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.14x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 38.3 ms: 1.14x faster                                                    |
| pylint                           | 128 ms                                                   | 113 ms: 1.14x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.3 ms: 1.13x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.78 ms: 1.13x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.71 ms: 1.12x faster                                                    |
| sphinx                           | 434 ms                                                   | 387 ms: 1.12x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 60.7 ms: 1.12x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.0 ms: 1.11x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.2 ms: 1.11x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 22.9 ms: 1.11x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.2 ms: 1.11x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.49 ms: 1.11x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 21.2 ms: 1.09x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.39 ms: 1.09x faster                                                    |
| pycparser                        | 497 ms                                                   | 460 ms: 1.08x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 622 ms: 1.07x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 308 ms: 1.07x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 94.1 ms: 1.06x faster                                                    |
| thrift                           | 322 us                                                   | 304 us: 1.06x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 97.8 us: 1.05x faster                                                    |
| fannkuch                         | 176 ms                                                   | 167 ms: 1.05x faster                                                     |
| sympy_str                        | 104 ms                                                   | 99.2 ms: 1.05x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 54.8 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| json                             | 1.93 ms                                                  | 1.86 ms: 1.04x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 934 ns: 1.03x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 21.1 ms: 1.03x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.7 ms: 1.03x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.6 us: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.00 sec: 1.02x faster                                                   |
| 2to3                             | 114 ms                                                   | 112 ms: 1.01x faster                                                     |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.49 ms: 1.01x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.73 ms: 1.01x faster                                                    |
| pickle_pure_python               | 139 us                                                   | 138 us: 1.01x faster                                                     |
| pidigits                         | 161 ms                                                   | 161 ms: 1.00x faster                                                     |
| sympy_expand                     | 167 ms                                                   | 168 ms: 1.00x slower                                                     |
| shortest_path                    | 219 ms                                                   | 220 ms: 1.00x slower                                                     |
| connected_components             | 201 ms                                                   | 204 ms: 1.02x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 48.7 ms: 1.02x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.06 ms: 1.03x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 431 us: 1.03x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 119 ms: 1.06x slower                                                     |
| django_template                  | 13.6 ms                                                  | 14.4 ms: 1.06x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.80 ms: 1.07x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.70 ms: 1.09x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 902 us: 1.09x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.28 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 235 ms: 1.10x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 44.7 ms: 1.13x slower                                                    |
| coverage                         | 26.9 ms                                                  | 31.8 ms: 1.19x slower                                                    |
| many_optionals                   | 195 us                                                   | 252 us: 1.29x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.9 ms: 2.46x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.17x faster                                                             |
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260209-3.15.0a5+-432ddd9/bm-20260209-macm4pro-arm64-python-432ddd99e2b06a75a4f4-3.15.0a5+-432ddd9.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.172x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: 1.23x