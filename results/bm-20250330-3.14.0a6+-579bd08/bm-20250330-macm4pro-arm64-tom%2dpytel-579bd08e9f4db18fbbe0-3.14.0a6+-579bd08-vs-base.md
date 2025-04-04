# Results vs. base

- fork: tom-pytel
- ref: 579bd08e9f4db18fbbe0
- machine: darwin-arm64
- commit hash: 579bd08
- commit date: 2025-03-30
- overall geometric mean: 1.000x slower
- HPT reliability: 75.47%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 116 ms                                                                   | 115 ms: 1.01x faster                                                          |
| docutils       | 1.07 sec                                                                 | 1.06 sec: 1.01x faster                                                        |
| Geometric mean | (ref)                                                                    | 1.00x faster                                                                  |

Benchmark hidden because not significant (2): html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                     | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|-------------------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_eager_cpu_io_mixed | 223 ms                                                                   | 222 ms: 1.00x faster                                                          |
| async_tree_cpu_io_mixed       | 266 ms                                                                   | 265 ms: 1.00x faster                                                          |
| async_tree_eager              | 43.4 ms                                                                  | 43.7 ms: 1.01x slower                                                         |
| coroutines                    | 10.7 ms                                                                  | 10.9 ms: 1.02x slower                                                         |
| Geometric mean                | (ref)                                                                    | 1.00x slower                                                                  |

Benchmark hidden because not significant (15): async_tree_eager_io, async_tree_cpu_io_mixed_tg, async_tree_eager_cpu_io_mixed_tg, async_tree_none_tg, async_tree_eager_memoization_tg, async_tree_none, asyncio_websockets, async_tree_eager_tg, async_tree_memoization_tg, async_tree_eager_memoization, async_tree_io_tg, async_tree_memoization, async_generators, async_tree_eager_io_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pidigits       | 167 ms                                                                   | 166 ms: 1.00x faster                                                          |
| nbody          | 51.2 ms                                                                  | 51.5 ms: 1.01x slower                                                         |
| Geometric mean | (ref)                                                                    | 1.00x slower                                                                  |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 50.2 ms                                                                  | 50.0 ms: 1.00x faster                                                         |
| Geometric mean | (ref)                                                                    | 1.00x faster                                                                  |

Benchmark hidden because not significant (3): regex_effbot, regex_v8, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| xml_etree_iterparse  | 45.8 ms                                                                  | 43.8 ms: 1.05x faster                                                         |
| json_loads           | 11.7 us                                                                  | 11.5 us: 1.02x faster                                                         |
| unpickle_pure_python | 105 us                                                                   | 105 us: 1.00x faster                                                          |
| pickle_pure_python   | 151 us                                                                   | 150 us: 1.00x faster                                                          |
| xml_etree_generate   | 37.0 ms                                                                  | 36.9 ms: 1.00x faster                                                         |
| json_dumps           | 5.08 ms                                                                  | 5.12 ms: 1.01x slower                                                         |
| xml_etree_parse      | 64.3 ms                                                                  | 67.1 ms: 1.04x slower                                                         |
| Geometric mean       | (ref)                                                                    | 1.00x faster                                                                  |

