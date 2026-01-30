# Results vs. base

- fork: DinoV
- ref: lazy_review_updates2
- machine: linux-x86_64
- commit hash: 8fd3f20
- commit date: 2026-01-27
- overall geometric mean: 1.001x faster
- HPT reliability: 65.41%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 | bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5+-8fd3f20 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 2.57 sec                                                               | 2.58 sec: 1.00x slower                                                |
| html5lib       | 59.2 ms                                                                | 61.3 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (2): 2to3, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 | bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5+-8fd3f20 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 587 ms                                                                 | 566 ms: 1.04x faster                                                  |
| async_tree_memoization_tg  | 305 ms                                                                 | 295 ms: 1.03x faster                                                  |
| coroutines                 | 24.4 ms                                                                | 23.8 ms: 1.03x faster                                                 |
| async_generators           | 338 ms                                                                 | 342 ms: 1.01x slower                                                  |
| async_tree_cpu_io_mixed    | 477 ms                                                                 | 483 ms: 1.01x slower                                                  |
| async_tree_cpu_io_mixed_tg | 478 ms                                                                 | 486 ms: 1.02x slower                                                  |
| async_tree_none            | 243 ms                                                                 | 248 ms: 1.02x slower                                                  |
| async_tree_io              | 554 ms                                                                 | 574 ms: 1.04x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (3): async_tree_memoization, asyncio_websockets, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 | bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5+-8fd3f20 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 197 ms                                                                 | 193 ms: 1.02x faster                                                  |
| float          | 71.1 ms                                                                | 70.0 ms: 1.01x faster                                                 |
| nbody          | 91.4 ms                                                                | 91.0 ms: 1.00x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 | bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5+-8fd3f20 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 22.2 ms                                                                | 21.8 ms: 1.02x faster                                                 |
| regex_compile  | 124 ms                                                                 | 123 ms: 1.01x faster                                                  |
| regex_dna      | 180 ms                                                                 | 179 ms: 1.01x faster                                                  |
| regex_effbot   | 2.91 ms                                                                | 2.93 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 | bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5+-8fd3f20 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| unpickle_pure_python | 213 us                                                                 | 209 us: 1.02x faster                                                  |
| pickle_pure_python   | 310 us                                                                 | 305 us: 1.02x faster                                                  |
| tomli_loads          | 1.86 sec                                                               | 1.83 sec: 1.02x faster                                                |
| json_loads           | 28.2 us                                                                | 28.3 us: 1.00x slower                                                 |
| xml_etree_generate   | 82.6 ms                                                                | 83.4 ms: 1.01x slower                                                 |
| json_dumps           | 9.58 ms                                                                | 9.84 ms: 1.03x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (3): xml_etree_process, xml_etree_iterparse, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 | bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5+-8fd3f20 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.28 ms                                                                | 7.34 ms: 1.01x slower                                                 |
| python_startup         | 12.4 ms                                                                | 12.5 ms: 1.01x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 | bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5+-8fd3f20 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 12.1 ms                                                                | 11.8 ms: 1.03x faster                                                 |
| django_template | 35.6 ms                                                                | 35.1 ms: 1.01x faster                                                 |
| genshi_xml      | 49.7 ms                                                                | 49.2 ms: 1.01x faster                                                 |
| genshi_text     | 21.6 ms                                                                | 21.5 ms: 1.00x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 | bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5+-8fd3f20 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| deepcopy                   | 238 us                                                                 | 229 us: 1.04x faster                                                  |
| async_tree_io_tg           | 587 ms                                                                 | 566 ms: 1.04x faster                                                  |
| async_tree_memoization_tg  | 305 ms                                                                 | 295 ms: 1.03x faster                                                  |
| crypto_pyaes               | 69.7 ms                                                                | 67.8 ms: 1.03x faster                                                 |
| coroutines                 | 24.4 ms                                                                | 23.8 ms: 1.03x faster                                                 |
| mako                       | 12.1 ms                                                                | 11.8 ms: 1.03x faster                                                 |
| pidigits                   | 197 ms                                                                 | 193 ms: 1.02x faster                                                  |
| regex_v8                   | 22.2 ms                                                                | 21.8 ms: 1.02x faster                                                 |
| deepcopy_reduce            | 2.59 us                                                                | 2.54 us: 1.02x faster                                                 |
| shortest_path              | 436 ms                                                                 | 428 ms: 1.02x faster                                                  |
| unpickle_pure_python       | 213 us                                                                 | 209 us: 1.02x faster                                                  |
| sqlglot_v2_optimize        | 51.7 ms                                                                | 50.7 ms: 1.02x faster                                                 |
| pickle_pure_python         | 310 us                                                                 | 305 us: 1.02x faster                                                  |
| deepcopy_memo              | 26.9 us                                                                | 26.5 us: 1.02x faster                                                 |
| sqlglot_v2_transpile       | 1.53 ms                                                                | 1.50 ms: 1.02x faster                                                 |
| fannkuch                   | 388 ms                                                                 | 382 ms: 1.02x faster                                                  |
| tomli_loads                | 1.86 sec                                                               | 1.83 sec: 1.02x faster                                                |
| scimark_fft                | 305 ms                                                                 | 300 ms: 1.02x faster                                                  |
| sqlite_synth               | 2.28 us                                                                | 2.25 us: 1.01x faster                                                 |
| float                      | 71.1 ms                                                                | 70.0 ms: 1.01x faster                                                 |
| deltablue                  | 3.32 ms                                                                | 3.28 ms: 1.01x faster                                                 |
| sympy_str                  | 280 ms                                                                 | 276 ms: 1.01x faster                                                  |
| django_template            | 35.6 ms                                                                | 35.1 ms: 1.01x faster                                                 |
| json                       | 5.04 ms                                                                | 4.99 ms: 1.01x faster                                                 |
| sqlglot_v2_parse           | 1.22 ms                                                                | 1.21 ms: 1.01x faster                                                 |
| sympy_integrate            | 19.2 ms                                                                | 19.0 ms: 1.01x faster                                                 |
| nqueens                    | 79.2 ms                                                                | 78.5 ms: 1.01x faster                                                 |
| scimark_monte_carlo        | 62.2 ms                                                                | 61.6 ms: 1.01x faster                                                 |
| genshi_xml                 | 49.7 ms                                                                | 49.2 ms: 1.01x faster                                                 |
| subparsers                 | 9.28 ms                                                                | 9.19 ms: 1.01x faster                                                 |
| regex_compile              | 124 ms                                                                 | 123 ms: 1.01x faster                                                  |
| sympy_sum                  | 156 ms                                                                 | 155 ms: 1.01x faster                                                  |
| raytrace                   | 253 ms                                                                 | 251 ms: 1.01x faster                                                  |
| regex_dna                  | 180 ms                                                                 | 179 ms: 1.01x faster                                                  |
| scimark_lu                 | 109 ms                                                                 | 108 ms: 1.01x faster                                                  |
| sqlglot_v2_normalize       | 102 ms                                                                 | 101 ms: 1.01x faster                                                  |
| k_core                     | 1.89 sec                                                               | 1.88 sec: 1.00x faster                                                |
| nbody                      | 91.4 ms                                                                | 91.0 ms: 1.00x faster                                                 |
| genshi_text                | 21.6 ms                                                                | 21.5 ms: 1.00x faster                                                 |
| scimark_sor                | 106 ms                                                                 | 106 ms: 1.00x slower                                                  |
| logging_silent             | 101 ns                                                                 | 101 ns: 1.00x slower                                                  |
| json_loads                 | 28.2 us                                                                | 28.3 us: 1.00x slower                                                 |
| chaos                      | 55.9 ms                                                                | 56.1 ms: 1.00x slower                                                 |
| create_gc_cycles           | 1.86 ms                                                                | 1.87 ms: 1.00x slower                                                 |
| docutils                   | 2.57 sec                                                               | 2.58 sec: 1.00x slower                                                |
| pprint_pformat             | 1.43 sec                                                               | 1.44 sec: 1.00x slower                                                |
| pprint_safe_repr           | 702 ms                                                                 | 706 ms: 1.00x slower                                                  |
| connected_components       | 389 ms                                                                 | 391 ms: 1.01x slower                                                  |
| pyflate                    | 409 ms                                                                 | 411 ms: 1.01x slower                                                  |
| thrift                     | 768 us                                                                 | 772 us: 1.01x slower                                                  |
| coverage                   | 81.5 ms                                                                | 82.0 ms: 1.01x slower                                                 |
| python_startup_no_site     | 7.28 ms                                                                | 7.34 ms: 1.01x slower                                                 |
| regex_effbot               | 2.91 ms                                                                | 2.93 ms: 1.01x slower                                                 |
| xml_etree_generate         | 82.6 ms                                                                | 83.4 ms: 1.01x slower                                                 |
| spectral_norm              | 96.0 ms                                                                | 96.9 ms: 1.01x slower                                                 |
| python_startup             | 12.4 ms                                                                | 12.5 ms: 1.01x slower                                                 |
| dulwich_log                | 67.6 ms                                                                | 68.3 ms: 1.01x slower                                                 |
| go                         | 105 ms                                                                 | 106 ms: 1.01x slower                                                  |
| async_generators           | 338 ms                                                                 | 342 ms: 1.01x slower                                                  |
| async_tree_cpu_io_mixed    | 477 ms                                                                 | 483 ms: 1.01x slower                                                  |
| generators                 | 28.0 ms                                                                | 28.4 ms: 1.01x slower                                                 |
| async_tree_cpu_io_mixed_tg | 478 ms                                                                 | 486 ms: 1.02x slower                                                  |
| richards_super             | 48.8 ms                                                                | 49.7 ms: 1.02x slower                                                 |
| logging_simple             | 5.92 us                                                                | 6.05 us: 1.02x slower                                                 |
| async_tree_none            | 243 ms                                                                 | 248 ms: 1.02x slower                                                  |
| logging_format             | 6.59 us                                                                | 6.76 us: 1.03x slower                                                 |
| json_dumps                 | 9.58 ms                                                                | 9.84 ms: 1.03x slower                                                 |
| scimark_sparse_mat_mult    | 4.37 ms                                                                | 4.51 ms: 1.03x slower                                                 |
| html5lib                   | 59.2 ms                                                                | 61.3 ms: 1.04x slower                                                 |
| async_tree_io              | 554 ms                                                                 | 574 ms: 1.04x slower                                                  |
| gc_traversal               | 4.00 ms                                                                | 4.42 ms: 1.11x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (23): bench_mp_pool, async_tree_memoization, typing_runtime_protocols, xml_etree_process, xml_etree_iterparse, mdp, meteor_contest, hexiom, 2to3, bpe_tokeniser, asyncio_websockets, pathlib, many_optionals, pycparser, comprehensions, sphinx, sympy_expand, xml_etree_parse, richards, telco, pylint, bench_thread_pool, async_tree_none_tg

- Geometric mean (including insignificant results): 1.001x faster

# HPT report

- Reliability score: 65.41% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x