# Results vs. 3.12.6

- fork: colesbury
- ref: gh_131586_lookup_spe
- machine: linux-x86_64
- commit hash: 4c6bf78
- commit date: 2025-03-25
- overall geometric mean: 1.142x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 244 ms: 1.08x faster                                                      |
| docutils       | 2.64 sec                                               | 2.52 sec: 1.05x faster                                                    |
| Geometric mean | (ref)                                                  | 1.06x faster                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 289 ms: 1.94x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 298 ms: 1.86x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 586 ms: 1.85x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 241 ms: 1.85x faster                                                      |
| async_tree_io_tg           | 1.11 sec                                               | 603 ms: 1.84x faster                                                      |
| async_tree_none            | 464 ms                                                 | 260 ms: 1.79x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 451 ms: 1.60x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 473 ms: 1.51x faster                                                      |
| async_generators           | 384 ms                                                 | 313 ms: 1.23x faster                                                      |
| coroutines                 | 23.9 ms                                                | 20.5 ms: 1.17x faster                                                     |
| Geometric mean             | (ref)                                                  | 1.57x faster                                                              |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 68.9 ms: 1.17x faster                                                     |
| nbody          | 89.3 ms                                                | 81.2 ms: 1.10x faster                                                     |
| pidigits       | 184 ms                                                 | 191 ms: 1.04x slower                                                      |
| Geometric mean | (ref)                                                  | 1.08x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 122 ms: 1.16x faster                                                      |
| regex_effbot   | 3.17 ms                                                | 2.99 ms: 1.06x faster                                                     |
| regex_v8       | 20.6 ms                                                | 21.8 ms: 1.06x slower                                                     |
| regex_dna      | 168 ms                                                 | 184 ms: 1.09x slower                                                      |
| Geometric mean | (ref)                                                  | 1.02x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.76 sec: 1.20x faster                                                    |
| unpickle_pure_python | 221 us                                                 | 204 us: 1.08x faster                                                      |
| xml_etree_process    | 59.0 ms                                                | 55.4 ms: 1.06x faster                                                     |
| xml_etree_generate   | 85.2 ms                                                | 81.3 ms: 1.05x faster                                                     |
| pickle_pure_python   | 308 us                                                 | 296 us: 1.04x faster                                                      |
| xml_etree_iterparse  | 96.7 ms                                                | 96.2 ms: 1.01x faster                                                     |
| xml_etree_parse      | 139 ms                                                 | 149 ms: 1.07x slower                                                      |
| json_dumps           | 10.4 ms                                                | 11.6 ms: 1.12x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                              |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 8.62 ms: 1.20x slower                                                     |
| python_startup         | 9.93 ms                                                | 14.9 ms: 1.50x slower                                                     |
| Geometric mean         | (ref)                                                  | 1.34x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 19.3 ms: 1.18x faster                                                     |
| genshi_xml      | 50.2 ms                                                | 45.4 ms: 1.11x faster                                                     |
| django_template | 34.7 ms                                                | 32.6 ms: 1.06x faster                                                     |
| mako            | 11.0 ms                                                | 11.5 ms: 1.04x slower                                                     |
| Geometric mean  | (ref)                                                  | 1.07x faster                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 289 ms: 1.94x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 298 ms: 1.86x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 586 ms: 1.85x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 241 ms: 1.85x faster                                                      |
| async_tree_io_tg           | 1.11 sec                                               | 603 ms: 1.84x faster                                                      |
| async_tree_none            | 464 ms                                                 | 260 ms: 1.79x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 451 ms: 1.60x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 473 ms: 1.51x faster                                                      |
| deepcopy                   | 352 us                                                 | 234 us: 1.50x faster                                                      |
| deepcopy_memo              | 40.3 us                                                | 27.0 us: 1.49x faster                                                     |
| spectral_norm              | 110 ms                                                 | 80.6 ms: 1.37x faster                                                     |
| go                         | 139 ms                                                 | 104 ms: 1.34x faster                                                      |
| comprehensions             | 19.8 us                                                | 14.8 us: 1.34x faster                                                     |
| deepcopy_reduce            | 3.08 us                                                | 2.33 us: 1.32x faster                                                     |
| scimark_sor                | 130 ms                                                 | 99.2 ms: 1.31x faster                                                     |
| logging_silent             | 109 ns                                                 | 86.3 ns: 1.26x faster                                                     |
| raytrace                   | 299 ms                                                 | 238 ms: 1.26x faster                                                      |
| chaos                      | 62.8 ms                                                | 50.5 ms: 1.25x faster                                                     |
| scimark_fft                | 342 ms                                                 | 275 ms: 1.24x faster                                                      |
| async_generators           | 384 ms                                                 | 313 ms: 1.23x faster                                                      |
| scimark_monte_carlo        | 68.4 ms                                                | 56.0 ms: 1.22x faster                                                     |
| generators                 | 32.2 ms                                                | 26.5 ms: 1.22x faster                                                     |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 3.62 ms: 1.21x faster                                                     |
| deltablue                  | 3.45 ms                                                | 2.84 ms: 1.21x faster                                                     |
| dulwich_log                | 78.9 ms                                                | 65.6 ms: 1.20x faster                                                     |
| richards                   | 45.9 ms                                                | 38.3 ms: 1.20x faster                                                     |
| tomli_loads                | 2.11 sec                                               | 1.76 sec: 1.20x faster                                                    |
| logging_simple             | 6.63 us                                                | 5.59 us: 1.19x faster                                                     |
| genshi_text                | 22.8 ms                                                | 19.3 ms: 1.18x faster                                                     |
| pylint                     | 319 ms                                                 | 271 ms: 1.18x faster                                                      |
| float                      | 80.8 ms                                                | 68.9 ms: 1.17x faster                                                     |
| coroutines                 | 23.9 ms                                                | 20.5 ms: 1.17x faster                                                     |
| logging_format             | 7.35 us                                                | 6.28 us: 1.17x faster                                                     |
| richards_super             | 51.9 ms                                                | 44.4 ms: 1.17x faster                                                     |
| regex_compile              | 142 ms                                                 | 122 ms: 1.16x faster                                                      |
| pyflate                    | 448 ms                                                 | 387 ms: 1.16x faster                                                      |
| pathlib                    | 21.5 ms                                                | 18.7 ms: 1.15x faster                                                     |
| bpe_tokeniser              | 4.74 sec                                               | 4.12 sec: 1.15x faster                                                    |
| sqlalchemy_declarative     | 143 ms                                                 | 125 ms: 1.14x faster                                                      |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.2 ms: 1.14x faster                                                     |
| hexiom                     | 6.17 ms                                                | 5.44 ms: 1.13x faster                                                     |
| scimark_lu                 | 114 ms                                                 | 101 ms: 1.13x faster                                                      |
| crypto_pyaes               | 76.6 ms                                                | 67.9 ms: 1.13x faster                                                     |
| typing_runtime_protocols   | 163 us                                                 | 146 us: 1.12x faster                                                      |
| sympy_str                  | 292 ms                                                 | 263 ms: 1.11x faster                                                      |
| sympy_sum                  | 166 ms                                                 | 150 ms: 1.11x faster                                                      |
| sympy_integrate            | 20.5 ms                                                | 18.6 ms: 1.11x faster                                                     |
| genshi_xml                 | 50.2 ms                                                | 45.4 ms: 1.11x faster                                                     |
| nqueens                    | 80.1 ms                                                | 72.5 ms: 1.10x faster                                                     |
| nbody                      | 89.3 ms                                                | 81.2 ms: 1.10x faster                                                     |
| thrift                     | 791 us                                                 | 726 us: 1.09x faster                                                      |
| pycparser                  | 1.17 sec                                               | 1.08 sec: 1.09x faster                                                    |
| unpickle_pure_python       | 221 us                                                 | 204 us: 1.08x faster                                                      |
| 2to3                       | 264 ms                                                 | 244 ms: 1.08x faster                                                      |
| xml_etree_process          | 59.0 ms                                                | 55.4 ms: 1.06x faster                                                     |
| django_template            | 34.7 ms                                                | 32.6 ms: 1.06x faster                                                     |
| sympy_expand               | 468 ms                                                 | 441 ms: 1.06x faster                                                      |
| regex_effbot               | 3.17 ms                                                | 2.99 ms: 1.06x faster                                                     |
| pprint_pformat             | 1.52 sec                                               | 1.44 sec: 1.05x faster                                                    |
| docutils                   | 2.64 sec                                               | 2.52 sec: 1.05x faster                                                    |
| xml_etree_generate         | 85.2 ms                                                | 81.3 ms: 1.05x faster                                                     |
| pprint_safe_repr           | 743 ms                                                 | 711 ms: 1.05x faster                                                      |
| pickle_pure_python         | 308 us                                                 | 296 us: 1.04x faster                                                      |
| json                       | 5.02 ms                                                | 4.89 ms: 1.03x faster                                                     |
| sqlite_synth               | 2.20 us                                                | 2.16 us: 1.02x faster                                                     |
| xml_etree_iterparse        | 96.7 ms                                                | 96.2 ms: 1.01x faster                                                     |
| mdp                        | 2.42 sec                                               | 2.45 sec: 1.01x slower                                                    |
| fannkuch                   | 372 ms                                                 | 379 ms: 1.02x slower                                                      |
| coverage                   | 71.4 ms                                                | 73.6 ms: 1.03x slower                                                     |
| pidigits                   | 184 ms                                                 | 191 ms: 1.04x slower                                                      |
| mako                       | 11.0 ms                                                | 11.5 ms: 1.04x slower                                                     |
| telco                      | 6.53 ms                                                | 6.82 ms: 1.04x slower                                                     |
| regex_v8                   | 20.6 ms                                                | 21.8 ms: 1.06x slower                                                     |
| bench_thread_pool          | 941 us                                                 | 1.01 ms: 1.07x slower                                                     |
| xml_etree_parse            | 139 ms                                                 | 149 ms: 1.07x slower                                                      |
| regex_dna                  | 168 ms                                                 | 184 ms: 1.09x slower                                                      |
| json_dumps                 | 10.4 ms                                                | 11.6 ms: 1.12x slower                                                     |
| python_startup_no_site     | 7.16 ms                                                | 8.62 ms: 1.20x slower                                                     |
| gc_traversal               | 3.46 ms                                                | 4.38 ms: 1.27x slower                                                     |
| python_startup             | 9.93 ms                                                | 14.9 ms: 1.50x slower                                                     |
| create_gc_cycles           | 1.09 ms                                                | 1.92 ms: 1.76x slower                                                     |
| bench_mp_pool              | 10.8 ms                                                | 87.8 ms: 8.13x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.11x faster                                                              |

Benchmark hidden because not significant (3): asyncio_websockets, json_loads, meteor_contest
Ignored benchmarks (20) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250325-3.14.0a6+-4c6bf78-CLANG/bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.142x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: 1.15x