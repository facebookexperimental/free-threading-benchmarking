# Results vs. base

- fork: nascheme
- ref: gh_115999_load_super
- machine: linux-x86_64
- commit hash: a515a0d
- commit date: 2024-11-25
- overall geometric mean: 1.175x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 409 ms                                                                 | 455 ms: 1.11x slower                                                     |
| docutils       | 3.31 sec                                                               | 3.33 sec: 1.01x slower                                                   |
| sphinx         | 1.27 sec                                                               | 1.45 sec: 1.14x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_generators           | 489 ms                                                                 | 480 ms: 1.02x faster                                                     |
| asyncio_websockets         | 521 ms                                                                 | 523 ms: 1.00x slower                                                     |
| coroutines                 | 29.6 ms                                                                | 29.7 ms: 1.00x slower                                                    |
| async_tree_cpu_io_mixed_tg | 646 ms                                                                 | 815 ms: 1.26x slower                                                     |
| async_tree_memoization_tg  | 478 ms                                                                 | 725 ms: 1.52x slower                                                     |
| async_tree_cpu_io_mixed    | 679 ms                                                                 | 1.08 sec: 1.60x slower                                                   |
| async_tree_none            | 412 ms                                                                 | 664 ms: 1.61x slower                                                     |
| async_tree_memoization     | 508 ms                                                                 | 998 ms: 1.97x slower                                                     |
| async_tree_io_tg           | 899 ms                                                                 | 3.36 sec: 3.73x slower                                                   |
| async_tree_io              | 921 ms                                                                 | 3.62 sec: 3.93x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.57x slower                                                             |

Benchmark hidden because not significant (1): async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 186 ms                                                                 | 199 ms: 1.07x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                             |

