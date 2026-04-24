# Results vs. base

- fork: nascheme
- ref: ft_gc_threshold_fix_
- machine: linux-x86_64
- commit hash: ac09833
- commit date: 2026-04-23
- overall geometric mean: 1.007x slower
- HPT reliability: 64.96%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260423-vultr-x86_64-python-448d7b96c181d13ca7f8-3.15.0a8+-448d7b9 | bm-20260423-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-ac09833 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                                 | 287 ms: 1.02x slower                                                     |
| docutils       | 2.63 sec                                                               | 2.76 sec: 1.05x slower                                                   |
| html5lib       | 65.7 ms                                                                | 68.9 ms: 1.05x slower                                                    |
| sphinx         | 1.06 sec                                                               | 1.07 sec: 1.02x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20260423-vultr-x86_64-python-448d7b96c181d13ca7f8-3.15.0a8+-448d7b9 | bm-20260423-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-ac09833 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_generators           | 384 ms                                                                 | 379 ms: 1.01x faster                                                     |
| asyncio_websockets         | 510 ms                                                                 | 513 ms: 1.01x slower                                                     |
| async_tree_io              | 639 ms                                                                 | 650 ms: 1.02x slower                                                     |
| coroutines                 | 24.1 ms                                                                | 24.6 ms: 1.02x slower                                                    |
| async_tree_cpu_io_mixed_tg | 508 ms                                                                 | 545 ms: 1.07x slower                                                     |
| async_tree_cpu_io_mixed    | 531 ms                                                                 | 570 ms: 1.07x slower                                                     |
| async_tree_none            | 287 ms                                                                 | 309 ms: 1.08x slower                                                     |
| async_tree_io_tg           | 600 ms                                                                 | 646 ms: 1.08x slower                                                     |
| async_tree_memoization     | 352 ms                                                                 | 382 ms: 1.09x slower                                                     |
| async_tree_memoization_tg  | 324 ms                                                                 | 357 ms: 1.10x slower                                                     |
| async_tree_none_tg         | 258 ms                                                                 | 293 ms: 1.14x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.06x slower                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260423-vultr-x86_64-python-448d7b96c181d13ca7f8-3.15.0a8+-448d7b9 | bm-20260423-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-ac09833 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 183 ms                                                                 | 180 ms: 1.02x faster                                                     |
| nbody          | 123 ms                                                                 | 122 ms: 1.01x faster                                                     |
| float          | 74.7 ms                                                                | 77.9 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260423-vultr-x86_64-python-448d7b96c181d13ca7f8-3.15.0a8+-448d7b9 | bm-20260423-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-ac09833 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 183 ms                                                                 | 184 ms: 1.00x slower                                                     |
| regex_compile  | 140 ms                                                                 | 141 ms: 1.01x slower                                                     |
| regex_v8       | 21.2 ms                                                                | 21.5 ms: 1.01x slower                                                    |
| regex_effbot   | 3.01 ms                                                                | 3.06 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20260423-vultr-x86_64-python-448d7b96c181d13ca7f8-3.15.0a8+-448d7b9 | bm-20260423-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-ac09833 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_process    | 69.2 ms                                                                | 68.2 ms: 1.02x faster                                                    |
| xml_etree_generate   | 96.7 ms                                                                | 95.4 ms: 1.01x faster                                                    |
| json_loads           | 30.7 us                                                                | 30.4 us: 1.01x faster                                                    |
| unpickle_pure_python | 239 us                                                                 | 237 us: 1.01x faster                                                     |
| tomli_loads          | 1.93 sec                                                               | 1.92 sec: 1.01x faster                                                   |
| json_dumps           | 10.6 ms                                                                | 10.7 ms: 1.01x slower                                                    |
| xml_etree_parse      | 132 ms                                                                 | 134 ms: 1.01x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (2): pickle_pure_python, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20260423-vultr-x86_64-python-448d7b96c181d13ca7f8-3.15.0a8+-448d7b9 | bm-20260423-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-ac09833 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 9.17 ms                                                                | 8.95 ms: 1.02x faster                                                    |
| python_startup         | 15.7 ms                                                                | 15.5 ms: 1.02x faster                                                    |
| Geometric mean         | (ref)                                                                  | 1.02x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20260423-vultr-x86_64-python-448d7b96c181d13ca7f8-3.15.0a8+-448d7b9 | bm-20260423-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-ac09833 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 39.5 ms                                                                | 39.0 ms: 1.01x faster                                                    |
| genshi_xml      | 54.8 ms                                                                | 54.3 ms: 1.01x faster                                                    |
| genshi_text     | 25.5 ms                                                                | 25.7 ms: 1.01x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20260423-vultr-x86_64-python-448d7b96c181d13ca7f8-3.15.0a8+-448d7b9 | bm-20260423-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-ac09833 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| bench_mp_pool              | 8.50 ms                                                                | 7.27 ms: 1.17x faster                                                    |
| scimark_sor                | 123 ms                                                                 | 119 ms: 1.03x faster                                                     |
| scimark_lu                 | 127 ms                                                                 | 123 ms: 1.03x faster                                                     |
| scimark_fft                | 346 ms                                                                 | 337 ms: 1.03x faster                                                     |
| spectral_norm              | 114 ms                                                                 | 111 ms: 1.03x faster                                                     |
| python_startup_no_site     | 9.17 ms                                                                | 8.95 ms: 1.02x faster                                                    |
| nqueens                    | 88.2 ms                                                                | 86.3 ms: 1.02x faster                                                    |
| pyflate                    | 464 ms                                                                 | 454 ms: 1.02x faster                                                     |
| logging_format             | 7.85 us                                                                | 7.70 us: 1.02x faster                                                    |
| create_gc_cycles           | 1.52 ms                                                                | 1.49 ms: 1.02x faster                                                    |
| logging_simple             | 6.88 us                                                                | 6.76 us: 1.02x faster                                                    |
| python_startup             | 15.7 ms                                                                | 15.5 ms: 1.02x faster                                                    |
| pidigits                   | 183 ms                                                                 | 180 ms: 1.02x faster                                                     |
| xml_etree_process          | 69.2 ms                                                                | 68.2 ms: 1.02x faster                                                    |
| deepcopy_reduce            | 2.95 us                                                                | 2.91 us: 1.01x faster                                                    |
| gc_traversal               | 1.94 ms                                                                | 1.91 ms: 1.01x faster                                                    |
| async_generators           | 384 ms                                                                 | 379 ms: 1.01x faster                                                     |
| dulwich_log                | 70.6 ms                                                                | 69.6 ms: 1.01x faster                                                    |
| xml_etree_generate         | 96.7 ms                                                                | 95.4 ms: 1.01x faster                                                    |
| json_loads                 | 30.7 us                                                                | 30.4 us: 1.01x faster                                                    |
| django_template            | 39.5 ms                                                                | 39.0 ms: 1.01x faster                                                    |
| telco                      | 174 ms                                                                 | 172 ms: 1.01x faster                                                     |
| sympy_str                  | 315 ms                                                                 | 312 ms: 1.01x faster                                                     |
| thrift                     | 903 us                                                                 | 893 us: 1.01x faster                                                     |
| bpe_tokeniser              | 4.36 sec                                                               | 4.32 sec: 1.01x faster                                                   |
| sympy_expand               | 526 ms                                                                 | 520 ms: 1.01x faster                                                     |
| genshi_xml                 | 54.8 ms                                                                | 54.3 ms: 1.01x faster                                                    |
| unpickle_pure_python       | 239 us                                                                 | 237 us: 1.01x faster                                                     |
| tomli_loads                | 1.93 sec                                                               | 1.92 sec: 1.01x faster                                                   |
| hexiom                     | 6.55 ms                                                                | 6.49 ms: 1.01x faster                                                    |
| nbody                      | 123 ms                                                                 | 122 ms: 1.01x faster                                                     |
| generators                 | 32.2 ms                                                                | 32.0 ms: 1.01x faster                                                    |
| fannkuch                   | 461 ms                                                                 | 458 ms: 1.01x faster                                                     |
| sqlglot_v2_normalize       | 115 ms                                                                 | 114 ms: 1.01x faster                                                     |
| crypto_pyaes               | 87.6 ms                                                                | 87.1 ms: 1.01x faster                                                    |
| sqlglot_v2_optimize        | 56.7 ms                                                                | 56.4 ms: 1.01x faster                                                    |
| mdp                        | 1.31 sec                                                               | 1.31 sec: 1.01x faster                                                   |
| scimark_monte_carlo        | 77.8 ms                                                                | 77.4 ms: 1.01x faster                                                    |
| regex_dna                  | 183 ms                                                                 | 184 ms: 1.00x slower                                                     |
| chaos                      | 62.5 ms                                                                | 62.7 ms: 1.00x slower                                                    |
| go                         | 121 ms                                                                 | 121 ms: 1.01x slower                                                     |
| connected_components       | 493 ms                                                                 | 496 ms: 1.01x slower                                                     |
| asyncio_websockets         | 510 ms                                                                 | 513 ms: 1.01x slower                                                     |
| genshi_text                | 25.5 ms                                                                | 25.7 ms: 1.01x slower                                                    |
| richards_super             | 59.1 ms                                                                | 59.5 ms: 1.01x slower                                                    |
| pycparser                  | 1.11 sec                                                               | 1.12 sec: 1.01x slower                                                   |
| pprint_safe_repr           | 794 ms                                                                 | 800 ms: 1.01x slower                                                     |
| sympy_integrate            | 21.6 ms                                                                | 21.8 ms: 1.01x slower                                                    |
| pprint_pformat             | 1.64 sec                                                               | 1.66 sec: 1.01x slower                                                   |
| shortest_path              | 532 ms                                                                 | 537 ms: 1.01x slower                                                     |
| json_dumps                 | 10.6 ms                                                                | 10.7 ms: 1.01x slower                                                    |
| regex_compile              | 140 ms                                                                 | 141 ms: 1.01x slower                                                     |
| typing_runtime_protocols   | 192 us                                                                 | 194 us: 1.01x slower                                                     |
| regex_v8                   | 21.2 ms                                                                | 21.5 ms: 1.01x slower                                                    |
| meteor_contest             | 125 ms                                                                 | 127 ms: 1.01x slower                                                     |
| xml_etree_parse            | 132 ms                                                                 | 134 ms: 1.01x slower                                                     |
| comprehensions             | 17.3 us                                                                | 17.6 us: 1.02x slower                                                    |
| logging_silent             | 103 ns                                                                 | 104 ns: 1.02x slower                                                     |
| regex_effbot               | 3.01 ms                                                                | 3.06 ms: 1.02x slower                                                    |
| sphinx                     | 1.06 sec                                                               | 1.07 sec: 1.02x slower                                                   |
| subparsers                 | 10.1 ms                                                                | 10.3 ms: 1.02x slower                                                    |
| 2to3                       | 282 ms                                                                 | 287 ms: 1.02x slower                                                     |
| async_tree_io              | 639 ms                                                                 | 650 ms: 1.02x slower                                                     |
| deepcopy_memo              | 31.0 us                                                                | 31.5 us: 1.02x slower                                                    |
| coroutines                 | 24.1 ms                                                                | 24.6 ms: 1.02x slower                                                    |
| richards                   | 51.6 ms                                                                | 52.7 ms: 1.02x slower                                                    |
| deltablue                  | 3.52 ms                                                                | 3.64 ms: 1.03x slower                                                    |
| float                      | 74.7 ms                                                                | 77.9 ms: 1.04x slower                                                    |
| docutils                   | 2.63 sec                                                               | 2.76 sec: 1.05x slower                                                   |
| html5lib                   | 65.7 ms                                                                | 68.9 ms: 1.05x slower                                                    |
| async_tree_cpu_io_mixed_tg | 508 ms                                                                 | 545 ms: 1.07x slower                                                     |
| async_tree_cpu_io_mixed    | 531 ms                                                                 | 570 ms: 1.07x slower                                                     |
| async_tree_none            | 287 ms                                                                 | 309 ms: 1.08x slower                                                     |
| async_tree_io_tg           | 600 ms                                                                 | 646 ms: 1.08x slower                                                     |
| async_tree_memoization     | 352 ms                                                                 | 382 ms: 1.09x slower                                                     |
| pylint                     | 120 ms                                                                 | 131 ms: 1.09x slower                                                     |
| async_tree_memoization_tg  | 324 ms                                                                 | 357 ms: 1.10x slower                                                     |
| async_tree_none_tg         | 258 ms                                                                 | 293 ms: 1.14x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (16): json, bench_thread_pool, deepcopy, scimark_sparse_mat_mult, sqlite_synth, coverage, sympy_sum, k_core, mako, pickle_pure_python, xml_etree_iterparse, pathlib, raytrace, sqlglot_v2_parse, sqlglot_v2_transpile, many_optionals

- Geometric mean (including insignificant results): 1.007x slower

# HPT report

- Reliability score: 64.96% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.98x