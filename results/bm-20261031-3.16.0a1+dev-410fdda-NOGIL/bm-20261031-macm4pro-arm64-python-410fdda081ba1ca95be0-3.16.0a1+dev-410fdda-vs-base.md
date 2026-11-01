# Results vs. base

- fork: python
- ref: 410fdda081ba1ca95be0
- machine: darwin-arm64
- commit hash: 410fdda
- commit date: 2026-10-31
- overall geometric mean: 1.001x faster
- HPT reliability: 96.24%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 124 ms                                                                      | 124 ms: 1.00x faster                                                        |
| docutils       | 1.02 sec                                                                    | 1.02 sec: 1.00x faster                                                      |
| Geometric mean | (ref)                                                                       | 1.00x faster                                                                |

Benchmark hidden because not significant (2): html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                    | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|------------------------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_io_tg             | 290 ms                                                                      | 289 ms: 1.00x faster                                                        |
| asyncio_websockets           | 182 ms                                                                      | 181 ms: 1.00x faster                                                        |
| async_tree_eager             | 48.6 ms                                                                     | 48.8 ms: 1.00x slower                                                       |
| async_tree_eager_memoization | 124 ms                                                                      | 124 ms: 1.00x slower                                                        |
| Geometric mean               | (ref)                                                                       | 1.00x slower                                                                |

Benchmark hidden because not significant (15): coroutines, async_tree_memoization_tg, async_tree_eager_io_tg, async_tree_eager_io, async_tree_none_tg, async_generators, async_tree_eager_memoization_tg, async_tree_cpu_io_mixed_tg, async_tree_eager_tg, async_tree_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_memoization, async_tree_eager_cpu_io_mixed, async_tree_io, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 32.5 ms                                                                     | 32.7 ms: 1.00x slower                                                       |
| nbody          | 58.0 ms                                                                     | 58.3 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                                       | 1.00x slower                                                                |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 62.6 ms                                                                     | 62.5 ms: 1.00x faster                                                       |
| regex_effbot   | 1.30 ms                                                                     | 1.31 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                                       | 1.00x slower                                                                |

Benchmark hidden because not significant (2): regex_dna, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|--------------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps         | 3.74 ms                                                                     | 3.65 ms: 1.02x faster                                                       |
| tomli_loads        | 873 ms                                                                      | 865 ms: 1.01x faster                                                        |
| xml_etree_process  | 28.9 ms                                                                     | 28.8 ms: 1.00x faster                                                       |
| xml_etree_generate | 37.7 ms                                                                     | 37.8 ms: 1.00x slower                                                       |
| xml_etree_parse    | 57.3 ms                                                                     | 57.6 ms: 1.01x slower                                                       |
| json_loads         | 10.5 us                                                                     | 10.6 us: 1.01x slower                                                       |
| Geometric mean     | (ref)                                                                       | 1.00x faster                                                                |

Benchmark hidden because not significant (3): unpickle_pure_python, pickle_pure_python, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup | 8.77 ms                                                                     | 8.78 ms: 1.00x slower                                                       |
| Geometric mean | (ref)                                                                       | 1.00x slower                                                                |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|-----------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| django_template | 16.8 ms                                                                     | 16.6 ms: 1.01x faster                                                       |
| mako            | 5.42 ms                                                                     | 5.40 ms: 1.00x faster                                                       |
| Geometric mean  | (ref)                                                                       | 1.01x faster                                                                |

All benchmarks:
===============

