# Results vs. base

- fork: nascheme
- ref: ft_ra_memory_order
- machine: darwin-arm64
- commit hash: f14d6e1
- commit date: 2026-11-09
- overall geometric mean: 1.004x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20261109-macm4pro-arm64-python-e891a9117985888df3e5-3.16.0a1+dev-e891a91 | bm-20261109-macm4pro-arm64-nascheme-ft_ra_memory_order-3.16.0a1+dev-f14d6e1 |
|----------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 120 ms                                                                      | 121 ms: 1.01x slower                                                        |
| docutils       | 988 ms                                                                      | 997 ms: 1.01x slower                                                        |
| html5lib       | 21.6 ms                                                                     | 21.9 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                                       | 1.01x slower                                                                |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                     | bm-20261109-macm4pro-arm64-python-e891a9117985888df3e5-3.16.0a1+dev-e891a91 | bm-20261109-macm4pro-arm64-nascheme-ft_ra_memory_order-3.16.0a1+dev-f14d6e1 |
|-------------------------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| coroutines                    | 10.6 ms                                                                     | 10.5 ms: 1.01x faster                                                       |
| asyncio_websockets            | 184 ms                                                                      | 184 ms: 1.00x slower                                                        |
| async_tree_eager_memoization  | 118 ms                                                                      | 118 ms: 1.01x slower                                                        |
| async_generators              | 132 ms                                                                      | 133 ms: 1.01x slower                                                        |
| async_tree_eager_cpu_io_mixed | 221 ms                                                                      | 223 ms: 1.01x slower                                                        |
| async_tree_cpu_io_mixed       | 284 ms                                                                      | 287 ms: 1.01x slower                                                        |
| async_tree_eager_io           | 281 ms                                                                      | 284 ms: 1.01x slower                                                        |
| async_tree_eager              | 44.8 ms                                                                     | 45.4 ms: 1.01x slower                                                       |
| Geometric mean                | (ref)                                                                       | 1.01x slower                                                                |

Benchmark hidden because not significant (11): async_tree_io_tg, async_tree_none_tg, async_tree_memoization, async_tree_eager_memoization_tg, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_eager_io_tg, async_tree_eager_tg, async_tree_eager_cpu_io_mixed_tg, async_tree_io, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20261109-macm4pro-arm64-python-e891a9117985888df3e5-3.16.0a1+dev-e891a91 | bm-20261109-macm4pro-arm64-nascheme-ft_ra_memory_order-3.16.0a1+dev-f14d6e1 |
|----------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 143 ms                                                                      | 144 ms: 1.01x slower                                                        |
| float          | 30.7 ms                                                                     | 31.0 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                                       | 1.01x slower                                                                |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20261109-macm4pro-arm64-python-e891a9117985888df3e5-3.16.0a1+dev-e891a91 | bm-20261109-macm4pro-arm64-nascheme-ft_ra_memory_order-3.16.0a1+dev-f14d6e1 |
|----------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 58.8 ms                                                                     | 59.3 ms: 1.01x slower                                                       |
| regex_v8       | 8.70 ms                                                                     | 8.77 ms: 1.01x slower                                                       |
| regex_dna      | 86.9 ms                                                                     | 88.5 ms: 1.02x slower                                                       |
| Geometric mean | (ref)                                                                       | 1.01x slower                                                                |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20261109-macm4pro-arm64-python-e891a9117985888df3e5-3.16.0a1+dev-e891a91 | bm-20261109-macm4pro-arm64-nascheme-ft_ra_memory_order-3.16.0a1+dev-f14d6e1 |
|----------------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_parse      | 57.3 ms                                                                     | 56.0 ms: 1.02x faster                                                       |
| json_loads           | 10.9 us                                                                     | 10.8 us: 1.01x faster                                                       |
| xml_etree_process    | 26.5 ms                                                                     | 26.6 ms: 1.00x slower                                                       |
| xml_etree_generate   | 34.6 ms                                                                     | 34.8 ms: 1.01x slower                                                       |
| unpickle_pure_python | 95.2 us                                                                     | 97.8 us: 1.03x slower                                                       |
| pickle_pure_python   | 145 us                                                                      | 149 us: 1.03x slower                                                        |
| Geometric mean       | (ref)                                                                       | 1.00x slower                                                                |

