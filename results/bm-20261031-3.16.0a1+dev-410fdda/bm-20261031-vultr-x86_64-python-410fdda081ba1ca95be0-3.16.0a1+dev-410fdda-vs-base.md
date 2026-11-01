# Results vs. base

- fork: python
- ref: 410fdda081ba1ca95be0
- machine: linux-x86_64
- commit hash: 410fdda
- commit date: 2026-10-31
- overall geometric mean: 1.006x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20261031-vultr-x86_64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------|:-------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| docutils       | 2.31 sec                                                                  | 2.33 sec: 1.01x slower                                                    |
| html5lib       | 56.5 ms                                                                   | 57.6 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                                     | 1.01x slower                                                              |

Benchmark hidden because not significant (2): 2to3, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20261031-vultr-x86_64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|---------------------------|:-------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_generators          | 227 ms                                                                    | 226 ms: 1.01x faster                                                      |
| async_tree_none           | 273 ms                                                                    | 277 ms: 1.02x slower                                                      |
| async_tree_memoization_tg | 341 ms                                                                    | 349 ms: 1.02x slower                                                      |
| async_tree_none_tg        | 275 ms                                                                    | 282 ms: 1.03x slower                                                      |
| Geometric mean            | (ref)                                                                     | 1.01x slower                                                              |

Benchmark hidden because not significant (7): coroutines, async_tree_cpu_io_mixed, asyncio_websockets, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20261031-vultr-x86_64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------|:-------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| nbody          | 90.7 ms                                                                   | 89.6 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                                     | 1.01x faster                                                              |

Benchmark hidden because not significant (2): float, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20261031-vultr-x86_64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------|:-------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_v8       | 21.6 ms                                                                   | 21.2 ms: 1.02x faster                                                     |
| regex_effbot   | 2.81 ms                                                                   | 2.76 ms: 1.02x faster                                                     |
| regex_dna      | 180 ms                                                                    | 179 ms: 1.00x faster                                                      |
| regex_compile  | 148 ms                                                                    | 149 ms: 1.01x slower                                                      |
| Geometric mean | (ref)                                                                     | 1.01x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20261031-vultr-x86_64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|---------------------|:-------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| tomli_loads         | 1.82 sec                                                                  | 1.79 sec: 1.02x faster                                                    |
| xml_etree_parse     | 142 ms                                                                    | 141 ms: 1.01x faster                                                      |
| json_loads          | 27.2 us                                                                   | 27.3 us: 1.00x slower                                                     |
| xml_etree_generate  | 86.9 ms                                                                   | 87.2 ms: 1.00x slower                                                     |
| xml_etree_iterparse | 91.5 ms                                                                   | 92.1 ms: 1.01x slower                                                     |
| xml_etree_process   | 61.4 ms                                                                   | 62.0 ms: 1.01x slower                                                     |
| pickle_pure_python  | 313 us                                                                    | 316 us: 1.01x slower                                                      |
| json_dumps          | 8.98 ms                                                                   | 9.20 ms: 1.02x slower                                                     |
| Geometric mean      | (ref)                                                                     | 1.00x slower                                                              |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20261031-vultr-x86_64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|------------------------|:-------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                                   | 11.5 ms: 1.00x slower                                                     |
| python_startup_no_site | 7.51 ms                                                                   | 7.55 ms: 1.00x slower                                                     |
| Geometric mean         | (ref)                                                                     | 1.00x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20261031-vultr-x86_64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|-----------------|:-------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| django_template | 35.7 ms                                                                   | 36.0 ms: 1.01x slower                                                     |
| mako            | 11.6 ms                                                                   | 11.8 ms: 1.02x slower                                                     |
| Geometric mean  | (ref)                                                                     | 1.01x slower                                                              |

All benchmarks:
===============

