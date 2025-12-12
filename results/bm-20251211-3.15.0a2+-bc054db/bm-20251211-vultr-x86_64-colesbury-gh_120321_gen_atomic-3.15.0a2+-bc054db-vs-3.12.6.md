# Results vs. 3.12.6

- fork: colesbury
- ref: gh_120321_gen_atomic
- machine: linux-x86_64
- commit hash: bc054db
- commit date: 2025-12-11
- overall geometric mean: 1.076x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 246 ms: 1.07x faster                                                      |
| docutils       | 2.64 sec                                               | 2.55 sec: 1.04x faster                                                    |
| html5lib       | 63.6 ms                                                | 60.4 ms: 1.05x faster                                                     |
| Geometric mean | (ref)                                                  | 1.05x faster                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 550 ms: 1.97x faster                                                      |
| async_tree_none            | 464 ms                                                 | 243 ms: 1.91x faster                                                      |
| async_tree_io_tg           | 1.11 sec                                               | 582 ms: 1.91x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 241 ms: 1.85x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 302 ms: 1.84x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 305 ms: 1.84x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 487 ms: 1.48x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 487 ms: 1.47x faster                                                      |
| async_generators           | 384 ms                                                 | 336 ms: 1.14x faster                                                      |
| coroutines                 | 23.9 ms                                                | 23.3 ms: 1.03x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                      |
| Geometric mean             | (ref)                                                  | 1.53x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 68.1 ms: 1.19x faster                                                     |
| nbody          | 89.3 ms                                                | 88.1 ms: 1.01x faster                                                     |
| pidigits       | 184 ms                                                 | 198 ms: 1.07x slower                                                      |
| Geometric mean | (ref)                                                  | 1.04x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 123 ms: 1.16x faster                                                      |
| regex_effbot   | 3.17 ms                                                | 3.05 ms: 1.04x faster                                                     |
| regex_v8       | 20.6 ms                                                | 21.9 ms: 1.07x slower                                                     |
| regex_dna      | 168 ms                                                 | 190 ms: 1.13x slower                                                      |
| Geometric mean | (ref)                                                  | 1.00x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 84.4 ms: 1.15x faster                                                     |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                      |
| json_dumps           | 10.4 ms                                                | 9.79 ms: 1.06x faster                                                     |
| unpickle_pure_python | 221 us                                                 | 213 us: 1.03x faster                                                      |
| xml_etree_generate   | 85.2 ms                                                | 82.5 ms: 1.03x faster                                                     |
| xml_etree_process    | 59.0 ms                                                | 57.6 ms: 1.02x faster                                                     |
| pickle_pure_python   | 308 us                                                 | 308 us: 1.00x slower                                                      |
| tomli_loads          | 2.11 sec                                               | 2.18 sec: 1.03x slower                                                    |
| json_loads           | 26.5 us                                                | 27.8 us: 1.05x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.25 ms: 1.01x slower                                                     |
| python_startup         | 9.93 ms                                                | 12.4 ms: 1.25x slower                                                     |
| Geometric mean         | (ref)                                                  | 1.12x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_text    | 22.8 ms                                                | 20.6 ms: 1.11x faster                                                     |
| genshi_xml     | 50.2 ms                                                | 47.9 ms: 1.05x faster                                                     |
| mako           | 11.0 ms                                                | 11.8 ms: 1.08x slower                                                     |
| Geometric mean | (ref)                                                  | 1.02x faster                                                              |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.15 sec: 2.09x faster                                                    |
| async_tree_io              | 1.08 sec                                               | 550 ms: 1.97x faster                                                      |
| async_tree_none            | 464 ms                                                 | 243 ms: 1.91x faster                                                      |
| async_tree_io_tg           | 1.11 sec                                               | 582 ms: 1.91x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 241 ms: 1.85x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 302 ms: 1.84x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 305 ms: 1.84x faster                                                      |
| deepcopy_memo              | 40.3 us                                                | 26.9 us: 1.50x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 487 ms: 1.48x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 487 ms: 1.47x faster                                                      |
| deepcopy                   | 352 us                                                 | 244 us: 1.44x faster                                                      |
| go                         | 139 ms                                                 | 106 ms: 1.31x faster                                                      |
| comprehensions             | 19.8 us                                                | 15.6 us: 1.27x faster                                                     |
| pathlib                    | 21.5 ms                                                | 17.4 ms: 1.23x faster                                                     |
| scimark_sor                | 130 ms                                                 | 108 ms: 1.21x faster                                                      |
| raytrace                   | 299 ms                                                 | 250 ms: 1.19x faster                                                      |
| float                      | 80.8 ms                                                | 68.1 ms: 1.19x faster                                                     |
| deepcopy_reduce            | 3.08 us                                                | 2.60 us: 1.18x faster                                                     |
| generators                 | 32.2 ms                                                | 27.4 ms: 1.18x faster                                                     |
| dulwich_log                | 78.9 ms                                                | 67.9 ms: 1.16x faster                                                     |
| regex_compile              | 142 ms                                                 | 123 ms: 1.16x faster                                                      |
| spectral_norm              | 110 ms                                                 | 95.4 ms: 1.16x faster                                                     |
| xml_etree_iterparse        | 96.7 ms                                                | 84.4 ms: 1.15x faster                                                     |
| logging_simple             | 6.63 us                                                | 5.79 us: 1.15x faster                                                     |
| async_generators           | 384 ms                                                 | 336 ms: 1.14x faster                                                      |
| bpe_tokeniser              | 4.74 sec                                               | 4.20 sec: 1.13x faster                                                    |
| chaos                      | 62.8 ms                                                | 55.7 ms: 1.13x faster                                                     |
| pylint                     | 319 ms                                                 | 284 ms: 1.12x faster                                                      |
| scimark_fft                | 342 ms                                                 | 305 ms: 1.12x faster                                                      |
| logging_format             | 7.35 us                                                | 6.61 us: 1.11x faster                                                     |
| genshi_text                | 22.8 ms                                                | 20.6 ms: 1.11x faster                                                     |
| crypto_pyaes               | 76.6 ms                                                | 69.1 ms: 1.11x faster                                                     |
| sympy_integrate            | 20.5 ms                                                | 18.7 ms: 1.10x faster                                                     |
| richards                   | 45.9 ms                                                | 42.3 ms: 1.09x faster                                                     |
| sympy_sum                  | 166 ms                                                 | 153 ms: 1.08x faster                                                      |
| richards_super             | 51.9 ms                                                | 48.1 ms: 1.08x faster                                                     |
| scimark_monte_carlo        | 68.4 ms                                                | 63.7 ms: 1.07x faster                                                     |
| logging_silent             | 109 ns                                                 | 101 ns: 1.07x faster                                                      |
| 2to3                       | 264 ms                                                 | 246 ms: 1.07x faster                                                      |
| pprint_safe_repr           | 743 ms                                                 | 692 ms: 1.07x faster                                                      |
| pprint_pformat             | 1.52 sec                                               | 1.42 sec: 1.07x faster                                                    |
| sympy_str                  | 292 ms                                                 | 272 ms: 1.07x faster                                                      |
| hexiom                     | 6.17 ms                                                | 5.77 ms: 1.07x faster                                                     |
| typing_runtime_protocols   | 163 us                                                 | 153 us: 1.06x faster                                                      |
| pyflate                    | 448 ms                                                 | 421 ms: 1.06x faster                                                      |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                      |
| json_dumps                 | 10.4 ms                                                | 9.79 ms: 1.06x faster                                                     |
| html5lib                   | 63.6 ms                                                | 60.4 ms: 1.05x faster                                                     |
| pycparser                  | 1.17 sec                                               | 1.11 sec: 1.05x faster                                                    |
| genshi_xml                 | 50.2 ms                                                | 47.9 ms: 1.05x faster                                                     |
| scimark_lu                 | 114 ms                                                 | 109 ms: 1.05x faster                                                      |
| thrift                     | 791 us                                                 | 758 us: 1.04x faster                                                      |
| regex_effbot               | 3.17 ms                                                | 3.05 ms: 1.04x faster                                                     |
| docutils                   | 2.64 sec                                               | 2.55 sec: 1.04x faster                                                    |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.24 ms: 1.04x faster                                                     |
| deltablue                  | 3.45 ms                                                | 3.33 ms: 1.04x faster                                                     |
| unpickle_pure_python       | 221 us                                                 | 213 us: 1.03x faster                                                      |
| xml_etree_generate         | 85.2 ms                                                | 82.5 ms: 1.03x faster                                                     |
| meteor_contest             | 104 ms                                                 | 101 ms: 1.03x faster                                                      |
| coroutines                 | 23.9 ms                                                | 23.3 ms: 1.03x faster                                                     |
| xml_etree_process          | 59.0 ms                                                | 57.6 ms: 1.02x faster                                                     |
| nbody                      | 89.3 ms                                                | 88.1 ms: 1.01x faster                                                     |
| nqueens                    | 80.1 ms                                                | 79.3 ms: 1.01x faster                                                     |
| pickle_pure_python         | 308 us                                                 | 308 us: 1.00x slower                                                      |
| python_startup_no_site     | 7.16 ms                                                | 7.25 ms: 1.01x slower                                                     |
| sympy_expand               | 468 ms                                                 | 475 ms: 1.02x slower                                                      |
| tomli_loads                | 2.11 sec                                               | 2.18 sec: 1.03x slower                                                    |
| sqlite_synth               | 2.20 us                                                | 2.30 us: 1.05x slower                                                     |
| json_loads                 | 26.5 us                                                | 27.8 us: 1.05x slower                                                     |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                      |
| fannkuch                   | 372 ms                                                 | 395 ms: 1.06x slower                                                      |
| regex_v8                   | 20.6 ms                                                | 21.9 ms: 1.07x slower                                                     |
| pidigits                   | 184 ms                                                 | 198 ms: 1.07x slower                                                      |
| mako                       | 11.0 ms                                                | 11.8 ms: 1.08x slower                                                     |
| regex_dna                  | 168 ms                                                 | 190 ms: 1.13x slower                                                      |
| coverage                   | 71.4 ms                                                | 82.2 ms: 1.15x slower                                                     |
| gc_traversal               | 3.46 ms                                                | 4.18 ms: 1.21x slower                                                     |
| python_startup             | 9.93 ms                                                | 12.4 ms: 1.25x slower                                                     |
| bench_thread_pool          | 941 us                                                 | 1.31 ms: 1.39x slower                                                     |
| create_gc_cycles           | 1.09 ms                                                | 1.82 ms: 1.67x slower                                                     |
| telco                      | 6.53 ms                                                | 156 ms: 23.91x slower                                                     |
| bench_mp_pool              | 10.8 ms                                                | 329 ms: 30.46x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                              |

Benchmark hidden because not significant (2): json, django_template
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251211-3.15.0a2+-bc054db/bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.076x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.16x