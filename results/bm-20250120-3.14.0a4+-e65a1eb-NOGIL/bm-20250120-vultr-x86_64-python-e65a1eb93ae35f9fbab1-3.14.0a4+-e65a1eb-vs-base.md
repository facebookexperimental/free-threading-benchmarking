# Results vs. base

- fork: python
- ref: e65a1eb93ae35f9fbab1
- machine: linux-x86_64
- commit hash: e65a1eb
- commit date: 2025-01-20
- overall geometric mean: 1.004x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250120-vultr-x86_64-python-e54ac3b69edacf414998-3.14.0a4+-e54ac3b | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 316 ms                                                                 | 313 ms: 1.01x faster                                                   |
| docutils       | 2.87 sec                                                               | 2.84 sec: 1.01x faster                                                 |
| html5lib       | 74.0 ms                                                                | 72.5 ms: 1.02x faster                                                  |
| sphinx         | 1.14 sec                                                               | 1.13 sec: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250120-vultr-x86_64-python-e54ac3b69edacf414998-3.14.0a4+-e54ac3b | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 588 ms                                                                 | 580 ms: 1.01x faster                                                   |
| coroutines                 | 25.2 ms                                                                | 25.0 ms: 1.01x faster                                                  |
| async_tree_io              | 616 ms                                                                 | 611 ms: 1.01x faster                                                   |
| async_tree_memoization     | 356 ms                                                                 | 354 ms: 1.01x faster                                                   |
| async_generators           | 370 ms                                                                 | 376 ms: 1.01x slower                                                   |
| async_tree_cpu_io_mixed    | 537 ms                                                                 | 603 ms: 1.12x slower                                                   |
| async_tree_cpu_io_mixed_tg | 501 ms                                                                 | 569 ms: 1.13x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                                           |

