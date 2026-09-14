# Results vs. 3.12.6

- fork: python
- ref: fd0970c0ab7eb8c685ef
- machine: darwin-arm64
- commit hash: fd0970c
- commit date: 2026-09-13
- overall geometric mean: 1.084x faster
- HPT reliability: 98.19%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260913-macm4pro-arm64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 126 ms: 1.11x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.02x slower                                                  |
| html5lib       | 23.0 ms                                                  | 22.6 ms: 1.02x faster                                                   |
| sphinx         | 434 ms                                                   | 436 ms: 1.00x slower                                                    |
| Geometric mean | (ref)                                                    | 1.03x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260913-macm4pro-arm64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 293 ms: 1.69x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 288 ms: 1.67x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 285 ms: 1.57x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 296 ms: 1.55x faster                                                    |
| async_generators                 | 206 ms                                                   | 153 ms: 1.35x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 176 ms: 1.31x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 136 ms: 1.26x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 150 ms: 1.19x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 188 ms: 1.18x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 289 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 298 ms: 1.12x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 144 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 253 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 271 ms: 1.28x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 64.3 ms: 1.41x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 161 ms: 1.43x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 111 ms: 3.46x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260913-macm4pro-arm64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 31.1 ms: 1.22x faster                                                   |
| nbody          | 54.2 ms                                                  | 51.6 ms: 1.05x faster                                                   |
| pidigits       | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260913-macm4pro-arm64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.34 ms: 1.25x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 93.5 ms: 1.07x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.14 ms: 1.05x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 60.7 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260913-macm4pro-arm64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 41.7 ms: 1.24x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.70 ms: 1.15x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 60.7 ms: 1.12x faster                                                   |
| tomli_loads          | 957 ms                                                   | 880 ms: 1.09x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.1 ms: 1.05x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 104 us: 1.01x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.3 us: 1.04x slower                                                   |
| xml_etree_process    | 26.7 ms                                                  | 27.9 ms: 1.04x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 149 us: 1.07x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260913-macm4pro-arm64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 10.3 ms: 1.29x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 7.61 ms: 1.33x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.31x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260913-macm4pro-arm64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 5.51 ms: 1.15x slower                                                   |
| django_template | 13.6 ms                                                  | 16.2 ms: 1.19x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.17x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260913-macm4pro-arm64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.14 ms: 5.01x faster                                                   |
| gc_traversal                     | 2.01 ms                                                  | 785 us: 2.56x faster                                                    |
| pylint                           | 128 ms                                                   | 53.3 ms: 2.40x faster                                                   |
| mdp                              | 1.09 sec                                                 | 586 ms: 1.86x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 293 ms: 1.69x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 498 us: 1.67x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 288 ms: 1.67x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 285 ms: 1.57x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 296 ms: 1.55x faster                                                    |
| deepcopy                         | 161 us                                                   | 108 us: 1.49x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 13.4 us: 1.37x faster                                                   |
| async_generators                 | 206 ms                                                   | 153 ms: 1.35x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 53.7 us: 1.32x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.44 us: 1.32x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 176 ms: 1.31x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 136 ms: 1.26x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.17 us: 1.25x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.34 ms: 1.25x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 41.7 ms: 1.24x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 790 ns: 1.22x faster                                                    |
| float                            | 37.9 ms                                                  | 31.1 ms: 1.22x faster                                                   |
| go                               | 70.0 ms                                                  | 57.4 ms: 1.22x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 45.4 ms: 1.20x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.87 sec: 1.20x faster                                                  |
| async_tree_none                  | 178 ms                                                   | 150 ms: 1.19x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 188 ms: 1.18x faster                                                    |
| pyflate                          | 216 ms                                                   | 184 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 289 ms: 1.17x faster                                                    |
| raytrace                         | 145 ms                                                   | 126 ms: 1.15x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.70 ms: 1.15x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 37.9 ms: 1.15x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.15x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 124 ms: 1.14x faster                                                    |
| k_core                           | 1.12 sec                                                 | 982 ms: 1.14x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 45.2 ns: 1.13x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.9 ms: 1.12x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 298 ms: 1.12x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 60.7 ms: 1.12x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 55.3 ms: 1.10x faster                                                   |
| generators                       | 21.9 ms                                                  | 20.0 ms: 1.10x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 880 ms: 1.09x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.38 us: 1.08x faster                                                   |
| chaos                            | 28.9 ms                                                  | 26.9 ms: 1.08x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 93.5 ms: 1.07x faster                                                   |
| pycparser                        | 497 ms                                                   | 468 ms: 1.06x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.65 us: 1.06x faster                                                   |
| nbody                            | 54.2 ms                                                  | 51.6 ms: 1.05x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.14 ms: 1.05x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 37.1 ms: 1.05x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.00 ms: 1.04x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.67 ms: 1.03x faster                                                   |
| fannkuch                         | 176 ms                                                   | 170 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 22.6 ms: 1.02x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 31.8 ms: 1.01x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 3.00 ms: 1.01x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.94 ms: 1.01x faster                                                   |
| sphinx                           | 434 ms                                                   | 436 ms: 1.00x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 104 us: 1.01x slower                                                    |
| json                             | 1.93 ms                                                  | 1.97 ms: 1.02x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.02x slower                                                  |
| richards                         | 22.4 ms                                                  | 23.0 ms: 1.03x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 338 ms: 1.03x slower                                                    |
| sympy_str                        | 104 ms                                                   | 108 ms: 1.03x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 26.3 ms: 1.03x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 692 ms: 1.04x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.3 us: 1.04x slower                                                   |
| pidigits                         | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.9 ms: 1.04x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 60.2 ms: 1.05x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 40.6 ms: 1.05x slower                                                   |
| thrift                           | 322 us                                                   | 341 us: 1.06x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 149 us: 1.07x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 52.1 ms: 1.09x slower                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 144 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 253 ms: 1.09x slower                                                    |
| 2to3                             | 114 ms                                                   | 126 ms: 1.11x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 185 ms: 1.11x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 44.1 ms: 1.11x slower                                                   |
| regex_compile                    | 54.6 ms                                                  | 60.7 ms: 1.11x slower                                                   |
| shortest_path                    | 219 ms                                                   | 249 ms: 1.14x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.51 ms: 1.15x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.07 ms: 1.18x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.2 ms: 1.19x slower                                                   |
| connected_components             | 201 ms                                                   | 241 ms: 1.20x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 63.4 ms: 1.24x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 271 ms: 1.28x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 10.3 ms: 1.29x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 551 us: 1.32x slower                                                    |
| many_optionals                   | 195 us                                                   | 260 us: 1.33x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.61 ms: 1.33x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 64.3 ms: 1.41x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 161 ms: 1.43x slower                                                    |
| coverage                         | 26.9 ms                                                  | 39.7 ms: 1.48x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 111 ms: 3.46x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                            |
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260913-3.16.0a0-fd0970c-NOGIL/bm-20260913-macm4pro-arm64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.084x faster

# HPT report

- Reliability score: 98.19% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.36x