# Results vs. 3.12.6

- fork: python
- ref: 1a0edb1fa899c067f19b
- machine: darwin-arm64
- commit hash: 1a0edb1
- commit date: 2026-04-09
- overall geometric mean: 1.166x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.24x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8+-1a0edb1 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| docutils       | 1.02 sec                                                 | 998 ms: 1.02x faster                                                     |
| html5lib       | 23.0 ms                                                  | 21.2 ms: 1.08x faster                                                    |
| sphinx         | 434 ms                                                   | 394 ms: 1.10x faster                                                     |
| Geometric mean | (ref)                                                    | 1.05x faster                                                             |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8+-1a0edb1 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 221 ms: 2.25x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 225 ms: 2.13x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 218 ms: 2.04x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 233 ms: 1.97x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 100.0 ms: 1.78x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 100 ms: 1.72x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 136 ms: 1.70x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 135 ms: 1.65x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 247 ms: 1.37x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 250 ms: 1.33x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 104 ms: 1.26x faster                                                     |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.0 ms: 1.14x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 119 ms: 1.06x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 235 ms: 1.10x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.8 ms: 2.51x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.34x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8+-1a0edb1 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 26.6 ms: 1.42x faster                                                    |
| nbody          | 54.2 ms                                                  | 43.6 ms: 1.24x faster                                                    |
| Geometric mean | (ref)                                                    | 1.21x faster                                                             |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8+-1a0edb1 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 46.0 ms: 1.19x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 95.5 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8+-1a0edb1 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.6 ms: 1.30x faster                                                    |
| tomli_loads          | 957 ms                                                   | 808 ms: 1.19x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.71 ms: 1.15x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 35.3 ms: 1.10x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 25.0 ms: 1.07x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 97.5 us: 1.06x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 64.4 ms: 1.05x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.02x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 138 us: 1.01x faster                                                     |
| Geometric mean       | (ref)                                                    | 1.10x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8+-1a0edb1 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.72 ms: 1.09x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.26 ms: 1.10x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8+-1a0edb1 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.56 ms: 1.10x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 20.9 ms: 1.04x faster                                                    |
| mako            | 4.77 ms                                                  | 4.74 ms: 1.01x faster                                                    |
| django_template | 13.6 ms                                                  | 14.8 ms: 1.09x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.01x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8+-1a0edb1 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.99 ms: 5.21x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 221 ms: 2.25x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 225 ms: 2.13x faster                                                     |
| mdp                              | 1.09 sec                                                 | 529 ms: 2.06x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 218 ms: 2.04x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 233 ms: 1.97x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 100.0 ms: 1.78x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 100 ms: 1.72x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 136 ms: 1.70x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 135 ms: 1.65x faster                                                     |
| deepcopy                         | 161 us                                                   | 98.0 us: 1.65x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 11.7 us: 1.56x faster                                                    |
| float                            | 37.9 ms                                                  | 26.6 ms: 1.42x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.01 us: 1.40x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 247 ms: 1.37x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.08 us: 1.36x faster                                                    |
| go                               | 70.0 ms                                                  | 52.0 ms: 1.35x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 250 ms: 1.33x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.6 ms: 1.30x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 42.3 ms: 1.29x faster                                                    |
| raytrace                         | 145 ms                                                   | 114 ms: 1.27x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 104 ms: 1.26x faster                                                     |
| k_core                           | 1.12 sec                                                 | 895 ms: 1.25x faster                                                     |
| nbody                            | 54.2 ms                                                  | 43.6 ms: 1.24x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 49.9 ms: 1.22x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 42.0 ns: 1.21x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.3 ms: 1.20x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 36.3 ms: 1.20x faster                                                    |
| chaos                            | 28.9 ms                                                  | 24.2 ms: 1.19x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.45 ms: 1.19x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 46.0 ms: 1.19x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 808 ms: 1.19x faster                                                     |
| pyflate                          | 216 ms                                                   | 183 ms: 1.18x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 120 ms: 1.18x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.18 us: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                     |
| logging_format                   | 2.80 us                                                  | 2.39 us: 1.17x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.92 sec: 1.17x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.16x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.7 ms: 1.16x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.4 ms: 1.15x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.71 ms: 1.15x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.0 ms: 1.14x faster                                                    |
| pylint                           | 128 ms                                                   | 113 ms: 1.13x faster                                                     |
| scimark_lu                       | 51.3 ms                                                  | 45.5 ms: 1.13x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.73 ms: 1.11x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 22.8 ms: 1.11x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 63.9 us: 1.11x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.87 ms: 1.11x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.3 ms: 1.10x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 35.3 ms: 1.10x faster                                                    |
| sphinx                           | 434 ms                                                   | 394 ms: 1.10x faster                                                     |
| genshi_text                      | 10.5 ms                                                  | 9.56 ms: 1.10x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 21.2 ms: 1.08x faster                                                    |
| pycparser                        | 497 ms                                                   | 460 ms: 1.08x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.44 ms: 1.08x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.0 ms: 1.07x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 97.5 us: 1.06x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 64.4 ms: 1.05x faster                                                    |
| fannkuch                         | 176 ms                                                   | 167 ms: 1.05x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 635 ms: 1.05x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 314 ms: 1.05x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 95.5 ms: 1.04x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 55.3 ms: 1.04x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 20.9 ms: 1.04x faster                                                    |
| json                             | 1.93 ms                                                  | 1.87 ms: 1.04x faster                                                    |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                     |
| docutils                         | 1.02 sec                                                 | 998 ms: 1.02x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 945 ns: 1.02x faster                                                     |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.02x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 38.4 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                     |
| mako                             | 4.77 ms                                                  | 4.74 ms: 1.01x faster                                                    |
| pickle_pure_python               | 139 us                                                   | 138 us: 1.01x faster                                                     |
| shortest_path                    | 219 ms                                                   | 222 ms: 1.01x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 429 us: 1.02x slower                                                     |
| connected_components             | 201 ms                                                   | 206 ms: 1.03x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 172 ms: 1.03x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 49.4 ms: 1.03x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 119 ms: 1.06x slower                                                     |
| django_template                  | 13.6 ms                                                  | 14.8 ms: 1.09x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.72 ms: 1.09x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.26 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 235 ms: 1.10x slower                                                     |
| telco                            | 2.61 ms                                                  | 2.88 ms: 1.11x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 948 us: 1.14x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 45.8 ms: 1.15x slower                                                    |
| coverage                         | 26.9 ms                                                  | 31.9 ms: 1.19x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.42 ms: 1.20x slower                                                    |
| many_optionals                   | 195 us                                                   | 247 us: 1.26x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.8 ms: 2.51x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.16x faster                                                             |

Benchmark hidden because not significant (4): thrift, pidigits, regex_v8, 2to3
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260409-3.15.0a8+-1a0edb1/bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8+-1a0edb1.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.166x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.24x