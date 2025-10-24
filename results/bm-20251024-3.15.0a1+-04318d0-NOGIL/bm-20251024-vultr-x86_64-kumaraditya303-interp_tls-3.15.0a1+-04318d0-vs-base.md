# Results vs. base

- fork: kumaraditya303
- ref: interp_tls
- machine: linux-x86_64
- commit hash: 04318d0
- commit date: 2025-10-24
- overall geometric mean: 1.001x slower
- HPT reliability: 76.86%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251024-vultr-x86_64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 281 ms                                                                 | 280 ms: 1.00x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                         |

Benchmark hidden because not significant (3): docutils, html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark              | bm-20251024-vultr-x86_64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_generators       | 375 ms                                                                 | 367 ms: 1.02x faster                                                 |
| async_tree_memoization | 311 ms                                                                 | 308 ms: 1.01x faster                                                 |
| async_tree_io          | 543 ms                                                                 | 540 ms: 1.01x faster                                                 |
| async_tree_io_tg       | 515 ms                                                                 | 519 ms: 1.01x slower                                                 |
| coroutines             | 24.5 ms                                                                | 25.7 ms: 1.05x slower                                                |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (6): async_tree_none, async_tree_memoization_tg, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251024-vultr-x86_64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 125 ms                                                                 | 122 ms: 1.02x faster                                                 |
| pidigits       | 190 ms                                                                 | 196 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251024-vultr-x86_64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 2.64 ms                                                                | 2.66 ms: 1.01x slower                                                |
| regex_dna      | 171 ms                                                                 | 174 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                         |

Benchmark hidden because not significant (2): regex_compile, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251024-vultr-x86_64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_parse      | 133 ms                                                                 | 131 ms: 1.01x faster                                                 |
| json_loads           | 31.3 us                                                                | 30.9 us: 1.01x faster                                                |
| pickle_pure_python   | 341 us                                                                 | 339 us: 1.01x faster                                                 |
| xml_etree_generate   | 95.6 ms                                                                | 95.8 ms: 1.00x slower                                                |
| xml_etree_process    | 68.7 ms                                                                | 68.9 ms: 1.00x slower                                                |
| unpickle_pure_python | 232 us                                                                 | 235 us: 1.01x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                         |

Benchmark hidden because not significant (3): xml_etree_iterparse, tomli_loads, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251024-vultr-x86_64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 9.60 ms                                                                | 9.54 ms: 1.01x faster                                                |
| python_startup         | 15.8 ms                                                                | 15.7 ms: 1.01x faster                                                |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251024-vultr-x86_64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 58.7 ms                                                                | 56.4 ms: 1.04x faster                                                |
| genshi_text     | 26.7 ms                                                                | 26.5 ms: 1.01x faster                                                |
| django_template | 40.6 ms                                                                | 40.3 ms: 1.01x faster                                                |
| mako            | 15.6 ms                                                                | 15.6 ms: 1.00x faster                                                |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                         |

All benchmarks:
===============

