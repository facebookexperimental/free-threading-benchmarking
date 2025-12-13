# Results vs. base

- fork: nascheme
- ref: set_lockfree_contain
- machine: linux-x86_64
- commit hash: 235b6eb
- commit date: 2025-12-13
- overall geometric mean: 1.002x faster
- HPT reliability: 99.06%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251213-vultr-x86_64-python-3e36d375352632be85b9-3.15.0a2+-3e36d37 | bm-20251213-vultr-x86_64-nascheme-set_lockfree_contain-3.15.0a2+-235b6eb |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 280 ms                                                                 | 281 ms: 1.01x slower                                                     |
| docutils       | 2.75 sec                                                               | 2.74 sec: 1.00x faster                                                   |
| sphinx         | 1.06 sec                                                               | 1.07 sec: 1.01x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20251213-vultr-x86_64-python-3e36d375352632be85b9-3.15.0a2+-3e36d37 | bm-20251213-vultr-x86_64-nascheme-set_lockfree_contain-3.15.0a2+-235b6eb |
|------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| coroutines       | 24.1 ms                                                                | 23.6 ms: 1.02x faster                                                    |
| async_tree_io    | 627 ms                                                                 | 614 ms: 1.02x faster                                                     |
| async_generators | 384 ms                                                                 | 380 ms: 1.01x faster                                                     |
| Geometric mean   | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (8): async_tree_none, async_tree_memoization, async_tree_none_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251213-vultr-x86_64-python-3e36d375352632be85b9-3.15.0a2+-3e36d37 | bm-20251213-vultr-x86_64-nascheme-set_lockfree_contain-3.15.0a2+-235b6eb |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 124 ms                                                                 | 123 ms: 1.01x faster                                                     |
| float          | 74.2 ms                                                                | 73.4 ms: 1.01x faster                                                    |
| pidigits       | 188 ms                                                                 | 203 ms: 1.08x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251213-vultr-x86_64-python-3e36d375352632be85b9-3.15.0a2+-3e36d37 | bm-20251213-vultr-x86_64-nascheme-set_lockfree_contain-3.15.0a2+-235b6eb |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 2.83 ms                                                                | 2.72 ms: 1.04x faster                                                    |
| regex_v8       | 21.0 ms                                                                | 21.0 ms: 1.00x faster                                                    |
| regex_dna      | 173 ms                                                                 | 176 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20251213-vultr-x86_64-python-3e36d375352632be85b9-3.15.0a2+-3e36d37 | bm-20251213-vultr-x86_64-nascheme-set_lockfree_contain-3.15.0a2+-235b6eb |
|--------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pickle_pure_python | 343 us                                                                 | 335 us: 1.02x faster                                                     |
| tomli_loads        | 2.28 sec                                                               | 2.27 sec: 1.00x faster                                                   |
| json_loads         | 31.4 us                                                                | 31.5 us: 1.00x slower                                                    |
| xml_etree_process  | 70.1 ms                                                                | 70.5 ms: 1.01x slower                                                    |
| xml_etree_generate | 97.2 ms                                                                | 98.1 ms: 1.01x slower                                                    |
| Geometric mean     | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (4): xml_etree_iterparse, unpickle_pure_python, xml_etree_parse, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20251213-vultr-x86_64-python-3e36d375352632be85b9-3.15.0a2+-3e36d37 | bm-20251213-vultr-x86_64-nascheme-set_lockfree_contain-3.15.0a2+-235b6eb |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup | 15.9 ms                                                                | 15.9 ms: 1.00x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251213-vultr-x86_64-python-3e36d375352632be85b9-3.15.0a2+-3e36d37 | bm-20251213-vultr-x86_64-nascheme-set_lockfree_contain-3.15.0a2+-235b6eb |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 26.6 ms                                                                | 26.9 ms: 1.01x slower                                                    |
| django_template | 40.7 ms                                                                | 41.1 ms: 1.01x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (2): genshi_xml, mako

All benchmarks:
===============

