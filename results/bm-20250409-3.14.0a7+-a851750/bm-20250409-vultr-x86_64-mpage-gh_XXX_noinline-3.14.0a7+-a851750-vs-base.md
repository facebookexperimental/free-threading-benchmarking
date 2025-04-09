# Results vs. base

- fork: mpage
- ref: gh_XXX_noinline
- machine: linux-x86_64
- commit hash: a851750
- commit date: 2025-04-09
- overall geometric mean: 1.009x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250409-vultr-x86_64-python-1f5682f3a27516833f7c-3.14.0a7+-1f5682f | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| 2to3           | 246 ms                                                                 | 246 ms: 1.00x slower                                             |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                     |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20250409-vultr-x86_64-python-1f5682f3a27516833f7c-3.14.0a7+-1f5682f | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| async_tree_io    | 616 ms                                                                 | 608 ms: 1.01x faster                                             |
| coroutines       | 23.6 ms                                                                | 23.4 ms: 1.01x faster                                            |
| async_generators | 320 ms                                                                 | 325 ms: 1.02x slower                                             |
| Geometric mean   | (ref)                                                                  | 1.00x faster                                                     |

Benchmark hidden because not significant (8): async_tree_io_tg, async_tree_none_tg, async_tree_memoization_tg, async_tree_memoization, async_tree_cpu_io_mixed_tg, asyncio_websockets, async_tree_none, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250409-vultr-x86_64-python-1f5682f3a27516833f7c-3.14.0a7+-1f5682f | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| float          | 66.8 ms                                                                | 69.2 ms: 1.04x slower                                            |
| nbody          | 81.1 ms                                                                | 84.9 ms: 1.05x slower                                            |
| pidigits       | 190 ms                                                                 | 201 ms: 1.06x slower                                             |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250409-vultr-x86_64-python-1f5682f3a27516833f7c-3.14.0a7+-1f5682f | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| regex_v8       | 21.0 ms                                                                | 22.1 ms: 1.05x slower                                            |
| regex_effbot   | 2.60 ms                                                                | 2.84 ms: 1.09x slower                                            |
| regex_dna      | 165 ms                                                                 | 181 ms: 1.09x slower                                             |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                     |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250409-vultr-x86_64-python-1f5682f3a27516833f7c-3.14.0a7+-1f5682f | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| json_loads           | 28.4 us                                                                | 28.3 us: 1.00x faster                                            |
| pickle_pure_python   | 300 us                                                                 | 303 us: 1.01x slower                                             |
| xml_etree_iterparse  | 90.7 ms                                                                | 91.6 ms: 1.01x slower                                            |
| xml_etree_generate   | 82.9 ms                                                                | 83.9 ms: 1.01x slower                                            |
| xml_etree_process    | 58.3 ms                                                                | 59.0 ms: 1.01x slower                                            |
| json_dumps           | 11.0 ms                                                                | 11.2 ms: 1.01x slower                                            |
| unpickle_pure_python | 209 us                                                                 | 212 us: 1.02x slower                                             |
| xml_etree_parse      | 127 ms                                                                 | 130 ms: 1.02x slower                                             |
| tomli_loads          | 1.82 sec                                                               | 1.89 sec: 1.04x slower                                           |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20250409-vultr-x86_64-python-1f5682f3a27516833f7c-3.14.0a7+-1f5682f | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| python_startup | 15.1 ms                                                                | 15.0 ms: 1.00x faster                                            |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                     |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250409-vultr-x86_64-python-1f5682f3a27516833f7c-3.14.0a7+-1f5682f | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| django_template | 35.1 ms                                                                | 34.9 ms: 1.01x faster                                            |
| genshi_xml      | 47.3 ms                                                                | 47.6 ms: 1.01x slower                                            |
| genshi_text     | 20.1 ms                                                                | 20.3 ms: 1.01x slower                                            |
| mako            | 11.7 ms                                                                | 12.1 ms: 1.03x slower                                            |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                     |

All benchmarks:
===============