Benchmark hidden because not significant (4): async_tree_memoization_tg, async_tree_none_tg, asyncio_websockets, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250120-vultr-x86_64-python-e54ac3b69edacf414998-3.14.0a4+-e54ac3b | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 142 ms                                                                 | 137 ms: 1.03x faster                                                   |
| float          | 79.8 ms                                                                | 77.2 ms: 1.03x faster                                                  |
| pidigits       | 200 ms                                                                 | 217 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250120-vultr-x86_64-python-e54ac3b69edacf414998-3.14.0a4+-e54ac3b | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 2.83 ms                                                                | 2.68 ms: 1.06x faster                                                  |
| regex_v8       | 24.0 ms                                                                | 23.1 ms: 1.04x faster                                                  |
| regex_dna      | 182 ms                                                                 | 182 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250120-vultr-x86_64-python-e54ac3b69edacf414998-3.14.0a4+-e54ac3b | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 399 us                                                                 | 395 us: 1.01x faster                                                   |
| xml_etree_generate   | 100 ms                                                                 | 98.9 ms: 1.01x faster                                                  |
| unpickle_pure_python | 282 us                                                                 | 280 us: 1.01x faster                                                   |
| tomli_loads          | 2.45 sec                                                               | 2.43 sec: 1.01x faster                                                 |
| xml_etree_process    | 75.6 ms                                                                | 75.3 ms: 1.01x faster                                                  |
| json_dumps           | 13.0 ms                                                                | 13.0 ms: 1.00x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (3): xml_etree_parse, json_loads, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250120-vultr-x86_64-python-e54ac3b69edacf414998-3.14.0a4+-e54ac3b | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 9.62 ms                                                                | 9.58 ms: 1.00x faster                                                  |
| python_startup         | 15.4 ms                                                                | 15.3 ms: 1.00x faster                                                  |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250120-vultr-x86_64-python-e54ac3b69edacf414998-3.14.0a4+-e54ac3b | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 63.8 ms                                                                | 63.0 ms: 1.01x faster                                                  |
| genshi_text     | 30.0 ms                                                                | 29.8 ms: 1.01x faster                                                  |
| django_template | 45.0 ms                                                                | 44.8 ms: 1.00x faster                                                  |
| mako            | 16.2 ms                                                                | 16.3 ms: 1.00x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20250120-vultr-x86_64-python-e54ac3b69edacf414998-3.14.0a4+-e54ac3b | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot               | 2.83 ms                                                                | 2.68 ms: 1.06x faster                                                  |
| scimark_sparse_mat_mult    | 5.93 ms                                                                | 5.64 ms: 1.05x faster                                                  |
| regex_v8                   | 24.0 ms                                                                | 23.1 ms: 1.04x faster                                                  |
| nbody                      | 142 ms                                                                 | 137 ms: 1.03x faster                                                   |
| float                      | 79.8 ms                                                                | 77.2 ms: 1.03x faster                                                  |
| pyflate                    | 521 ms                                                                 | 504 ms: 1.03x faster                                                   |
| go                         | 146 ms                                                                 | 142 ms: 1.03x faster                                                   |
| raytrace                   | 341 ms                                                                 | 334 ms: 1.02x faster                                                   |
| pycparser                  | 1.25 sec                                                               | 1.22 sec: 1.02x faster                                                 |
| html5lib                   | 74.0 ms                                                                | 72.5 ms: 1.02x faster                                                  |
| fannkuch                   | 501 ms                                                                 | 492 ms: 1.02x faster                                                   |
| sqlglot_transpile          | 1.99 ms                                                                | 1.95 ms: 1.02x faster                                                  |
| logging_silent             | 120 ns                                                                 | 118 ns: 1.02x faster                                                   |
| crypto_pyaes               | 89.3 ms                                                                | 87.8 ms: 1.02x faster                                                  |
| hexiom                     | 7.73 ms                                                                | 7.60 ms: 1.02x faster                                                  |
| scimark_monte_carlo        | 84.6 ms                                                                | 83.2 ms: 1.02x faster                                                  |
| deltablue                  | 4.85 ms                                                                | 4.77 ms: 1.02x faster                                                  |
| pathlib                    | 19.0 ms                                                                | 18.7 ms: 1.02x faster                                                  |
| typing_runtime_protocols   | 213 us                                                                 | 210 us: 1.01x faster                                                   |
| sqlglot_parse              | 1.64 ms                                                                | 1.62 ms: 1.01x faster                                                  |
| sphinx                     | 1.14 sec                                                               | 1.13 sec: 1.01x faster                                                 |
| connected_components       | 499 ms                                                                 | 493 ms: 1.01x faster                                                   |
| async_tree_io_tg           | 588 ms                                                                 | 580 ms: 1.01x faster                                                   |
| deepcopy                   | 327 us                                                                 | 323 us: 1.01x faster                                                   |
| meteor_contest             | 133 ms                                                                 | 131 ms: 1.01x faster                                                   |
| pickle_pure_python         | 399 us                                                                 | 395 us: 1.01x faster                                                   |
| genshi_xml                 | 63.8 ms                                                                | 63.0 ms: 1.01x faster                                                  |
| telco                      | 8.76 ms                                                                | 8.66 ms: 1.01x faster                                                  |
| comprehensions             | 21.6 us                                                                | 21.4 us: 1.01x faster                                                  |
| xml_etree_generate         | 100 ms                                                                 | 98.9 ms: 1.01x faster                                                  |
| scimark_fft                | 400 ms                                                                 | 395 ms: 1.01x faster                                                   |
| richards_super             | 66.4 ms                                                                | 65.7 ms: 1.01x faster                                                  |
| sqlalchemy_declarative     | 167 ms                                                                 | 166 ms: 1.01x faster                                                   |
| coroutines                 | 25.2 ms                                                                | 25.0 ms: 1.01x faster                                                  |
| sqlglot_normalize          | 125 ms                                                                 | 123 ms: 1.01x faster                                                   |
| subparsers                 | 26.7 ms                                                                | 26.4 ms: 1.01x faster                                                  |
| json                       | 5.38 ms                                                                | 5.33 ms: 1.01x faster                                                  |
| richards                   | 57.4 ms                                                                | 56.9 ms: 1.01x faster                                                  |
| scimark_sor                | 142 ms                                                                 | 140 ms: 1.01x faster                                                   |
| async_tree_io              | 616 ms                                                                 | 611 ms: 1.01x faster                                                   |
| unpickle_pure_python       | 282 us                                                                 | 280 us: 1.01x faster                                                   |
| chaos                      | 72.3 ms                                                                | 71.6 ms: 1.01x faster                                                  |
| tomli_loads                | 2.45 sec                                                               | 2.43 sec: 1.01x faster                                                 |
| sympy_expand               | 570 ms                                                                 | 565 ms: 1.01x faster                                                   |
| shortest_path              | 551 ms                                                                 | 546 ms: 1.01x faster                                                   |
| genshi_text                | 30.0 ms                                                                | 29.8 ms: 1.01x faster                                                  |
| docutils                   | 2.87 sec                                                               | 2.84 sec: 1.01x faster                                                 |
| sqlglot_optimize           | 63.5 ms                                                                | 63.1 ms: 1.01x faster                                                  |
| deepcopy_memo              | 40.2 us                                                                | 39.9 us: 1.01x faster                                                  |
| many_optionals             | 1.23 ms                                                                | 1.22 ms: 1.01x faster                                                  |
| 2to3                       | 316 ms                                                                 | 313 ms: 1.01x faster                                                   |
| sympy_str                  | 345 ms                                                                 | 343 ms: 1.01x faster                                                   |
| sympy_integrate            | 25.0 ms                                                                | 24.8 ms: 1.01x faster                                                  |
| create_gc_cycles           | 1.35 ms                                                                | 1.34 ms: 1.01x faster                                                  |
| regex_dna                  | 182 ms                                                                 | 182 ms: 1.01x faster                                                   |
| async_tree_memoization     | 356 ms                                                                 | 354 ms: 1.01x faster                                                   |
| xml_etree_process          | 75.6 ms                                                                | 75.3 ms: 1.01x faster                                                  |
| django_template            | 45.0 ms                                                                | 44.8 ms: 1.00x faster                                                  |
| python_startup_no_site     | 9.62 ms                                                                | 9.58 ms: 1.00x faster                                                  |
| bpe_tokeniser              | 4.82 sec                                                               | 4.80 sec: 1.00x faster                                                 |
| python_startup             | 15.4 ms                                                                | 15.3 ms: 1.00x faster                                                  |
| json_dumps                 | 13.0 ms                                                                | 13.0 ms: 1.00x slower                                                  |
| mako                       | 16.2 ms                                                                | 16.3 ms: 1.00x slower                                                  |
| thrift                     | 934 us                                                                 | 939 us: 1.01x slower                                                   |
| nqueens                    | 98.0 ms                                                                | 98.8 ms: 1.01x slower                                                  |
| deepcopy_reduce            | 3.34 us                                                                | 3.38 us: 1.01x slower                                                  |
| mdp                        | 2.76 sec                                                               | 2.79 sec: 1.01x slower                                                 |
| logging_format             | 8.88 us                                                                | 8.99 us: 1.01x slower                                                  |
| async_generators           | 370 ms                                                                 | 376 ms: 1.01x slower                                                   |
| logging_simple             | 7.75 us                                                                | 7.87 us: 1.02x slower                                                  |
| gc_traversal               | 3.16 ms                                                                | 3.37 ms: 1.07x slower                                                  |
| pidigits                   | 200 ms                                                                 | 217 ms: 1.09x slower                                                   |
| async_tree_cpu_io_mixed    | 537 ms                                                                 | 603 ms: 1.12x slower                                                   |
| async_tree_cpu_io_mixed_tg | 501 ms                                                                 | 569 ms: 1.13x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (22): pylint, sympy_sum, async_tree_memoization_tg, xml_etree_parse, async_tree_none_tg, dulwich_log, json_loads, k_core, asyncio_websockets, scimark_lu, xml_etree_iterparse, regex_compile, pprint_pformat, coverage, bench_mp_pool, bench_thread_pool, sqlalchemy_imperative, pprint_safe_repr, async_tree_none, generators, sqlite_synth, spectral_norm

- Geometric mean (including insignificant results): 1.004x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x