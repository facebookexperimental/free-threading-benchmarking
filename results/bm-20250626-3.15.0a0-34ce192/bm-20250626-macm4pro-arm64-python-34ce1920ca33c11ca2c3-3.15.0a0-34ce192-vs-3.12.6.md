# Results vs. 3.12.6

- fork: python
- ref: 34ce1920ca33c11ca2c3
- machine: darwin-arm64
- commit hash: 34ce192
- commit date: 2025-06-26
- overall geometric mean: 1.096x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250626-macm4pro-arm64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.1 ms: 1.05x slower                                                   |
| sphinx         | 434 ms                                                   | 412 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x slower                                                            |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250626-macm4pro-arm64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 251 ms: 1.98x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 258 ms: 1.86x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 259 ms: 1.77x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 255 ms: 1.75x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 110 ms: 1.56x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.56x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 150 ms: 1.54x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.50x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.31x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 265 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                    |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.8 ms: 1.06x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.17x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 249 ms: 1.17x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.4 ms: 2.75x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.23x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250626-macm4pro-arm64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.8 ms: 1.23x faster                                                   |
| nbody          | 54.2 ms                                                  | 48.7 ms: 1.11x faster                                                   |
| pidigits       | 161 ms                                                   | 167 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250626-macm4pro-arm64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 49.1 ms: 1.11x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 97.9 ms: 1.02x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.81 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250626-macm4pro-arm64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 43.8 ms: 1.18x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 60.9 ms: 1.12x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.0 ms: 1.08x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.7 ms: 1.04x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 100 us: 1.03x faster                                                    |
| tomli_loads          | 957 ms                                                   | 935 ms: 1.02x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 4.47 ms: 1.05x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 148 us: 1.06x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250626-macm4pro-arm64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.62 ms: 1.08x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.16 ms: 1.08x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.08x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250626-macm4pro-arm64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.1 ms: 1.03x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 22.3 ms: 1.02x slower                                                   |
| mako            | 4.77 ms                                                  | 4.93 ms: 1.03x slower                                                   |
| django_template | 13.6 ms                                                  | 15.7 ms: 1.15x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.04x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250626-macm4pro-arm64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.74 ms: 2.13x faster                                                   |
| mdp                              | 1.09 sec                                                 | 521 ms: 2.09x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 251 ms: 1.98x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 258 ms: 1.86x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 259 ms: 1.77x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 255 ms: 1.75x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 110 ms: 1.56x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.56x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 150 ms: 1.54x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.50x faster                                                    |
| deepcopy                         | 161 us                                                   | 113 us: 1.44x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.8 us: 1.42x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.53 us: 1.31x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.31x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 265 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 40.9 ns: 1.24x faster                                                   |
| float                            | 37.9 ms                                                  | 30.8 ms: 1.23x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.19 us: 1.22x faster                                                   |
| go                               | 70.0 ms                                                  | 57.4 ms: 1.22x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 45.3 ms: 1.20x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 51.4 ms: 1.19x faster                                                   |
| generators                       | 21.9 ms                                                  | 18.5 ms: 1.18x faster                                                   |
| raytrace                         | 145 ms                                                   | 123 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.8 ms: 1.18x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.1 ms: 1.18x faster                                                   |
| k_core                           | 1.12 sec                                                 | 951 ms: 1.18x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                  |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 60.9 ms: 1.12x faster                                                   |
| pylint                           | 128 ms                                                   | 115 ms: 1.11x faster                                                    |
| nbody                            | 54.2 ms                                                  | 48.7 ms: 1.11x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 49.1 ms: 1.11x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 64.1 us: 1.11x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.56 ms: 1.10x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.2 ms: 1.10x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.89 ms: 1.10x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 39.7 ms: 1.10x faster                                                   |
| pyflate                          | 216 ms                                                   | 198 ms: 1.09x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.5 ms: 1.09x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 131 ms: 1.08x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.8 ms: 1.08x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 36.0 ms: 1.08x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.84 ms: 1.07x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.63 us: 1.07x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 42.8 ms: 1.06x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.55 ms: 1.06x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.43 us: 1.06x faster                                                   |
| sphinx                           | 434 ms                                                   | 412 ms: 1.05x faster                                                    |
| thrift                           | 322 us                                                   | 309 us: 1.04x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.7 ms: 1.04x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 10.1 ms: 1.03x faster                                                   |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.03x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 100 us: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 935 ms: 1.02x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 38.1 ms: 1.02x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 97.9 ms: 1.02x faster                                                   |
| richards                         | 22.4 ms                                                  | 22.1 ms: 1.01x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 50.7 ms: 1.01x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 25.1 ms: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 57.1 ms: 1.01x faster                                                   |
| json                             | 1.93 ms                                                  | 1.92 ms: 1.01x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| shortest_path                    | 219 ms                                                   | 221 ms: 1.01x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 48.4 ms: 1.01x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 170 ms: 1.02x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 676 ms: 1.02x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 335 ms: 1.02x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.81 ms: 1.02x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 22.3 ms: 1.02x slower                                                   |
| connected_components             | 201 ms                                                   | 206 ms: 1.02x slower                                                    |
| fannkuch                         | 176 ms                                                   | 180 ms: 1.03x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| mako                             | 4.77 ms                                                  | 4.93 ms: 1.03x slower                                                   |
| pidigits                         | 161 ms                                                   | 167 ms: 1.03x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 437 us: 1.04x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 24.1 ms: 1.05x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.47 ms: 1.05x slower                                                   |
| gc_traversal                     | 2.01 ms                                                  | 2.13 ms: 1.06x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 148 us: 1.06x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.62 ms: 1.08x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.16 ms: 1.08x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.1 ms: 1.11x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 957 us: 1.15x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.7 ms: 1.15x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.17x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.05 ms: 1.17x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 249 ms: 1.17x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.8 ms: 1.22x slower                                                   |
| many_optionals                   | 195 us                                                   | 247 us: 1.26x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.4 ms: 2.75x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                            |

Benchmark hidden because not significant (4): json_loads, sqlite_synth, 2to3, pycparser
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250626-3.15.0a0-34ce192/bm-20250626-macm4pro-arm64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.096x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.15x