| Benchmark                | bm-20250409-vultr-x86_64-python-1f5682f3a27516833f7c-3.14.0a7+-1f5682f | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|--------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| generators               | 27.2 ms                                                                | 26.8 ms: 1.01x faster                                            |
| sqlalchemy_imperative    | 19.9 ms                                                                | 19.6 ms: 1.01x faster                                            |
| pathlib                  | 19.1 ms                                                                | 18.9 ms: 1.01x faster                                            |
| spectral_norm            | 92.5 ms                                                                | 91.3 ms: 1.01x faster                                            |
| async_tree_io            | 616 ms                                                                 | 608 ms: 1.01x faster                                             |
| coroutines               | 23.6 ms                                                                | 23.4 ms: 1.01x faster                                            |
| many_optionals           | 1.02 ms                                                                | 1.01 ms: 1.01x faster                                            |
| django_template          | 35.1 ms                                                                | 34.9 ms: 1.01x faster                                            |
| hexiom                   | 5.67 ms                                                                | 5.64 ms: 1.01x faster                                            |
| pycparser                | 1.10 sec                                                               | 1.09 sec: 1.01x faster                                           |
| json_loads               | 28.4 us                                                                | 28.3 us: 1.00x faster                                            |
| python_startup           | 15.1 ms                                                                | 15.0 ms: 1.00x faster                                            |
| 2to3                     | 246 ms                                                                 | 246 ms: 1.00x slower                                             |
| nqueens                  | 75.8 ms                                                                | 76.1 ms: 1.00x slower                                            |
| pprint_pformat           | 1.44 sec                                                               | 1.44 sec: 1.00x slower                                           |
| deltablue                | 3.20 ms                                                                | 3.21 ms: 1.01x slower                                            |
| chaos                    | 52.3 ms                                                                | 52.6 ms: 1.01x slower                                            |
| bpe_tokeniser            | 4.18 sec                                                               | 4.20 sec: 1.01x slower                                           |
| genshi_xml               | 47.3 ms                                                                | 47.6 ms: 1.01x slower                                            |
| pprint_safe_repr         | 703 ms                                                                 | 707 ms: 1.01x slower                                             |
| sympy_str                | 269 ms                                                                 | 271 ms: 1.01x slower                                             |
| scimark_sor              | 108 ms                                                                 | 108 ms: 1.01x slower                                             |
| mdp                      | 1.13 sec                                                               | 1.13 sec: 1.01x slower                                           |
| pickle_pure_python       | 300 us                                                                 | 303 us: 1.01x slower                                             |
| sqlglot_v2_optimize      | 50.1 ms                                                                | 50.5 ms: 1.01x slower                                            |
| scimark_monte_carlo      | 59.4 ms                                                                | 60.0 ms: 1.01x slower                                            |
| genshi_text              | 20.1 ms                                                                | 20.3 ms: 1.01x slower                                            |
| xml_etree_iterparse      | 90.7 ms                                                                | 91.6 ms: 1.01x slower                                            |
| sympy_integrate          | 18.8 ms                                                                | 19.0 ms: 1.01x slower                                            |
| richards                 | 40.3 ms                                                                | 40.7 ms: 1.01x slower                                            |
| scimark_sparse_mat_mult  | 4.32 ms                                                                | 4.37 ms: 1.01x slower                                            |
| xml_etree_generate       | 82.9 ms                                                                | 83.9 ms: 1.01x slower                                            |
| raytrace                 | 244 ms                                                                 | 246 ms: 1.01x slower                                             |
| deepcopy                 | 248 us                                                                 | 251 us: 1.01x slower                                             |
| sqlglot_v2_normalize     | 100 ms                                                                 | 101 ms: 1.01x slower                                             |
| crypto_pyaes             | 66.3 ms                                                                | 67.1 ms: 1.01x slower                                            |
| xml_etree_process        | 58.3 ms                                                                | 59.0 ms: 1.01x slower                                            |
| json_dumps               | 11.0 ms                                                                | 11.2 ms: 1.01x slower                                            |
| sqlglot_v2_transpile     | 1.50 ms                                                                | 1.52 ms: 1.01x slower                                            |
| sqlite_synth             | 2.18 us                                                                | 2.22 us: 1.02x slower                                            |
| sqlglot_v2_parse         | 1.21 ms                                                                | 1.23 ms: 1.02x slower                                            |
| richards_super           | 46.0 ms                                                                | 46.8 ms: 1.02x slower                                            |
| unpickle_pure_python     | 209 us                                                                 | 212 us: 1.02x slower                                             |
| xml_etree_parse          | 127 ms                                                                 | 130 ms: 1.02x slower                                             |
| deepcopy_memo            | 29.0 us                                                                | 29.5 us: 1.02x slower                                            |
| async_generators         | 320 ms                                                                 | 325 ms: 1.02x slower                                             |
| telco                    | 7.02 ms                                                                | 7.15 ms: 1.02x slower                                            |
| deepcopy_reduce          | 2.60 us                                                                | 2.65 us: 1.02x slower                                            |
| scimark_lu               | 111 ms                                                                 | 113 ms: 1.02x slower                                             |
| logging_simple           | 5.86 us                                                                | 5.99 us: 1.02x slower                                            |
| typing_runtime_protocols | 153 us                                                                 | 157 us: 1.03x slower                                             |
| comprehensions           | 16.2 us                                                                | 16.6 us: 1.03x slower                                            |
| logging_silent           | 94.5 ns                                                                | 97.4 ns: 1.03x slower                                            |
| mako                     | 11.7 ms                                                                | 12.1 ms: 1.03x slower                                            |
| float                    | 66.8 ms                                                                | 69.2 ms: 1.04x slower                                            |
| tomli_loads              | 1.82 sec                                                               | 1.89 sec: 1.04x slower                                           |
| nbody                    | 81.1 ms                                                                | 84.9 ms: 1.05x slower                                            |
| regex_v8                 | 21.0 ms                                                                | 22.1 ms: 1.05x slower                                            |
| pidigits                 | 190 ms                                                                 | 201 ms: 1.06x slower                                             |
| regex_effbot             | 2.60 ms                                                                | 2.84 ms: 1.09x slower                                            |
| regex_dna                | 165 ms                                                                 | 181 ms: 1.09x slower                                             |
| Geometric mean           | (ref)                                                                  | 1.01x slower                                                     |

Benchmark hidden because not significant (33): async_tree_io_tg, async_tree_none_tg, async_tree_memoization_tg, scimark_fft, pyflate, json, subparsers, gc_traversal, async_tree_memoization, bench_thread_pool, regex_compile, shortest_path, go, async_tree_cpu_io_mixed_tg, logging_format, sympy_sum, pylint, python_startup_no_site, asyncio_websockets, bench_mp_pool, docutils, meteor_contest, sqlalchemy_declarative, dulwich_log, fannkuch, async_tree_none, sympy_expand, connected_components, create_gc_cycles, sphinx, coverage, async_tree_cpu_io_mixed, k_core

- Geometric mean (including insignificant results): 1.009x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x