| Benchmark                    | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|------------------------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| scimark_lu                   | 66.0 ms                                                                     | 63.4 ms: 1.04x faster                                                       |
| json_dumps                   | 3.74 ms                                                                     | 3.65 ms: 1.02x faster                                                       |
| richards                     | 23.9 ms                                                                     | 23.5 ms: 1.02x faster                                                       |
| mdp                          | 578 ms                                                                      | 569 ms: 1.02x faster                                                        |
| django_template              | 16.8 ms                                                                     | 16.6 ms: 1.01x faster                                                       |
| raytrace                     | 135 ms                                                                      | 134 ms: 1.01x faster                                                        |
| tomli_loads                  | 873 ms                                                                      | 865 ms: 1.01x faster                                                        |
| thrift                       | 341 us                                                                      | 338 us: 1.01x faster                                                        |
| sqlglot_v2_normalize         | 48.5 ms                                                                     | 48.1 ms: 1.01x faster                                                       |
| deepcopy_memo                | 14.0 us                                                                     | 13.9 us: 1.01x faster                                                       |
| richards_super               | 27.2 ms                                                                     | 27.1 ms: 1.01x faster                                                       |
| chaos                        | 28.4 ms                                                                     | 28.3 ms: 1.01x faster                                                       |
| generators                   | 22.8 ms                                                                     | 22.7 ms: 1.01x faster                                                       |
| crypto_pyaes                 | 41.0 ms                                                                     | 40.7 ms: 1.01x faster                                                       |
| fannkuch                     | 180 ms                                                                      | 179 ms: 1.01x faster                                                        |
| xml_etree_process            | 28.9 ms                                                                     | 28.8 ms: 1.00x faster                                                       |
| shortest_path                | 246 ms                                                                      | 245 ms: 1.00x faster                                                        |
| mako                         | 5.42 ms                                                                     | 5.40 ms: 1.00x faster                                                       |
| many_optionals               | 247 us                                                                      | 246 us: 1.00x faster                                                        |
| dulwich_log                  | 18.8 ms                                                                     | 18.7 ms: 1.00x faster                                                       |
| async_tree_io_tg             | 290 ms                                                                      | 289 ms: 1.00x faster                                                        |
| sqlglot_v2_parse             | 565 us                                                                      | 563 us: 1.00x faster                                                        |
| docutils                     | 1.02 sec                                                                    | 1.02 sec: 1.00x faster                                                      |
| go                           | 59.4 ms                                                                     | 59.3 ms: 1.00x faster                                                       |
| connected_components         | 238 ms                                                                      | 237 ms: 1.00x faster                                                        |
| bpe_tokeniser                | 1.92 sec                                                                    | 1.91 sec: 1.00x faster                                                      |
| asyncio_websockets           | 182 ms                                                                      | 181 ms: 1.00x faster                                                        |
| hexiom                       | 3.12 ms                                                                     | 3.12 ms: 1.00x faster                                                       |
| regex_compile                | 62.6 ms                                                                     | 62.5 ms: 1.00x faster                                                       |
| 2to3                         | 124 ms                                                                      | 124 ms: 1.00x faster                                                        |
| python_startup               | 8.77 ms                                                                     | 8.78 ms: 1.00x slower                                                       |
| meteor_contest               | 51.7 ms                                                                     | 51.8 ms: 1.00x slower                                                       |
| xml_etree_generate           | 37.7 ms                                                                     | 37.8 ms: 1.00x slower                                                       |
| bench_thread_pool            | 467 us                                                                      | 469 us: 1.00x slower                                                        |
| async_tree_eager             | 48.6 ms                                                                     | 48.8 ms: 1.00x slower                                                       |
| sympy_integrate              | 7.93 ms                                                                     | 7.97 ms: 1.00x slower                                                       |
| float                        | 32.5 ms                                                                     | 32.7 ms: 1.00x slower                                                       |
| async_tree_eager_memoization | 124 ms                                                                      | 124 ms: 1.00x slower                                                        |
| scimark_sor                  | 57.4 ms                                                                     | 57.7 ms: 1.00x slower                                                       |
| pprint_pformat               | 706 ms                                                                      | 709 ms: 1.01x slower                                                        |
| xml_etree_parse              | 57.3 ms                                                                     | 57.6 ms: 1.01x slower                                                       |
| regex_effbot                 | 1.30 ms                                                                     | 1.31 ms: 1.01x slower                                                       |
| nbody                        | 58.0 ms                                                                     | 58.3 ms: 1.01x slower                                                       |
| scimark_sparse_mat_mult      | 2.16 ms                                                                     | 2.18 ms: 1.01x slower                                                       |
| telco                        | 3.00 ms                                                                     | 3.02 ms: 1.01x slower                                                       |
| typing_runtime_protocols     | 53.2 us                                                                     | 53.6 us: 1.01x slower                                                       |
| comprehensions               | 8.00 us                                                                     | 8.07 us: 1.01x slower                                                       |
| scimark_fft                  | 130 ms                                                                      | 132 ms: 1.01x slower                                                        |
| k_core                       | 985 ms                                                                      | 994 ms: 1.01x slower                                                        |
| json_loads                   | 10.5 us                                                                     | 10.6 us: 1.01x slower                                                       |
| Geometric mean               | (ref)                                                                       | 1.00x faster                                                                |

Benchmark hidden because not significant (50): coroutines, create_gc_cycles, logging_format, regex_dna, async_tree_memoization_tg, async_tree_eager_io_tg, sympy_str, async_tree_eager_io, sqlite_synth, deepcopy_reduce, pathlib, logging_simple, sphinx, html5lib, pycparser, sqlglot_v2_transpile, sqlglot_v2_optimize, sympy_sum, pyflate, async_tree_none_tg, regex_v8, python_startup_no_site, spectral_norm, unpickle_pure_python, pylint, async_generators, sympy_expand, pickle_pure_python, nqueens, async_tree_eager_memoization_tg, async_tree_cpu_io_mixed_tg, logging_silent, async_tree_eager_tg, subparsers, pprint_safe_repr, deltablue, json, async_tree_cpu_io_mixed, scimark_monte_carlo, bench_mp_pool, async_tree_eager_cpu_io_mixed_tg, pidigits, async_tree_memoization, async_tree_eager_cpu_io_mixed, xml_etree_iterparse, deepcopy, async_tree_io, coverage, async_tree_none, gc_traversal
Ignored benchmarks (8) of results/bm-20261031-3.16.0a1+dev-47c249a-NOGIL/bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.001x faster

# HPT report

- Reliability score: 96.24% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x