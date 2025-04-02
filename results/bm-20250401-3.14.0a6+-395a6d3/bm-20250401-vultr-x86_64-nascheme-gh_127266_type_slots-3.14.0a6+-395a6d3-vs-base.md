# Results vs. base

- fork: nascheme
- ref: gh_127266_type_slots
- machine: linux-x86_64
- commit hash: 395a6d3
- commit date: 2025-04-01
- overall geometric mean: 1.005x faster
- HPT reliability: 98.65%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 249 ms                                                                 | 248 ms: 1.01x faster                                                     |
| docutils       | 2.53 sec                                                               | 2.51 sec: 1.01x faster                                                   |
| sphinx         | 979 ms                                                                 | 967 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 495 ms                                                                 | 491 ms: 1.01x faster                                                     |
| coroutines                 | 22.9 ms                                                                | 22.7 ms: 1.01x faster                                                    |
| async_tree_cpu_io_mixed    | 502 ms                                                                 | 499 ms: 1.01x faster                                                     |
| async_generators           | 326 ms                                                                 | 327 ms: 1.00x slower                                                     |
| async_tree_io              | 603 ms                                                                 | 610 ms: 1.01x slower                                                     |
| async_tree_none_tg         | 252 ms                                                                 | 256 ms: 1.02x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (5): async_tree_none, asyncio_websockets, async_tree_memoization_tg, async_tree_memoization, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 213 ms                                                                 | 196 ms: 1.09x faster                                                     |
| float          | 70.7 ms                                                                | 71.6 ms: 1.01x slower                                                    |
| nbody          | 94.1 ms                                                                | 97.2 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 2.86 ms                                                                | 2.61 ms: 1.09x faster                                                    |
| regex_dna      | 181 ms                                                                 | 167 ms: 1.08x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                             |

Benchmark hidden because not significant (2): regex_compile, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_loads           | 27.8 us                                                                | 27.0 us: 1.03x faster                                                    |
| pickle_pure_python   | 306 us                                                                 | 302 us: 1.01x faster                                                     |
| xml_etree_iterparse  | 92.0 ms                                                                | 91.3 ms: 1.01x faster                                                    |
| unpickle_pure_python | 212 us                                                                 | 211 us: 1.01x faster                                                     |
| xml_etree_generate   | 83.3 ms                                                                | 83.8 ms: 1.01x slower                                                    |
| tomli_loads          | 1.91 sec                                                               | 1.94 sec: 1.02x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (3): json_dumps, xml_etree_process, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 8.64 ms                                                                | 8.58 ms: 1.01x faster                                                    |
| python_startup         | 15.0 ms                                                                | 14.9 ms: 1.00x faster                                                    |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako           | 11.9 ms                                                                | 11.8 ms: 1.01x faster                                                    |
| genshi_xml     | 47.4 ms                                                                | 47.7 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (2): genshi_text, django_template

All benchmarks:
===============

