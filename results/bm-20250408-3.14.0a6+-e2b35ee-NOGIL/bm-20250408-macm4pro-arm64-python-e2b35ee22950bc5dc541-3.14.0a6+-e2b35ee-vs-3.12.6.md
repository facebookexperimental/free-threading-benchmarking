# Results vs. 3.12.6

- fork: python
- ref: e2b35ee22950bc5dc541
- machine: darwin-arm64
- commit hash: e2b35ee
- commit date: 2025-04-08
- overall geometric mean: 1.107x faster
- HPT reliability: 99.62%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-macm4pro-arm64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 119 ms: 1.05x slower                                                     |
| docutils       | 1.02 sec                                                 | 983 ms: 1.04x faster                                                     |
| html5lib       | 23.0 ms                                                  | 23.9 ms: 1.04x slower                                                    |
| sphinx         | 434 ms                                                   | 414 ms: 1.05x faster                                                     |
| Geometric mean | (ref)                                                    | 1.00x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-macm4pro-arm64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 196 ms: 2.45x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 205 ms: 2.42x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.29x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.20x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 85.9 ms: 2.01x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 230 ms: 1.47x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 240 ms: 1.39x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.31x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                     |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 222 ms: 1.05x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 50.6 ms: 1.11x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.7 ms: 2.42x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.38x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-macm4pro-arm64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.9 ms: 1.36x faster                                                    |
| pidigits       | 161 ms                                                   | 158 ms: 1.02x faster                                                     |
| nbody          | 54.2 ms                                                  | 53.4 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                    | 1.12x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-macm4pro-arm64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.56 ms: 1.07x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 52.4 ms: 1.04x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 101 ms: 1.01x slower                                                     |
| regex_v8       | 9.59 ms                                                  | 9.70 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                    | 1.02x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-macm4pro-arm64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 36.8 ms: 1.40x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 56.9 ms: 1.19x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 36.3 ms: 1.07x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 26.4 ms: 1.01x faster                                                    |
| tomli_loads          | 957 ms                                                   | 948 ms: 1.01x faster                                                     |
| unpickle_pure_python | 103 us                                                   | 107 us: 1.04x slower                                                     |
| pickle_pure_python   | 139 us                                                   | 148 us: 1.06x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.7 us: 1.08x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.97 ms: 1.17x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-macm4pro-arm64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.41 ms: 1.17x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.50 ms: 1.31x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.24x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-macm4pro-arm64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.2 ms: 1.06x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                    |
| mako            | 4.77 ms                                                  | 5.52 ms: 1.16x slower                                                    |
| django_template | 13.6 ms                                                  | 16.4 ms: 1.20x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.12x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-macm4pro-arm64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 732 us: 2.74x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 196 ms: 2.45x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 205 ms: 2.42x faster                                                     |
| subparsers                       | 20.8 ms                                                  | 8.77 ms: 2.37x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.29x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.20x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 85.9 ms: 2.01x faster                                                    |
| mdp                              | 1.09 sec                                                 | 563 ms: 1.94x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 446 us: 1.86x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 230 ms: 1.47x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 36.8 ms: 1.40x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 240 ms: 1.39x faster                                                     |
| float                            | 37.9 ms                                                  | 27.9 ms: 1.36x faster                                                    |
| deepcopy                         | 161 us                                                   | 122 us: 1.33x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.31x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 14.4 us: 1.27x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 802 ns: 1.21x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 56.9 ms: 1.19x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                     |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                     |
| generators                       | 21.9 ms                                                  | 18.6 ms: 1.18x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.25 us: 1.17x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.2 ms: 1.17x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.47 us: 1.16x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                   |
| k_core                           | 1.12 sec                                                 | 985 ms: 1.13x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                    |
| raytrace                         | 145 ms                                                   | 129 ms: 1.13x faster                                                     |
| go                               | 70.0 ms                                                  | 62.4 ms: 1.12x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 54.5 ms: 1.12x faster                                                    |
| pylint                           | 128 ms                                                   | 116 ms: 1.10x faster                                                     |
| pyflate                          | 216 ms                                                   | 197 ms: 1.10x faster                                                     |
| pycparser                        | 497 ms                                                   | 460 ms: 1.08x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 36.3 ms: 1.07x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.8 ms: 1.07x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.56 ms: 1.07x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 47.9 ns: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.05x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.64 ms: 1.05x faster                                                    |
| sphinx                           | 434 ms                                                   | 414 ms: 1.05x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 41.5 ms: 1.05x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 136 ms: 1.04x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 52.4 ms: 1.04x faster                                                    |
| docutils                         | 1.02 sec                                                 | 983 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| pidigits                         | 161 ms                                                   | 158 ms: 1.02x faster                                                     |
| nbody                            | 54.2 ms                                                  | 53.4 ms: 1.02x faster                                                    |
| chaos                            | 28.9 ms                                                  | 28.5 ms: 1.02x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.92 ms: 1.01x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.4 ms: 1.01x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 948 ms: 1.01x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.55 us: 1.01x faster                                                    |
| json                             | 1.93 ms                                                  | 1.95 ms: 1.01x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.10 ms: 1.01x slower                                                    |
| regex_dna                        | 99.6 ms                                                  | 101 ms: 1.01x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.70 ms: 1.01x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 72.0 us: 1.01x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.7 ms: 1.02x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 52.2 ms: 1.02x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.10 ms: 1.02x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 41.0 ms: 1.03x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 107 us: 1.04x slower                                                     |
| html5lib                         | 23.0 ms                                                  | 23.9 ms: 1.04x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 59.8 ms: 1.04x slower                                                    |
| sympy_str                        | 104 ms                                                   | 109 ms: 1.05x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 222 ms: 1.05x slower                                                     |
| 2to3                             | 114 ms                                                   | 119 ms: 1.05x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 40.8 ms: 1.05x slower                                                    |
| sqlalchemy_declarative           | 46.8 ms                                                  | 49.2 ms: 1.05x slower                                                    |
| shortest_path                    | 219 ms                                                   | 230 ms: 1.05x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 148 us: 1.06x slower                                                     |
| genshi_xml                       | 21.8 ms                                                  | 23.2 ms: 1.06x slower                                                    |
| richards                         | 22.4 ms                                                  | 24.0 ms: 1.07x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.7 us: 1.08x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 27.5 ms: 1.08x slower                                                    |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.61 ms: 1.09x slower                                                    |
| connected_components             | 201 ms                                                   | 218 ms: 1.09x slower                                                     |
| fannkuch                         | 176 ms                                                   | 192 ms: 1.09x slower                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 359 ms: 1.10x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 729 ms: 1.10x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 50.6 ms: 1.11x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 186 ms: 1.12x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 54.3 ms: 1.14x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.52 ms: 1.16x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.97 ms: 1.17x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.41 ms: 1.17x slower                                                    |
| django_template                  | 13.6 ms                                                  | 16.4 ms: 1.20x slower                                                    |
| many_optionals                   | 195 us                                                   | 238 us: 1.22x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.22 ms: 1.23x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.50 ms: 1.31x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 576 us: 1.38x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.5 ms: 1.43x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.7 ms: 2.42x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (2): logging_format, async_tree_eager_memoization_tg
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250408-3.14.0a6+-e2b35ee-NOGIL/bm-20250408-macm4pro-arm64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.107x faster

# HPT report

- Reliability score: 99.62% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.22x