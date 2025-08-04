# Results vs. 3.12.6

- fork: python
- ref: 406dc714f6b4dbc18d4e
- machine: darwin-arm64
- commit hash: 406dc71
- commit date: 2025-08-03
- overall geometric mean: 1.103x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 113 ms: 1.01x faster                                                    |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.1 ms: 1.05x slower                                                   |
| sphinx         | 434 ms                                                   | 408 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.00x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 243 ms: 2.04x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 247 ms: 1.94x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 250 ms: 1.84x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 252 ms: 1.77x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.64x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.61x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 145 ms: 1.54x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.97 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 262 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 262 ms: 1.27x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                    |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.1 ms: 1.11x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.05x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 246 ms: 1.16x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 86.9 ms: 2.70x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.26x faster                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 31.0 ms: 1.22x faster                                                   |
| nbody          | 54.2 ms                                                  | 48.5 ms: 1.12x faster                                                   |
| pidigits       | 161 ms                                                   | 164 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 48.6 ms: 1.12x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 96.7 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 43.1 ms: 1.20x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 60.9 ms: 1.12x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.1 ms: 1.11x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.2 ms: 1.06x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 99.0 us: 1.04x faster                                                   |
| tomli_loads          | 957 ms                                                   | 927 ms: 1.03x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.01x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 143 us: 1.03x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.49 ms: 1.05x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.63 ms: 1.08x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.19 ms: 1.08x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.08x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.86 ms: 1.06x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 21.4 ms: 1.02x faster                                                   |
| mako            | 4.77 ms                                                  | 4.90 ms: 1.03x slower                                                   |
| django_template | 13.6 ms                                                  | 15.2 ms: 1.11x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.01x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 243 ms: 2.04x faster                                                    |
| mdp                              | 1.09 sec                                                 | 538 ms: 2.03x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 247 ms: 1.94x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 250 ms: 1.84x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 252 ms: 1.77x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.64x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.61x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 145 ms: 1.54x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.3 us: 1.49x faster                                                   |
| deepcopy                         | 161 us                                                   | 110 us: 1.47x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.97 ms: 1.36x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.43 us: 1.32x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 262 ms: 1.29x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.14 us: 1.28x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 262 ms: 1.27x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 40.3 ns: 1.26x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.4 ms: 1.26x faster                                                   |
| go                               | 70.0 ms                                                  | 55.9 ms: 1.25x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 44.4 ms: 1.23x faster                                                   |
| float                            | 37.9 ms                                                  | 31.0 ms: 1.22x faster                                                   |
| raytrace                         | 145 ms                                                   | 119 ms: 1.22x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 17.2 ms: 1.21x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 50.8 ms: 1.20x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.1 ms: 1.20x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.0 ms: 1.18x faster                                                   |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                    |
| k_core                           | 1.12 sec                                                 | 959 ms: 1.17x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.52 ms: 1.14x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.14x faster                                                  |
| nqueens                          | 43.5 ms                                                  | 38.5 ms: 1.13x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 48.6 ms: 1.12x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.12x faster                                                   |
| pylint                           | 128 ms                                                   | 114 ms: 1.12x faster                                                    |
| nbody                            | 54.2 ms                                                  | 48.5 ms: 1.12x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 63.5 us: 1.12x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 60.9 ms: 1.12x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 35.1 ms: 1.11x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 41.1 ms: 1.11x faster                                                   |
| pyflate                          | 216 ms                                                   | 197 ms: 1.10x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.5 ms: 1.09x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.79 ms: 1.09x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.37 us: 1.08x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.59 us: 1.08x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.8 ms: 1.08x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.93 ms: 1.08x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 132 ms: 1.08x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.49 ms: 1.07x faster                                                   |
| sphinx                           | 434 ms                                                   | 408 ms: 1.06x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.86 ms: 1.06x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 23.9 ms: 1.06x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 25.2 ms: 1.06x faster                                                   |
| richards                         | 22.4 ms                                                  | 21.2 ms: 1.06x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.05x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.1 ms: 1.05x faster                                                   |
| thrift                           | 322 us                                                   | 308 us: 1.04x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 99.0 us: 1.04x faster                                                   |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.04x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 927 ms: 1.03x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.7 ms: 1.03x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 56.1 ms: 1.03x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 50.1 ms: 1.02x faster                                                   |
| genshi_xml                       | 21.8 ms                                                  | 21.4 ms: 1.02x faster                                                   |
| pprint_pformat                   | 665 ms                                                   | 655 ms: 1.02x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 323 ms: 1.01x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                    |
| 2to3                             | 114 ms                                                   | 113 ms: 1.01x faster                                                    |
| shortest_path                    | 219 ms                                                   | 217 ms: 1.01x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 957 ns: 1.01x faster                                                    |
| sympy_expand                     | 167 ms                                                   | 170 ms: 1.02x slower                                                    |
| pidigits                         | 161 ms                                                   | 164 ms: 1.02x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                  |
| mako                             | 4.77 ms                                                  | 4.90 ms: 1.03x slower                                                   |
| gc_traversal                     | 2.01 ms                                                  | 2.07 ms: 1.03x slower                                                   |
| fannkuch                         | 176 ms                                                   | 181 ms: 1.03x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 143 us: 1.03x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.6 ms: 1.04x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 24.1 ms: 1.05x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 438 us: 1.05x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.49 ms: 1.05x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.63 ms: 1.08x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.19 ms: 1.08x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 43.3 ms: 1.09x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.2 ms: 1.11x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 941 us: 1.13x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 246 ms: 1.16x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.04 ms: 1.17x slower                                                   |
| coverage                         | 26.9 ms                                                  | 32.4 ms: 1.21x slower                                                   |
| many_optionals                   | 195 us                                                   | 315 us: 1.61x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 86.9 ms: 2.70x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                            |

Benchmark hidden because not significant (5): pycparser, json, asyncio_websockets, regex_v8, connected_components
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250803-3.15.0a0-406dc71/bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.103x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.14x