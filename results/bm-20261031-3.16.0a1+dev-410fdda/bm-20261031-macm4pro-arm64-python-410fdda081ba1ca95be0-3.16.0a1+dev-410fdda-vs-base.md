# Results vs. base

- fork: python
- ref: 410fdda081ba1ca95be0
- machine: darwin-arm64
- commit hash: 410fdda
- commit date: 2026-10-31
- overall geometric mean: 1.001x slower
- HPT reliability: 83.27%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

Benchmark hidden because not significant (4): 2to3, docutils, html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|--------------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| coroutines         | 9.64 ms                                                                     | 9.59 ms: 1.00x faster                                                       |
| asyncio_websockets | 187 ms                                                                      | 186 ms: 1.00x faster                                                        |
| async_tree_eager   | 40.3 ms                                                                     | 40.1 ms: 1.00x faster                                                       |
| async_generators   | 97.6 ms                                                                     | 98.2 ms: 1.01x slower                                                       |
| Geometric mean     | (ref)                                                                       | 1.00x faster                                                                |

Benchmark hidden because not significant (15): async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_io_tg, async_tree_none, async_tree_eager_memoization, async_tree_eager_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_eager_cpu_io_mixed, async_tree_eager_io_tg, async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_eager_memoization_tg, async_tree_eager_io, async_tree_eager_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 44.2 ms                                                                     | 42.8 ms: 1.03x faster                                                       |
| float          | 26.8 ms                                                                     | 27.0 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                                       | 1.01x faster                                                                |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_dna      | 88.4 ms                                                                     | 87.6 ms: 1.01x faster                                                       |
| regex_v8       | 8.97 ms                                                                     | 8.99 ms: 1.00x slower                                                       |
| regex_compile  | 52.4 ms                                                                     | 52.9 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                                       | 1.00x slower                                                                |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| unpickle_pure_python | 92.6 us                                                                     | 89.9 us: 1.03x faster                                                       |
| tomli_loads          | 797 ms                                                                      | 785 ms: 1.01x faster                                                        |
| pickle_pure_python   | 137 us                                                                      | 136 us: 1.00x faster                                                        |
| xml_etree_process    | 24.4 ms                                                                     | 24.5 ms: 1.01x slower                                                       |
| xml_etree_iterparse  | 40.3 ms                                                                     | 40.6 ms: 1.01x slower                                                       |
| xml_etree_generate   | 34.2 ms                                                                     | 34.6 ms: 1.01x slower                                                       |
| xml_etree_parse      | 61.6 ms                                                                     | 62.7 ms: 1.02x slower                                                       |
| Geometric mean       | (ref)                                                                       | 1.00x faster                                                                |

Benchmark hidden because not significant (2): json_loads, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup | 8.12 ms                                                                     | 8.13 ms: 1.00x slower                                                       |
| Geometric mean | (ref)                                                                       | 1.00x slower                                                                |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|-----------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.32 ms                                                                     | 4.37 ms: 1.01x slower                                                       |
| django_template | 14.4 ms                                                                     | 14.6 ms: 1.02x slower                                                       |
| Geometric mean  | (ref)                                                                       | 1.01x slower                                                                |

All benchmarks:
===============

