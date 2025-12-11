# Results vs. 3.12.6

- fork: colesbury
- ref: gh_142472_stackrefs
- machine: linux-x86_64
- commit hash: 7cfe81b
- commit date: 2025-12-11
- overall geometric mean: 1.074x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251211-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-7cfe81b |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 248 ms: 1.06x faster                                                     |
| docutils       | 2.64 sec                                               | 2.57 sec: 1.03x faster                                                   |
| html5lib       | 63.6 ms                                                | 60.2 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                  | 1.05x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251211-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-7cfe81b |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 547 ms: 1.98x faster                                                     |
| async_tree_io_tg           | 1.11 sec                                               | 582 ms: 1.91x faster                                                     |
| async_tree_none            | 464 ms                                                 | 244 ms: 1.91x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 240 ms: 1.86x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 301 ms: 1.84x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 304 ms: 1.84x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 489 ms: 1.48x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 490 ms: 1.46x faster                                                     |
| async_generators           | 384 ms                                                 | 338 ms: 1.14x faster                                                     |
| coroutines                 | 23.9 ms                                                | 23.5 ms: 1.02x faster                                                    |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.53x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251211-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-7cfe81b |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 69.8 ms: 1.16x faster                                                    |
| nbody          | 89.3 ms                                                | 91.5 ms: 1.02x slower                                                    |
| pidigits       | 184 ms                                                 | 206 ms: 1.12x slower                                                     |
| Geometric mean | (ref)                                                  | 1.00x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251211-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-7cfe81b |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.75 ms: 1.15x faster                                                    |
| regex_compile  | 142 ms                                                 | 124 ms: 1.15x faster                                                     |
| regex_dna      | 168 ms                                                 | 169 ms: 1.01x slower                                                     |
| regex_v8       | 20.6 ms                                                | 21.9 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                  | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251211-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-7cfe81b |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 84.4 ms: 1.15x faster                                                    |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                     |
| unpickle_pure_python | 221 us                                                 | 211 us: 1.04x faster                                                     |
| xml_etree_generate   | 85.2 ms                                                | 82.2 ms: 1.04x faster                                                    |
| json_dumps           | 10.4 ms                                                | 10.0 ms: 1.03x faster                                                    |
| xml_etree_process    | 59.0 ms                                                | 57.8 ms: 1.02x faster                                                    |
| tomli_loads          | 2.11 sec                                               | 2.16 sec: 1.02x slower                                                   |
| json_loads           | 26.5 us                                                | 27.9 us: 1.05x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                             |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251211-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-7cfe81b |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.29 ms: 1.02x slower                                                    |
| python_startup         | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251211-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-7cfe81b |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.6 ms: 1.11x faster                                                    |
| genshi_xml      | 50.2 ms                                                | 48.5 ms: 1.04x faster                                                    |
| django_template | 34.7 ms                                                | 35.0 ms: 1.01x slower                                                    |
| mako            | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.02x faster                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251211-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-7cfe81b |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.15 sec: 2.11x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 547 ms: 1.98x faster                                                     |
| async_tree_io_tg           | 1.11 sec                                               | 582 ms: 1.91x faster                                                     |
| async_tree_none            | 464 ms                                                 | 244 ms: 1.91x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 240 ms: 1.86x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 301 ms: 1.84x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 304 ms: 1.84x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 489 ms: 1.48x faster                                                     |
| deepcopy_memo              | 40.3 us                                                | 27.4 us: 1.47x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 490 ms: 1.46x faster                                                     |
| deepcopy                   | 352 us                                                 | 247 us: 1.43x faster                                                     |
| go                         | 139 ms                                                 | 106 ms: 1.32x faster                                                     |
| comprehensions             | 19.8 us                                                | 16.1 us: 1.23x faster                                                    |
| scimark_sor                | 130 ms                                                 | 107 ms: 1.21x faster                                                     |
| pathlib                    | 21.5 ms                                                | 17.9 ms: 1.20x faster                                                    |
| raytrace                   | 299 ms                                                 | 253 ms: 1.18x faster                                                     |
| dulwich_log                | 78.9 ms                                                | 66.6 ms: 1.18x faster                                                    |
| spectral_norm              | 110 ms                                                 | 94.4 ms: 1.17x faster                                                    |
| deepcopy_reduce            | 3.08 us                                                | 2.65 us: 1.16x faster                                                    |
| float                      | 80.8 ms                                                | 69.8 ms: 1.16x faster                                                    |
| regex_effbot               | 3.17 ms                                                | 2.75 ms: 1.15x faster                                                    |
| regex_compile              | 142 ms                                                 | 124 ms: 1.15x faster                                                     |
| logging_simple             | 6.63 us                                                | 5.78 us: 1.15x faster                                                    |
| xml_etree_iterparse        | 96.7 ms                                                | 84.4 ms: 1.15x faster                                                    |
| async_generators           | 384 ms                                                 | 338 ms: 1.14x faster                                                     |
| scimark_fft                | 342 ms                                                 | 300 ms: 1.14x faster                                                     |
| logging_format             | 7.35 us                                                | 6.50 us: 1.13x faster                                                    |
| bpe_tokeniser              | 4.74 sec                                               | 4.21 sec: 1.12x faster                                                   |
| pylint                     | 319 ms                                                 | 283 ms: 1.12x faster                                                     |
| generators                 | 32.2 ms                                                | 28.8 ms: 1.12x faster                                                    |
| genshi_text                | 22.8 ms                                                | 20.6 ms: 1.11x faster                                                    |
| chaos                      | 62.8 ms                                                | 56.7 ms: 1.11x faster                                                    |
| logging_silent             | 109 ns                                                 | 98.9 ns: 1.10x faster                                                    |
| crypto_pyaes               | 76.6 ms                                                | 69.9 ms: 1.10x faster                                                    |
| sympy_integrate            | 20.5 ms                                                | 18.9 ms: 1.09x faster                                                    |
| richards                   | 45.9 ms                                                | 42.2 ms: 1.09x faster                                                    |
| richards_super             | 51.9 ms                                                | 48.0 ms: 1.08x faster                                                    |
| sympy_sum                  | 166 ms                                                 | 154 ms: 1.08x faster                                                     |
| hexiom                     | 6.17 ms                                                | 5.73 ms: 1.08x faster                                                    |
| scimark_monte_carlo        | 68.4 ms                                                | 63.5 ms: 1.08x faster                                                    |
| pyflate                    | 448 ms                                                 | 417 ms: 1.07x faster                                                     |
| sympy_str                  | 292 ms                                                 | 272 ms: 1.07x faster                                                     |
| pycparser                  | 1.17 sec                                               | 1.09 sec: 1.07x faster                                                   |
| 2to3                       | 264 ms                                                 | 248 ms: 1.06x faster                                                     |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                     |
| html5lib                   | 63.6 ms                                                | 60.2 ms: 1.06x faster                                                    |
| scimark_lu                 | 114 ms                                                 | 108 ms: 1.05x faster                                                     |
| typing_runtime_protocols   | 163 us                                                 | 155 us: 1.05x faster                                                     |
| pprint_pformat             | 1.52 sec                                               | 1.45 sec: 1.05x faster                                                   |
| pprint_safe_repr           | 743 ms                                                 | 710 ms: 1.05x faster                                                     |
| deltablue                  | 3.45 ms                                                | 3.30 ms: 1.05x faster                                                    |
| unpickle_pure_python       | 221 us                                                 | 211 us: 1.04x faster                                                     |
| xml_etree_generate         | 85.2 ms                                                | 82.2 ms: 1.04x faster                                                    |
| genshi_xml                 | 50.2 ms                                                | 48.5 ms: 1.04x faster                                                    |
| meteor_contest             | 104 ms                                                 | 100 ms: 1.03x faster                                                     |
| json_dumps                 | 10.4 ms                                                | 10.0 ms: 1.03x faster                                                    |
| docutils                   | 2.64 sec                                               | 2.57 sec: 1.03x faster                                                   |
| thrift                     | 791 us                                                 | 770 us: 1.03x faster                                                     |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.28 ms: 1.03x faster                                                    |
| xml_etree_process          | 59.0 ms                                                | 57.8 ms: 1.02x faster                                                    |
| coroutines                 | 23.9 ms                                                | 23.5 ms: 1.02x faster                                                    |
| nqueens                    | 80.1 ms                                                | 79.6 ms: 1.01x faster                                                    |
| regex_dna                  | 168 ms                                                 | 169 ms: 1.01x slower                                                     |
| django_template            | 34.7 ms                                                | 35.0 ms: 1.01x slower                                                    |
| python_startup_no_site     | 7.16 ms                                                | 7.29 ms: 1.02x slower                                                    |
| tomli_loads                | 2.11 sec                                               | 2.16 sec: 1.02x slower                                                   |
| nbody                      | 89.3 ms                                                | 91.5 ms: 1.02x slower                                                    |
| sqlite_synth               | 2.20 us                                                | 2.28 us: 1.03x slower                                                    |
| json_loads                 | 26.5 us                                                | 27.9 us: 1.05x slower                                                    |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                     |
| fannkuch                   | 372 ms                                                 | 395 ms: 1.06x slower                                                     |
| regex_v8                   | 20.6 ms                                                | 21.9 ms: 1.06x slower                                                    |
| mako                       | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                    |
| pidigits                   | 184 ms                                                 | 206 ms: 1.12x slower                                                     |
| coverage                   | 71.4 ms                                                | 80.8 ms: 1.13x slower                                                    |
| python_startup             | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                    |
| gc_traversal               | 3.46 ms                                                | 4.39 ms: 1.27x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 1.30 ms: 1.39x slower                                                    |
| create_gc_cycles           | 1.09 ms                                                | 1.86 ms: 1.71x slower                                                    |
| telco                      | 6.53 ms                                                | 162 ms: 24.75x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 315 ms: 29.13x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                             |

Benchmark hidden because not significant (3): pickle_pure_python, json, sympy_expand
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251211-3.15.0a2+-7cfe81b/bm-20251211-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-7cfe81b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.074x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.16x