| Benchmark                 | bm-20261031-vultr-x86_64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|---------------------------|:-------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| bench_mp_pool             | 292 ms                                                                    | 233 ms: 1.26x faster                                                      |
| typing_runtime_protocols  | 114 us                                                                    | 111 us: 1.03x faster                                                      |
| regex_v8                  | 21.6 ms                                                                   | 21.2 ms: 1.02x faster                                                     |
| regex_effbot              | 2.81 ms                                                                   | 2.76 ms: 1.02x faster                                                     |
| tomli_loads               | 1.82 sec                                                                  | 1.79 sec: 1.02x faster                                                    |
| scimark_sparse_mat_mult   | 4.73 ms                                                                   | 4.67 ms: 1.01x faster                                                     |
| nbody                     | 90.7 ms                                                                   | 89.6 ms: 1.01x faster                                                     |
| async_generators          | 227 ms                                                                    | 226 ms: 1.01x faster                                                      |
| nqueens                   | 76.1 ms                                                                   | 75.5 ms: 1.01x faster                                                     |
| pycparser                 | 1.10 sec                                                                  | 1.10 sec: 1.01x faster                                                    |
| crypto_pyaes              | 66.6 ms                                                                   | 66.2 ms: 1.01x faster                                                     |
| xml_etree_parse           | 142 ms                                                                    | 141 ms: 1.01x faster                                                      |
| thrift                    | 794 us                                                                    | 789 us: 1.01x faster                                                      |
| regex_dna                 | 180 ms                                                                    | 179 ms: 1.00x faster                                                      |
| chaos                     | 54.7 ms                                                                   | 54.5 ms: 1.00x faster                                                     |
| bpe_tokeniser             | 4.21 sec                                                                  | 4.20 sec: 1.00x faster                                                    |
| python_startup            | 11.5 ms                                                                   | 11.5 ms: 1.00x slower                                                     |
| richards_super            | 51.0 ms                                                                   | 51.1 ms: 1.00x slower                                                     |
| pylint                    | 108 ms                                                                    | 108 ms: 1.00x slower                                                      |
| deltablue                 | 3.30 ms                                                                   | 3.31 ms: 1.00x slower                                                     |
| json_loads                | 27.2 us                                                                   | 27.3 us: 1.00x slower                                                     |
| xml_etree_generate        | 86.9 ms                                                                   | 87.2 ms: 1.00x slower                                                     |
| python_startup_no_site    | 7.51 ms                                                                   | 7.55 ms: 1.00x slower                                                     |
| deepcopy_memo             | 27.5 us                                                                   | 27.7 us: 1.01x slower                                                     |
| mdp                       | 1.14 sec                                                                  | 1.15 sec: 1.01x slower                                                    |
| xml_etree_iterparse       | 91.5 ms                                                                   | 92.1 ms: 1.01x slower                                                     |
| go                        | 104 ms                                                                    | 105 ms: 1.01x slower                                                      |
| logging_format            | 6.91 us                                                                   | 6.97 us: 1.01x slower                                                     |
| xml_etree_process         | 61.4 ms                                                                   | 62.0 ms: 1.01x slower                                                     |
| pickle_pure_python        | 313 us                                                                    | 316 us: 1.01x slower                                                      |
| django_template           | 35.7 ms                                                                   | 36.0 ms: 1.01x slower                                                     |
| dulwich_log               | 67.4 ms                                                                   | 68.0 ms: 1.01x slower                                                     |
| telco                     | 159 ms                                                                    | 160 ms: 1.01x slower                                                      |
| fannkuch                  | 369 ms                                                                    | 373 ms: 1.01x slower                                                      |
| scimark_lu                | 120 ms                                                                    | 121 ms: 1.01x slower                                                      |
| docutils                  | 2.31 sec                                                                  | 2.33 sec: 1.01x slower                                                    |
| regex_compile             | 148 ms                                                                    | 149 ms: 1.01x slower                                                      |
| sympy_str                 | 279 ms                                                                    | 283 ms: 1.01x slower                                                      |
| deepcopy                  | 230 us                                                                    | 233 us: 1.01x slower                                                      |
| sympy_integrate           | 19.1 ms                                                                   | 19.4 ms: 1.01x slower                                                     |
| sqlglot_v2_optimize       | 50.5 ms                                                                   | 51.1 ms: 1.01x slower                                                     |
| json                      | 4.93 ms                                                                   | 5.00 ms: 1.01x slower                                                     |
| hexiom                    | 5.59 ms                                                                   | 5.67 ms: 1.01x slower                                                     |
| scimark_sor               | 110 ms                                                                    | 112 ms: 1.01x slower                                                      |
| scimark_monte_carlo       | 62.3 ms                                                                   | 63.2 ms: 1.01x slower                                                     |
| raytrace                  | 254 ms                                                                    | 258 ms: 1.01x slower                                                      |
| sympy_expand              | 476 ms                                                                    | 483 ms: 1.02x slower                                                      |
| async_tree_none           | 273 ms                                                                    | 277 ms: 1.02x slower                                                      |
| sympy_sum                 | 157 ms                                                                    | 159 ms: 1.02x slower                                                      |
| pprint_safe_repr          | 718 ms                                                                    | 730 ms: 1.02x slower                                                      |
| spectral_norm             | 90.0 ms                                                                   | 91.5 ms: 1.02x slower                                                     |
| pprint_pformat            | 1.46 sec                                                                  | 1.48 sec: 1.02x slower                                                    |
| comprehensions            | 15.7 us                                                                   | 16.0 us: 1.02x slower                                                     |
| mako                      | 11.6 ms                                                                   | 11.8 ms: 1.02x slower                                                     |
| html5lib                  | 56.5 ms                                                                   | 57.6 ms: 1.02x slower                                                     |
| many_optionals            | 872 us                                                                    | 890 us: 1.02x slower                                                      |
| async_tree_memoization_tg | 341 ms                                                                    | 349 ms: 1.02x slower                                                      |
| json_dumps                | 8.98 ms                                                                   | 9.20 ms: 1.02x slower                                                     |
| logging_silent            | 95.5 ns                                                                   | 97.9 ns: 1.03x slower                                                     |
| sqlglot_v2_normalize      | 100 ms                                                                    | 103 ms: 1.03x slower                                                      |
| async_tree_none_tg        | 275 ms                                                                    | 282 ms: 1.03x slower                                                      |
| create_gc_cycles          | 1.34 ms                                                                   | 1.38 ms: 1.03x slower                                                     |
| generators                | 28.8 ms                                                                   | 29.6 ms: 1.03x slower                                                     |
| logging_simple            | 6.05 us                                                                   | 6.24 us: 1.03x slower                                                     |
| gc_traversal              | 3.41 ms                                                                   | 3.61 ms: 1.06x slower                                                     |
| Geometric mean            | (ref)                                                                     | 1.00x slower                                                              |

Benchmark hidden because not significant (27): sqlite_synth, coroutines, float, pathlib, async_tree_cpu_io_mixed, richards, asyncio_websockets, pidigits, coverage, meteor_contest, sqlglot_v2_parse, async_tree_cpu_io_mixed_tg, 2to3, connected_components, scimark_fft, unpickle_pure_python, k_core, shortest_path, deepcopy_reduce, pyflate, sqlglot_v2_transpile, async_tree_io, subparsers, async_tree_io_tg, async_tree_memoization, sphinx, bench_thread_pool
Ignored benchmarks (8) of results/bm-20261031-3.16.0a1+dev-47c249a/bm-20261031-vultr-x86_64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.006x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x