Benchmark hidden because not significant (2): float, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 189 ms                                                                 | 188 ms: 1.00x faster                                                     |
| regex_effbot   | 2.84 ms                                                                | 2.85 ms: 1.00x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (2): regex_compile, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_process    | 87.7 ms                                                                | 86.2 ms: 1.02x faster                                                    |
| unpickle_pure_python | 386 us                                                                 | 381 us: 1.01x faster                                                     |
| json_dumps           | 15.0 ms                                                                | 14.8 ms: 1.01x faster                                                    |
| xml_etree_generate   | 106 ms                                                                 | 107 ms: 1.00x slower                                                     |
| xml_etree_parse      | 131 ms                                                                 | 132 ms: 1.01x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (4): tomli_loads, pickle_pure_python, json_loads, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 10.3 ms                                                                | 11.3 ms: 1.09x slower                                                    |
| python_startup         | 17.6 ms                                                                | 20.3 ms: 1.15x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.12x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 36.8 ms                                                                | 36.2 ms: 1.01x faster                                                    |
| genshi_xml      | 75.0 ms                                                                | 74.5 ms: 1.01x faster                                                    |
| mako            | 20.0 ms                                                                | 20.1 ms: 1.00x slower                                                    |
| django_template | 59.5 ms                                                                | 61.8 ms: 1.04x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| meteor_contest             | 143 ms                                                                 | 139 ms: 1.03x faster                                                     |
| sqlglot_transpile          | 3.29 ms                                                                | 3.21 ms: 1.02x faster                                                    |
| coverage                   | 104 ms                                                                 | 102 ms: 1.02x faster                                                     |
| nqueens                    | 115 ms                                                                 | 112 ms: 1.02x faster                                                     |
| create_gc_cycles           | 1.85 ms                                                                | 1.81 ms: 1.02x faster                                                    |
| async_generators           | 489 ms                                                                 | 480 ms: 1.02x faster                                                     |
| xml_etree_process          | 87.7 ms                                                                | 86.2 ms: 1.02x faster                                                    |
| scimark_lu                 | 217 ms                                                                 | 213 ms: 1.02x faster                                                     |
| pycparser                  | 1.68 sec                                                               | 1.66 sec: 1.01x faster                                                   |
| genshi_text                | 36.8 ms                                                                | 36.2 ms: 1.01x faster                                                    |
| unpickle_pure_python       | 386 us                                                                 | 381 us: 1.01x faster                                                     |
| raytrace                   | 627 ms                                                                 | 619 ms: 1.01x faster                                                     |
| generators                 | 41.5 ms                                                                | 41.0 ms: 1.01x faster                                                    |
| json_dumps                 | 15.0 ms                                                                | 14.8 ms: 1.01x faster                                                    |
| hexiom                     | 11.8 ms                                                                | 11.7 ms: 1.01x faster                                                    |
| go                         | 291 ms                                                                 | 288 ms: 1.01x faster                                                     |
| sqlglot_parse              | 2.80 ms                                                                | 2.78 ms: 1.01x faster                                                    |
| scimark_monte_carlo        | 124 ms                                                                 | 123 ms: 1.01x faster                                                     |
| fannkuch                   | 566 ms                                                                 | 561 ms: 1.01x faster                                                     |
| genshi_xml                 | 75.0 ms                                                                | 74.5 ms: 1.01x faster                                                    |
| comprehensions             | 29.9 us                                                                | 29.7 us: 1.01x faster                                                    |
| sqlglot_optimize           | 80.7 ms                                                                | 80.2 ms: 1.01x faster                                                    |
| chaos                      | 119 ms                                                                 | 119 ms: 1.00x faster                                                     |
| regex_dna                  | 189 ms                                                                 | 188 ms: 1.00x faster                                                     |
| xml_etree_generate         | 106 ms                                                                 | 107 ms: 1.00x slower                                                     |
| k_core                     | 2.55 sec                                                               | 2.55 sec: 1.00x slower                                                   |
| regex_effbot               | 2.84 ms                                                                | 2.85 ms: 1.00x slower                                                    |
| bpe_tokeniser              | 5.72 sec                                                               | 5.74 sec: 1.00x slower                                                   |
| pyflate                    | 761 ms                                                                 | 763 ms: 1.00x slower                                                     |
| asyncio_websockets         | 521 ms                                                                 | 523 ms: 1.00x slower                                                     |
| mako                       | 20.0 ms                                                                | 20.1 ms: 1.00x slower                                                    |
| coroutines                 | 29.6 ms                                                                | 29.7 ms: 1.00x slower                                                    |
| pathlib                    | 21.0 ms                                                                | 21.1 ms: 1.01x slower                                                    |
| typing_runtime_protocols   | 221 us                                                                 | 222 us: 1.01x slower                                                     |
| docutils                   | 3.31 sec                                                               | 3.33 sec: 1.01x slower                                                   |
| pprint_pformat             | 2.41 sec                                                               | 2.43 sec: 1.01x slower                                                   |
| xml_etree_parse            | 131 ms                                                                 | 132 ms: 1.01x slower                                                     |
| spectral_norm              | 155 ms                                                                 | 157 ms: 1.01x slower                                                     |
| crypto_pyaes               | 106 ms                                                                 | 108 ms: 1.01x slower                                                     |
| deepcopy_memo              | 45.8 us                                                                | 46.4 us: 1.01x slower                                                    |
| scimark_sparse_mat_mult    | 5.93 ms                                                                | 6.02 ms: 1.02x slower                                                    |
| logging_silent             | 206 ns                                                                 | 209 ns: 1.02x slower                                                     |
| connected_components       | 519 ms                                                                 | 534 ms: 1.03x slower                                                     |
| scimark_fft                | 411 ms                                                                 | 427 ms: 1.04x slower                                                     |
| django_template            | 59.5 ms                                                                | 61.8 ms: 1.04x slower                                                    |
| gc_traversal               | 3.32 ms                                                                | 3.48 ms: 1.05x slower                                                    |
| pidigits                   | 186 ms                                                                 | 199 ms: 1.07x slower                                                     |
| python_startup_no_site     | 10.3 ms                                                                | 11.3 ms: 1.09x slower                                                    |
| 2to3                       | 409 ms                                                                 | 455 ms: 1.11x slower                                                     |
| sphinx                     | 1.27 sec                                                               | 1.45 sec: 1.14x slower                                                   |
| python_startup             | 17.6 ms                                                                | 20.3 ms: 1.15x slower                                                    |
| sympy_expand               | 1.02 sec                                                               | 1.25 sec: 1.22x slower                                                   |
| bench_thread_pool          | 3.47 ms                                                                | 4.32 ms: 1.25x slower                                                    |
| async_tree_cpu_io_mixed_tg | 646 ms                                                                 | 815 ms: 1.26x slower                                                     |
| sympy_integrate            | 32.2 ms                                                                | 42.2 ms: 1.31x slower                                                    |
| dulwich_log                | 102 ms                                                                 | 145 ms: 1.42x slower                                                     |
| sympy_sum                  | 372 ms                                                                 | 535 ms: 1.44x slower                                                     |
| async_tree_memoization_tg  | 478 ms                                                                 | 725 ms: 1.52x slower                                                     |
| pylint                     | 407 ms                                                                 | 642 ms: 1.58x slower                                                     |
| async_tree_cpu_io_mixed    | 679 ms                                                                 | 1.08 sec: 1.60x slower                                                   |
| async_tree_none            | 412 ms                                                                 | 664 ms: 1.61x slower                                                     |
| bench_mp_pool              | 110 ms                                                                 | 202 ms: 1.83x slower                                                     |
| sympy_str                  | 524 ms                                                                 | 1.01 sec: 1.93x slower                                                   |
| async_tree_memoization     | 508 ms                                                                 | 998 ms: 1.97x slower                                                     |
| many_optionals             | 1.39 ms                                                                | 3.29 ms: 2.36x slower                                                    |
| subparsers                 | 34.2 ms                                                                | 87.7 ms: 2.56x slower                                                    |
| async_tree_io_tg           | 899 ms                                                                 | 3.36 sec: 3.73x slower                                                   |
| async_tree_io              | 921 ms                                                                 | 3.62 sec: 3.93x slower                                                   |
| deltablue                  | 9.00 ms                                                                | 43.9 ms: 4.88x slower                                                    |
| mdp                        | 3.07 sec                                                               | 16.3 sec: 5.30x slower                                                   |
| thrift                     | 1.23 ms                                                                | 6.57 ms: 5.36x slower                                                    |
| richards_super             | 103 ms                                                                 | 1.82 sec: 17.69x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.21x slower                                                             |

Benchmark hidden because not significant (22): tomli_loads, scimark_sor, pickle_pure_python, sqlglot_normalize, json, regex_compile, deepcopy_reduce, json_loads, sqlite_synth, logging_format, xml_etree_iterparse, float, shortest_path, deepcopy, richards, pprint_safe_repr, html5lib, async_tree_none_tg, regex_v8, nbody, telco, logging_simple

- Geometric mean (including insignificant results): 1.175x slower
# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x