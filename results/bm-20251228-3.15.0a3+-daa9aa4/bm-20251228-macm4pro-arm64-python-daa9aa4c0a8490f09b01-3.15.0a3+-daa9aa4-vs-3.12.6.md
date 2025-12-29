# Results vs. 3.12.6

- fork: python
- ref: daa9aa4c0a8490f09b01
- machine: darwin-arm64
- commit hash: daa9aa4
- commit date: 2025-12-28
- overall geometric mean: 1.157x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3+-daa9aa4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 113 ms: 1.01x faster                                                     |
| html5lib       | 23.0 ms                                                  | 21.9 ms: 1.05x faster                                                    |
| sphinx         | 434 ms                                                   | 396 ms: 1.10x faster                                                     |
| Geometric mean | (ref)                                                    | 1.04x faster                                                             |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3+-daa9aa4 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 223 ms: 2.23x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 224 ms: 2.14x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 220 ms: 2.02x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 233 ms: 1.97x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 103 ms: 1.73x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 99.9 ms: 1.72x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 136 ms: 1.70x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 139 ms: 1.60x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 255 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 252 ms: 1.32x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                     |
| async_generators                 | 206 ms                                                   | 176 ms: 1.17x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.8 ms: 1.12x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 122 ms: 1.08x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.13x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 81.8 ms: 2.55x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.32x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3+-daa9aa4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.6 ms: 1.37x faster                                                    |
| nbody          | 54.2 ms                                                  | 45.5 ms: 1.19x faster                                                    |
| pidigits       | 161 ms                                                   | 166 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                    | 1.17x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3+-daa9aa4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 45.4 ms: 1.20x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 97.1 ms: 1.03x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.83 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3+-daa9aa4 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.7 ms: 1.33x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.81 ms: 1.12x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 34.9 ms: 1.12x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.7 ms: 1.08x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 63.1 ms: 1.08x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 98.1 us: 1.05x faster                                                    |
| tomli_loads          | 957 ms                                                   | 926 ms: 1.03x faster                                                     |
| json_loads           | 10.9 us                                                  | 10.8 us: 1.01x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 140 us: 1.01x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3+-daa9aa4 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.89 ms: 1.11x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.40 ms: 1.12x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.11x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3+-daa9aa4 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.73 ms: 1.08x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.0 ms: 1.04x faster                                                    |
| mako            | 4.77 ms                                                  | 4.70 ms: 1.02x faster                                                    |
| django_template | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.01x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3+-daa9aa4 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.06 ms: 5.11x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 223 ms: 2.23x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 224 ms: 2.14x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 220 ms: 2.02x faster                                                     |
| mdp                              | 1.09 sec                                                 | 544 ms: 2.01x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 233 ms: 1.97x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 103 ms: 1.73x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 99.9 ms: 1.72x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 136 ms: 1.70x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.2 us: 1.63x faster                                                    |
| deepcopy                         | 161 us                                                   | 100 us: 1.61x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 139 ms: 1.60x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 7.04 us: 1.40x faster                                                    |
| float                            | 37.9 ms                                                  | 27.6 ms: 1.37x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.07 us: 1.37x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.7 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 255 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 252 ms: 1.32x faster                                                     |
| go                               | 70.0 ms                                                  | 53.1 ms: 1.32x faster                                                    |
| raytrace                         | 145 ms                                                   | 114 ms: 1.27x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 41.0 ns: 1.24x faster                                                    |
| k_core                           | 1.12 sec                                                 | 905 ms: 1.24x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 49.6 ms: 1.23x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 44.8 ms: 1.21x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 45.4 ms: 1.20x faster                                                    |
| nbody                            | 54.2 ms                                                  | 45.5 ms: 1.19x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 120 ms: 1.18x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.46 ms: 1.18x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.6 ms: 1.18x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.76 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 176 ms: 1.17x faster                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.5 ms: 1.17x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 44.0 ms: 1.17x faster                                                    |
| pyflate                          | 216 ms                                                   | 186 ms: 1.17x faster                                                     |
| chaos                            | 28.9 ms                                                  | 24.9 ms: 1.16x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.22 us: 1.16x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.45 us: 1.14x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 62.1 us: 1.14x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.14x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.8 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.99 sec: 1.12x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.81 ms: 1.12x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.8 ms: 1.12x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 22.7 ms: 1.12x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 34.9 ms: 1.12x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.1 ms: 1.11x faster                                                    |
| pylint                           | 128 ms                                                   | 115 ms: 1.11x faster                                                     |
| hexiom                           | 3.04 ms                                                  | 2.74 ms: 1.11x faster                                                    |
| sphinx                           | 434 ms                                                   | 396 ms: 1.10x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 39.9 ms: 1.09x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.7 ms: 1.08x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.73 ms: 1.08x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 63.1 ms: 1.08x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.47 ms: 1.07x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 620 ms: 1.07x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 307 ms: 1.07x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 36.8 ms: 1.06x faster                                                    |
| pycparser                        | 497 ms                                                   | 472 ms: 1.05x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 21.9 ms: 1.05x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 98.1 us: 1.05x faster                                                    |
| thrift                           | 322 us                                                   | 308 us: 1.04x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 21.0 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| sympy_sum                        | 57.6 ms                                                  | 55.6 ms: 1.04x faster                                                    |
| fannkuch                         | 176 ms                                                   | 170 ms: 1.03x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 926 ms: 1.03x faster                                                     |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.03x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 97.1 ms: 1.03x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.70 ms: 1.02x faster                                                    |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                     |
| 2to3                             | 114 ms                                                   | 113 ms: 1.01x faster                                                     |
| json                             | 1.93 ms                                                  | 1.92 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| json_loads                       | 10.9 us                                                  | 10.8 us: 1.01x faster                                                    |
| pickle_pure_python               | 139 us                                                   | 140 us: 1.01x slower                                                     |
| shortest_path                    | 219 ms                                                   | 221 ms: 1.01x slower                                                     |
| connected_components             | 201 ms                                                   | 204 ms: 1.01x slower                                                     |
| sqlite_synth                     | 967 ns                                                   | 982 ns: 1.02x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 170 ms: 1.02x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 427 us: 1.02x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.83 ms: 1.02x slower                                                    |
| pidigits                         | 161 ms                                                   | 166 ms: 1.03x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.08 ms: 1.03x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 50.5 ms: 1.06x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 122 ms: 1.08x slower                                                     |
| django_template                  | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.89 ms: 1.11x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.91 ms: 1.12x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 930 us: 1.12x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.40 ms: 1.12x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 44.9 ms: 1.13x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.13x slower                                                     |
| coverage                         | 26.9 ms                                                  | 31.5 ms: 1.17x slower                                                    |
| many_optionals                   | 195 us                                                   | 255 us: 1.30x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 81.8 ms: 2.55x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.15x faster                                                             |

Benchmark hidden because not significant (1): docutils
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251228-3.15.0a3+-daa9aa4/bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3+-daa9aa4.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.157x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.21x