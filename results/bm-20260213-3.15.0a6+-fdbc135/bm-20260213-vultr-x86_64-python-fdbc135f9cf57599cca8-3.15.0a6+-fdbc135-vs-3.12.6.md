# Results vs. 3.12.6

- fork: python
- ref: fdbc135f9cf57599cca8
- machine: linux-x86_64
- commit hash: fdbc135
- commit date: 2026-02-13
- overall geometric mean: 1.078x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260213-vultr-x86_64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 249 ms: 1.06x faster                                                   |
| docutils       | 2.64 sec                                               | 2.55 sec: 1.04x faster                                                 |
| html5lib       | 63.6 ms                                                | 58.9 ms: 1.08x faster                                                  |
| Geometric mean | (ref)                                                  | 1.06x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260213-vultr-x86_64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 558 ms: 1.99x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 294 ms: 1.91x faster                                                   |
| async_tree_none            | 464 ms                                                 | 247 ms: 1.88x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 580 ms: 1.87x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 300 ms: 1.85x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 248 ms: 1.80x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 486 ms: 1.47x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 494 ms: 1.46x faster                                                   |
| async_generators           | 384 ms                                                 | 340 ms: 1.13x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.3 ms: 1.03x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.53x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260213-vultr-x86_64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 69.6 ms: 1.16x faster                                                  |
| nbody          | 89.3 ms                                                | 88.2 ms: 1.01x faster                                                  |
| pidigits       | 184 ms                                                 | 193 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260213-vultr-x86_64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 121 ms: 1.18x faster                                                   |
| regex_effbot   | 3.17 ms                                                | 2.92 ms: 1.08x faster                                                  |
| regex_dna      | 168 ms                                                 | 185 ms: 1.10x slower                                                   |
| regex_v8       | 20.6 ms                                                | 23.1 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260213-vultr-x86_64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 84.5 ms: 1.14x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 1.86 sec: 1.13x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                   |
| unpickle_pure_python | 221 us                                                 | 209 us: 1.06x faster                                                   |
| json_dumps           | 10.4 ms                                                | 9.88 ms: 1.05x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 84.7 ms: 1.01x faster                                                  |
| pickle_pure_python   | 308 us                                                 | 309 us: 1.00x slower                                                   |
| json_loads           | 26.5 us                                                | 28.6 us: 1.08x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260213-vultr-x86_64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.34 ms: 1.02x slower                                                  |
| python_startup         | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260213-vultr-x86_64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text    | 22.8 ms                                                | 20.9 ms: 1.09x faster                                                  |
| genshi_xml     | 50.2 ms                                                | 49.5 ms: 1.01x faster                                                  |
| mako           | 11.0 ms                                                | 11.6 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260213-vultr-x86_64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.14 sec: 2.12x faster                                                 |
| async_tree_io_tg           | 1.11 sec                                               | 558 ms: 1.99x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 294 ms: 1.91x faster                                                   |
| async_tree_none            | 464 ms                                                 | 247 ms: 1.88x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 580 ms: 1.87x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 300 ms: 1.85x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 248 ms: 1.80x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 26.2 us: 1.54x faster                                                  |
| deepcopy                   | 352 us                                                 | 230 us: 1.53x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 486 ms: 1.47x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 494 ms: 1.46x faster                                                   |
| go                         | 139 ms                                                 | 104 ms: 1.34x faster                                                   |
| pathlib                    | 21.5 ms                                                | 17.4 ms: 1.24x faster                                                  |
| comprehensions             | 19.8 us                                                | 16.1 us: 1.24x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.52 us: 1.22x faster                                                  |
| scimark_sor                | 130 ms                                                 | 107 ms: 1.21x faster                                                   |
| raytrace                   | 299 ms                                                 | 251 ms: 1.19x faster                                                   |
| regex_compile              | 142 ms                                                 | 121 ms: 1.18x faster                                                   |
| spectral_norm              | 110 ms                                                 | 94.5 ms: 1.17x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 67.8 ms: 1.16x faster                                                  |
| float                      | 80.8 ms                                                | 69.6 ms: 1.16x faster                                                  |
| generators                 | 32.2 ms                                                | 27.9 ms: 1.16x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 84.5 ms: 1.14x faster                                                  |
| chaos                      | 62.8 ms                                                | 55.1 ms: 1.14x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.17 sec: 1.13x faster                                                 |
| logging_silent             | 109 ns                                                 | 96.0 ns: 1.13x faster                                                  |
| async_generators           | 384 ms                                                 | 340 ms: 1.13x faster                                                   |
| logging_simple             | 6.63 us                                                | 5.86 us: 1.13x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.86 sec: 1.13x faster                                                 |
| pylint                     | 319 ms                                                 | 282 ms: 1.13x faster                                                   |
| scimark_fft                | 342 ms                                                 | 304 ms: 1.12x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 68.2 ms: 1.12x faster                                                  |
| logging_format             | 7.35 us                                                | 6.58 us: 1.12x faster                                                  |
| richards                   | 45.9 ms                                                | 41.8 ms: 1.10x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.62 ms: 1.10x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 62.4 ms: 1.10x faster                                                  |
| genshi_text                | 22.8 ms                                                | 20.9 ms: 1.09x faster                                                  |
| pyflate                    | 448 ms                                                 | 412 ms: 1.09x faster                                                   |
| richards_super             | 51.9 ms                                                | 47.8 ms: 1.09x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.92 ms: 1.08x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.41 sec: 1.08x faster                                                 |
| html5lib                   | 63.6 ms                                                | 58.9 ms: 1.08x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 691 ms: 1.08x faster                                                   |
| sympy_integrate            | 20.5 ms                                                | 19.1 ms: 1.07x faster                                                  |
| scimark_lu                 | 114 ms                                                 | 107 ms: 1.07x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.09 sec: 1.07x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                   |
| sympy_str                  | 292 ms                                                 | 275 ms: 1.06x faster                                                   |
| 2to3                       | 264 ms                                                 | 249 ms: 1.06x faster                                                   |
| sympy_sum                  | 166 ms                                                 | 157 ms: 1.06x faster                                                   |
| unpickle_pure_python       | 221 us                                                 | 209 us: 1.06x faster                                                   |
| json_dumps                 | 10.4 ms                                                | 9.88 ms: 1.05x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.29 ms: 1.05x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 157 us: 1.04x faster                                                   |
| docutils                   | 2.64 sec                                               | 2.55 sec: 1.04x faster                                                 |
| meteor_contest             | 104 ms                                                 | 101 ms: 1.03x faster                                                   |
| thrift                     | 791 us                                                 | 770 us: 1.03x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.3 ms: 1.03x faster                                                  |
| genshi_xml                 | 50.2 ms                                                | 49.5 ms: 1.01x faster                                                  |
| nbody                      | 89.3 ms                                                | 88.2 ms: 1.01x faster                                                  |
| nqueens                    | 80.1 ms                                                | 79.1 ms: 1.01x faster                                                  |
| xml_etree_generate         | 85.2 ms                                                | 84.7 ms: 1.01x faster                                                  |
| pickle_pure_python         | 308 us                                                 | 309 us: 1.00x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.44 ms: 1.01x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.34 ms: 1.02x slower                                                  |
| sympy_expand               | 468 ms                                                 | 482 ms: 1.03x slower                                                   |
| json                       | 5.02 ms                                                | 5.20 ms: 1.04x slower                                                  |
| fannkuch                   | 372 ms                                                 | 388 ms: 1.04x slower                                                   |
| pidigits                   | 184 ms                                                 | 193 ms: 1.05x slower                                                   |
| mako                       | 11.0 ms                                                | 11.6 ms: 1.05x slower                                                  |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                   |
| json_loads                 | 26.5 us                                                | 28.6 us: 1.08x slower                                                  |
| regex_dna                  | 168 ms                                                 | 185 ms: 1.10x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 23.1 ms: 1.12x slower                                                  |
| coverage                   | 71.4 ms                                                | 81.4 ms: 1.14x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.25 ms: 1.23x slower                                                  |
| python_startup             | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.31 ms: 1.39x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.84 ms: 1.69x slower                                                  |
| telco                      | 6.53 ms                                                | 157 ms: 24.02x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 285 ms: 26.36x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (3): xml_etree_process, django_template, sqlite_synth
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260213-3.15.0a6+-fdbc135/bm-20260213-vultr-x86_64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.078x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.17x