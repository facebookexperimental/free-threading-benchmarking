# Results vs. 3.12.6

- fork: python
- ref: f96f7c9f5b5db35e8a22
- machine: darwin-arm64
- commit hash: f96f7c9
- commit date: 2025-09-11
- overall geometric mean: 1.105x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 115 ms: 1.01x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.06 sec: 1.04x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.2 ms: 1.05x slower                                                   |
| sphinx         | 434 ms                                                   | 408 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 252 ms: 1.97x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 253 ms: 1.90x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 253 ms: 1.82x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 252 ms: 1.77x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.57x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.49x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.89 ms: 1.37x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 264 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 179 ms: 1.15x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.2 ms: 1.08x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.18x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.0 ms: 2.74x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.8 ms: 1.27x faster                                                   |
| nbody          | 54.2 ms                                                  | 47.6 ms: 1.14x faster                                                   |
| pidigits       | 161 ms                                                   | 165 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.12x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 48.2 ms: 1.13x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 97.6 ms: 1.02x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.85 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 44.6 ms: 1.15x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.80 ms: 1.12x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.1 ms: 1.11x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 61.3 ms: 1.11x faster                                                   |
| tomli_loads          | 957 ms                                                   | 890 ms: 1.08x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 25.1 ms: 1.06x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 98.9 us: 1.04x faster                                                   |
| json_loads           | 10.9 us                                                  | 10.9 us: 1.01x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 143 us: 1.03x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.69 ms: 1.08x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.23 ms: 1.09x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.80 ms: 1.07x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 21.4 ms: 1.02x faster                                                   |
| mako            | 4.77 ms                                                  | 4.91 ms: 1.03x slower                                                   |
| django_template | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.02x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.09 sec                                                 | 539 ms: 2.03x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 252 ms: 1.97x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 253 ms: 1.90x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 253 ms: 1.82x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 252 ms: 1.77x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.57x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                    |
| deepcopy                         | 161 us                                                   | 105 us: 1.54x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.1 us: 1.52x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.49x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.89 ms: 1.37x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.38 us: 1.33x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.11 us: 1.32x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 39.5 ns: 1.29x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 264 ms: 1.28x faster                                                    |
| float                            | 37.9 ms                                                  | 29.8 ms: 1.27x faster                                                   |
| go                               | 70.0 ms                                                  | 55.6 ms: 1.26x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 43.5 ms: 1.25x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.6 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                    |
| raytrace                         | 145 ms                                                   | 118 ms: 1.22x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 50.0 ms: 1.22x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 17.4 ms: 1.19x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.0 ms: 1.18x faster                                                   |
| k_core                           | 1.12 sec                                                 | 954 ms: 1.17x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.17x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.6 ms: 1.15x faster                                                   |
| async_generators                 | 206 ms                                                   | 179 ms: 1.15x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.51 ms: 1.14x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.96 sec: 1.14x faster                                                  |
| nbody                            | 54.2 ms                                                  | 47.6 ms: 1.14x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 62.4 us: 1.14x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 48.2 ms: 1.13x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 38.6 ms: 1.13x faster                                                   |
| pylint                           | 128 ms                                                   | 114 ms: 1.13x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.80 ms: 1.12x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.50 us: 1.12x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.31 us: 1.11x faster                                                   |
| pyflate                          | 216 ms                                                   | 195 ms: 1.11x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.1 ms: 1.11x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 35.1 ms: 1.11x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 61.3 ms: 1.11x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.4 ms: 1.10x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.90 ms: 1.09x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.79 ms: 1.09x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 131 ms: 1.09x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.2 ms: 1.08x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 890 ms: 1.08x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.47 ms: 1.07x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 9.80 ms: 1.07x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 48.2 ms: 1.06x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 25.1 ms: 1.06x faster                                                   |
| sphinx                           | 434 ms                                                   | 408 ms: 1.06x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 24.0 ms: 1.06x faster                                                   |
| richards                         | 22.4 ms                                                  | 21.2 ms: 1.06x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 98.9 us: 1.04x faster                                                   |
| sympy_str                        | 104 ms                                                   | 100 ms: 1.04x faster                                                    |
| thrift                           | 322 us                                                   | 312 us: 1.03x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 56.0 ms: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.9 ms: 1.03x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 97.6 ms: 1.02x faster                                                   |
| pprint_pformat                   | 665 ms                                                   | 653 ms: 1.02x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.4 ms: 1.02x faster                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 323 ms: 1.02x faster                                                    |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 958 ns: 1.01x faster                                                    |
| shortest_path                    | 219 ms                                                   | 217 ms: 1.01x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.9 us: 1.01x slower                                                   |
| 2to3                             | 114 ms                                                   | 115 ms: 1.01x slower                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 169 ms: 1.01x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 427 us: 1.02x slower                                                    |
| pidigits                         | 161 ms                                                   | 165 ms: 1.02x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.85 ms: 1.03x slower                                                   |
| mako                             | 4.77 ms                                                  | 4.91 ms: 1.03x slower                                                   |
| fannkuch                         | 176 ms                                                   | 181 ms: 1.03x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 143 us: 1.03x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.07 ms: 1.03x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.06 sec: 1.04x slower                                                  |
| html5lib                         | 23.0 ms                                                  | 24.2 ms: 1.05x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 50.7 ms: 1.06x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 42.3 ms: 1.07x slower                                                   |
| telco                            | 2.61 ms                                                  | 2.80 ms: 1.07x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.69 ms: 1.08x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.23 ms: 1.09x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 935 us: 1.13x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.18x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.8 ms: 1.22x slower                                                   |
| many_optionals                   | 195 us                                                   | 323 us: 1.65x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.0 ms: 2.74x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.11x faster                                                            |

Benchmark hidden because not significant (3): pycparser, json, connected_components
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250911-3.15.0a0-f96f7c9/bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.105x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.15x