| Benchmark               | bm-20251024-vultr-x86_64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|-------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| scimark_sparse_mat_mult | 5.44 ms                                                                | 5.19 ms: 1.05x faster                                                |
| genshi_xml              | 58.7 ms                                                                | 56.4 ms: 1.04x faster                                                |
| nbody                   | 125 ms                                                                 | 122 ms: 1.02x faster                                                 |
| async_generators        | 375 ms                                                                 | 367 ms: 1.02x faster                                                 |
| connected_components    | 495 ms                                                                 | 488 ms: 1.01x faster                                                 |
| xml_etree_parse         | 133 ms                                                                 | 131 ms: 1.01x faster                                                 |
| async_tree_memoization  | 311 ms                                                                 | 308 ms: 1.01x faster                                                 |
| json_loads              | 31.3 us                                                                | 30.9 us: 1.01x faster                                                |
| hexiom                  | 6.48 ms                                                                | 6.42 ms: 1.01x faster                                                |
| shortest_path           | 540 ms                                                                 | 534 ms: 1.01x faster                                                 |
| generators              | 31.5 ms                                                                | 31.2 ms: 1.01x faster                                                |
| scimark_lu              | 130 ms                                                                 | 129 ms: 1.01x faster                                                 |
| mdp                     | 1.33 sec                                                               | 1.31 sec: 1.01x faster                                               |
| genshi_text             | 26.7 ms                                                                | 26.5 ms: 1.01x faster                                                |
| raytrace                | 301 ms                                                                 | 298 ms: 1.01x faster                                                 |
| bpe_tokeniser           | 4.41 sec                                                               | 4.38 sec: 1.01x faster                                               |
| nqueens                 | 89.0 ms                                                                | 88.4 ms: 1.01x faster                                                |
| async_tree_io           | 543 ms                                                                 | 540 ms: 1.01x faster                                                 |
| python_startup_no_site  | 9.60 ms                                                                | 9.54 ms: 1.01x faster                                                |
| django_template         | 40.6 ms                                                                | 40.3 ms: 1.01x faster                                                |
| python_startup          | 15.8 ms                                                                | 15.7 ms: 1.01x faster                                                |
| pickle_pure_python      | 341 us                                                                 | 339 us: 1.01x faster                                                 |
| gc_traversal            | 1.91 ms                                                                | 1.90 ms: 1.00x faster                                                |
| sympy_expand            | 518 ms                                                                 | 516 ms: 1.00x faster                                                 |
| comprehensions          | 18.0 us                                                                | 17.9 us: 1.00x faster                                                |
| fannkuch                | 453 ms                                                                 | 452 ms: 1.00x faster                                                 |
| bench_thread_pool       | 3.07 ms                                                                | 3.06 ms: 1.00x faster                                                |
| mako                    | 15.6 ms                                                                | 15.6 ms: 1.00x faster                                                |
| sqlglot_v2_normalize    | 115 ms                                                                 | 115 ms: 1.00x faster                                                 |
| 2to3                    | 281 ms                                                                 | 280 ms: 1.00x faster                                                 |
| xml_etree_generate      | 95.6 ms                                                                | 95.8 ms: 1.00x slower                                                |
| xml_etree_process       | 68.7 ms                                                                | 68.9 ms: 1.00x slower                                                |
| pathlib                 | 17.7 ms                                                                | 17.8 ms: 1.00x slower                                                |
| go                      | 122 ms                                                                 | 122 ms: 1.00x slower                                                 |
| sympy_integrate         | 21.8 ms                                                                | 22.0 ms: 1.01x slower                                                |
| richards_super          | 59.2 ms                                                                | 59.6 ms: 1.01x slower                                                |
| crypto_pyaes            | 85.2 ms                                                                | 85.8 ms: 1.01x slower                                                |
| async_tree_io_tg        | 515 ms                                                                 | 519 ms: 1.01x slower                                                 |
| regex_effbot            | 2.64 ms                                                                | 2.66 ms: 1.01x slower                                                |
| logging_format          | 7.80 us                                                                | 7.86 us: 1.01x slower                                                |
| pprint_safe_repr        | 776 ms                                                                 | 785 ms: 1.01x slower                                                 |
| deepcopy                | 277 us                                                                 | 281 us: 1.01x slower                                                 |
| unpickle_pure_python    | 232 us                                                                 | 235 us: 1.01x slower                                                 |
| scimark_fft             | 348 ms                                                                 | 353 ms: 1.01x slower                                                 |
| deepcopy_memo           | 30.6 us                                                                | 31.0 us: 1.01x slower                                                |
| meteor_contest          | 119 ms                                                                 | 121 ms: 1.01x slower                                                 |
| richards                | 51.0 ms                                                                | 51.8 ms: 1.01x slower                                                |
| pprint_pformat          | 1.60 sec                                                               | 1.62 sec: 1.01x slower                                               |
| regex_dna               | 171 ms                                                                 | 174 ms: 1.02x slower                                                 |
| scimark_monte_carlo     | 77.9 ms                                                                | 79.2 ms: 1.02x slower                                                |
| logging_simple          | 6.78 us                                                                | 6.91 us: 1.02x slower                                                |
| telco                   | 173 ms                                                                 | 178 ms: 1.03x slower                                                 |
| scimark_sor             | 122 ms                                                                 | 125 ms: 1.03x slower                                                 |
| deepcopy_reduce         | 3.02 us                                                                | 3.10 us: 1.03x slower                                                |
| pidigits                | 190 ms                                                                 | 196 ms: 1.03x slower                                                 |
| spectral_norm           | 109 ms                                                                 | 114 ms: 1.05x slower                                                 |
| logging_silent          | 102 ns                                                                 | 107 ns: 1.05x slower                                                 |
| coroutines              | 24.5 ms                                                                | 25.7 ms: 1.05x slower                                                |
| Geometric mean          | (ref)                                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (36): async_tree_none, pylint, sqlite_synth, sqlglot_v2_optimize, pyflate, async_tree_memoization_tg, create_gc_cycles, docutils, async_tree_none_tg, sympy_sum, sympy_str, json, k_core, regex_compile, pycparser, async_tree_cpu_io_mixed, regex_v8, dulwich_log, float, coverage, xml_etree_iterparse, async_tree_cpu_io_mixed_tg, asyncio_websockets, tomli_loads, html5lib, sphinx, chaos, typing_runtime_protocols, bench_mp_pool, json_dumps, deltablue, thrift, sqlglot_v2_transpile, many_optionals, subparsers, sqlglot_v2_parse

- Geometric mean (including insignificant results): 1.001x slower

# HPT report

- Reliability score: 76.86% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x