Benchmark hidden because not significant (3): xml_etree_iterparse, json_dumps, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20261109-macm4pro-arm64-python-e891a9117985888df3e5-3.16.0a1+dev-e891a91 | bm-20261109-macm4pro-arm64-nascheme-ft_ra_memory_order-3.16.0a1+dev-f14d6e1 |
|------------------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 6.63 ms                                                                     | 6.68 ms: 1.01x slower                                                       |
| python_startup         | 8.48 ms                                                                     | 8.57 ms: 1.01x slower                                                       |
| Geometric mean         | (ref)                                                                       | 1.01x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20261109-macm4pro-arm64-python-e891a9117985888df3e5-3.16.0a1+dev-e891a91 | bm-20261109-macm4pro-arm64-nascheme-ft_ra_memory_order-3.16.0a1+dev-f14d6e1 |
|----------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako           | 5.56 ms                                                                     | 5.52 ms: 1.01x faster                                                       |
| Geometric mean | (ref)                                                                       | 1.00x faster                                                                |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                     | bm-20261109-macm4pro-arm64-python-e891a9117985888df3e5-3.16.0a1+dev-e891a91 | bm-20261109-macm4pro-arm64-nascheme-ft_ra_memory_order-3.16.0a1+dev-f14d6e1 |
|-------------------------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_parse               | 57.3 ms                                                                     | 56.0 ms: 1.02x faster                                                       |
| scimark_sor                   | 53.6 ms                                                                     | 52.7 ms: 1.02x faster                                                       |
| logging_silent                | 42.5 ns                                                                     | 41.9 ns: 1.01x faster                                                       |
| json_loads                    | 10.9 us                                                                     | 10.8 us: 1.01x faster                                                       |
| coroutines                    | 10.6 ms                                                                     | 10.5 ms: 1.01x faster                                                       |
| telco                         | 3.04 ms                                                                     | 3.01 ms: 1.01x faster                                                       |
| mako                          | 5.56 ms                                                                     | 5.52 ms: 1.01x faster                                                       |
| bpe_tokeniser                 | 1.84 sec                                                                    | 1.83 sec: 1.01x faster                                                      |
| nqueens                       | 38.4 ms                                                                     | 38.5 ms: 1.00x slower                                                       |
| deltablue                     | 1.58 ms                                                                     | 1.59 ms: 1.00x slower                                                       |
| sympy_str                     | 105 ms                                                                      | 105 ms: 1.00x slower                                                        |
| xml_etree_process             | 26.5 ms                                                                     | 26.6 ms: 1.00x slower                                                       |
| richards                      | 22.2 ms                                                                     | 22.3 ms: 1.00x slower                                                       |
| mdp                           | 540 ms                                                                      | 542 ms: 1.00x slower                                                        |
| go                            | 55.0 ms                                                                     | 55.2 ms: 1.00x slower                                                       |
| asyncio_websockets            | 184 ms                                                                      | 184 ms: 1.00x slower                                                        |
| richards_super                | 25.5 ms                                                                     | 25.6 ms: 1.00x slower                                                       |
| sqlglot_v2_parse              | 529 us                                                                      | 531 us: 1.00x slower                                                        |
| sqlglot_v2_normalize          | 44.4 ms                                                                     | 44.7 ms: 1.01x slower                                                       |
| chaos                         | 26.7 ms                                                                     | 26.9 ms: 1.01x slower                                                       |
| sqlglot_v2_optimize           | 21.9 ms                                                                     | 22.0 ms: 1.01x slower                                                       |
| async_tree_eager_memoization  | 118 ms                                                                      | 118 ms: 1.01x slower                                                        |
| k_core                        | 955 ms                                                                      | 960 ms: 1.01x slower                                                        |
| pidigits                      | 143 ms                                                                      | 144 ms: 1.01x slower                                                        |
| xml_etree_generate            | 34.6 ms                                                                     | 34.8 ms: 1.01x slower                                                       |
| async_generators              | 132 ms                                                                      | 133 ms: 1.01x slower                                                        |
| python_startup_no_site        | 6.63 ms                                                                     | 6.68 ms: 1.01x slower                                                       |
| subparsers                    | 3.99 ms                                                                     | 4.02 ms: 1.01x slower                                                       |
| pycparser                     | 465 ms                                                                      | 468 ms: 1.01x slower                                                        |
| raytrace                      | 120 ms                                                                      | 121 ms: 1.01x slower                                                        |
| regex_compile                 | 58.8 ms                                                                     | 59.3 ms: 1.01x slower                                                       |
| regex_v8                      | 8.70 ms                                                                     | 8.77 ms: 1.01x slower                                                       |
| logging_format                | 2.49 us                                                                     | 2.51 us: 1.01x slower                                                       |
| thrift                        | 325 us                                                                      | 327 us: 1.01x slower                                                        |
| 2to3                          | 120 ms                                                                      | 121 ms: 1.01x slower                                                        |
| docutils                      | 988 ms                                                                      | 997 ms: 1.01x slower                                                        |
| async_tree_eager_cpu_io_mixed | 221 ms                                                                      | 223 ms: 1.01x slower                                                        |
| sympy_sum                     | 57.4 ms                                                                     | 57.9 ms: 1.01x slower                                                       |
| float                         | 30.7 ms                                                                     | 31.0 ms: 1.01x slower                                                       |
| sympy_expand                  | 178 ms                                                                      | 179 ms: 1.01x slower                                                        |
| bench_mp_pool                 | 40.4 ms                                                                     | 40.8 ms: 1.01x slower                                                       |
| deepcopy                      | 101 us                                                                      | 102 us: 1.01x slower                                                        |
| pprint_pformat                | 690 ms                                                                      | 696 ms: 1.01x slower                                                        |
| sqlite_synth                  | 809 ns                                                                      | 817 ns: 1.01x slower                                                        |
| python_startup                | 8.48 ms                                                                     | 8.57 ms: 1.01x slower                                                       |
| dulwich_log                   | 18.6 ms                                                                     | 18.8 ms: 1.01x slower                                                       |
| bench_thread_pool             | 459 us                                                                      | 464 us: 1.01x slower                                                        |
| html5lib                      | 21.6 ms                                                                     | 21.9 ms: 1.01x slower                                                       |
| pprint_safe_repr              | 329 ms                                                                      | 332 ms: 1.01x slower                                                        |
| async_tree_cpu_io_mixed       | 284 ms                                                                      | 287 ms: 1.01x slower                                                        |
| async_tree_eager_io           | 281 ms                                                                      | 284 ms: 1.01x slower                                                        |
| many_optionals                | 240 us                                                                      | 243 us: 1.01x slower                                                        |
| scimark_monte_carlo           | 31.7 ms                                                                     | 32.1 ms: 1.01x slower                                                       |
| sympy_integrate               | 7.64 ms                                                                     | 7.74 ms: 1.01x slower                                                       |
| async_tree_eager              | 44.8 ms                                                                     | 45.4 ms: 1.01x slower                                                       |
| hexiom                        | 2.84 ms                                                                     | 2.88 ms: 1.01x slower                                                       |
| pyflate                       | 188 ms                                                                      | 191 ms: 1.02x slower                                                        |
| pathlib                       | 10.3 ms                                                                     | 10.5 ms: 1.02x slower                                                       |
| regex_dna                     | 86.9 ms                                                                     | 88.5 ms: 1.02x slower                                                       |
| comprehensions                | 7.49 us                                                                     | 7.66 us: 1.02x slower                                                       |
| unpickle_pure_python          | 95.2 us                                                                     | 97.8 us: 1.03x slower                                                       |
| pickle_pure_python            | 145 us                                                                      | 149 us: 1.03x slower                                                        |
| Geometric mean                | (ref)                                                                       | 1.01x slower                                                                |

Benchmark hidden because not significant (38): xml_etree_iterparse, async_tree_io_tg, json_dumps, shortest_path, logging_simple, json, scimark_sparse_mat_mult, create_gc_cycles, django_template, typing_runtime_protocols, spectral_norm, sqlglot_v2_transpile, crypto_pyaes, coverage, async_tree_none_tg, nbody, scimark_fft, scimark_lu, async_tree_memoization, sphinx, fannkuch, meteor_contest, regex_effbot, gc_traversal, async_tree_eager_memoization_tg, connected_components, async_tree_cpu_io_mixed_tg, tomli_loads, async_tree_memoization_tg, async_tree_eager_io_tg, deepcopy_memo, deepcopy_reduce, async_tree_eager_tg, async_tree_eager_cpu_io_mixed_tg, async_tree_io, pylint, generators, async_tree_none

- Geometric mean (including insignificant results): 1.004x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x