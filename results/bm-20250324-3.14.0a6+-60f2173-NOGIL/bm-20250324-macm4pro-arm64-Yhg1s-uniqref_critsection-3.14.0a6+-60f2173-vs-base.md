# Results vs. base

- fork: Yhg1s
- ref: uniqref_critsection
- machine: darwin-arm64
- commit hash: 60f2173
- commit date: 2025-03-24
- overall geometric mean: 1.005x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250324-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 133 ms                                                                   | 130 ms: 1.02x faster                                                   |
| docutils       | 1.05 sec                                                                 | 1.04 sec: 1.01x faster                                                 |
| sphinx         | 441 ms                                                                   | 439 ms: 1.00x faster                                                   |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250324-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|----------------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| coroutines                       | 12.1 ms                                                                  | 11.7 ms: 1.04x faster                                                  |
| async_tree_eager                 | 56.5 ms                                                                  | 55.6 ms: 1.02x faster                                                  |
| async_tree_eager_tg              | 89.0 ms                                                                  | 88.0 ms: 1.01x faster                                                  |
| async_tree_eager_cpu_io_mixed    | 232 ms                                                                   | 229 ms: 1.01x faster                                                   |
| async_tree_cpu_io_mixed          | 255 ms                                                                   | 253 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed_tg | 234 ms                                                                   | 232 ms: 1.01x faster                                                   |
| async_generators                 | 193 ms                                                                   | 191 ms: 1.01x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 244 ms                                                                   | 242 ms: 1.01x faster                                                   |
| async_tree_none_tg               | 100 ms                                                                   | 99.4 ms: 1.01x faster                                                  |
| async_tree_eager_io_tg           | 224 ms                                                                   | 223 ms: 1.01x faster                                                   |
| asyncio_websockets               | 190 ms                                                                   | 188 ms: 1.01x faster                                                   |
| async_tree_none                  | 116 ms                                                                   | 115 ms: 1.00x faster                                                   |
| async_tree_memoization_tg        | 137 ms                                                                   | 136 ms: 1.00x faster                                                   |
| async_tree_eager_memoization     | 120 ms                                                                   | 120 ms: 1.00x faster                                                   |
| async_tree_io                    | 241 ms                                                                   | 241 ms: 1.00x slower                                                   |
| Geometric mean                   | (ref)                                                                    | 1.01x faster                                                           |

Benchmark hidden because not significant (4): async_tree_memoization, async_tree_io_tg, async_tree_eager_memoization_tg, async_tree_eager_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250324-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 36.1 ms                                                                  | 35.6 ms: 1.02x faster                                                  |
| pidigits       | 162 ms                                                                   | 161 ms: 1.00x faster                                                   |
| nbody          | 78.5 ms                                                                  | 78.8 ms: 1.00x slower                                                  |
| Geometric mean | (ref)                                                                    | 1.00x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250324-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 93.3 ms                                                                  | 92.4 ms: 1.01x faster                                                  |
| regex_v8       | 9.68 ms                                                                  | 9.58 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                                    | 1.00x faster                                                           |

Benchmark hidden because not significant (2): regex_compile, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250324-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|----------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_loads           | 11.9 us                                                                  | 11.4 us: 1.04x faster                                                  |
| xml_etree_generate   | 41.2 ms                                                                  | 40.8 ms: 1.01x faster                                                  |
| xml_etree_process    | 30.6 ms                                                                  | 30.5 ms: 1.00x faster                                                  |
| unpickle_pure_python | 128 us                                                                   | 128 us: 1.00x slower                                                   |
| pickle_pure_python   | 170 us                                                                   | 171 us: 1.01x slower                                                   |
| xml_etree_parse      | 55.8 ms                                                                  | 57.1 ms: 1.02x slower                                                  |
| xml_etree_iterparse  | 39.5 ms                                                                  | 41.1 ms: 1.04x slower                                                  |
| Geometric mean       | (ref)                                                                    | 1.00x slower                                                           |

Benchmark hidden because not significant (2): tomli_loads, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250324-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 9.26 ms                                                                  | 9.21 ms: 1.01x faster                                                  |
| python_startup_no_site | 7.30 ms                                                                  | 7.26 ms: 1.00x faster                                                  |
| Geometric mean         | (ref)                                                                    | 1.01x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250324-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|-----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 18.3 ms                                                                  | 18.2 ms: 1.01x faster                                                  |
| genshi_text     | 13.2 ms                                                                  | 13.1 ms: 1.01x faster                                                  |
| genshi_xml      | 26.3 ms                                                                  | 26.2 ms: 1.01x faster                                                  |
| mako            | 6.20 ms                                                                  | 6.23 ms: 1.01x slower                                                  |
| Geometric mean  | (ref)                                                                    | 1.00x faster                                                           |