| Benchmark               | bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|-------------------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| scimark_sparse_mat_mult | 1.76 ms                                                                     | 1.70 ms: 1.03x faster                                                       |
| nbody                   | 44.2 ms                                                                     | 42.8 ms: 1.03x faster                                                       |
| unpickle_pure_python    | 92.6 us                                                                     | 89.9 us: 1.03x faster                                                       |
| scimark_sor             | 48.6 ms                                                                     | 47.7 ms: 1.02x faster                                                       |
| scimark_lu              | 45.7 ms                                                                     | 45.0 ms: 1.01x faster                                                       |
| tomli_loads             | 797 ms                                                                      | 785 ms: 1.01x faster                                                        |
| deepcopy                | 95.0 us                                                                     | 93.7 us: 1.01x faster                                                       |
| create_gc_cycles        | 617 us                                                                      | 610 us: 1.01x faster                                                        |
| sqlite_synth            | 912 ns                                                                      | 901 ns: 1.01x faster                                                        |
| regex_dna               | 88.4 ms                                                                     | 87.6 ms: 1.01x faster                                                       |
| deepcopy_reduce         | 1.03 us                                                                     | 1.03 us: 1.01x faster                                                       |
| telco                   | 2.79 ms                                                                     | 2.78 ms: 1.00x faster                                                       |
| coroutines              | 9.64 ms                                                                     | 9.59 ms: 1.00x faster                                                       |
| pickle_pure_python      | 137 us                                                                      | 136 us: 1.00x faster                                                        |
| asyncio_websockets      | 187 ms                                                                      | 186 ms: 1.00x faster                                                        |
| async_tree_eager        | 40.3 ms                                                                     | 40.1 ms: 1.00x faster                                                       |
| thrift                  | 298 us                                                                      | 296 us: 1.00x faster                                                        |
| pprint_pformat          | 621 ms                                                                      | 619 ms: 1.00x faster                                                        |
| python_startup          | 8.12 ms                                                                     | 8.13 ms: 1.00x slower                                                       |
| regex_v8                | 8.97 ms                                                                     | 8.99 ms: 1.00x slower                                                       |
| generators              | 16.7 ms                                                                     | 16.8 ms: 1.00x slower                                                       |
| bench_thread_pool       | 407 us                                                                      | 409 us: 1.00x slower                                                        |
| pycparser               | 456 ms                                                                      | 459 ms: 1.00x slower                                                        |
| shortest_path           | 224 ms                                                                      | 225 ms: 1.00x slower                                                        |
| subparsers              | 3.88 ms                                                                     | 3.90 ms: 1.00x slower                                                       |
| xml_etree_process       | 24.4 ms                                                                     | 24.5 ms: 1.01x slower                                                       |
| xml_etree_iterparse     | 40.3 ms                                                                     | 40.6 ms: 1.01x slower                                                       |
| float                   | 26.8 ms                                                                     | 27.0 ms: 1.01x slower                                                       |
| deepcopy_memo           | 11.4 us                                                                     | 11.5 us: 1.01x slower                                                       |
| nqueens                 | 34.1 ms                                                                     | 34.3 ms: 1.01x slower                                                       |
| deltablue               | 1.42 ms                                                                     | 1.42 ms: 1.01x slower                                                       |
| sympy_expand            | 165 ms                                                                      | 166 ms: 1.01x slower                                                        |
| async_generators        | 97.6 ms                                                                     | 98.2 ms: 1.01x slower                                                       |
| sqlglot_v2_optimize     | 20.8 ms                                                                     | 20.9 ms: 1.01x slower                                                       |
| connected_components    | 207 ms                                                                      | 209 ms: 1.01x slower                                                        |
| sqlglot_v2_normalize    | 42.8 ms                                                                     | 43.1 ms: 1.01x slower                                                       |
| scimark_monte_carlo     | 26.3 ms                                                                     | 26.5 ms: 1.01x slower                                                       |
| chaos                   | 24.2 ms                                                                     | 24.4 ms: 1.01x slower                                                       |
| richards_super          | 22.4 ms                                                                     | 22.6 ms: 1.01x slower                                                       |
| bpe_tokeniser           | 1.89 sec                                                                    | 1.91 sec: 1.01x slower                                                      |
| xml_etree_generate      | 34.2 ms                                                                     | 34.6 ms: 1.01x slower                                                       |
| mako                    | 4.32 ms                                                                     | 4.37 ms: 1.01x slower                                                       |
| regex_compile           | 52.4 ms                                                                     | 52.9 ms: 1.01x slower                                                       |
| pyflate                 | 178 ms                                                                      | 180 ms: 1.01x slower                                                        |
| logging_format          | 2.34 us                                                                     | 2.37 us: 1.01x slower                                                       |
| richards                | 19.7 ms                                                                     | 20.0 ms: 1.01x slower                                                       |
| django_template         | 14.4 ms                                                                     | 14.6 ms: 1.02x slower                                                       |
| many_optionals          | 220 us                                                                      | 224 us: 1.02x slower                                                        |
| xml_etree_parse         | 61.6 ms                                                                     | 62.7 ms: 1.02x slower                                                       |
| spectral_norm           | 40.5 ms                                                                     | 41.3 ms: 1.02x slower                                                       |
| logging_simple          | 2.11 us                                                                     | 2.15 us: 1.02x slower                                                       |
| scimark_fft             | 108 ms                                                                      | 111 ms: 1.02x slower                                                        |
| Geometric mean          | (ref)                                                                       | 1.00x slower                                                                |

Benchmark hidden because not significant (47): async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_io_tg, async_tree_none, json, async_tree_eager_memoization, gc_traversal, async_tree_eager_cpu_io_mixed_tg, sqlglot_v2_parse, async_tree_memoization_tg, async_tree_eager_cpu_io_mixed, docutils, json_loads, async_tree_eager_io_tg, async_tree_none_tg, k_core, comprehensions, async_tree_cpu_io_mixed_tg, pathlib, fannkuch, raytrace, meteor_contest, async_tree_eager_memoization_tg, async_tree_eager_io, logging_silent, pprint_safe_repr, crypto_pyaes, bench_mp_pool, sympy_sum, pidigits, dulwich_log, python_startup_no_site, async_tree_eager_tg, mdp, sqlglot_v2_transpile, 2to3, regex_effbot, go, sympy_str, sphinx, hexiom, sympy_integrate, pylint, json_dumps, typing_runtime_protocols, html5lib
Ignored benchmarks (8) of results/bm-20261031-3.16.0a1+dev-47c249a/bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.001x slower

# HPT report

- Reliability score: 83.27% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x