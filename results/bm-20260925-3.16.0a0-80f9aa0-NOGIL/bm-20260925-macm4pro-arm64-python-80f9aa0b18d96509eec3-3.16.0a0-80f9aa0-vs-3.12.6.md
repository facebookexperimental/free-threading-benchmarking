# Results vs. 3.12.6

- fork: python
- ref: 80f9aa0b18d96509eec3
- machine: darwin-arm64
- commit hash: 80f9aa0
- commit date: 2026-09-25
- overall geometric mean: 1.003x faster
- HPT reliability: 80.85%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260925-macm4pro-arm64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 137 ms: 1.20x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.10 sec: 1.08x slower                                                  |
| html5lib       | 23.0 ms                                                  | 23.9 ms: 1.04x slower                                                   |
| sphinx         | 434 ms                                                   | 469 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                    | 1.10x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260925-macm4pro-arm64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 316 ms: 1.57x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 310 ms: 1.55x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 306 ms: 1.46x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 321 ms: 1.43x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 186 ms: 1.24x faster                                                    |
| async_generators                 | 206 ms                                                   | 167 ms: 1.24x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 147 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 306 ms: 1.10x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 203 ms: 1.10x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 164 ms: 1.09x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 12.7 ms: 1.06x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 317 ms: 1.05x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 150 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 266 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 284 ms: 1.34x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 167 ms: 1.48x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 71.0 ms: 1.56x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 119 ms: 3.70x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.00x slower                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260925-macm4pro-arm64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 35.2 ms: 1.08x faster                                                   |
| pidigits       | 161 ms                                                   | 164 ms: 1.02x slower                                                    |
| nbody          | 54.2 ms                                                  | 62.3 ms: 1.15x slower                                                   |
| Geometric mean | (ref)                                                    | 1.03x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260925-macm4pro-arm64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.33 ms: 1.25x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 91.2 ms: 1.09x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.20 ms: 1.04x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 69.7 ms: 1.28x slower                                                   |
| Geometric mean | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260925-macm4pro-arm64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 43.2 ms: 1.19x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.77 ms: 1.13x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 60.7 ms: 1.12x faster                                                   |
| tomli_loads          | 957 ms                                                   | 949 ms: 1.01x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 39.5 ms: 1.02x slower                                                   |
| json_loads           | 10.9 us                                                  | 11.1 us: 1.03x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 119 us: 1.15x slower                                                    |
| xml_etree_process    | 26.7 ms                                                  | 31.3 ms: 1.17x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 165 us: 1.18x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260925-macm4pro-arm64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 10.1 ms: 1.26x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 7.37 ms: 1.29x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.28x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260925-macm4pro-arm64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 6.02 ms: 1.26x slower                                                   |
| django_template | 13.6 ms                                                  | 18.1 ms: 1.33x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.29x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260925-macm4pro-arm64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.59 ms: 4.52x faster                                                   |
| gc_traversal                     | 2.01 ms                                                  | 777 us: 2.58x faster                                                    |
| pylint                           | 128 ms                                                   | 53.9 ms: 2.37x faster                                                   |
| mdp                              | 1.09 sec                                                 | 636 ms: 1.72x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 492 us: 1.69x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 316 ms: 1.57x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 310 ms: 1.55x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 306 ms: 1.46x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 321 ms: 1.43x faster                                                    |
| deepcopy                         | 161 us                                                   | 119 us: 1.36x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.33 ms: 1.25x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 186 ms: 1.24x faster                                                    |
| async_generators                 | 206 ms                                                   | 167 ms: 1.24x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.2 ms: 1.19x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 820 ns: 1.18x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 147 ms: 1.17x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 61.0 us: 1.16x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.27 us: 1.15x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.77 ms: 1.13x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 60.7 ms: 1.12x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.00 sec: 1.12x faster                                                  |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.11x faster                                                   |
| k_core                           | 1.12 sec                                                 | 1.01 sec: 1.11x faster                                                  |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 306 ms: 1.10x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 16.6 us: 1.10x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 8.93 us: 1.10x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 203 ms: 1.10x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 91.2 ms: 1.09x faster                                                   |
| async_tree_none                  | 178 ms                                                   | 164 ms: 1.09x faster                                                    |
| float                            | 37.9 ms                                                  | 35.2 ms: 1.08x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 19.9 ms: 1.07x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 12.7 ms: 1.06x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 317 ms: 1.05x faster                                                    |
| go                               | 70.0 ms                                                  | 67.1 ms: 1.04x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.20 ms: 1.04x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 52.7 ms: 1.03x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 138 ms: 1.03x faster                                                    |
| pyflate                          | 216 ms                                                   | 213 ms: 1.01x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 949 ms: 1.01x faster                                                    |
| pycparser                        | 497 ms                                                   | 504 ms: 1.01x slower                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 39.5 ms: 1.02x slower                                                   |
| pidigits                         | 161 ms                                                   | 164 ms: 1.02x slower                                                    |
| raytrace                         | 145 ms                                                   | 148 ms: 1.02x slower                                                    |
| logging_simple                   | 2.57 us                                                  | 2.64 us: 1.03x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.1 us: 1.03x slower                                                   |
| nqueens                          | 43.5 ms                                                  | 44.7 ms: 1.03x slower                                                   |
| json                             | 1.93 ms                                                  | 1.99 ms: 1.03x slower                                                   |
| logging_format                   | 2.80 us                                                  | 2.89 us: 1.03x slower                                                   |
| scimark_sor                      | 61.0 ms                                                  | 63.4 ms: 1.04x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 23.9 ms: 1.04x slower                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 8.45 ms: 1.05x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.21 ms: 1.06x slower                                                   |
| chaos                            | 28.9 ms                                                  | 31.0 ms: 1.07x slower                                                   |
| fannkuch                         | 176 ms                                                   | 189 ms: 1.07x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.10 sec: 1.08x slower                                                  |
| sphinx                           | 434 ms                                                   | 469 ms: 1.08x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 62.6 ms: 1.09x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 42.4 ms: 1.09x slower                                                   |
| sympy_str                        | 104 ms                                                   | 115 ms: 1.11x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 44.0 ms: 1.11x slower                                                   |
| thrift                           | 322 us                                                   | 358 us: 1.11x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 35.8 ms: 1.11x slower                                                   |
| generators                       | 21.9 ms                                                  | 24.8 ms: 1.13x slower                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 150 ms: 1.14x slower                                                    |
| nbody                            | 54.2 ms                                                  | 62.3 ms: 1.15x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 266 ms: 1.15x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 55.1 ms: 1.15x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 119 us: 1.15x slower                                                    |
| shortest_path                    | 219 ms                                                   | 254 ms: 1.16x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 383 ms: 1.17x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 195 ms: 1.17x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.56 ms: 1.17x slower                                                   |
| xml_etree_process                | 26.7 ms                                                  | 31.3 ms: 1.17x slower                                                   |
| deltablue                        | 1.73 ms                                                  | 2.02 ms: 1.17x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 165 us: 1.18x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 789 ms: 1.19x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 30.2 ms: 1.19x slower                                                   |
| richards                         | 22.4 ms                                                  | 26.7 ms: 1.19x slower                                                   |
| 2to3                             | 114 ms                                                   | 137 ms: 1.20x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.15 ms: 1.21x slower                                                   |
| connected_components             | 201 ms                                                   | 243 ms: 1.21x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 10.1 ms: 1.26x slower                                                   |
| mako                             | 4.77 ms                                                  | 6.02 ms: 1.26x slower                                                   |
| regex_compile                    | 54.6 ms                                                  | 69.7 ms: 1.28x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 7.37 ms: 1.29x slower                                                   |
| django_template                  | 13.6 ms                                                  | 18.1 ms: 1.33x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 284 ms: 1.34x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 69.3 ms: 1.35x slower                                                   |
| many_optionals                   | 195 us                                                   | 275 us: 1.41x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 589 us: 1.41x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 167 ms: 1.48x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.4 ms: 1.50x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 71.0 ms: 1.56x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 119 ms: 3.70x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.00x slower                                                            |

Benchmark hidden because not significant (1): logging_silent
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260925-3.16.0a0-80f9aa0-NOGIL/bm-20260925-macm4pro-arm64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.003x faster

# HPT report

- Reliability score: 80.85% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.33x