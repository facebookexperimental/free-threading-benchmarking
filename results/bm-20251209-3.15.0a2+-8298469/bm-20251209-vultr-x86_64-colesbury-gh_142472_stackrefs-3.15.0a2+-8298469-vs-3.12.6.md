# Results vs. 3.12.6

- fork: colesbury
- ref: gh_142472_stackrefs
- machine: linux-x86_64
- commit hash: 8298469
- commit date: 2025-12-09
- overall geometric mean: 1.070x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-8298469 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 247 ms: 1.07x faster                                                     |
| docutils       | 2.64 sec                                               | 2.53 sec: 1.04x faster                                                   |
| html5lib       | 63.6 ms                                                | 60.0 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                  | 1.06x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-8298469 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 554 ms: 1.96x faster                                                     |
| async_tree_none            | 464 ms                                                 | 245 ms: 1.90x faster                                                     |
| async_tree_io_tg           | 1.11 sec                                               | 586 ms: 1.89x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 304 ms: 1.84x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 302 ms: 1.84x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 244 ms: 1.83x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 487 ms: 1.48x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 487 ms: 1.47x faster                                                     |
| async_generators           | 384 ms                                                 | 342 ms: 1.13x faster                                                     |
| coroutines                 | 23.9 ms                                                | 24.4 ms: 1.02x slower                                                    |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.52x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-8298469 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 71.2 ms: 1.13x faster                                                    |
| nbody          | 89.3 ms                                                | 92.4 ms: 1.04x slower                                                    |
| pidigits       | 184 ms                                                 | 208 ms: 1.13x slower                                                     |
| Geometric mean | (ref)                                                  | 1.01x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-8298469 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 124 ms: 1.15x faster                                                     |
| regex_effbot   | 3.17 ms                                                | 2.86 ms: 1.11x faster                                                    |
| regex_dna      | 168 ms                                                 | 177 ms: 1.06x slower                                                     |
| regex_v8       | 20.6 ms                                                | 22.7 ms: 1.10x slower                                                    |
| Geometric mean | (ref)                                                  | 1.02x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-8298469 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 84.7 ms: 1.14x faster                                                    |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                     |
| json_dumps           | 10.4 ms                                                | 9.82 ms: 1.05x faster                                                    |
| unpickle_pure_python | 221 us                                                 | 213 us: 1.04x faster                                                     |
| xml_etree_generate   | 85.2 ms                                                | 82.4 ms: 1.03x faster                                                    |
| xml_etree_process    | 59.0 ms                                                | 57.5 ms: 1.03x faster                                                    |
| pickle_pure_python   | 308 us                                                 | 306 us: 1.00x faster                                                     |
| tomli_loads          | 2.11 sec                                               | 2.18 sec: 1.03x slower                                                   |
| json_loads           | 26.5 us                                                | 28.4 us: 1.07x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-8298469 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.31 ms: 1.02x slower                                                    |
| python_startup         | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-8298469 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.4 ms: 1.12x faster                                                    |
| genshi_xml      | 50.2 ms                                                | 48.0 ms: 1.05x faster                                                    |
| django_template | 34.7 ms                                                | 34.0 ms: 1.02x faster                                                    |
| mako            | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.03x faster                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-8298469 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.15 sec: 2.11x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 554 ms: 1.96x faster                                                     |
| async_tree_none            | 464 ms                                                 | 245 ms: 1.90x faster                                                     |
| async_tree_io_tg           | 1.11 sec                                               | 586 ms: 1.89x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 304 ms: 1.84x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 302 ms: 1.84x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 244 ms: 1.83x faster                                                     |
| deepcopy_memo              | 40.3 us                                                | 26.9 us: 1.50x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 487 ms: 1.48x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 487 ms: 1.47x faster                                                     |
| deepcopy                   | 352 us                                                 | 246 us: 1.43x faster                                                     |
| go                         | 139 ms                                                 | 107 ms: 1.30x faster                                                     |
| comprehensions             | 19.8 us                                                | 16.0 us: 1.24x faster                                                    |
| pathlib                    | 21.5 ms                                                | 17.6 ms: 1.23x faster                                                    |
| scimark_sor                | 130 ms                                                 | 107 ms: 1.21x faster                                                     |
| raytrace                   | 299 ms                                                 | 252 ms: 1.19x faster                                                     |
| deepcopy_reduce            | 3.08 us                                                | 2.60 us: 1.18x faster                                                    |
| generators                 | 32.2 ms                                                | 27.6 ms: 1.17x faster                                                    |
| dulwich_log                | 78.9 ms                                                | 68.1 ms: 1.16x faster                                                    |
| regex_compile              | 142 ms                                                 | 124 ms: 1.15x faster                                                     |
| spectral_norm              | 110 ms                                                 | 96.0 ms: 1.15x faster                                                    |
| xml_etree_iterparse        | 96.7 ms                                                | 84.7 ms: 1.14x faster                                                    |
| float                      | 80.8 ms                                                | 71.2 ms: 1.13x faster                                                    |
| scimark_fft                | 342 ms                                                 | 302 ms: 1.13x faster                                                     |
| bpe_tokeniser              | 4.74 sec                                               | 4.21 sec: 1.13x faster                                                   |
| async_generators           | 384 ms                                                 | 342 ms: 1.13x faster                                                     |
| genshi_text                | 22.8 ms                                                | 20.4 ms: 1.12x faster                                                    |
| pylint                     | 319 ms                                                 | 284 ms: 1.12x faster                                                     |
| logging_simple             | 6.63 us                                                | 5.93 us: 1.12x faster                                                    |
| chaos                      | 62.8 ms                                                | 56.3 ms: 1.12x faster                                                    |
| regex_effbot               | 3.17 ms                                                | 2.86 ms: 1.11x faster                                                    |
| logging_format             | 7.35 us                                                | 6.67 us: 1.10x faster                                                    |
| crypto_pyaes               | 76.6 ms                                                | 69.8 ms: 1.10x faster                                                    |
| sympy_integrate            | 20.5 ms                                                | 18.8 ms: 1.09x faster                                                    |
| hexiom                     | 6.17 ms                                                | 5.68 ms: 1.09x faster                                                    |
| sympy_sum                  | 166 ms                                                 | 154 ms: 1.08x faster                                                     |
| richards                   | 45.9 ms                                                | 42.6 ms: 1.08x faster                                                    |
| logging_silent             | 109 ns                                                 | 101 ns: 1.08x faster                                                     |
| pyflate                    | 448 ms                                                 | 417 ms: 1.07x faster                                                     |
| sympy_str                  | 292 ms                                                 | 272 ms: 1.07x faster                                                     |
| scimark_monte_carlo        | 68.4 ms                                                | 63.9 ms: 1.07x faster                                                    |
| 2to3                       | 264 ms                                                 | 247 ms: 1.07x faster                                                     |
| typing_runtime_protocols   | 163 us                                                 | 153 us: 1.07x faster                                                     |
| pycparser                  | 1.17 sec                                               | 1.10 sec: 1.06x faster                                                   |
| richards_super             | 51.9 ms                                                | 48.8 ms: 1.06x faster                                                    |
| html5lib                   | 63.6 ms                                                | 60.0 ms: 1.06x faster                                                    |
| pprint_safe_repr           | 743 ms                                                 | 701 ms: 1.06x faster                                                     |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                     |
| pprint_pformat             | 1.52 sec                                               | 1.44 sec: 1.05x faster                                                   |
| json_dumps                 | 10.4 ms                                                | 9.82 ms: 1.05x faster                                                    |
| scimark_lu                 | 114 ms                                                 | 109 ms: 1.05x faster                                                     |
| genshi_xml                 | 50.2 ms                                                | 48.0 ms: 1.05x faster                                                    |
| docutils                   | 2.64 sec                                               | 2.53 sec: 1.04x faster                                                   |
| thrift                     | 791 us                                                 | 759 us: 1.04x faster                                                     |
| meteor_contest             | 104 ms                                                 | 99.9 ms: 1.04x faster                                                    |
| unpickle_pure_python       | 221 us                                                 | 213 us: 1.04x faster                                                     |
| xml_etree_generate         | 85.2 ms                                                | 82.4 ms: 1.03x faster                                                    |
| deltablue                  | 3.45 ms                                                | 3.35 ms: 1.03x faster                                                    |
| xml_etree_process          | 59.0 ms                                                | 57.5 ms: 1.03x faster                                                    |
| django_template            | 34.7 ms                                                | 34.0 ms: 1.02x faster                                                    |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.35 ms: 1.01x faster                                                    |
| pickle_pure_python         | 308 us                                                 | 306 us: 1.00x faster                                                     |
| coroutines                 | 23.9 ms                                                | 24.4 ms: 1.02x slower                                                    |
| python_startup_no_site     | 7.16 ms                                                | 7.31 ms: 1.02x slower                                                    |
| json                       | 5.02 ms                                                | 5.15 ms: 1.03x slower                                                    |
| sympy_expand               | 468 ms                                                 | 482 ms: 1.03x slower                                                     |
| sqlite_synth               | 2.20 us                                                | 2.28 us: 1.03x slower                                                    |
| tomli_loads                | 2.11 sec                                               | 2.18 sec: 1.03x slower                                                   |
| nbody                      | 89.3 ms                                                | 92.4 ms: 1.04x slower                                                    |
| fannkuch                   | 372 ms                                                 | 390 ms: 1.05x slower                                                     |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                     |
| regex_dna                  | 168 ms                                                 | 177 ms: 1.06x slower                                                     |
| mako                       | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                    |
| json_loads                 | 26.5 us                                                | 28.4 us: 1.07x slower                                                    |
| regex_v8                   | 20.6 ms                                                | 22.7 ms: 1.10x slower                                                    |
| pidigits                   | 184 ms                                                 | 208 ms: 1.13x slower                                                     |
| coverage                   | 71.4 ms                                                | 82.3 ms: 1.15x slower                                                    |
| python_startup             | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                    |
| gc_traversal               | 3.46 ms                                                | 4.47 ms: 1.29x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 1.31 ms: 1.40x slower                                                    |
| create_gc_cycles           | 1.09 ms                                                | 1.93 ms: 1.77x slower                                                    |
| telco                      | 6.53 ms                                                | 157 ms: 24.02x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 352 ms: 32.59x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                             |

Benchmark hidden because not significant (1): nqueens
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251209-3.15.0a2+-8298469/bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-8298469.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.070x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.16x