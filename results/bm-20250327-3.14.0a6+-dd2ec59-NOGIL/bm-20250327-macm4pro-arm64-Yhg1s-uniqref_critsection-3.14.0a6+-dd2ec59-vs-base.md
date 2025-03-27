# Results vs. base

- fork: Yhg1s
- ref: uniqref_critsection
- machine: darwin-arm64
- commit hash: dd2ec59
- commit date: 2025-03-27
- overall geometric mean: 1.007x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250327-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-dd2ec59 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 133 ms                                                                   | 132 ms: 1.01x faster                                                   |
| docutils       | 1.05 sec                                                                 | 1.04 sec: 1.01x faster                                                 |
| html5lib       | 24.3 ms                                                                  | 24.2 ms: 1.01x faster                                                  |
| sphinx         | 441 ms                                                                   | 437 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250327-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-dd2ec59 |
|----------------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_eager_tg              | 89.0 ms                                                                  | 87.9 ms: 1.01x faster                                                  |
| async_tree_eager                 | 56.5 ms                                                                  | 55.9 ms: 1.01x faster                                                  |
| async_generators                 | 193 ms                                                                   | 191 ms: 1.01x faster                                                   |
| async_tree_none_tg               | 100 ms                                                                   | 99.4 ms: 1.01x faster                                                  |
| async_tree_eager_io_tg           | 224 ms                                                                   | 223 ms: 1.01x faster                                                   |
| async_tree_none                  | 116 ms                                                                   | 115 ms: 1.01x faster                                                   |
| async_tree_io                    | 241 ms                                                                   | 239 ms: 1.01x faster                                                   |
| async_tree_io_tg                 | 226 ms                                                                   | 225 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed_tg | 234 ms                                                                   | 233 ms: 1.00x faster                                                   |
| async_tree_eager_memoization     | 120 ms                                                                   | 120 ms: 1.00x faster                                                   |
| async_tree_eager_io              | 233 ms                                                                   | 232 ms: 1.00x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 232 ms                                                                   | 231 ms: 1.00x faster                                                   |
| asyncio_websockets               | 190 ms                                                                   | 189 ms: 1.00x faster                                                   |
| async_tree_cpu_io_mixed          | 255 ms                                                                   | 255 ms: 1.00x faster                                                   |
| coroutines                       | 12.1 ms                                                                  | 12.3 ms: 1.01x slower                                                  |
| Geometric mean                   | (ref)                                                                    | 1.00x faster                                                           |

Benchmark hidden because not significant (4): async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, async_tree_memoization, async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250327-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-dd2ec59 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 162 ms                                                                   | 159 ms: 1.01x faster                                                   |
| nbody          | 78.5 ms                                                                  | 77.9 ms: 1.01x faster                                                  |
| float          | 36.1 ms                                                                  | 36.0 ms: 1.00x faster                                                  |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250327-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-dd2ec59 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 93.3 ms                                                                  | 91.9 ms: 1.02x faster                                                  |
| regex_compile  | 59.4 ms                                                                  | 58.7 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                           |

Benchmark hidden because not significant (2): regex_effbot, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250327-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-dd2ec59 |
|----------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_loads           | 11.9 us                                                                  | 11.5 us: 1.04x faster                                                  |
| tomli_loads          | 1.09 sec                                                                 | 1.07 sec: 1.02x faster                                                 |
| xml_etree_generate   | 41.2 ms                                                                  | 40.6 ms: 1.02x faster                                                  |
| xml_etree_process    | 30.6 ms                                                                  | 30.2 ms: 1.01x faster                                                  |
| unpickle_pure_python | 128 us                                                                   | 129 us: 1.01x slower                                                   |
| xml_etree_iterparse  | 39.5 ms                                                                  | 40.3 ms: 1.02x slower                                                  |
| xml_etree_parse      | 55.8 ms                                                                  | 57.6 ms: 1.03x slower                                                  |
| Geometric mean       | (ref)                                                                    | 1.00x faster                                                           |

Benchmark hidden because not significant (2): json_dumps, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250327-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-dd2ec59 |
|------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.30 ms                                                                  | 7.23 ms: 1.01x faster                                                  |
| python_startup         | 9.26 ms                                                                  | 9.20 ms: 1.01x faster                                                  |
| Geometric mean         | (ref)                                                                    | 1.01x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250327-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-dd2ec59 |
|-----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 13.2 ms                                                                  | 13.1 ms: 1.00x faster                                                  |
| genshi_xml      | 26.3 ms                                                                  | 26.2 ms: 1.00x faster                                                  |
| mako            | 6.20 ms                                                                  | 6.18 ms: 1.00x faster                                                  |
| django_template | 18.3 ms                                                                  | 18.3 ms: 1.00x faster                                                  |
| Geometric mean  | (ref)                                                                    | 1.00x faster                                                           |

All benchmarks:
===============