Benchmark hidden because not significant (2): xml_etree_process, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup | 9.04 ms                                                                  | 9.03 ms: 1.00x faster                                                         |
| Geometric mean | (ref)                                                                    | 1.00x faster                                                                  |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|-----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| genshi_xml      | 22.6 ms                                                                  | 22.5 ms: 1.00x faster                                                         |
| django_template | 15.8 ms                                                                  | 15.9 ms: 1.01x slower                                                         |
| genshi_text     | 10.5 ms                                                                  | 10.6 ms: 1.01x slower                                                         |
| Geometric mean  | (ref)                                                                    | 1.00x slower                                                                  |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                     | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|-------------------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| xml_etree_iterparse           | 45.8 ms                                                                  | 43.8 ms: 1.05x faster                                                         |
| json_loads                    | 11.7 us                                                                  | 11.5 us: 1.02x faster                                                         |
| generators                    | 18.3 ms                                                                  | 18.0 ms: 1.01x faster                                                         |
| fannkuch                      | 192 ms                                                                   | 190 ms: 1.01x faster                                                          |
| sympy_expand                  | 172 ms                                                                   | 171 ms: 1.01x faster                                                          |
| chaos                         | 28.7 ms                                                                  | 28.4 ms: 1.01x faster                                                         |
| shortest_path                 | 221 ms                                                                   | 219 ms: 1.01x faster                                                          |
| docutils                      | 1.07 sec                                                                 | 1.06 sec: 1.01x faster                                                        |
| connected_components          | 204 ms                                                                   | 203 ms: 1.01x faster                                                          |
| scimark_sor                   | 53.2 ms                                                                  | 52.9 ms: 1.01x faster                                                         |
| 2to3                          | 116 ms                                                                   | 115 ms: 1.01x faster                                                          |
| nqueens                       | 41.7 ms                                                                  | 41.5 ms: 1.01x faster                                                         |
| go                            | 61.9 ms                                                                  | 61.6 ms: 1.00x faster                                                         |
| pathlib                       | 11.2 ms                                                                  | 11.2 ms: 1.00x faster                                                         |
| subparsers                    | 9.04 ms                                                                  | 9.01 ms: 1.00x faster                                                         |
| deepcopy                      | 114 us                                                                   | 114 us: 1.00x faster                                                          |
| genshi_xml                    | 22.6 ms                                                                  | 22.5 ms: 1.00x faster                                                         |
| async_tree_eager_cpu_io_mixed | 223 ms                                                                   | 222 ms: 1.00x faster                                                          |
| many_optionals                | 241 us                                                                   | 240 us: 1.00x faster                                                          |
| unpickle_pure_python          | 105 us                                                                   | 105 us: 1.00x faster                                                          |
| bench_mp_pool                 | 41.4 ms                                                                  | 41.2 ms: 1.00x faster                                                         |
| pickle_pure_python            | 151 us                                                                   | 150 us: 1.00x faster                                                          |
| regex_compile                 | 50.2 ms                                                                  | 50.0 ms: 1.00x faster                                                         |
| async_tree_cpu_io_mixed       | 266 ms                                                                   | 265 ms: 1.00x faster                                                          |
| xml_etree_generate            | 37.0 ms                                                                  | 36.9 ms: 1.00x faster                                                         |
| pidigits                      | 167 ms                                                                   | 166 ms: 1.00x faster                                                          |
| python_startup                | 9.04 ms                                                                  | 9.03 ms: 1.00x faster                                                         |
| spectral_norm                 | 46.9 ms                                                                  | 47.0 ms: 1.00x slower                                                         |
| sqlglot_v2_optimize           | 23.7 ms                                                                  | 23.8 ms: 1.00x slower                                                         |
| sqlglot_v2_normalize          | 48.2 ms                                                                  | 48.3 ms: 1.00x slower                                                         |
| scimark_monte_carlo           | 30.5 ms                                                                  | 30.6 ms: 1.00x slower                                                         |
| richards                      | 22.6 ms                                                                  | 22.7 ms: 1.00x slower                                                         |
| richards_super                | 25.4 ms                                                                  | 25.5 ms: 1.00x slower                                                         |
| pprint_pformat                | 681 ms                                                                   | 684 ms: 1.00x slower                                                          |
| sqlalchemy_declarative        | 45.9 ms                                                                  | 46.1 ms: 1.00x slower                                                         |
| sympy_sum                     | 57.1 ms                                                                  | 57.4 ms: 1.00x slower                                                         |
| scimark_sparse_mat_mult       | 2.00 ms                                                                  | 2.01 ms: 1.00x slower                                                         |
| django_template               | 15.8 ms                                                                  | 15.9 ms: 1.01x slower                                                         |
| nbody                         | 51.2 ms                                                                  | 51.5 ms: 1.01x slower                                                         |
| pyflate                       | 210 ms                                                                   | 212 ms: 1.01x slower                                                          |
| async_tree_eager              | 43.4 ms                                                                  | 43.7 ms: 1.01x slower                                                         |
| scimark_lu                    | 47.2 ms                                                                  | 47.5 ms: 1.01x slower                                                         |
| json_dumps                    | 5.08 ms                                                                  | 5.12 ms: 1.01x slower                                                         |
| logging_silent                | 42.9 ns                                                                  | 43.3 ns: 1.01x slower                                                         |
| genshi_text                   | 10.5 ms                                                                  | 10.6 ms: 1.01x slower                                                         |
| sqlite_synth                  | 957 ns                                                                   | 966 ns: 1.01x slower                                                          |
| mdp                           | 1.08 sec                                                                 | 1.10 sec: 1.02x slower                                                        |
| coroutines                    | 10.7 ms                                                                  | 10.9 ms: 1.02x slower                                                         |
| xml_etree_parse               | 64.3 ms                                                                  | 67.1 ms: 1.04x slower                                                         |
| deltablue                     | 1.59 ms                                                                  | 1.67 ms: 1.05x slower                                                         |
| Geometric mean                | (ref)                                                                    | 1.00x slower                                                                  |

Benchmark hidden because not significant (55): async_tree_eager_io, logging_format, thrift, async_tree_cpu_io_mixed_tg, regex_effbot, async_tree_eager_cpu_io_mixed_tg, sphinx, scimark_fft, telco, raytrace, async_tree_none_tg, sympy_str, meteor_contest, async_tree_eager_memoization_tg, async_tree_none, deepcopy_reduce, hexiom, pycparser, mako, crypto_pyaes, comprehensions, dulwich_log, dask, python_startup_no_site, asyncio_websockets, bpe_tokeniser, regex_v8, float, json, logging_simple, sqlglot_v2_transpile, regex_dna, async_tree_eager_tg, async_tree_memoization_tg, async_tree_eager_memoization, bench_thread_pool, create_gc_cycles, sympy_integrate, async_tree_io_tg, sqlglot_v2_parse, async_tree_memoization, k_core, xml_etree_process, typing_runtime_protocols, async_generators, pylint, deepcopy_memo, html5lib, sqlalchemy_imperative, pprint_safe_repr, coverage, gc_traversal, tomli_loads, async_tree_eager_io_tg, async_tree_io

- Geometric mean (including insignificant results): 1.000x slower

# HPT report

- Reliability score: 75.47% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x