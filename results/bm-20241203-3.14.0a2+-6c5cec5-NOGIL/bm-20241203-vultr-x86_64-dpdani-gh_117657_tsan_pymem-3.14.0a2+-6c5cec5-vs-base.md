# Results vs. base

- fork: dpdani
- ref: gh_117657_tsan_pymem
- machine: linux-x86_64
- commit hash: 6c5cec5
- commit date: 2024-12-03
- overall geometric mean: 1.007x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2+-6c5cec5 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 377 ms                                                                 | 376 ms: 1.00x faster                                                   |
| docutils       | 3.22 sec                                                               | 3.20 sec: 1.01x faster                                                 |
| html5lib       | 102 ms                                                                 | 99.2 ms: 1.03x faster                                                  |
| sphinx         | 1.24 sec                                                               | 1.23 sec: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2+-6c5cec5 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| coroutines                 | 28.7 ms                                                                | 28.1 ms: 1.02x faster                                                  |
| async_generators           | 471 ms                                                                 | 465 ms: 1.01x faster                                                   |
| async_tree_memoization     | 493 ms                                                                 | 488 ms: 1.01x faster                                                   |
| async_tree_none_tg         | 368 ms                                                                 | 364 ms: 1.01x faster                                                   |
| async_tree_none            | 400 ms                                                                 | 397 ms: 1.01x faster                                                   |
| async_tree_cpu_io_mixed_tg | 624 ms                                                                 | 621 ms: 1.00x faster                                                   |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (5): async_tree_memoization_tg, async_tree_io, async_tree_io_tg, asyncio_websockets, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2+-6c5cec5 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 134 ms                                                                 | 130 ms: 1.03x faster                                                   |
| pidigits       | 184 ms                                                                 | 181 ms: 1.02x faster                                                   |
| float          | 142 ms                                                                 | 143 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2+-6c5cec5 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.03 ms                                                                | 2.89 ms: 1.05x faster                                                  |
| regex_dna      | 187 ms                                                                 | 183 ms: 1.02x faster                                                   |
| regex_compile  | 194 ms                                                                 | 191 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2+-6c5cec5 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| unpickle_pure_python | 386 us                                                                 | 379 us: 1.02x faster                                                   |
| tomli_loads          | 2.77 sec                                                               | 2.74 sec: 1.01x faster                                                 |
| pickle_pure_python   | 562 us                                                                 | 556 us: 1.01x faster                                                   |
| json_dumps           | 14.5 ms                                                                | 14.5 ms: 1.00x faster                                                  |
| xml_etree_generate   | 102 ms                                                                 | 102 ms: 1.00x faster                                                   |
| xml_etree_process    | 82.2 ms                                                                | 81.9 ms: 1.00x faster                                                  |
| xml_etree_parse      | 129 ms                                                                 | 130 ms: 1.01x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (2): xml_etree_iterparse, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2+-6c5cec5 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 10.2 ms                                                                | 10.3 ms: 1.00x slower                                                  |
| python_startup         | 17.4 ms                                                                | 17.5 ms: 1.01x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2+-6c5cec5 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml     | 67.6 ms                                                                | 66.0 ms: 1.02x faster                                                  |
| mako           | 20.0 ms                                                                | 19.6 ms: 1.02x faster                                                  |
| genshi_text    | 33.6 ms                                                                | 33.2 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2+-6c5cec5 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot               | 3.03 ms                                                                | 2.89 ms: 1.05x faster                                                  |
| deepcopy_memo              | 45.8 us                                                                | 44.2 us: 1.04x faster                                                  |
| fannkuch                   | 517 ms                                                                 | 500 ms: 1.03x faster                                                   |
| logging_format             | 12.5 us                                                                | 12.1 us: 1.03x faster                                                  |
| spectral_norm              | 132 ms                                                                 | 129 ms: 1.03x faster                                                   |
| scimark_sparse_mat_mult    | 5.90 ms                                                                | 5.73 ms: 1.03x faster                                                  |
| html5lib                   | 102 ms                                                                 | 99.2 ms: 1.03x faster                                                  |
| nbody                      | 134 ms                                                                 | 130 ms: 1.03x faster                                                   |
| logging_simple             | 11.2 us                                                                | 10.9 us: 1.03x faster                                                  |
| pprint_safe_repr           | 1.08 sec                                                               | 1.05 sec: 1.03x faster                                                 |
| genshi_xml                 | 67.6 ms                                                                | 66.0 ms: 1.02x faster                                                  |
| scimark_fft                | 408 ms                                                                 | 398 ms: 1.02x faster                                                   |
| pprint_pformat             | 2.24 sec                                                               | 2.19 sec: 1.02x faster                                                 |
| typing_runtime_protocols   | 213 us                                                                 | 208 us: 1.02x faster                                                   |
| mako                       | 20.0 ms                                                                | 19.6 ms: 1.02x faster                                                  |
| coroutines                 | 28.7 ms                                                                | 28.1 ms: 1.02x faster                                                  |
| shortest_path              | 572 ms                                                                 | 560 ms: 1.02x faster                                                   |
| richards_super             | 101 ms                                                                 | 99.1 ms: 1.02x faster                                                  |
| unpickle_pure_python       | 386 us                                                                 | 379 us: 1.02x faster                                                   |
| bpe_tokeniser              | 5.51 sec                                                               | 5.40 sec: 1.02x faster                                                 |
| regex_dna                  | 187 ms                                                                 | 183 ms: 1.02x faster                                                   |
| pidigits                   | 184 ms                                                                 | 181 ms: 1.02x faster                                                   |
| meteor_contest             | 135 ms                                                                 | 133 ms: 1.02x faster                                                   |
| richards                   | 84.0 ms                                                                | 82.7 ms: 1.02x faster                                                  |
| raytrace                   | 611 ms                                                                 | 602 ms: 1.02x faster                                                   |
| coverage                   | 102 ms                                                                 | 100 ms: 1.01x faster                                                   |
| regex_compile              | 194 ms                                                                 | 191 ms: 1.01x faster                                                   |
| genshi_text                | 33.6 ms                                                                | 33.2 ms: 1.01x faster                                                  |
| async_generators           | 471 ms                                                                 | 465 ms: 1.01x faster                                                   |
| thrift                     | 1.21 ms                                                                | 1.20 ms: 1.01x faster                                                  |
| tomli_loads                | 2.77 sec                                                               | 2.74 sec: 1.01x faster                                                 |
| crypto_pyaes               | 93.8 ms                                                                | 92.8 ms: 1.01x faster                                                  |
| pickle_pure_python         | 562 us                                                                 | 556 us: 1.01x faster                                                   |
| async_tree_memoization     | 493 ms                                                                 | 488 ms: 1.01x faster                                                   |
| async_tree_none_tg         | 368 ms                                                                 | 364 ms: 1.01x faster                                                   |
| sphinx                     | 1.24 sec                                                               | 1.23 sec: 1.01x faster                                                 |
| pyflate                    | 737 ms                                                                 | 731 ms: 1.01x faster                                                   |
| deepcopy                   | 354 us                                                                 | 351 us: 1.01x faster                                                   |
| docutils                   | 3.22 sec                                                               | 3.20 sec: 1.01x faster                                                 |
| sqlalchemy_declarative     | 208 ms                                                                 | 207 ms: 1.01x faster                                                   |
| k_core                     | 2.45 sec                                                               | 2.43 sec: 1.01x faster                                                 |
| generators                 | 39.1 ms                                                                | 38.9 ms: 1.01x faster                                                  |
| async_tree_none            | 400 ms                                                                 | 397 ms: 1.01x faster                                                   |
| go                         | 283 ms                                                                 | 281 ms: 1.01x faster                                                   |
| hexiom                     | 10.8 ms                                                                | 10.7 ms: 1.01x faster                                                  |
| pycparser                  | 1.61 sec                                                               | 1.60 sec: 1.01x faster                                                 |
| async_tree_cpu_io_mixed_tg | 624 ms                                                                 | 621 ms: 1.00x faster                                                   |
| json_dumps                 | 14.5 ms                                                                | 14.5 ms: 1.00x faster                                                  |
| comprehensions             | 29.2 us                                                                | 29.1 us: 1.00x faster                                                  |
| 2to3                       | 377 ms                                                                 | 376 ms: 1.00x faster                                                   |
| deepcopy_reduce            | 3.74 us                                                                | 3.72 us: 1.00x faster                                                  |
| xml_etree_generate         | 102 ms                                                                 | 102 ms: 1.00x faster                                                   |
| xml_etree_process          | 82.2 ms                                                                | 81.9 ms: 1.00x faster                                                  |
| bench_mp_pool              | 110 ms                                                                 | 110 ms: 1.00x slower                                                   |
| sympy_str                  | 492 ms                                                                 | 493 ms: 1.00x slower                                                   |
| logging_silent             | 201 ns                                                                 | 202 ns: 1.00x slower                                                   |
| python_startup_no_site     | 10.2 ms                                                                | 10.3 ms: 1.00x slower                                                  |
| python_startup             | 17.4 ms                                                                | 17.5 ms: 1.01x slower                                                  |
| xml_etree_parse            | 129 ms                                                                 | 130 ms: 1.01x slower                                                   |
| float                      | 142 ms                                                                 | 143 ms: 1.01x slower                                                   |
| subparsers                 | 33.0 ms                                                                | 33.4 ms: 1.01x slower                                                  |
| sqlite_synth               | 2.31 us                                                                | 2.33 us: 1.01x slower                                                  |
| create_gc_cycles           | 1.82 ms                                                                | 1.87 ms: 1.02x slower                                                  |
| telco                      | 8.73 ms                                                                | 9.03 ms: 1.04x slower                                                  |
| gc_traversal               | 3.19 ms                                                                | 3.53 ms: 1.11x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (31): sqlalchemy_imperative, async_tree_memoization_tg, sqlglot_normalize, django_template, async_tree_io, json, sqlglot_optimize, pylint, xml_etree_iterparse, json_loads, sympy_expand, connected_components, scimark_sor, bench_thread_pool, dulwich_log, chaos, sympy_integrate, many_optionals, async_tree_io_tg, regex_v8, asyncio_websockets, mdp, async_tree_cpu_io_mixed, pathlib, scimark_lu, sqlglot_transpile, scimark_monte_carlo, sympy_sum, sqlglot_parse, nqueens, deltablue

- Geometric mean (including insignificant results): 1.007x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x