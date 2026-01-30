# Results vs. 3.12.6

- fork: DinoV
- ref: lazy_review_updates2
- machine: linux-x86_64
- commit hash: 8fd3f20
- commit date: 2026-01-27
- overall geometric mean: 1.073x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5+-8fd3f20 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 249 ms: 1.06x faster                                                  |
| docutils       | 2.64 sec                                               | 2.58 sec: 1.02x faster                                                |
| html5lib       | 63.6 ms                                                | 61.3 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                  | 1.04x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5+-8fd3f20 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 566 ms: 1.96x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 295 ms: 1.90x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 574 ms: 1.89x faster                                                  |
| async_tree_none            | 464 ms                                                 | 248 ms: 1.87x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 300 ms: 1.85x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 246 ms: 1.81x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 486 ms: 1.49x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 483 ms: 1.48x faster                                                  |
| async_generators           | 384 ms                                                 | 342 ms: 1.12x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.53x faster                                                          |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5+-8fd3f20 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.0 ms: 1.15x faster                                                 |
| nbody          | 89.3 ms                                                | 91.0 ms: 1.02x slower                                                 |
| pidigits       | 184 ms                                                 | 193 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5+-8fd3f20 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 123 ms: 1.16x faster                                                  |
| regex_effbot   | 3.17 ms                                                | 2.93 ms: 1.08x faster                                                 |
| regex_v8       | 20.6 ms                                                | 21.8 ms: 1.06x slower                                                 |
| regex_dna      | 168 ms                                                 | 179 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5+-8fd3f20 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.83 sec: 1.15x faster                                                |
| xml_etree_iterparse  | 96.7 ms                                                | 84.8 ms: 1.14x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.05x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 209 us: 1.05x faster                                                  |
| json_dumps           | 10.4 ms                                                | 9.84 ms: 1.05x faster                                                 |
| xml_etree_generate   | 85.2 ms                                                | 83.4 ms: 1.02x faster                                                 |
| xml_etree_process    | 59.0 ms                                                | 58.0 ms: 1.02x faster                                                 |
| pickle_pure_python   | 308 us                                                 | 305 us: 1.01x faster                                                  |
| json_loads           | 26.5 us                                                | 28.3 us: 1.07x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.05x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5+-8fd3f20 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.34 ms: 1.02x slower                                                 |
| python_startup         | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5+-8fd3f20 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.5 ms: 1.06x faster                                                 |
| genshi_xml      | 50.2 ms                                                | 49.2 ms: 1.02x faster                                                 |
| django_template | 34.7 ms                                                | 35.1 ms: 1.01x slower                                                 |
| mako            | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.00x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5+-8fd3f20 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.16 sec: 2.08x faster                                                |
| async_tree_io_tg           | 1.11 sec                                               | 566 ms: 1.96x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 295 ms: 1.90x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 574 ms: 1.89x faster                                                  |
| async_tree_none            | 464 ms                                                 | 248 ms: 1.87x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 300 ms: 1.85x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 246 ms: 1.81x faster                                                  |
| deepcopy                   | 352 us                                                 | 229 us: 1.54x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 26.5 us: 1.52x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 486 ms: 1.49x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 483 ms: 1.48x faster                                                  |
| go                         | 139 ms                                                 | 106 ms: 1.31x faster                                                  |
| comprehensions             | 19.8 us                                                | 16.1 us: 1.23x faster                                                 |
| scimark_sor                | 130 ms                                                 | 106 ms: 1.22x faster                                                  |
| pathlib                    | 21.5 ms                                                | 17.7 ms: 1.22x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.54 us: 1.21x faster                                                 |
| raytrace                   | 299 ms                                                 | 251 ms: 1.19x faster                                                  |
| regex_compile              | 142 ms                                                 | 123 ms: 1.16x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 68.3 ms: 1.15x faster                                                 |
| float                      | 80.8 ms                                                | 70.0 ms: 1.15x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.83 sec: 1.15x faster                                                |
| xml_etree_iterparse        | 96.7 ms                                                | 84.8 ms: 1.14x faster                                                 |
| scimark_fft                | 342 ms                                                 | 300 ms: 1.14x faster                                                  |
| spectral_norm              | 110 ms                                                 | 96.9 ms: 1.14x faster                                                 |
| generators                 | 32.2 ms                                                | 28.4 ms: 1.14x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 67.8 ms: 1.13x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.21 sec: 1.12x faster                                                |
| async_generators           | 384 ms                                                 | 342 ms: 1.12x faster                                                  |
| chaos                      | 62.8 ms                                                | 56.1 ms: 1.12x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 61.6 ms: 1.11x faster                                                 |
| pylint                     | 319 ms                                                 | 287 ms: 1.11x faster                                                  |
| logging_simple             | 6.63 us                                                | 6.05 us: 1.10x faster                                                 |
| hexiom                     | 6.17 ms                                                | 5.65 ms: 1.09x faster                                                 |
| pyflate                    | 448 ms                                                 | 411 ms: 1.09x faster                                                  |
| logging_format             | 7.35 us                                                | 6.76 us: 1.09x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 19.0 ms: 1.08x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.93 ms: 1.08x faster                                                 |
| logging_silent             | 109 ns                                                 | 101 ns: 1.07x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 155 ms: 1.07x faster                                                  |
| richards                   | 45.9 ms                                                | 43.0 ms: 1.07x faster                                                 |
| pycparser                  | 1.17 sec                                               | 1.10 sec: 1.07x faster                                                |
| genshi_text                | 22.8 ms                                                | 21.5 ms: 1.06x faster                                                 |
| 2to3                       | 264 ms                                                 | 249 ms: 1.06x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.44 sec: 1.06x faster                                                |
| scimark_lu                 | 114 ms                                                 | 108 ms: 1.06x faster                                                  |
| sympy_str                  | 292 ms                                                 | 276 ms: 1.06x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.05x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 209 us: 1.05x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 706 ms: 1.05x faster                                                  |
| json_dumps                 | 10.4 ms                                                | 9.84 ms: 1.05x faster                                                 |
| deltablue                  | 3.45 ms                                                | 3.28 ms: 1.05x faster                                                 |
| richards_super             | 51.9 ms                                                | 49.7 ms: 1.04x faster                                                 |
| html5lib                   | 63.6 ms                                                | 61.3 ms: 1.04x faster                                                 |
| typing_runtime_protocols   | 163 us                                                 | 158 us: 1.04x faster                                                  |
| meteor_contest             | 104 ms                                                 | 101 ms: 1.03x faster                                                  |
| thrift                     | 791 us                                                 | 772 us: 1.02x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.58 sec: 1.02x faster                                                |
| xml_etree_generate         | 85.2 ms                                                | 83.4 ms: 1.02x faster                                                 |
| nqueens                    | 80.1 ms                                                | 78.5 ms: 1.02x faster                                                 |
| genshi_xml                 | 50.2 ms                                                | 49.2 ms: 1.02x faster                                                 |
| xml_etree_process          | 59.0 ms                                                | 58.0 ms: 1.02x faster                                                 |
| pickle_pure_python         | 308 us                                                 | 305 us: 1.01x faster                                                  |
| json                       | 5.02 ms                                                | 4.99 ms: 1.01x faster                                                 |
| django_template            | 34.7 ms                                                | 35.1 ms: 1.01x slower                                                 |
| nbody                      | 89.3 ms                                                | 91.0 ms: 1.02x slower                                                 |
| sqlite_synth               | 2.20 us                                                | 2.25 us: 1.02x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 7.34 ms: 1.02x slower                                                 |
| fannkuch                   | 372 ms                                                 | 382 ms: 1.03x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.51 ms: 1.03x slower                                                 |
| pidigits                   | 184 ms                                                 | 193 ms: 1.05x slower                                                  |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                  |
| sympy_expand               | 468 ms                                                 | 493 ms: 1.05x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 21.8 ms: 1.06x slower                                                 |
| json_loads                 | 26.5 us                                                | 28.3 us: 1.07x slower                                                 |
| regex_dna                  | 168 ms                                                 | 179 ms: 1.07x slower                                                  |
| mako                       | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                 |
| coverage                   | 71.4 ms                                                | 82.0 ms: 1.15x slower                                                 |
| python_startup             | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.42 ms: 1.28x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.32 ms: 1.40x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.87 ms: 1.71x slower                                                 |
| telco                      | 6.53 ms                                                | 160 ms: 24.58x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 269 ms: 24.92x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (1): coroutines
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260127-3.15.0a5+-8fd3f20/bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5+-8fd3f20.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.073x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.17x