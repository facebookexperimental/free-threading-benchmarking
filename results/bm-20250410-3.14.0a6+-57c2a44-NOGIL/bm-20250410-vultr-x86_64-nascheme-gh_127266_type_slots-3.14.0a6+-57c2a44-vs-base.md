# Results vs. base

- fork: nascheme
- ref: gh_127266_type_slots
- machine: linux-x86_64
- commit hash: 57c2a44
- commit date: 2025-04-10
- overall geometric mean: 1.007x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250410-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-57c2a44 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 313 ms                                                                 | 316 ms: 1.01x slower                                                     |
| docutils       | 2.89 sec                                                               | 2.91 sec: 1.01x slower                                                   |
| html5lib       | 75.4 ms                                                                | 76.9 ms: 1.02x slower                                                    |
| sphinx         | 1.15 sec                                                               | 1.15 sec: 1.00x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250410-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-57c2a44 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| coroutines                 | 25.9 ms                                                                | 25.6 ms: 1.01x faster                                                    |
| async_tree_io_tg           | 577 ms                                                                 | 580 ms: 1.01x slower                                                     |
| async_generators           | 387 ms                                                                 | 389 ms: 1.01x slower                                                     |
| async_tree_io              | 608 ms                                                                 | 613 ms: 1.01x slower                                                     |
| async_tree_memoization     | 346 ms                                                                 | 349 ms: 1.01x slower                                                     |
| async_tree_cpu_io_mixed    | 532 ms                                                                 | 551 ms: 1.03x slower                                                     |
| async_tree_cpu_io_mixed_tg | 501 ms                                                                 | 520 ms: 1.04x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (4): async_tree_none, async_tree_none_tg, asyncio_websockets, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250410-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-57c2a44 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 215 ms                                                                 | 202 ms: 1.06x faster                                                     |
| nbody          | 149 ms                                                                 | 152 ms: 1.02x slower                                                     |
| float          | 81.8 ms                                                                | 84.0 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250410-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-57c2a44 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 22.2 ms                                                                | 21.1 ms: 1.05x faster                                                    |
| regex_effbot   | 2.84 ms                                                                | 2.77 ms: 1.03x faster                                                    |
| regex_dna      | 179 ms                                                                 | 181 ms: 1.01x slower                                                     |
| regex_compile  | 170 ms                                                                 | 173 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250410-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-57c2a44 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 13.2 ms                                                                | 13.1 ms: 1.01x faster                                                    |
| xml_etree_parse      | 131 ms                                                                 | 130 ms: 1.01x faster                                                     |
| xml_etree_generate   | 101 ms                                                                 | 102 ms: 1.00x slower                                                     |
| xml_etree_iterparse  | 92.5 ms                                                                | 92.9 ms: 1.00x slower                                                    |
| tomli_loads          | 2.58 sec                                                               | 2.62 sec: 1.02x slower                                                   |
| unpickle_pure_python | 277 us                                                                 | 282 us: 1.02x slower                                                     |
| pickle_pure_python   | 388 us                                                                 | 399 us: 1.03x slower                                                     |
| json_loads           | 30.0 us                                                                | 30.9 us: 1.03x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250410-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-57c2a44 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 15.9 ms                                                                | 15.9 ms: 1.00x faster                                                    |
| python_startup_no_site | 11.2 ms                                                                | 11.2 ms: 1.00x faster                                                    |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250410-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-57c2a44 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 44.9 ms                                                                | 45.4 ms: 1.01x slower                                                    |
| mako            | 16.4 ms                                                                | 16.6 ms: 1.01x slower                                                    |
| genshi_xml      | 66.6 ms                                                                | 67.4 ms: 1.01x slower                                                    |
| genshi_text     | 30.2 ms                                                                | 31.6 ms: 1.05x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.02x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250410-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-57c2a44 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits                   | 215 ms                                                                 | 202 ms: 1.06x faster                                                     |
| regex_v8                   | 22.2 ms                                                                | 21.1 ms: 1.05x faster                                                    |
| scimark_sparse_mat_mult    | 6.24 ms                                                                | 6.04 ms: 1.03x faster                                                    |
| regex_effbot               | 2.84 ms                                                                | 2.77 ms: 1.03x faster                                                    |
| pathlib                    | 20.1 ms                                                                | 19.8 ms: 1.02x faster                                                    |
| coroutines                 | 25.9 ms                                                                | 25.6 ms: 1.01x faster                                                    |
| nqueens                    | 103 ms                                                                 | 102 ms: 1.01x faster                                                     |
| json_dumps                 | 13.2 ms                                                                | 13.1 ms: 1.01x faster                                                    |
| typing_runtime_protocols   | 209 us                                                                 | 206 us: 1.01x faster                                                     |
| mdp                        | 1.47 sec                                                               | 1.46 sec: 1.01x faster                                                   |
| scimark_fft                | 415 ms                                                                 | 412 ms: 1.01x faster                                                     |
| crypto_pyaes               | 94.6 ms                                                                | 94.0 ms: 1.01x faster                                                    |
| xml_etree_parse            | 131 ms                                                                 | 130 ms: 1.01x faster                                                     |
| python_startup             | 15.9 ms                                                                | 15.9 ms: 1.00x faster                                                    |
| python_startup_no_site     | 11.2 ms                                                                | 11.2 ms: 1.00x faster                                                    |
| comprehensions             | 22.4 us                                                                | 22.5 us: 1.00x slower                                                    |
| xml_etree_generate         | 101 ms                                                                 | 102 ms: 1.00x slower                                                     |
| sphinx                     | 1.15 sec                                                               | 1.15 sec: 1.00x slower                                                   |
| bpe_tokeniser              | 5.00 sec                                                               | 5.02 sec: 1.00x slower                                                   |
| deepcopy                   | 337 us                                                                 | 339 us: 1.00x slower                                                     |
| xml_etree_iterparse        | 92.5 ms                                                                | 92.9 ms: 1.00x slower                                                    |
| pprint_pformat             | 1.86 sec                                                               | 1.87 sec: 1.00x slower                                                   |
| pprint_safe_repr           | 896 ms                                                                 | 901 ms: 1.01x slower                                                     |
| many_optionals             | 1.23 ms                                                                | 1.23 ms: 1.01x slower                                                    |
| async_tree_io_tg           | 577 ms                                                                 | 580 ms: 1.01x slower                                                     |
| docutils                   | 2.89 sec                                                               | 2.91 sec: 1.01x slower                                                   |
| async_generators           | 387 ms                                                                 | 389 ms: 1.01x slower                                                     |
| sympy_sum                  | 194 ms                                                                 | 196 ms: 1.01x slower                                                     |
| logging_simple             | 8.33 us                                                                | 8.40 us: 1.01x slower                                                    |
| sympy_integrate            | 24.4 ms                                                                | 24.6 ms: 1.01x slower                                                    |
| spectral_norm              | 121 ms                                                                 | 122 ms: 1.01x slower                                                     |
| async_tree_io              | 608 ms                                                                 | 613 ms: 1.01x slower                                                     |
| telco                      | 8.92 ms                                                                | 9.00 ms: 1.01x slower                                                    |
| scimark_sor                | 164 ms                                                                 | 165 ms: 1.01x slower                                                     |
| gc_traversal               | 1.79 ms                                                                | 1.81 ms: 1.01x slower                                                    |
| async_tree_memoization     | 346 ms                                                                 | 349 ms: 1.01x slower                                                     |
| dulwich_log                | 76.9 ms                                                                | 77.7 ms: 1.01x slower                                                    |
| pycparser                  | 1.25 sec                                                               | 1.26 sec: 1.01x slower                                                   |
| 2to3                       | 313 ms                                                                 | 316 ms: 1.01x slower                                                     |
| django_template            | 44.9 ms                                                                | 45.4 ms: 1.01x slower                                                    |
| fannkuch                   | 536 ms                                                                 | 542 ms: 1.01x slower                                                     |
| mako                       | 16.4 ms                                                                | 16.6 ms: 1.01x slower                                                    |
| sqlglot_v2_optimize        | 64.8 ms                                                                | 65.6 ms: 1.01x slower                                                    |
| genshi_xml                 | 66.6 ms                                                                | 67.4 ms: 1.01x slower                                                    |
| coverage                   | 109 ms                                                                 | 111 ms: 1.01x slower                                                     |
| sqlglot_v2_normalize       | 129 ms                                                                 | 131 ms: 1.01x slower                                                     |
| hexiom                     | 8.15 ms                                                                | 8.25 ms: 1.01x slower                                                    |
| regex_dna                  | 179 ms                                                                 | 181 ms: 1.01x slower                                                     |
| deepcopy_reduce            | 3.40 us                                                                | 3.45 us: 1.02x slower                                                    |
| regex_compile              | 170 ms                                                                 | 173 ms: 1.02x slower                                                     |
| chaos                      | 75.9 ms                                                                | 77.2 ms: 1.02x slower                                                    |
| tomli_loads                | 2.58 sec                                                               | 2.62 sec: 1.02x slower                                                   |
| meteor_contest             | 138 ms                                                                 | 140 ms: 1.02x slower                                                     |
| raytrace                   | 350 ms                                                                 | 356 ms: 1.02x slower                                                     |
| logging_format             | 9.30 us                                                                | 9.47 us: 1.02x slower                                                    |
| nbody                      | 149 ms                                                                 | 152 ms: 1.02x slower                                                     |
| html5lib                   | 75.4 ms                                                                | 76.9 ms: 1.02x slower                                                    |
| unpickle_pure_python       | 277 us                                                                 | 282 us: 1.02x slower                                                     |
| create_gc_cycles           | 1.36 ms                                                                | 1.39 ms: 1.02x slower                                                    |
| richards_super             | 68.5 ms                                                                | 70.1 ms: 1.02x slower                                                    |
| pyflate                    | 541 ms                                                                 | 553 ms: 1.02x slower                                                     |
| go                         | 157 ms                                                                 | 161 ms: 1.02x slower                                                     |
| sqlglot_v2_transpile       | 2.06 ms                                                                | 2.11 ms: 1.03x slower                                                    |
| float                      | 81.8 ms                                                                | 84.0 ms: 1.03x slower                                                    |
| pickle_pure_python         | 388 us                                                                 | 399 us: 1.03x slower                                                     |
| json_loads                 | 30.0 us                                                                | 30.9 us: 1.03x slower                                                    |
| sqlglot_v2_parse           | 1.70 ms                                                                | 1.75 ms: 1.03x slower                                                    |
| json                       | 5.16 ms                                                                | 5.32 ms: 1.03x slower                                                    |
| scimark_lu                 | 148 ms                                                                 | 153 ms: 1.03x slower                                                     |
| richards                   | 60.1 ms                                                                | 62.1 ms: 1.03x slower                                                    |
| deltablue                  | 4.49 ms                                                                | 4.64 ms: 1.03x slower                                                    |
| async_tree_cpu_io_mixed    | 532 ms                                                                 | 551 ms: 1.03x slower                                                     |
| async_tree_cpu_io_mixed_tg | 501 ms                                                                 | 520 ms: 1.04x slower                                                     |
| genshi_text                | 30.2 ms                                                                | 31.6 ms: 1.05x slower                                                    |
| logging_silent             | 124 ns                                                                 | 131 ns: 1.06x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (20): async_tree_none, k_core, bench_thread_pool, xml_etree_process, scimark_monte_carlo, generators, shortest_path, sqlite_synth, async_tree_none_tg, deepcopy_memo, bench_mp_pool, sympy_str, sqlalchemy_declarative, sympy_expand, subparsers, asyncio_websockets, sqlalchemy_imperative, async_tree_memoization_tg, connected_components, pylint

- Geometric mean (including insignificant results): 1.007x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.99x