# Results vs. 3.12.6

- fork: python
- ref: 98b4cd6fe9348ac24d5c
- machine: darwin-arm64
- commit hash: 98b4cd6
- commit date: 2025-09-02
- overall geometric mean: 1.075x faster
- HPT reliability: 93.22%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.26x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 124 ms: 1.09x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.00 sec: 1.02x faster                                                  |
| html5lib       | 23.0 ms                                                  | 23.8 ms: 1.03x slower                                                   |
| sphinx         | 434 ms                                                   | 416 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 207 ms: 2.40x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 201 ms: 2.39x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 198 ms: 2.26x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 212 ms: 2.17x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 88.3 ms: 1.95x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 125 ms: 1.84x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.69x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 237 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 244 ms: 1.36x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 11.0 ms: 1.23x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 182 ms: 1.13x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 228 ms: 1.07x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.5 ms: 1.09x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.1 ms: 2.46x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.36x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.8 ms: 1.27x faster                                                   |
| pidigits       | 161 ms                                                   | 166 ms: 1.03x slower                                                    |
| nbody          | 54.2 ms                                                  | 58.0 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.36 ms: 1.02x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 97.5 ms: 1.02x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 53.6 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.6 ms: 1.34x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 60.1 ms: 1.13x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 4.06 ms: 1.05x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 37.1 ms: 1.05x faster                                                   |
| tomli_loads          | 957 ms                                                   | 975 ms: 1.02x slower                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.4 ms: 1.02x slower                                                   |
| json_loads           | 10.9 us                                                  | 11.4 us: 1.05x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 112 us: 1.09x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 157 us: 1.13x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.02x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.67 ms: 1.21x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 7.02 ms: 1.23x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.22x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 24.5 ms: 1.13x slower                                                   |
| genshi_text     | 10.5 ms                                                  | 11.8 ms: 1.13x slower                                                   |
| django_template | 13.6 ms                                                  | 16.6 ms: 1.22x slower                                                   |
| mako            | 4.77 ms                                                  | 5.90 ms: 1.24x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.18x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 779 us: 2.58x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 207 ms: 2.40x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 201 ms: 2.39x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 198 ms: 2.26x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 212 ms: 2.17x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 88.3 ms: 1.95x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 125 ms: 1.84x faster                                                    |
| mdp                              | 1.09 sec                                                 | 602 ms: 1.81x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 479 us: 1.73x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.69x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 237 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 244 ms: 1.36x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.6 ms: 1.34x faster                                                   |
| deepcopy                         | 161 us                                                   | 122 us: 1.32x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 14.3 us: 1.28x faster                                                   |
| float                            | 37.9 ms                                                  | 29.8 ms: 1.27x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 11.0 ms: 1.23x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.39 us: 1.17x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 828 ns: 1.17x faster                                                    |
| generators                       | 21.9 ms                                                  | 19.2 ms: 1.14x faster                                                   |
| async_generators                 | 206 ms                                                   | 182 ms: 1.13x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 60.1 ms: 1.13x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.29 us: 1.13x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                   |
| subparsers                       | 20.8 ms                                                  | 18.5 ms: 1.12x faster                                                   |
| k_core                           | 1.12 sec                                                 | 997 ms: 1.12x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 19.0 ms: 1.12x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 45.5 ns: 1.12x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.12x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.01 sec: 1.11x faster                                                  |
| go                               | 70.0 ms                                                  | 63.1 ms: 1.11x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 55.7 ms: 1.09x faster                                                   |
| raytrace                         | 145 ms                                                   | 133 ms: 1.09x faster                                                    |
| pylint                           | 128 ms                                                   | 119 ms: 1.07x faster                                                    |
| pyflate                          | 216 ms                                                   | 203 ms: 1.07x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 51.4 ms: 1.06x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.06 ms: 1.05x faster                                                   |
| pycparser                        | 497 ms                                                   | 474 ms: 1.05x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.1 ms: 1.05x faster                                                   |
| sphinx                           | 434 ms                                                   | 416 ms: 1.04x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.67 ms: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.36 ms: 1.02x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 97.5 ms: 1.02x faster                                                   |
| docutils                         | 1.02 sec                                                 | 1.00 sec: 1.02x faster                                                  |
| regex_compile                    | 54.6 ms                                                  | 53.6 ms: 1.02x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.55 us: 1.01x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 43.3 ms: 1.00x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 143 ms: 1.01x slower                                                    |
| logging_format                   | 2.80 us                                                  | 2.84 us: 1.01x slower                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 8.13 ms: 1.01x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 975 ms: 1.02x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.4 ms: 1.02x slower                                                   |
| chaos                            | 28.9 ms                                                  | 29.8 ms: 1.03x slower                                                   |
| json                             | 1.93 ms                                                  | 1.99 ms: 1.03x slower                                                   |
| pidigits                         | 161 ms                                                   | 166 ms: 1.03x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.8 ms: 1.03x slower                                                   |
| hexiom                           | 3.04 ms                                                  | 3.17 ms: 1.04x slower                                                   |
| thrift                           | 322 us                                                   | 338 us: 1.05x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 348 ms: 1.06x slower                                                    |
| fannkuch                         | 176 ms                                                   | 186 ms: 1.06x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 34.2 ms: 1.06x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 708 ms: 1.07x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.22 ms: 1.07x slower                                                   |
| nbody                            | 54.2 ms                                                  | 58.0 ms: 1.07x slower                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 75.9 us: 1.07x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 61.6 ms: 1.07x slower                                                   |
| shortest_path                    | 219 ms                                                   | 235 ms: 1.07x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 228 ms: 1.07x slower                                                    |
| richards                         | 22.4 ms                                                  | 24.1 ms: 1.08x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 27.3 ms: 1.08x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 43.1 ms: 1.09x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 49.5 ms: 1.09x slower                                                   |
| sympy_str                        | 104 ms                                                   | 113 ms: 1.09x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 112 us: 1.09x slower                                                    |
| 2to3                             | 114 ms                                                   | 124 ms: 1.09x slower                                                    |
| connected_components             | 201 ms                                                   | 223 ms: 1.11x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 43.7 ms: 1.13x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 24.5 ms: 1.13x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 57.8 ms: 1.13x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 157 us: 1.13x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.8 ms: 1.13x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.00 ms: 1.15x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 193 ms: 1.16x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 56.9 ms: 1.19x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.67 ms: 1.21x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.6 ms: 1.22x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 7.02 ms: 1.23x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.90 ms: 1.24x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 592 us: 1.41x slower                                                    |
| coverage                         | 26.9 ms                                                  | 39.8 ms: 1.48x slower                                                   |
| many_optionals                   | 195 us                                                   | 336 us: 1.72x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.1 ms: 2.46x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                            |

Benchmark hidden because not significant (2): dask, async_tree_eager_memoization_tg
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250902-3.15.0a0-98b4cd6-NOGIL/bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.075x faster

# HPT report

- Reliability score: 93.22% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.26x