| Benchmark                        | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250327-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-dd2ec59 |
|----------------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_loads                       | 11.9 us                                                                  | 11.5 us: 1.04x faster                                                  |
| json                             | 2.02 ms                                                                  | 1.97 ms: 1.03x faster                                                  |
| sympy_expand                     | 204 ms                                                                   | 200 ms: 1.02x faster                                                   |
| scimark_lu                       | 67.7 ms                                                                  | 66.2 ms: 1.02x faster                                                  |
| spectral_norm                    | 60.2 ms                                                                  | 58.9 ms: 1.02x faster                                                  |
| tomli_loads                      | 1.09 sec                                                                 | 1.07 sec: 1.02x faster                                                 |
| richards                         | 27.9 ms                                                                  | 27.4 ms: 1.02x faster                                                  |
| sqlalchemy_declarative           | 51.7 ms                                                                  | 50.8 ms: 1.02x faster                                                  |
| pyflate                          | 234 ms                                                                   | 230 ms: 1.02x faster                                                   |
| xml_etree_generate               | 41.2 ms                                                                  | 40.6 ms: 1.02x faster                                                  |
| meteor_contest                   | 60.3 ms                                                                  | 59.3 ms: 1.02x faster                                                  |
| regex_dna                        | 93.3 ms                                                                  | 91.9 ms: 1.02x faster                                                  |
| many_optionals                   | 256 us                                                                   | 252 us: 1.02x faster                                                   |
| sympy_integrate                  | 9.15 ms                                                                  | 9.02 ms: 1.02x faster                                                  |
| subparsers                       | 9.46 ms                                                                  | 9.32 ms: 1.01x faster                                                  |
| sympy_sum                        | 64.3 ms                                                                  | 63.4 ms: 1.01x faster                                                  |
| deepcopy_reduce                  | 1.39 us                                                                  | 1.37 us: 1.01x faster                                                  |
| pidigits                         | 162 ms                                                                   | 159 ms: 1.01x faster                                                   |
| mdp                              | 1.20 sec                                                                 | 1.18 sec: 1.01x faster                                                 |
| xml_etree_process                | 30.6 ms                                                                  | 30.2 ms: 1.01x faster                                                  |
| logging_silent                   | 55.4 ns                                                                  | 54.6 ns: 1.01x faster                                                  |
| deltablue                        | 2.02 ms                                                                  | 1.99 ms: 1.01x faster                                                  |
| regex_compile                    | 59.4 ms                                                                  | 58.7 ms: 1.01x faster                                                  |
| async_tree_eager_tg              | 89.0 ms                                                                  | 87.9 ms: 1.01x faster                                                  |
| sqlalchemy_imperative            | 5.93 ms                                                                  | 5.86 ms: 1.01x faster                                                  |
| fannkuch                         | 226 ms                                                                   | 223 ms: 1.01x faster                                                   |
| sympy_str                        | 120 ms                                                                   | 119 ms: 1.01x faster                                                   |
| docutils                         | 1.05 sec                                                                 | 1.04 sec: 1.01x faster                                                 |
| sqlglot_v2_normalize             | 53.7 ms                                                                  | 53.1 ms: 1.01x faster                                                  |
| typing_runtime_protocols         | 81.3 us                                                                  | 80.4 us: 1.01x faster                                                  |
| sqlite_synth                     | 846 ns                                                                   | 837 ns: 1.01x faster                                                   |
| sqlglot_v2_transpile             | 841 us                                                                   | 832 us: 1.01x faster                                                   |
| sqlglot_v2_optimize              | 26.5 ms                                                                  | 26.2 ms: 1.01x faster                                                  |
| sqlglot_v2_parse                 | 705 us                                                                   | 698 us: 1.01x faster                                                   |
| gc_traversal                     | 931 us                                                                   | 922 us: 1.01x faster                                                   |
| bench_mp_pool                    | 40.4 ms                                                                  | 40.0 ms: 1.01x faster                                                  |
| async_tree_eager                 | 56.5 ms                                                                  | 55.9 ms: 1.01x faster                                                  |
| sphinx                           | 441 ms                                                                   | 437 ms: 1.01x faster                                                   |
| pathlib                          | 11.7 ms                                                                  | 11.6 ms: 1.01x faster                                                  |
| async_generators                 | 193 ms                                                                   | 191 ms: 1.01x faster                                                   |
| pprint_safe_repr                 | 417 ms                                                                   | 413 ms: 1.01x faster                                                   |
| dulwich_log                      | 19.8 ms                                                                  | 19.6 ms: 1.01x faster                                                  |
| python_startup_no_site           | 7.30 ms                                                                  | 7.23 ms: 1.01x faster                                                  |
| thrift                           | 349 us                                                                   | 346 us: 1.01x faster                                                   |
| shortest_path                    | 250 ms                                                                   | 248 ms: 1.01x faster                                                   |
| raytrace                         | 162 ms                                                                   | 160 ms: 1.01x faster                                                   |
| async_tree_none_tg               | 100 ms                                                                   | 99.4 ms: 1.01x faster                                                  |
| generators                       | 22.2 ms                                                                  | 22.0 ms: 1.01x faster                                                  |
| nbody                            | 78.5 ms                                                                  | 77.9 ms: 1.01x faster                                                  |
| python_startup                   | 9.26 ms                                                                  | 9.20 ms: 1.01x faster                                                  |
| chaos                            | 33.5 ms                                                                  | 33.3 ms: 1.01x faster                                                  |
| pprint_pformat                   | 849 ms                                                                   | 843 ms: 1.01x faster                                                   |
| scimark_sor                      | 70.7 ms                                                                  | 70.2 ms: 1.01x faster                                                  |
| telco                            | 3.64 ms                                                                  | 3.62 ms: 1.01x faster                                                  |
| 2to3                             | 133 ms                                                                   | 132 ms: 1.01x faster                                                   |
| create_gc_cycles                 | 501 us                                                                   | 498 us: 1.01x faster                                                   |
| async_tree_eager_io_tg           | 224 ms                                                                   | 223 ms: 1.01x faster                                                   |
| html5lib                         | 24.3 ms                                                                  | 24.2 ms: 1.01x faster                                                  |
| async_tree_none                  | 116 ms                                                                   | 115 ms: 1.01x faster                                                   |
| logging_simple                   | 2.88 us                                                                  | 2.87 us: 1.01x faster                                                  |
| nqueens                          | 49.7 ms                                                                  | 49.4 ms: 1.01x faster                                                  |
| async_tree_io                    | 241 ms                                                                   | 239 ms: 1.01x faster                                                   |
| richards_super                   | 31.2 ms                                                                  | 31.1 ms: 1.01x faster                                                  |
| async_tree_io_tg                 | 226 ms                                                                   | 225 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed_tg | 234 ms                                                                   | 233 ms: 1.00x faster                                                   |
| async_tree_eager_memoization     | 120 ms                                                                   | 120 ms: 1.00x faster                                                   |
| logging_format                   | 3.15 us                                                                  | 3.13 us: 1.00x faster                                                  |
| async_tree_eager_io              | 233 ms                                                                   | 232 ms: 1.00x faster                                                   |
| crypto_pyaes                     | 46.8 ms                                                                  | 46.6 ms: 1.00x faster                                                  |
| async_tree_eager_cpu_io_mixed    | 232 ms                                                                   | 231 ms: 1.00x faster                                                   |
| asyncio_websockets               | 190 ms                                                                   | 189 ms: 1.00x faster                                                   |
| genshi_text                      | 13.2 ms                                                                  | 13.1 ms: 1.00x faster                                                  |
| genshi_xml                       | 26.3 ms                                                                  | 26.2 ms: 1.00x faster                                                  |
| float                            | 36.1 ms                                                                  | 36.0 ms: 1.00x faster                                                  |
| comprehensions                   | 10.2 us                                                                  | 10.2 us: 1.00x faster                                                  |
| async_tree_cpu_io_mixed          | 255 ms                                                                   | 255 ms: 1.00x faster                                                   |
| go                               | 74.8 ms                                                                  | 74.6 ms: 1.00x faster                                                  |
| mako                             | 6.20 ms                                                                  | 6.18 ms: 1.00x faster                                                  |
| django_template                  | 18.3 ms                                                                  | 18.3 ms: 1.00x faster                                                  |
| deepcopy_memo                    | 17.5 us                                                                  | 17.5 us: 1.00x slower                                                  |
| bpe_tokeniser                    | 2.26 sec                                                                 | 2.27 sec: 1.00x slower                                                 |
| k_core                           | 1.06 sec                                                                 | 1.06 sec: 1.01x slower                                                 |
| scimark_fft                      | 162 ms                                                                   | 163 ms: 1.01x slower                                                   |
| unpickle_pure_python             | 128 us                                                                   | 129 us: 1.01x slower                                                   |
| coroutines                       | 12.1 ms                                                                  | 12.3 ms: 1.01x slower                                                  |
| xml_etree_iterparse              | 39.5 ms                                                                  | 40.3 ms: 1.02x slower                                                  |
| scimark_sparse_mat_mult          | 2.50 ms                                                                  | 2.58 ms: 1.03x slower                                                  |
| xml_etree_parse                  | 55.8 ms                                                                  | 57.6 ms: 1.03x slower                                                  |
| Geometric mean                   | (ref)                                                                    | 1.01x faster                                                           |

Benchmark hidden because not significant (16): pylint, bench_thread_pool, pycparser, deepcopy, regex_effbot, async_tree_memoization_tg, regex_v8, json_dumps, async_tree_cpu_io_mixed_tg, hexiom, scimark_monte_carlo, connected_components, async_tree_memoization, async_tree_eager_memoization_tg, pickle_pure_python, coverage

- Geometric mean (including insignificant results): 1.007x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.99x