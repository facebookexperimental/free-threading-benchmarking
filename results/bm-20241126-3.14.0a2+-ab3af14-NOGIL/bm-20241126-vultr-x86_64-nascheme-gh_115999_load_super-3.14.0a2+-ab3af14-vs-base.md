# Results vs. base

- fork: nascheme
- ref: gh_115999_load_super
- machine: linux-x86_64
- commit hash: ab3af14
- commit date: 2024-11-26
- overall geometric mean: 1.004x faster
- HPT reliability: 99.76%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f | bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-ab3af14 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 409 ms                                                                 | 406 ms: 1.01x faster                                                     |
| docutils       | 3.31 sec                                                               | 3.29 sec: 1.01x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (2): html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f | bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-ab3af14 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_generators           | 489 ms                                                                 | 482 ms: 1.01x faster                                                     |
| coroutines                 | 29.6 ms                                                                | 29.2 ms: 1.01x faster                                                    |
| async_tree_io_tg           | 899 ms                                                                 | 893 ms: 1.01x faster                                                     |
| async_tree_memoization_tg  | 478 ms                                                                 | 480 ms: 1.01x slower                                                     |
| async_tree_cpu_io_mixed    | 679 ms                                                                 | 684 ms: 1.01x slower                                                     |
| async_tree_cpu_io_mixed_tg | 646 ms                                                                 | 657 ms: 1.02x slower                                                     |
| async_tree_none            | 412 ms                                                                 | 420 ms: 1.02x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (4): async_tree_io, asyncio_websockets, async_tree_memoization, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f | bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-ab3af14 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 201 ms                                                                 | 197 ms: 1.02x faster                                                     |
| pidigits       | 186 ms                                                                 | 183 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f | bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-ab3af14 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 2.84 ms                                                                | 2.86 ms: 1.00x slower                                                    |
| regex_dna      | 189 ms                                                                 | 191 ms: 1.01x slower                                                     |
| regex_v8       | 25.0 ms                                                                | 25.6 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f | bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-ab3af14 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 15.0 ms                                                                | 14.6 ms: 1.03x faster                                                    |
| xml_etree_process    | 87.7 ms                                                                | 86.5 ms: 1.01x faster                                                    |
| json_loads           | 28.6 us                                                                | 28.3 us: 1.01x faster                                                    |
| tomli_loads          | 3.07 sec                                                               | 3.05 sec: 1.01x faster                                                   |
| unpickle_pure_python | 386 us                                                                 | 383 us: 1.01x faster                                                     |
| xml_etree_parse      | 131 ms                                                                 | 131 ms: 1.00x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (3): pickle_pure_python, xml_etree_generate, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f | bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-ab3af14 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 10.3 ms                                                                | 10.3 ms: 1.01x faster                                                    |
| python_startup         | 17.6 ms                                                                | 17.5 ms: 1.00x faster                                                    |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f | bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-ab3af14 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 36.8 ms                                                                | 36.0 ms: 1.02x faster                                                    |
| django_template | 59.5 ms                                                                | 58.6 ms: 1.01x faster                                                    |
| mako            | 20.0 ms                                                                | 19.9 ms: 1.00x faster                                                    |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f | bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-ab3af14 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| richards_super             | 103 ms                                                                 | 94.8 ms: 1.08x faster                                                    |
| meteor_contest             | 143 ms                                                                 | 137 ms: 1.04x faster                                                     |
| deltablue                  | 9.00 ms                                                                | 8.72 ms: 1.03x faster                                                    |
| nqueens                    | 115 ms                                                                 | 112 ms: 1.03x faster                                                     |
| json_dumps                 | 15.0 ms                                                                | 14.6 ms: 1.03x faster                                                    |
| genshi_text                | 36.8 ms                                                                | 36.0 ms: 1.02x faster                                                    |
| fannkuch                   | 566 ms                                                                 | 555 ms: 1.02x faster                                                     |
| scimark_lu                 | 217 ms                                                                 | 212 ms: 1.02x faster                                                     |
| sqlglot_transpile          | 3.29 ms                                                                | 3.23 ms: 1.02x faster                                                    |
| nbody                      | 201 ms                                                                 | 197 ms: 1.02x faster                                                     |
| spectral_norm              | 155 ms                                                                 | 152 ms: 1.02x faster                                                     |
| create_gc_cycles           | 1.85 ms                                                                | 1.82 ms: 1.02x faster                                                    |
| pidigits                   | 186 ms                                                                 | 183 ms: 1.02x faster                                                     |
| async_generators           | 489 ms                                                                 | 482 ms: 1.01x faster                                                     |
| django_template            | 59.5 ms                                                                | 58.6 ms: 1.01x faster                                                    |
| pprint_safe_repr           | 1.16 sec                                                               | 1.15 sec: 1.01x faster                                                   |
| xml_etree_process          | 87.7 ms                                                                | 86.5 ms: 1.01x faster                                                    |
| coroutines                 | 29.6 ms                                                                | 29.2 ms: 1.01x faster                                                    |
| pycparser                  | 1.68 sec                                                               | 1.66 sec: 1.01x faster                                                   |
| pprint_pformat             | 2.41 sec                                                               | 2.38 sec: 1.01x faster                                                   |
| json_loads                 | 28.6 us                                                                | 28.3 us: 1.01x faster                                                    |
| deepcopy_reduce            | 3.98 us                                                                | 3.94 us: 1.01x faster                                                    |
| logging_simple             | 11.6 us                                                                | 11.5 us: 1.01x faster                                                    |
| many_optionals             | 1.39 ms                                                                | 1.38 ms: 1.01x faster                                                    |
| typing_runtime_protocols   | 221 us                                                                 | 218 us: 1.01x faster                                                     |
| hexiom                     | 11.8 ms                                                                | 11.7 ms: 1.01x faster                                                    |
| scimark_sor                | 274 ms                                                                 | 271 ms: 1.01x faster                                                     |
| sympy_str                  | 524 ms                                                                 | 519 ms: 1.01x faster                                                     |
| 2to3                       | 409 ms                                                                 | 406 ms: 1.01x faster                                                     |
| deepcopy                   | 382 us                                                                 | 379 us: 1.01x faster                                                     |
| tomli_loads                | 3.07 sec                                                               | 3.05 sec: 1.01x faster                                                   |
| json                       | 5.23 ms                                                                | 5.19 ms: 1.01x faster                                                    |
| unpickle_pure_python       | 386 us                                                                 | 383 us: 1.01x faster                                                     |
| generators                 | 41.5 ms                                                                | 41.2 ms: 1.01x faster                                                    |
| python_startup_no_site     | 10.3 ms                                                                | 10.3 ms: 1.01x faster                                                    |
| sympy_sum                  | 372 ms                                                                 | 370 ms: 1.01x faster                                                     |
| docutils                   | 3.31 sec                                                               | 3.29 sec: 1.01x faster                                                   |
| sympy_expand               | 1.02 sec                                                               | 1.02 sec: 1.01x faster                                                   |
| sympy_integrate            | 32.2 ms                                                                | 32.0 ms: 1.01x faster                                                    |
| async_tree_io_tg           | 899 ms                                                                 | 893 ms: 1.01x faster                                                     |
| shortest_path              | 577 ms                                                                 | 574 ms: 1.01x faster                                                     |
| bench_mp_pool              | 110 ms                                                                 | 110 ms: 1.01x faster                                                     |
| chaos                      | 119 ms                                                                 | 119 ms: 1.00x faster                                                     |
| python_startup             | 17.6 ms                                                                | 17.5 ms: 1.00x faster                                                    |
| mako                       | 20.0 ms                                                                | 19.9 ms: 1.00x faster                                                    |
| scimark_fft                | 411 ms                                                                 | 410 ms: 1.00x faster                                                     |
| k_core                     | 2.55 sec                                                               | 2.54 sec: 1.00x faster                                                   |
| xml_etree_parse            | 131 ms                                                                 | 131 ms: 1.00x slower                                                     |
| raytrace                   | 627 ms                                                                 | 630 ms: 1.00x slower                                                     |
| crypto_pyaes               | 106 ms                                                                 | 107 ms: 1.00x slower                                                     |
| regex_effbot               | 2.84 ms                                                                | 2.86 ms: 1.00x slower                                                    |
| comprehensions             | 29.9 us                                                                | 30.1 us: 1.00x slower                                                    |
| async_tree_memoization_tg  | 478 ms                                                                 | 480 ms: 1.01x slower                                                     |
| async_tree_cpu_io_mixed    | 679 ms                                                                 | 684 ms: 1.01x slower                                                     |
| pathlib                    | 21.0 ms                                                                | 21.2 ms: 1.01x slower                                                    |
| logging_format             | 12.8 us                                                                | 13.0 us: 1.01x slower                                                    |
| regex_dna                  | 189 ms                                                                 | 191 ms: 1.01x slower                                                     |
| pyflate                    | 761 ms                                                                 | 770 ms: 1.01x slower                                                     |
| scimark_sparse_mat_mult    | 5.93 ms                                                                | 6.00 ms: 1.01x slower                                                    |
| async_tree_cpu_io_mixed_tg | 646 ms                                                                 | 657 ms: 1.02x slower                                                     |
| async_tree_none            | 412 ms                                                                 | 420 ms: 1.02x slower                                                     |
| logging_silent             | 206 ns                                                                 | 210 ns: 1.02x slower                                                     |
| regex_v8                   | 25.0 ms                                                                | 25.6 ms: 1.02x slower                                                    |
| connected_components       | 519 ms                                                                 | 535 ms: 1.03x slower                                                     |
| mdp                        | 3.07 sec                                                               | 3.19 sec: 1.04x slower                                                   |
| gc_traversal               | 3.32 ms                                                                | 3.49 ms: 1.05x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (28): coverage, telco, sqlite_synth, pickle_pure_python, sqlglot_optimize, async_tree_io, float, regex_compile, sphinx, go, deepcopy_memo, sqlglot_parse, pylint, genshi_xml, bench_thread_pool, dulwich_log, asyncio_websockets, bpe_tokeniser, xml_etree_generate, subparsers, async_tree_memoization, thrift, xml_etree_iterparse, richards, scimark_monte_carlo, html5lib, async_tree_none_tg, sqlglot_normalize

- Geometric mean (including insignificant results): 1.004x faster

# HPT report

- Reliability score: 99.76% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x