All benchmarks:
===============

| Benchmark                        | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c | bm-20250324-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|----------------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_loads                       | 11.9 us                                                                  | 11.4 us: 1.04x faster                                                  |
| coroutines                       | 12.1 ms                                                                  | 11.7 ms: 1.04x faster                                                  |
| json                             | 2.02 ms                                                                  | 1.96 ms: 1.03x faster                                                  |
| many_optionals                   | 256 us                                                                   | 249 us: 1.03x faster                                                   |
| subparsers                       | 9.46 ms                                                                  | 9.21 ms: 1.03x faster                                                  |
| 2to3                             | 133 ms                                                                   | 130 ms: 1.02x faster                                                   |
| async_tree_eager                 | 56.5 ms                                                                  | 55.6 ms: 1.02x faster                                                  |
| scimark_lu                       | 67.7 ms                                                                  | 66.7 ms: 1.02x faster                                                  |
| fannkuch                         | 226 ms                                                                   | 223 ms: 1.02x faster                                                   |
| float                            | 36.1 ms                                                                  | 35.6 ms: 1.02x faster                                                  |
| spectral_norm                    | 60.2 ms                                                                  | 59.3 ms: 1.02x faster                                                  |
| raytrace                         | 162 ms                                                                   | 159 ms: 1.01x faster                                                   |
| sqlglot_v2_parse                 | 705 us                                                                   | 696 us: 1.01x faster                                                   |
| bench_mp_pool                    | 40.4 ms                                                                  | 39.9 ms: 1.01x faster                                                  |
| sqlglot_v2_transpile             | 841 us                                                                   | 830 us: 1.01x faster                                                   |
| pprint_safe_repr                 | 417 ms                                                                   | 412 ms: 1.01x faster                                                   |
| docutils                         | 1.05 sec                                                                 | 1.04 sec: 1.01x faster                                                 |
| async_tree_eager_tg              | 89.0 ms                                                                  | 88.0 ms: 1.01x faster                                                  |
| async_tree_eager_cpu_io_mixed    | 232 ms                                                                   | 229 ms: 1.01x faster                                                   |
| xml_etree_generate               | 41.2 ms                                                                  | 40.8 ms: 1.01x faster                                                  |
| async_tree_cpu_io_mixed          | 255 ms                                                                   | 253 ms: 1.01x faster                                                   |
| regex_dna                        | 93.3 ms                                                                  | 92.4 ms: 1.01x faster                                                  |
| sympy_sum                        | 64.3 ms                                                                  | 63.7 ms: 1.01x faster                                                  |
| deepcopy_reduce                  | 1.39 us                                                                  | 1.38 us: 1.01x faster                                                  |
| regex_v8                         | 9.68 ms                                                                  | 9.58 ms: 1.01x faster                                                  |
| chaos                            | 33.5 ms                                                                  | 33.2 ms: 1.01x faster                                                  |
| comprehensions                   | 10.2 us                                                                  | 10.1 us: 1.01x faster                                                  |
| async_tree_eager_cpu_io_mixed_tg | 234 ms                                                                   | 232 ms: 1.01x faster                                                   |
| async_generators                 | 193 ms                                                                   | 191 ms: 1.01x faster                                                   |
| shortest_path                    | 250 ms                                                                   | 248 ms: 1.01x faster                                                   |
| sqlglot_v2_normalize             | 53.7 ms                                                                  | 53.2 ms: 1.01x faster                                                  |
| scimark_sparse_mat_mult          | 2.50 ms                                                                  | 2.48 ms: 1.01x faster                                                  |
| async_tree_cpu_io_mixed_tg       | 244 ms                                                                   | 242 ms: 1.01x faster                                                   |
| async_tree_none_tg               | 100 ms                                                                   | 99.4 ms: 1.01x faster                                                  |
| sympy_integrate                  | 9.15 ms                                                                  | 9.08 ms: 1.01x faster                                                  |
| bench_thread_pool                | 615 us                                                                   | 610 us: 1.01x faster                                                   |
| django_template                  | 18.3 ms                                                                  | 18.2 ms: 1.01x faster                                                  |
| richards                         | 27.9 ms                                                                  | 27.6 ms: 1.01x faster                                                  |
| sqlglot_v2_optimize              | 26.5 ms                                                                  | 26.3 ms: 1.01x faster                                                  |
| scimark_sor                      | 70.7 ms                                                                  | 70.2 ms: 1.01x faster                                                  |
| async_tree_eager_io_tg           | 224 ms                                                                   | 223 ms: 1.01x faster                                                   |
| thrift                           | 349 us                                                                   | 346 us: 1.01x faster                                                   |
| genshi_text                      | 13.2 ms                                                                  | 13.1 ms: 1.01x faster                                                  |
| genshi_xml                       | 26.3 ms                                                                  | 26.2 ms: 1.01x faster                                                  |
| pprint_pformat                   | 849 ms                                                                   | 844 ms: 1.01x faster                                                   |
| dulwich_log                      | 19.8 ms                                                                  | 19.7 ms: 1.01x faster                                                  |
| asyncio_websockets               | 190 ms                                                                   | 188 ms: 1.01x faster                                                   |
| sqlalchemy_declarative           | 51.7 ms                                                                  | 51.4 ms: 1.01x faster                                                  |
| crypto_pyaes                     | 46.8 ms                                                                  | 46.5 ms: 1.01x faster                                                  |
| python_startup                   | 9.26 ms                                                                  | 9.21 ms: 1.01x faster                                                  |
| async_tree_none                  | 116 ms                                                                   | 115 ms: 1.00x faster                                                   |
| python_startup_no_site           | 7.30 ms                                                                  | 7.26 ms: 1.00x faster                                                  |
| nqueens                          | 49.7 ms                                                                  | 49.5 ms: 1.00x faster                                                  |
| xml_etree_process                | 30.6 ms                                                                  | 30.5 ms: 1.00x faster                                                  |
| sphinx                           | 441 ms                                                                   | 439 ms: 1.00x faster                                                   |
| pidigits                         | 162 ms                                                                   | 161 ms: 1.00x faster                                                   |
| telco                            | 3.64 ms                                                                  | 3.63 ms: 1.00x faster                                                  |
| async_tree_memoization_tg        | 137 ms                                                                   | 136 ms: 1.00x faster                                                   |
| async_tree_eager_memoization     | 120 ms                                                                   | 120 ms: 1.00x faster                                                   |
| bpe_tokeniser                    | 2.26 sec                                                                 | 2.25 sec: 1.00x faster                                                 |
| async_tree_io                    | 241 ms                                                                   | 241 ms: 1.00x slower                                                   |
| unpickle_pure_python             | 128 us                                                                   | 128 us: 1.00x slower                                                   |
| nbody                            | 78.5 ms                                                                  | 78.8 ms: 1.00x slower                                                  |
| richards_super                   | 31.2 ms                                                                  | 31.4 ms: 1.00x slower                                                  |
| pickle_pure_python               | 170 us                                                                   | 171 us: 1.01x slower                                                   |
| mako                             | 6.20 ms                                                                  | 6.23 ms: 1.01x slower                                                  |
| logging_silent                   | 55.4 ns                                                                  | 55.7 ns: 1.01x slower                                                  |
| deepcopy_memo                    | 17.5 us                                                                  | 17.6 us: 1.01x slower                                                  |
| hexiom                           | 3.95 ms                                                                  | 3.99 ms: 1.01x slower                                                  |
| meteor_contest                   | 60.3 ms                                                                  | 60.9 ms: 1.01x slower                                                  |
| k_core                           | 1.06 sec                                                                 | 1.07 sec: 1.01x slower                                                 |
| coverage                         | 40.2 ms                                                                  | 40.7 ms: 1.01x slower                                                  |
| xml_etree_parse                  | 55.8 ms                                                                  | 57.1 ms: 1.02x slower                                                  |
| xml_etree_iterparse              | 39.5 ms                                                                  | 41.1 ms: 1.04x slower                                                  |
| Geometric mean                   | (ref)                                                                    | 1.01x faster                                                           |

Benchmark hidden because not significant (30): pylint, sqlite_synth, deltablue, typing_runtime_protocols, pycparser, async_tree_memoization, sqlalchemy_imperative, create_gc_cycles, gc_traversal, async_tree_io_tg, sympy_expand, logging_simple, deepcopy, mdp, regex_compile, go, html5lib, async_tree_eager_memoization_tg, pathlib, scimark_monte_carlo, pyflate, logging_format, tomli_loads, generators, async_tree_eager_io, connected_components, scimark_fft, json_dumps, sympy_str, regex_effbot

- Geometric mean (including insignificant results): 1.005x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x