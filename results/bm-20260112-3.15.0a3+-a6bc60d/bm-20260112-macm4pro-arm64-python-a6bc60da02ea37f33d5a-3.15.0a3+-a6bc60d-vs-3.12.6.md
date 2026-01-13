# Results vs. 3.12.6

- fork: python
- ref: a6bc60da02ea37f33d5a
- machine: darwin-arm64
- commit hash: a6bc60d
- commit date: 2026-01-12
- overall geometric mean: 1.156x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260112-macm4pro-arm64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 115 ms: 1.01x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.01x slower                                                   |
| html5lib       | 23.0 ms                                                  | 21.8 ms: 1.05x faster                                                    |
| sphinx         | 434 ms                                                   | 395 ms: 1.10x faster                                                     |
| Geometric mean | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260112-macm4pro-arm64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 223 ms: 2.22x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 227 ms: 2.12x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 222 ms: 2.01x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 237 ms: 1.94x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 103 ms: 1.73x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 101 ms: 1.71x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 137 ms: 1.69x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 141 ms: 1.58x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 9.83 ms: 1.38x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 256 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 253 ms: 1.32x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                     |
| async_generators                 | 206 ms                                                   | 177 ms: 1.16x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.5 ms: 1.12x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 121 ms: 1.07x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 242 ms: 1.14x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.0 ms: 2.49x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.32x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260112-macm4pro-arm64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.2 ms: 1.39x faster                                                    |
| nbody          | 54.2 ms                                                  | 44.8 ms: 1.21x faster                                                    |
| pidigits       | 161 ms                                                   | 167 ms: 1.04x slower                                                     |
| Geometric mean | (ref)                                                    | 1.18x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260112-macm4pro-arm64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 46.0 ms: 1.19x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 96.6 ms: 1.03x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.77 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260112-macm4pro-arm64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.0 ms: 1.29x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 34.3 ms: 1.13x faster                                                    |
| tomli_loads          | 957 ms                                                   | 847 ms: 1.13x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.85 ms: 1.11x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 61.6 ms: 1.10x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.4 ms: 1.10x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 100 us: 1.03x faster                                                     |
| pickle_pure_python   | 139 us                                                   | 141 us: 1.01x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.09x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260112-macm4pro-arm64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.94 ms: 1.12x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.43 ms: 1.13x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.12x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260112-macm4pro-arm64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.77 ms: 1.07x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.2 ms: 1.03x faster                                                    |
| django_template | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.01x faster                                                             |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260112-macm4pro-arm64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.10 ms: 5.07x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 223 ms: 2.22x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 227 ms: 2.12x faster                                                     |
| mdp                              | 1.09 sec                                                 | 542 ms: 2.01x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 222 ms: 2.01x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 237 ms: 1.94x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 103 ms: 1.73x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 101 ms: 1.71x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 137 ms: 1.69x faster                                                     |
| deepcopy                         | 161 us                                                   | 99.9 us: 1.62x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 141 ms: 1.58x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.9 us: 1.54x faster                                                    |
| float                            | 37.9 ms                                                  | 27.2 ms: 1.39x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.83 ms: 1.38x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.06 us: 1.38x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.16 us: 1.37x faster                                                    |
| go                               | 70.0 ms                                                  | 52.8 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 256 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 253 ms: 1.32x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.0 ms: 1.29x faster                                                    |
| raytrace                         | 145 ms                                                   | 113 ms: 1.29x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 43.3 ms: 1.26x faster                                                    |
| k_core                           | 1.12 sec                                                 | 900 ms: 1.24x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 41.3 ns: 1.23x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 49.6 ms: 1.23x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                     |
| nbody                            | 54.2 ms                                                  | 44.8 ms: 1.21x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 46.0 ms: 1.19x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 120 ms: 1.18x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.46 ms: 1.18x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 43.8 ms: 1.17x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.5 ms: 1.17x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.8 ms: 1.17x faster                                                    |
| async_generators                 | 206 ms                                                   | 177 ms: 1.16x faster                                                     |
| pyflate                          | 216 ms                                                   | 187 ms: 1.16x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.22 us: 1.16x faster                                                    |
| chaos                            | 28.9 ms                                                  | 25.0 ms: 1.16x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.80 ms: 1.15x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.44 us: 1.15x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.14x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 62.2 us: 1.14x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 34.3 ms: 1.13x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 847 ms: 1.13x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 38.6 ms: 1.13x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.5 ms: 1.12x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.0 ms: 1.12x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 22.7 ms: 1.12x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 19.0 ms: 1.12x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.85 ms: 1.11x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.75 ms: 1.11x faster                                                    |
| pylint                           | 128 ms                                                   | 116 ms: 1.11x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 61.6 ms: 1.10x faster                                                    |
| sphinx                           | 434 ms                                                   | 395 ms: 1.10x faster                                                     |
| xml_etree_process                | 26.7 ms                                                  | 24.4 ms: 1.10x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 613 ms: 1.08x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 304 ms: 1.08x faster                                                     |
| genshi_text                      | 10.5 ms                                                  | 9.77 ms: 1.07x faster                                                    |
| pycparser                        | 497 ms                                                   | 465 ms: 1.07x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.52 ms: 1.07x faster                                                    |
| thrift                           | 322 us                                                   | 305 us: 1.06x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 21.8 ms: 1.05x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.1 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.04x faster                                                     |
| sympy_sum                        | 57.6 ms                                                  | 55.7 ms: 1.03x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.6 ms: 1.03x faster                                                    |
| fannkuch                         | 176 ms                                                   | 171 ms: 1.03x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 100 us: 1.03x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 21.2 ms: 1.03x faster                                                    |
| json                             | 1.93 ms                                                  | 1.91 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| 2to3                             | 114 ms                                                   | 115 ms: 1.01x slower                                                     |
| sqlite_synth                     | 967 ns                                                   | 974 ns: 1.01x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 169 ms: 1.01x slower                                                     |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.01x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 141 us: 1.01x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.77 ms: 1.02x slower                                                    |
| shortest_path                    | 219 ms                                                   | 223 ms: 1.02x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 431 us: 1.03x slower                                                     |
| connected_components             | 201 ms                                                   | 207 ms: 1.03x slower                                                     |
| pidigits                         | 161 ms                                                   | 167 ms: 1.04x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 50.6 ms: 1.06x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.13 ms: 1.06x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.79 ms: 1.07x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 121 ms: 1.07x slower                                                     |
| django_template                  | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.94 ms: 1.12x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.43 ms: 1.13x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 242 ms: 1.14x slower                                                     |
| create_gc_cycles                 | 830 us                                                   | 953 us: 1.15x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 45.9 ms: 1.16x slower                                                    |
| coverage                         | 26.9 ms                                                  | 31.9 ms: 1.19x slower                                                    |
| many_optionals                   | 195 us                                                   | 260 us: 1.33x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.0 ms: 2.49x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.15x faster                                                             |

Benchmark hidden because not significant (2): json_loads, mako
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260112-3.15.0a3+-a6bc60d/bm-20260112-macm4pro-arm64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.156x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.23x