| Benchmark                  | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot               | 2.86 ms                                                                | 2.61 ms: 1.09x faster                                                    |
| pidigits                   | 213 ms                                                                 | 196 ms: 1.09x faster                                                     |
| regex_dna                  | 181 ms                                                                 | 167 ms: 1.08x faster                                                     |
| typing_runtime_protocols   | 156 us                                                                 | 151 us: 1.03x faster                                                     |
| json_loads                 | 27.8 us                                                                | 27.0 us: 1.03x faster                                                    |
| scimark_lu                 | 113 ms                                                                 | 110 ms: 1.03x faster                                                     |
| json                       | 4.95 ms                                                                | 4.82 ms: 1.03x faster                                                    |
| telco                      | 7.43 ms                                                                | 7.26 ms: 1.02x faster                                                    |
| deepcopy_reduce            | 2.66 us                                                                | 2.61 us: 1.02x faster                                                    |
| sympy_sum                  | 155 ms                                                                 | 152 ms: 1.02x faster                                                     |
| sqlglot_v2_normalize       | 102 ms                                                                 | 100 ms: 1.02x faster                                                     |
| richards_super             | 47.2 ms                                                                | 46.4 ms: 1.02x faster                                                    |
| logging_silent             | 93.6 ns                                                                | 92.1 ns: 1.02x faster                                                    |
| pprint_pformat             | 1.45 sec                                                               | 1.43 sec: 1.02x faster                                                   |
| pprint_safe_repr           | 712 ms                                                                 | 702 ms: 1.01x faster                                                     |
| coverage                   | 79.9 ms                                                                | 78.8 ms: 1.01x faster                                                    |
| sphinx                     | 979 ms                                                                 | 967 ms: 1.01x faster                                                     |
| sqlglot_v2_optimize        | 51.7 ms                                                                | 51.1 ms: 1.01x faster                                                    |
| sqlalchemy_imperative      | 19.4 ms                                                                | 19.2 ms: 1.01x faster                                                    |
| mako                       | 11.9 ms                                                                | 11.8 ms: 1.01x faster                                                    |
| pickle_pure_python         | 306 us                                                                 | 302 us: 1.01x faster                                                     |
| deepcopy                   | 256 us                                                                 | 253 us: 1.01x faster                                                     |
| sympy_integrate            | 19.0 ms                                                                | 18.8 ms: 1.01x faster                                                    |
| async_tree_cpu_io_mixed_tg | 495 ms                                                                 | 491 ms: 1.01x faster                                                     |
| coroutines                 | 22.9 ms                                                                | 22.7 ms: 1.01x faster                                                    |
| create_gc_cycles           | 1.87 ms                                                                | 1.85 ms: 1.01x faster                                                    |
| xml_etree_iterparse        | 92.0 ms                                                                | 91.3 ms: 1.01x faster                                                    |
| sqlalchemy_declarative     | 128 ms                                                                 | 127 ms: 1.01x faster                                                     |
| bench_mp_pool              | 89.0 ms                                                                | 88.4 ms: 1.01x faster                                                    |
| python_startup_no_site     | 8.64 ms                                                                | 8.58 ms: 1.01x faster                                                    |
| crypto_pyaes               | 68.1 ms                                                                | 67.7 ms: 1.01x faster                                                    |
| deltablue                  | 2.99 ms                                                                | 2.97 ms: 1.01x faster                                                    |
| sympy_str                  | 271 ms                                                                 | 269 ms: 1.01x faster                                                     |
| docutils                   | 2.53 sec                                                               | 2.51 sec: 1.01x faster                                                   |
| dulwich_log                | 65.9 ms                                                                | 65.5 ms: 1.01x faster                                                    |
| unpickle_pure_python       | 212 us                                                                 | 211 us: 1.01x faster                                                     |
| 2to3                       | 249 ms                                                                 | 248 ms: 1.01x faster                                                     |
| richards                   | 41.1 ms                                                                | 40.9 ms: 1.01x faster                                                    |
| scimark_sor                | 113 ms                                                                 | 112 ms: 1.01x faster                                                     |
| async_tree_cpu_io_mixed    | 502 ms                                                                 | 499 ms: 1.01x faster                                                     |
| sqlglot_v2_transpile       | 1.53 ms                                                                | 1.52 ms: 1.01x faster                                                    |
| many_optionals             | 1.03 ms                                                                | 1.02 ms: 1.00x faster                                                    |
| python_startup             | 15.0 ms                                                                | 14.9 ms: 1.00x faster                                                    |
| deepcopy_memo              | 29.6 us                                                                | 29.4 us: 1.00x faster                                                    |
| sqlglot_v2_parse           | 1.23 ms                                                                | 1.22 ms: 1.00x faster                                                    |
| raytrace                   | 256 ms                                                                 | 255 ms: 1.00x faster                                                     |
| scimark_fft                | 321 ms                                                                 | 320 ms: 1.00x faster                                                     |
| async_generators           | 326 ms                                                                 | 327 ms: 1.00x slower                                                     |
| bpe_tokeniser              | 4.23 sec                                                               | 4.25 sec: 1.00x slower                                                   |
| logging_simple             | 5.96 us                                                                | 6.00 us: 1.01x slower                                                    |
| genshi_xml                 | 47.4 ms                                                                | 47.7 ms: 1.01x slower                                                    |
| xml_etree_generate         | 83.3 ms                                                                | 83.8 ms: 1.01x slower                                                    |
| mdp                        | 1.16 sec                                                               | 1.17 sec: 1.01x slower                                                   |
| spectral_norm              | 92.8 ms                                                                | 93.6 ms: 1.01x slower                                                    |
| pathlib                    | 19.0 ms                                                                | 19.2 ms: 1.01x slower                                                    |
| fannkuch                   | 387 ms                                                                 | 391 ms: 1.01x slower                                                     |
| async_tree_io              | 603 ms                                                                 | 610 ms: 1.01x slower                                                     |
| float                      | 70.7 ms                                                                | 71.6 ms: 1.01x slower                                                    |
| async_tree_none_tg         | 252 ms                                                                 | 256 ms: 1.02x slower                                                     |
| go                         | 109 ms                                                                 | 111 ms: 1.02x slower                                                     |
| hexiom                     | 5.77 ms                                                                | 5.86 ms: 1.02x slower                                                    |
| nqueens                    | 76.7 ms                                                                | 77.9 ms: 1.02x slower                                                    |
| tomli_loads                | 1.91 sec                                                               | 1.94 sec: 1.02x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                                | 4.49 ms: 1.02x slower                                                    |
| nbody                      | 94.1 ms                                                                | 97.2 ms: 1.03x slower                                                    |
| gc_traversal               | 4.36 ms                                                                | 4.60 ms: 1.05x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (28): pylint, connected_components, logging_format, sympy_expand, async_tree_none, genshi_text, pycparser, k_core, subparsers, pyflate, django_template, asyncio_websockets, bench_thread_pool, json_dumps, regex_compile, comprehensions, shortest_path, sqlite_synth, scimark_monte_carlo, chaos, meteor_contest, async_tree_memoization_tg, xml_etree_process, async_tree_memoization, xml_etree_parse, generators, async_tree_io_tg, regex_v8

- Geometric mean (including insignificant results): 1.005x faster

# HPT report

- Reliability score: 98.65% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x