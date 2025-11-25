# Results vs. 3.12.6

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: dc62b62
- commit date: 2025-11-24
- overall geometric mean: 1.166x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251124-macm4pro-arm64-python-main-3.15.0a2+-dc62b62 |
|----------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 118 ms: 1.03x slower                                     |
| html5lib       | 23.0 ms                                                  | 23.4 ms: 1.02x slower                                    |
| sphinx         | 434 ms                                                   | 8.74 ms: 49.61x faster                                   |
| Geometric mean | (ref)                                                    | 3.62x faster                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251124-macm4pro-arm64-python-main-3.15.0a2+-dc62b62 |
|----------------------------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 228 ms: 2.18x faster                                     |
| async_tree_io_tg                 | 480 ms                                                   | 229 ms: 2.10x faster                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 225 ms: 1.98x faster                                     |
| async_tree_io                    | 459 ms                                                   | 233 ms: 1.97x faster                                     |
| async_tree_none_tg               | 172 ms                                                   | 97.9 ms: 1.76x faster                                    |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.74x faster                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 140 ms: 1.65x faster                                     |
| async_tree_memoization           | 223 ms                                                   | 137 ms: 1.62x faster                                     |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 254 ms: 1.33x faster                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 252 ms: 1.32x faster                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                     |
| async_generators                 | 206 ms                                                   | 188 ms: 1.10x faster                                     |
| async_tree_eager                 | 45.6 ms                                                  | 42.9 ms: 1.06x faster                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 126 ms: 1.12x slower                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 83.0 ms: 2.58x slower                                    |
| Geometric mean                   | (ref)                                                    | 1.30x faster                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251124-macm4pro-arm64-python-main-3.15.0a2+-dc62b62 |
|----------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.7 ms: 1.28x faster                                    |
| pidigits       | 161 ms                                                   | 167 ms: 1.04x slower                                     |
| Geometric mean | (ref)                                                    | 1.07x faster                                             |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251124-macm4pro-arm64-python-main-3.15.0a2+-dc62b62 |
|----------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 45.5 ms: 1.20x faster                                    |
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                    |
| regex_dna      | 99.6 ms                                                  | 96.6 ms: 1.03x faster                                    |
| regex_v8       | 9.59 ms                                                  | 9.72 ms: 1.01x slower                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251124-macm4pro-arm64-python-main-3.15.0a2+-dc62b62 |
|----------------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.3 ms: 1.35x faster                                    |
| tomli_loads          | 957 ms                                                   | 818 ms: 1.17x faster                                     |
| xml_etree_generate   | 38.9 ms                                                  | 34.2 ms: 1.14x faster                                    |
| xml_etree_process    | 26.7 ms                                                  | 23.6 ms: 1.13x faster                                    |
| json_dumps           | 4.26 ms                                                  | 3.82 ms: 1.11x faster                                    |
| xml_etree_parse      | 67.9 ms                                                  | 61.5 ms: 1.11x faster                                    |
| unpickle_pure_python | 103 us                                                   | 93.9 us: 1.10x faster                                    |
| pickle_pure_python   | 139 us                                                   | 132 us: 1.06x faster                                     |
| json_loads           | 10.9 us                                                  | 10.9 us: 1.01x slower                                    |
| Geometric mean       | (ref)                                                    | 1.12x faster                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251124-macm4pro-arm64-python-main-3.15.0a2+-dc62b62 |
|------------------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.10 ms: 1.14x slower                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.53 ms: 1.14x slower                                    |
| Geometric mean         | (ref)                                                    | 1.14x slower                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251124-macm4pro-arm64-python-main-3.15.0a2+-dc62b62 |
|-----------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.37 ms: 1.09x faster                                    |
| genshi_text     | 10.5 ms                                                  | 10.3 ms: 1.02x faster                                    |
| genshi_xml      | 21.8 ms                                                  | 23.6 ms: 1.08x slower                                    |
| django_template | 13.6 ms                                                  | 14.8 ms: 1.09x slower                                    |
| Geometric mean  | (ref)                                                    | 1.01x slower                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251124-macm4pro-arm64-python-main-3.15.0a2+-dc62b62 |
|----------------------------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| sphinx                           | 434 ms                                                   | 8.74 ms: 49.61x faster                                   |
| async_tree_eager_io              | 496 ms                                                   | 228 ms: 2.18x faster                                     |
| async_tree_io_tg                 | 480 ms                                                   | 229 ms: 2.10x faster                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 225 ms: 1.98x faster                                     |
| async_tree_io                    | 459 ms                                                   | 233 ms: 1.97x faster                                     |
| async_tree_none_tg               | 172 ms                                                   | 97.9 ms: 1.76x faster                                    |
| mdp                              | 1.09 sec                                                 | 622 ms: 1.75x faster                                     |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.74x faster                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.0 us: 1.67x faster                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 140 ms: 1.65x faster                                     |
| async_tree_memoization           | 223 ms                                                   | 137 ms: 1.62x faster                                     |
| deepcopy                         | 161 us                                                   | 102 us: 1.58x faster                                     |
| richards                         | 22.4 ms                                                  | 14.6 ms: 1.53x faster                                    |
| richards_super                   | 25.4 ms                                                  | 16.6 ms: 1.53x faster                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.04 us: 1.41x faster                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.3 ms: 1.35x faster                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 254 ms: 1.33x faster                                     |
| comprehensions                   | 9.84 us                                                  | 7.41 us: 1.33x faster                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 252 ms: 1.32x faster                                     |
| float                            | 37.9 ms                                                  | 29.7 ms: 1.28x faster                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                     |
| scimark_sor                      | 61.0 ms                                                  | 50.7 ms: 1.20x faster                                    |
| regex_compile                    | 54.6 ms                                                  | 45.5 ms: 1.20x faster                                    |
| raytrace                         | 145 ms                                                   | 121 ms: 1.19x faster                                     |
| scimark_fft                      | 142 ms                                                   | 120 ms: 1.19x faster                                     |
| go                               | 70.0 ms                                                  | 59.5 ms: 1.18x faster                                    |
| tomli_loads                      | 957 ms                                                   | 818 ms: 1.17x faster                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.8 ms: 1.16x faster                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                    |
| logging_simple                   | 2.57 us                                                  | 2.26 us: 1.14x faster                                    |
| xml_etree_generate               | 38.9 ms                                                  | 34.2 ms: 1.14x faster                                    |
| pyflate                          | 216 ms                                                   | 190 ms: 1.14x faster                                     |
| pprint_safe_repr                 | 328 ms                                                   | 289 ms: 1.13x faster                                     |
| generators                       | 21.9 ms                                                  | 19.4 ms: 1.13x faster                                    |
| xml_etree_process                | 26.7 ms                                                  | 23.6 ms: 1.13x faster                                    |
| logging_format                   | 2.80 us                                                  | 2.48 us: 1.13x faster                                    |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.13x faster                                    |
| pprint_pformat                   | 665 ms                                                   | 591 ms: 1.13x faster                                     |
| subparsers                       | 20.8 ms                                                  | 18.5 ms: 1.12x faster                                    |
| deltablue                        | 1.73 ms                                                  | 1.54 ms: 1.12x faster                                    |
| spectral_norm                    | 54.4 ms                                                  | 48.6 ms: 1.12x faster                                    |
| json_dumps                       | 4.26 ms                                                  | 3.82 ms: 1.11x faster                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 61.5 ms: 1.11x faster                                    |
| async_generators                 | 206 ms                                                   | 188 ms: 1.10x faster                                     |
| unpickle_pure_python             | 103 us                                                   | 93.9 us: 1.10x faster                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 64.9 us: 1.09x faster                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.05 sec: 1.09x faster                                   |
| mako                             | 4.77 ms                                                  | 4.37 ms: 1.09x faster                                    |
| thrift                           | 322 us                                                   | 299 us: 1.08x faster                                     |
| dulwich_log                      | 21.3 ms                                                  | 20.0 ms: 1.06x faster                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.9 ms: 1.06x faster                                    |
| chaos                            | 28.9 ms                                                  | 27.4 ms: 1.06x faster                                    |
| pickle_pure_python               | 139 us                                                   | 132 us: 1.06x faster                                     |
| logging_silent                   | 50.9 ns                                                  | 48.6 ns: 1.05x faster                                    |
| pycparser                        | 497 ms                                                   | 479 ms: 1.04x faster                                     |
| regex_dna                        | 99.6 ms                                                  | 96.6 ms: 1.03x faster                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.02 ms: 1.03x faster                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 38.0 ms: 1.02x faster                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                     |
| genshi_text                      | 10.5 ms                                                  | 10.3 ms: 1.02x faster                                    |
| nqueens                          | 43.5 ms                                                  | 42.7 ms: 1.02x faster                                    |
| scimark_lu                       | 51.3 ms                                                  | 50.5 ms: 1.02x faster                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                     |
| json_loads                       | 10.9 us                                                  | 10.9 us: 1.01x slower                                    |
| regex_v8                         | 9.59 ms                                                  | 9.72 ms: 1.01x slower                                    |
| html5lib                         | 23.0 ms                                                  | 23.4 ms: 1.02x slower                                    |
| 2to3                             | 114 ms                                                   | 118 ms: 1.03x slower                                     |
| bench_thread_pool                | 419 us                                                   | 433 us: 1.03x slower                                     |
| pidigits                         | 161 ms                                                   | 167 ms: 1.04x slower                                     |
| telco                            | 2.61 ms                                                  | 2.72 ms: 1.04x slower                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.12 ms: 1.06x slower                                    |
| meteor_contest                   | 47.7 ms                                                  | 50.7 ms: 1.06x slower                                    |
| hexiom                           | 3.04 ms                                                  | 3.23 ms: 1.06x slower                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.65 ms: 1.08x slower                                    |
| genshi_xml                       | 21.8 ms                                                  | 23.6 ms: 1.08x slower                                    |
| sympy_sum                        | 57.6 ms                                                  | 62.3 ms: 1.08x slower                                    |
| django_template                  | 13.6 ms                                                  | 14.8 ms: 1.09x slower                                    |
| sympy_str                        | 104 ms                                                   | 115 ms: 1.11x slower                                     |
| sympy_expand                     | 167 ms                                                   | 185 ms: 1.11x slower                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 126 ms: 1.12x slower                                     |
| python_startup                   | 8.01 ms                                                  | 9.10 ms: 1.14x slower                                    |
| create_gc_cycles                 | 830 us                                                   | 949 us: 1.14x slower                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.53 ms: 1.14x slower                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 45.9 ms: 1.16x slower                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                     |
| coverage                         | 26.9 ms                                                  | 33.7 ms: 1.25x slower                                    |
| many_optionals                   | 195 us                                                   | 384 us: 1.96x slower                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 83.0 ms: 2.58x slower                                    |
| Geometric mean                   | (ref)                                                    | 1.16x faster                                             |

Benchmark hidden because not significant (5): json, nbody, sqlite_synth, fannkuch, pylint
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, connected_components, dask, djangocms, docutils, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251124-3.15.0a2+-dc62b62-JIT/bm-20251124-macm4pro-arm64-python-main-3.15.0a2+-dc62b62.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.166x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.23x