| Benchmark               | bm-20251213-vultr-x86_64-python-3e36d375352632be85b9-3.15.0a2+-3e36d37 | bm-20251213-vultr-x86_64-nascheme-set_lockfree_contain-3.15.0a2+-235b6eb |
|-------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| generators              | 31.3 ms                                                                | 29.6 ms: 1.06x faster                                                    |
| regex_effbot            | 2.83 ms                                                                | 2.72 ms: 1.04x faster                                                    |
| richards_super          | 61.3 ms                                                                | 59.2 ms: 1.03x faster                                                    |
| spectral_norm           | 112 ms                                                                 | 108 ms: 1.03x faster                                                     |
| scimark_sor             | 124 ms                                                                 | 121 ms: 1.03x faster                                                     |
| pyflate                 | 470 ms                                                                 | 459 ms: 1.02x faster                                                     |
| coroutines              | 24.1 ms                                                                | 23.6 ms: 1.02x faster                                                    |
| pickle_pure_python      | 343 us                                                                 | 335 us: 1.02x faster                                                     |
| richards                | 52.6 ms                                                                | 51.5 ms: 1.02x faster                                                    |
| async_tree_io           | 627 ms                                                                 | 614 ms: 1.02x faster                                                     |
| dulwich_log             | 71.2 ms                                                                | 69.9 ms: 1.02x faster                                                    |
| deepcopy_reduce         | 3.02 us                                                                | 2.98 us: 1.02x faster                                                    |
| create_gc_cycles        | 1.51 ms                                                                | 1.48 ms: 1.02x faster                                                    |
| logging_format          | 7.96 us                                                                | 7.85 us: 1.01x faster                                                    |
| sqlglot_v2_parse        | 1.46 ms                                                                | 1.44 ms: 1.01x faster                                                    |
| deepcopy                | 283 us                                                                 | 279 us: 1.01x faster                                                     |
| nbody                   | 124 ms                                                                 | 123 ms: 1.01x faster                                                     |
| gc_traversal            | 1.94 ms                                                                | 1.92 ms: 1.01x faster                                                    |
| async_generators        | 384 ms                                                                 | 380 ms: 1.01x faster                                                     |
| float                   | 74.2 ms                                                                | 73.4 ms: 1.01x faster                                                    |
| crypto_pyaes            | 86.2 ms                                                                | 85.4 ms: 1.01x faster                                                    |
| sympy_sum               | 178 ms                                                                 | 177 ms: 1.01x faster                                                     |
| sympy_integrate         | 21.9 ms                                                                | 21.7 ms: 1.01x faster                                                    |
| pprint_pformat          | 1.62 sec                                                               | 1.62 sec: 1.00x faster                                                   |
| bpe_tokeniser           | 4.42 sec                                                               | 4.40 sec: 1.00x faster                                                   |
| fannkuch                | 457 ms                                                                 | 455 ms: 1.00x faster                                                     |
| tomli_loads             | 2.28 sec                                                               | 2.27 sec: 1.00x faster                                                   |
| docutils                | 2.75 sec                                                               | 2.74 sec: 1.00x faster                                                   |
| regex_v8                | 21.0 ms                                                                | 21.0 ms: 1.00x faster                                                    |
| comprehensions          | 18.1 us                                                                | 18.0 us: 1.00x faster                                                    |
| python_startup          | 15.9 ms                                                                | 15.9 ms: 1.00x slower                                                    |
| coverage                | 111 ms                                                                 | 112 ms: 1.00x slower                                                     |
| json_loads              | 31.4 us                                                                | 31.5 us: 1.00x slower                                                    |
| sqlglot_v2_normalize    | 117 ms                                                                 | 117 ms: 1.00x slower                                                     |
| chaos                   | 62.3 ms                                                                | 62.7 ms: 1.01x slower                                                    |
| hexiom                  | 6.44 ms                                                                | 6.48 ms: 1.01x slower                                                    |
| xml_etree_process       | 70.1 ms                                                                | 70.5 ms: 1.01x slower                                                    |
| 2to3                    | 280 ms                                                                 | 281 ms: 1.01x slower                                                     |
| logging_silent          | 105 ns                                                                 | 105 ns: 1.01x slower                                                     |
| sphinx                  | 1.06 sec                                                               | 1.07 sec: 1.01x slower                                                   |
| nqueens                 | 88.3 ms                                                                | 89.1 ms: 1.01x slower                                                    |
| pycparser               | 1.14 sec                                                               | 1.15 sec: 1.01x slower                                                   |
| genshi_text             | 26.6 ms                                                                | 26.9 ms: 1.01x slower                                                    |
| xml_etree_generate      | 97.2 ms                                                                | 98.1 ms: 1.01x slower                                                    |
| telco                   | 175 ms                                                                 | 177 ms: 1.01x slower                                                     |
| pathlib                 | 18.0 ms                                                                | 18.2 ms: 1.01x slower                                                    |
| django_template         | 40.7 ms                                                                | 41.1 ms: 1.01x slower                                                    |
| thrift                  | 894 us                                                                 | 907 us: 1.01x slower                                                     |
| regex_dna               | 173 ms                                                                 | 176 ms: 1.02x slower                                                     |
| shortest_path           | 528 ms                                                                 | 536 ms: 1.02x slower                                                     |
| scimark_monte_carlo     | 77.9 ms                                                                | 79.3 ms: 1.02x slower                                                    |
| meteor_contest          | 121 ms                                                                 | 125 ms: 1.03x slower                                                     |
| scimark_sparse_mat_mult | 5.44 ms                                                                | 5.61 ms: 1.03x slower                                                    |
| pidigits                | 188 ms                                                                 | 203 ms: 1.08x slower                                                     |
| Geometric mean          | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (40): subparsers, async_tree_none, many_optionals, async_tree_memoization, sqlglot_v2_transpile, async_tree_none_tg, bench_thread_pool, async_tree_io_tg, genshi_xml, typing_runtime_protocols, async_tree_memoization_tg, logging_simple, sympy_expand, json, sympy_str, async_tree_cpu_io_mixed, go, xml_etree_iterparse, deltablue, unpickle_pure_python, scimark_fft, regex_compile, async_tree_cpu_io_mixed_tg, xml_etree_parse, mdp, html5lib, k_core, python_startup_no_site, deepcopy_memo, sqlglot_v2_optimize, asyncio_websockets, json_dumps, connected_components, raytrace, mako, pylint, sqlite_synth, pprint_safe_repr, bench_mp_pool, scimark_lu

- Geometric mean (including insignificant results): 1.002x faster

# HPT report

- Reliability score: 99.06% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x