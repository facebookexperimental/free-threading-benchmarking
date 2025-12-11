# Results vs. 3.13.0rc2

- fork: colesbury
- ref: gh_142472_stackrefs
- machine: linux-x86_64
- commit hash: 7cfe81b
- commit date: 2025-12-11
- overall geometric mean: 1.039x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251211-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-7cfe81b |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 248 ms: 1.05x faster                                                     |
| docutils       | 2.62 sec                                                     | 2.57 sec: 1.02x faster                                                   |
| html5lib       | 67.0 ms                                                      | 60.2 ms: 1.11x faster                                                    |
| Geometric mean | (ref)                                                        | 1.06x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251211-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-7cfe81b |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 547 ms: 1.60x faster                                                     |
| async_tree_io_tg           | 913 ms                                                       | 582 ms: 1.57x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 301 ms: 1.53x faster                                                     |
| async_tree_none            | 354 ms                                                       | 244 ms: 1.45x faster                                                     |
| async_tree_none_tg         | 336 ms                                                       | 240 ms: 1.40x faster                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 304 ms: 1.36x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 490 ms: 1.36x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 489 ms: 1.30x faster                                                     |
| async_generators           | 377 ms                                                       | 338 ms: 1.12x faster                                                     |
| coroutines                 | 23.6 ms                                                      | 23.5 ms: 1.00x faster                                                    |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.31x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251211-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-7cfe81b |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 69.8 ms: 1.11x faster                                                    |
| pidigits       | 217 ms                                                       | 206 ms: 1.05x faster                                                     |
| nbody          | 85.1 ms                                                      | 91.5 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                        | 1.03x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251211-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-7cfe81b |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.75 ms: 1.12x faster                                                    |
| regex_compile  | 132 ms                                                       | 124 ms: 1.07x faster                                                     |
| regex_dna      | 180 ms                                                       | 169 ms: 1.07x faster                                                     |
| regex_v8       | 22.7 ms                                                      | 21.9 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                        | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251211-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-7cfe81b |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 84.4 ms: 1.12x faster                                                    |
| json_dumps           | 10.5 ms                                                      | 10.0 ms: 1.05x faster                                                    |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                     |
| xml_etree_generate   | 85.4 ms                                                      | 82.2 ms: 1.04x faster                                                    |
| xml_etree_process    | 59.3 ms                                                      | 57.8 ms: 1.03x faster                                                    |
| unpickle_pure_python | 210 us                                                       | 211 us: 1.01x slower                                                     |
| json_loads           | 27.0 us                                                      | 27.9 us: 1.03x slower                                                    |
| pickle_pure_python   | 294 us                                                       | 307 us: 1.04x slower                                                     |
| tomli_loads          | 2.01 sec                                                     | 2.16 sec: 1.07x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251211-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-7cfe81b |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.29 ms: 1.01x faster                                                    |
| python_startup         | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                    |
| Geometric mean         | (ref)                                                        | 1.06x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251211-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-7cfe81b |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 20.6 ms: 1.05x faster                                                    |
| genshi_xml      | 48.8 ms                                                      | 48.5 ms: 1.01x faster                                                    |
| django_template | 34.1 ms                                                      | 35.0 ms: 1.03x slower                                                    |
| mako            | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                    |
| Geometric mean  | (ref)                                                        | 1.00x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251211-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-7cfe81b |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.15 sec: 2.05x faster                                                   |
| async_tree_io              | 876 ms                                                       | 547 ms: 1.60x faster                                                     |
| async_tree_io_tg           | 913 ms                                                       | 582 ms: 1.57x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 301 ms: 1.53x faster                                                     |
| async_tree_none            | 354 ms                                                       | 244 ms: 1.45x faster                                                     |
| deepcopy                   | 355 us                                                       | 247 us: 1.44x faster                                                     |
| deepcopy_memo              | 39.1 us                                                      | 27.4 us: 1.42x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 240 ms: 1.40x faster                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 304 ms: 1.36x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 490 ms: 1.36x faster                                                     |
| go                         | 141 ms                                                       | 106 ms: 1.33x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 489 ms: 1.30x faster                                                     |
| scimark_sor                | 134 ms                                                       | 107 ms: 1.26x faster                                                     |
| spectral_norm              | 111 ms                                                       | 94.4 ms: 1.18x faster                                                    |
| deepcopy_reduce            | 3.11 us                                                      | 2.65 us: 1.18x faster                                                    |
| scimark_fft                | 349 ms                                                       | 300 ms: 1.16x faster                                                     |
| xml_etree_iterparse        | 94.9 ms                                                      | 84.4 ms: 1.12x faster                                                    |
| dulwich_log                | 74.8 ms                                                      | 66.6 ms: 1.12x faster                                                    |
| regex_effbot               | 3.08 ms                                                      | 2.75 ms: 1.12x faster                                                    |
| pylint                     | 317 ms                                                       | 283 ms: 1.12x faster                                                     |
| async_generators           | 377 ms                                                       | 338 ms: 1.12x faster                                                     |
| html5lib                   | 67.0 ms                                                      | 60.2 ms: 1.11x faster                                                    |
| float                      | 77.5 ms                                                      | 69.8 ms: 1.11x faster                                                    |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.28 ms: 1.10x faster                                                    |
| pyflate                    | 449 ms                                                       | 417 ms: 1.08x faster                                                     |
| richards_super             | 51.6 ms                                                      | 48.0 ms: 1.08x faster                                                    |
| richards                   | 45.2 ms                                                      | 42.2 ms: 1.07x faster                                                    |
| pathlib                    | 19.2 ms                                                      | 17.9 ms: 1.07x faster                                                    |
| regex_compile              | 132 ms                                                       | 124 ms: 1.07x faster                                                     |
| regex_dna                  | 180 ms                                                       | 169 ms: 1.07x faster                                                     |
| logging_simple             | 6.16 us                                                      | 5.78 us: 1.07x faster                                                    |
| bpe_tokeniser              | 4.45 sec                                                     | 4.21 sec: 1.06x faster                                                   |
| pidigits                   | 217 ms                                                       | 206 ms: 1.05x faster                                                     |
| logging_format             | 6.84 us                                                      | 6.50 us: 1.05x faster                                                    |
| sympy_integrate            | 19.8 ms                                                      | 18.9 ms: 1.05x faster                                                    |
| json_dumps                 | 10.5 ms                                                      | 10.0 ms: 1.05x faster                                                    |
| 2to3                       | 260 ms                                                       | 248 ms: 1.05x faster                                                     |
| genshi_text                | 21.5 ms                                                      | 20.6 ms: 1.05x faster                                                    |
| hexiom                     | 5.99 ms                                                      | 5.73 ms: 1.05x faster                                                    |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                     |
| scimark_lu                 | 113 ms                                                       | 108 ms: 1.04x faster                                                     |
| xml_etree_generate         | 85.4 ms                                                      | 82.2 ms: 1.04x faster                                                    |
| pprint_safe_repr           | 738 ms                                                       | 710 ms: 1.04x faster                                                     |
| logging_silent             | 103 ns                                                       | 98.9 ns: 1.04x faster                                                    |
| regex_v8                   | 22.7 ms                                                      | 21.9 ms: 1.04x faster                                                    |
| pprint_pformat             | 1.50 sec                                                     | 1.45 sec: 1.03x faster                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 63.5 ms: 1.03x faster                                                    |
| xml_etree_process          | 59.3 ms                                                      | 57.8 ms: 1.03x faster                                                    |
| coverage                   | 83.0 ms                                                      | 80.8 ms: 1.03x faster                                                    |
| pycparser                  | 1.12 sec                                                     | 1.09 sec: 1.02x faster                                                   |
| docutils                   | 2.62 sec                                                     | 2.57 sec: 1.02x faster                                                   |
| comprehensions             | 16.5 us                                                      | 16.1 us: 1.02x faster                                                    |
| meteor_contest             | 102 ms                                                       | 100 ms: 1.02x faster                                                     |
| python_startup_no_site     | 7.39 ms                                                      | 7.29 ms: 1.01x faster                                                    |
| sympy_sum                  | 156 ms                                                       | 154 ms: 1.01x faster                                                     |
| chaos                      | 57.3 ms                                                      | 56.7 ms: 1.01x faster                                                    |
| thrift                     | 778 us                                                       | 770 us: 1.01x faster                                                     |
| sympy_str                  | 275 ms                                                       | 272 ms: 1.01x faster                                                     |
| genshi_xml                 | 48.8 ms                                                      | 48.5 ms: 1.01x faster                                                    |
| coroutines                 | 23.6 ms                                                      | 23.5 ms: 1.00x faster                                                    |
| unpickle_pure_python       | 210 us                                                       | 211 us: 1.01x slower                                                     |
| nqueens                    | 78.6 ms                                                      | 79.6 ms: 1.01x slower                                                    |
| json                       | 4.93 ms                                                      | 5.02 ms: 1.02x slower                                                    |
| sympy_expand               | 457 ms                                                       | 469 ms: 1.03x slower                                                     |
| django_template            | 34.1 ms                                                      | 35.0 ms: 1.03x slower                                                    |
| crypto_pyaes               | 67.9 ms                                                      | 69.9 ms: 1.03x slower                                                    |
| sqlite_synth               | 2.21 us                                                      | 2.28 us: 1.03x slower                                                    |
| json_loads                 | 27.0 us                                                      | 27.9 us: 1.03x slower                                                    |
| mako                       | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                    |
| pickle_pure_python         | 294 us                                                       | 307 us: 1.04x slower                                                     |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                     |
| deltablue                  | 3.12 ms                                                      | 3.30 ms: 1.06x slower                                                    |
| fannkuch                   | 370 ms                                                       | 395 ms: 1.07x slower                                                     |
| tomli_loads                | 2.01 sec                                                     | 2.16 sec: 1.07x slower                                                   |
| nbody                      | 85.1 ms                                                      | 91.5 ms: 1.07x slower                                                    |
| python_startup             | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                    |
| create_gc_cycles           | 1.34 ms                                                      | 1.86 ms: 1.39x slower                                                    |
| gc_traversal               | 3.14 ms                                                      | 4.39 ms: 1.40x slower                                                    |
| bench_thread_pool          | 919 us                                                       | 1.30 ms: 1.42x slower                                                    |
| telco                      | 7.82 ms                                                      | 162 ms: 20.65x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                      | 315 ms: 28.61x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.01x slower                                                             |

Benchmark hidden because not significant (3): generators, raytrace, typing_runtime_protocols
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251211-3.15.0a2+-7cfe81b/bm-20251211-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-7cfe81b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.039x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.15x