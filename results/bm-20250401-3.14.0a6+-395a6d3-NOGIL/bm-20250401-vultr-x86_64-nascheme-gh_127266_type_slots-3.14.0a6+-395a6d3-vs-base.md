# Results vs. base

- fork: nascheme
- ref: gh_127266_type_slots
- machine: linux-x86_64
- commit hash: 395a6d3
- commit date: 2025-04-01
- overall geometric mean: 1.001x faster
- HPT reliability: 50.32%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 313 ms                                                                 | 314 ms: 1.00x slower                                                     |
| html5lib       | 75.4 ms                                                                | 73.7 ms: 1.02x faster                                                    |
| sphinx         | 1.15 sec                                                               | 1.15 sec: 1.00x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| coroutines                 | 25.9 ms                                                                | 25.1 ms: 1.03x faster                                                    |
| async_tree_cpu_io_mixed    | 532 ms                                                                 | 521 ms: 1.02x faster                                                     |
| async_tree_cpu_io_mixed_tg | 501 ms                                                                 | 491 ms: 1.02x faster                                                     |
| async_tree_none_tg         | 255 ms                                                                 | 251 ms: 1.02x faster                                                     |
| async_tree_none            | 292 ms                                                                 | 288 ms: 1.01x faster                                                     |
| async_tree_io              | 608 ms                                                                 | 604 ms: 1.01x faster                                                     |
| async_tree_io_tg           | 577 ms                                                                 | 574 ms: 1.01x faster                                                     |
| async_generators           | 387 ms                                                                 | 388 ms: 1.00x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (3): async_tree_memoization_tg, async_tree_memoization, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 215 ms                                                                 | 195 ms: 1.10x faster                                                     |
| nbody          | 149 ms                                                                 | 148 ms: 1.01x faster                                                     |
| float          | 81.8 ms                                                                | 81.3 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 179 ms                                                                 | 173 ms: 1.04x faster                                                     |
| regex_effbot   | 2.84 ms                                                                | 2.77 ms: 1.03x faster                                                    |
| regex_v8       | 22.2 ms                                                                | 21.8 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                             |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 13.2 ms                                                                | 13.1 ms: 1.01x faster                                                    |
| tomli_loads          | 2.58 sec                                                               | 2.56 sec: 1.01x faster                                                   |
| unpickle_pure_python | 277 us                                                                 | 279 us: 1.01x slower                                                     |
| xml_etree_generate   | 101 ms                                                                 | 102 ms: 1.01x slower                                                     |
| xml_etree_iterparse  | 92.5 ms                                                                | 93.6 ms: 1.01x slower                                                    |
| pickle_pure_python   | 388 us                                                                 | 393 us: 1.01x slower                                                     |
| json_loads           | 30.0 us                                                                | 30.7 us: 1.02x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 15.9 ms                                                                | 15.8 ms: 1.01x faster                                                    |
| python_startup_no_site | 11.2 ms                                                                | 11.1 ms: 1.01x faster                                                    |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 66.6 ms                                                                | 66.4 ms: 1.00x faster                                                    |
| mako            | 16.4 ms                                                                | 16.5 ms: 1.00x slower                                                    |
| django_template | 44.9 ms                                                                | 45.1 ms: 1.00x slower                                                    |
| genshi_text     | 30.2 ms                                                                | 31.0 ms: 1.03x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits                   | 215 ms                                                                 | 195 ms: 1.10x faster                                                     |
| regex_dna                  | 179 ms                                                                 | 173 ms: 1.04x faster                                                     |
| coroutines                 | 25.9 ms                                                                | 25.1 ms: 1.03x faster                                                    |
| regex_effbot               | 2.84 ms                                                                | 2.77 ms: 1.03x faster                                                    |
| html5lib                   | 75.4 ms                                                                | 73.7 ms: 1.02x faster                                                    |
| scimark_sparse_mat_mult    | 6.24 ms                                                                | 6.10 ms: 1.02x faster                                                    |
| async_tree_cpu_io_mixed    | 532 ms                                                                 | 521 ms: 1.02x faster                                                     |
| regex_v8                   | 22.2 ms                                                                | 21.8 ms: 1.02x faster                                                    |
| pathlib                    | 20.1 ms                                                                | 19.7 ms: 1.02x faster                                                    |
| async_tree_cpu_io_mixed_tg | 501 ms                                                                 | 491 ms: 1.02x faster                                                     |
| async_tree_none_tg         | 255 ms                                                                 | 251 ms: 1.02x faster                                                     |
| async_tree_none            | 292 ms                                                                 | 288 ms: 1.01x faster                                                     |
| scimark_fft                | 415 ms                                                                 | 411 ms: 1.01x faster                                                     |
| chaos                      | 75.9 ms                                                                | 75.2 ms: 1.01x faster                                                    |
| json_dumps                 | 13.2 ms                                                                | 13.1 ms: 1.01x faster                                                    |
| spectral_norm              | 121 ms                                                                 | 120 ms: 1.01x faster                                                     |
| python_startup             | 15.9 ms                                                                | 15.8 ms: 1.01x faster                                                    |
| deepcopy_reduce            | 3.40 us                                                                | 3.37 us: 1.01x faster                                                    |
| python_startup_no_site     | 11.2 ms                                                                | 11.1 ms: 1.01x faster                                                    |
| nbody                      | 149 ms                                                                 | 148 ms: 1.01x faster                                                     |
| tomli_loads                | 2.58 sec                                                               | 2.56 sec: 1.01x faster                                                   |
| float                      | 81.8 ms                                                                | 81.3 ms: 1.01x faster                                                    |
| async_tree_io              | 608 ms                                                                 | 604 ms: 1.01x faster                                                     |
| bench_mp_pool              | 98.5 ms                                                                | 97.9 ms: 1.01x faster                                                    |
| async_tree_io_tg           | 577 ms                                                                 | 574 ms: 1.01x faster                                                     |
| scimark_monte_carlo        | 91.3 ms                                                                | 90.9 ms: 1.00x faster                                                    |
| crypto_pyaes               | 94.6 ms                                                                | 94.3 ms: 1.00x faster                                                    |
| genshi_xml                 | 66.6 ms                                                                | 66.4 ms: 1.00x faster                                                    |
| mdp                        | 1.47 sec                                                               | 1.47 sec: 1.00x faster                                                   |
| pprint_pformat             | 1.86 sec                                                               | 1.86 sec: 1.00x faster                                                   |
| bench_thread_pool          | 3.20 ms                                                                | 3.20 ms: 1.00x faster                                                    |
| 2to3                       | 313 ms                                                                 | 314 ms: 1.00x slower                                                     |
| deepcopy                   | 337 us                                                                 | 338 us: 1.00x slower                                                     |
| mako                       | 16.4 ms                                                                | 16.5 ms: 1.00x slower                                                    |
| sphinx                     | 1.15 sec                                                               | 1.15 sec: 1.00x slower                                                   |
| async_generators           | 387 ms                                                                 | 388 ms: 1.00x slower                                                     |
| sympy_integrate            | 24.4 ms                                                                | 24.5 ms: 1.00x slower                                                    |
| django_template            | 44.9 ms                                                                | 45.1 ms: 1.00x slower                                                    |
| dulwich_log                | 76.9 ms                                                                | 77.3 ms: 1.01x slower                                                    |
| telco                      | 8.92 ms                                                                | 8.97 ms: 1.01x slower                                                    |
| many_optionals             | 1.23 ms                                                                | 1.23 ms: 1.01x slower                                                    |
| richards_super             | 68.5 ms                                                                | 68.9 ms: 1.01x slower                                                    |
| unpickle_pure_python       | 277 us                                                                 | 279 us: 1.01x slower                                                     |
| bpe_tokeniser              | 5.00 sec                                                               | 5.03 sec: 1.01x slower                                                   |
| sympy_sum                  | 194 ms                                                                 | 195 ms: 1.01x slower                                                     |
| xml_etree_generate         | 101 ms                                                                 | 102 ms: 1.01x slower                                                     |
| coverage                   | 109 ms                                                                 | 110 ms: 1.01x slower                                                     |
| raytrace                   | 350 ms                                                                 | 353 ms: 1.01x slower                                                     |
| sqlglot_v2_transpile       | 2.06 ms                                                                | 2.08 ms: 1.01x slower                                                    |
| scimark_sor                | 164 ms                                                                 | 165 ms: 1.01x slower                                                     |
| sympy_expand               | 588 ms                                                                 | 595 ms: 1.01x slower                                                     |
| sympy_str                  | 351 ms                                                                 | 355 ms: 1.01x slower                                                     |
| logging_format             | 9.30 us                                                                | 9.41 us: 1.01x slower                                                    |
| xml_etree_iterparse        | 92.5 ms                                                                | 93.6 ms: 1.01x slower                                                    |
| pycparser                  | 1.25 sec                                                               | 1.27 sec: 1.01x slower                                                   |
| pickle_pure_python         | 388 us                                                                 | 393 us: 1.01x slower                                                     |
| deltablue                  | 4.49 ms                                                                | 4.55 ms: 1.01x slower                                                    |
| sqlglot_v2_optimize        | 64.8 ms                                                                | 65.8 ms: 1.01x slower                                                    |
| richards                   | 60.1 ms                                                                | 61.0 ms: 1.01x slower                                                    |
| sqlglot_v2_normalize       | 129 ms                                                                 | 131 ms: 1.02x slower                                                     |
| logging_silent             | 124 ns                                                                 | 126 ns: 1.02x slower                                                     |
| json_loads                 | 30.0 us                                                                | 30.7 us: 1.02x slower                                                    |
| genshi_text                | 30.2 ms                                                                | 31.0 ms: 1.03x slower                                                    |
| scimark_lu                 | 148 ms                                                                 | 153 ms: 1.03x slower                                                     |
| json                       | 5.16 ms                                                                | 5.34 ms: 1.04x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (30): async_tree_memoization_tg, xml_etree_parse, shortest_path, logging_simple, async_tree_memoization, deepcopy_memo, k_core, nqueens, connected_components, comprehensions, typing_runtime_protocols, meteor_contest, hexiom, pprint_safe_repr, fannkuch, sqlalchemy_declarative, regex_compile, create_gc_cycles, generators, docutils, pyflate, sqlalchemy_imperative, gc_traversal, xml_etree_process, go, asyncio_websockets, sqlglot_v2_parse, sqlite_synth, subparsers, pylint

- Geometric mean (including insignificant results): 1.001x faster

# HPT report

- Reliability score: 50.32% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.99x