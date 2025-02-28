# Results vs. 3.12.6

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: 0d98b60
- commit date: 2025-02-27
- overall geometric mean: 1.024x slower
- HPT reliability: 99.89%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-0d98b60 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 296 ms: 1.12x slower                                                  |
| docutils       | 2.64 sec                                               | 2.75 sec: 1.04x slower                                                |
| html5lib       | 63.6 ms                                                | 69.3 ms: 1.09x slower                                                 |
| Geometric mean | (ref)                                                  | 1.08x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-0d98b60 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 537 ms: 2.07x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 233 ms: 1.91x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 569 ms: 1.90x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 298 ms: 1.88x faster                                                  |
| async_tree_none            | 464 ms                                                 | 271 ms: 1.71x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 331 ms: 1.68x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 488 ms: 1.48x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 521 ms: 1.37x faster                                                  |
| async_generators           | 384 ms                                                 | 369 ms: 1.04x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 515 ms: 1.00x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.50x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-0d98b60 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.4 ms: 1.15x faster                                                 |
| pidigits       | 184 ms                                                 | 193 ms: 1.05x slower                                                  |
| nbody          | 89.3 ms                                                | 121 ms: 1.36x slower                                                  |
| Geometric mean | (ref)                                                  | 1.08x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-0d98b60 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.83 ms: 1.12x faster                                                 |
| regex_dna      | 168 ms                                                 | 172 ms: 1.02x slower                                                  |
| regex_compile  | 142 ms                                                 | 152 ms: 1.07x slower                                                  |
| regex_v8       | 20.6 ms                                                | 22.8 ms: 1.11x slower                                                 |
| Geometric mean | (ref)                                                  | 1.02x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-0d98b60 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.9 ms: 1.10x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.08x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 235 us: 1.07x slower                                                  |
| tomli_loads          | 2.11 sec                                               | 2.27 sec: 1.08x slower                                                |
| json_loads           | 26.5 us                                                | 28.9 us: 1.09x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 95.1 ms: 1.12x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 345 us: 1.12x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 68.1 ms: 1.16x slower                                                 |
| json_dumps           | 10.4 ms                                                | 12.7 ms: 1.22x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.07x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-0d98b60 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.61 ms: 1.34x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.6 ms: 1.57x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.45x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-0d98b60 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 57.6 ms: 1.15x slower                                                 |
| genshi_text     | 22.8 ms                                                | 26.7 ms: 1.17x slower                                                 |
| django_template | 34.7 ms                                                | 41.5 ms: 1.20x slower                                                 |
| mako            | 11.0 ms                                                | 15.6 ms: 1.41x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.23x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-0d98b60 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 537 ms: 2.07x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 1.71 ms: 2.02x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 233 ms: 1.91x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 569 ms: 1.90x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 298 ms: 1.88x faster                                                  |
| async_tree_none            | 464 ms                                                 | 271 ms: 1.71x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 331 ms: 1.68x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 488 ms: 1.48x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 521 ms: 1.37x faster                                                  |
| deepcopy                   | 352 us                                                 | 294 us: 1.20x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 35.0 us: 1.15x faster                                                 |
| float                      | 80.8 ms                                                | 70.4 ms: 1.15x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.83 ms: 1.12x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 87.9 ms: 1.10x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.6 ms: 1.10x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.02 us: 1.09x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.08x faster                                                  |
| go                         | 139 ms                                                 | 129 ms: 1.08x faster                                                  |
| async_generators           | 384 ms                                                 | 369 ms: 1.04x faster                                                  |
| comprehensions             | 19.8 us                                                | 19.2 us: 1.03x faster                                                 |
| logging_silent             | 109 ns                                                 | 106 ns: 1.03x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.63 sec: 1.02x faster                                                |
| spectral_norm              | 110 ms                                                 | 108 ms: 1.02x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 515 ms: 1.00x faster                                                  |
| generators                 | 32.2 ms                                                | 32.7 ms: 1.01x slower                                                 |
| regex_dna                  | 168 ms                                                 | 172 ms: 1.02x slower                                                  |
| scimark_sor                | 130 ms                                                 | 134 ms: 1.03x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.75 sec: 1.04x slower                                                |
| chaos                      | 62.8 ms                                                | 65.8 ms: 1.05x slower                                                 |
| deltablue                  | 3.45 ms                                                | 3.61 ms: 1.05x slower                                                 |
| pidigits                   | 184 ms                                                 | 193 ms: 1.05x slower                                                  |
| pyflate                    | 448 ms                                                 | 471 ms: 1.05x slower                                                  |
| dulwich_log                | 78.9 ms                                                | 83.1 ms: 1.05x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 792 ms: 1.07x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 235 us: 1.07x slower                                                  |
| regex_compile              | 142 ms                                                 | 152 ms: 1.07x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.63 sec: 1.07x slower                                                |
| logging_simple             | 6.63 us                                                | 7.12 us: 1.07x slower                                                 |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.5 ms: 1.08x slower                                                 |
| tomli_loads                | 2.11 sec                                               | 2.27 sec: 1.08x slower                                                |
| sqlglot_transpile          | 1.67 ms                                                | 1.82 ms: 1.09x slower                                                 |
| json_loads                 | 26.5 us                                                | 28.9 us: 1.09x slower                                                 |
| logging_format             | 7.35 us                                                | 7.99 us: 1.09x slower                                                 |
| html5lib                   | 63.6 ms                                                | 69.3 ms: 1.09x slower                                                 |
| sqlalchemy_declarative     | 143 ms                                                 | 156 ms: 1.09x slower                                                  |
| thrift                     | 791 us                                                 | 865 us: 1.09x slower                                                  |
| mdp                        | 2.42 sec                                               | 2.67 sec: 1.10x slower                                                |
| sqlglot_parse              | 1.36 ms                                                | 1.50 ms: 1.11x slower                                                 |
| sympy_sum                  | 166 ms                                                 | 184 ms: 1.11x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 22.8 ms: 1.11x slower                                                 |
| sqlglot_normalize          | 107 ms                                                 | 118 ms: 1.11x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 85.4 ms: 1.12x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 95.1 ms: 1.12x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 345 us: 1.12x slower                                                  |
| 2to3                       | 264 ms                                                 | 296 ms: 1.12x slower                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 60.0 ms: 1.13x slower                                                 |
| sympy_str                  | 292 ms                                                 | 332 ms: 1.14x slower                                                  |
| richards                   | 45.9 ms                                                | 52.4 ms: 1.14x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 23.5 ms: 1.14x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 57.6 ms: 1.15x slower                                                 |
| hexiom                     | 6.17 ms                                                | 7.12 ms: 1.15x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 68.1 ms: 1.16x slower                                                 |
| genshi_text                | 22.8 ms                                                | 26.7 ms: 1.17x slower                                                 |
| richards_super             | 51.9 ms                                                | 61.0 ms: 1.18x slower                                                 |
| sympy_expand               | 468 ms                                                 | 551 ms: 1.18x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.29 ms: 1.18x slower                                                 |
| django_template            | 34.7 ms                                                | 41.5 ms: 1.20x slower                                                 |
| nqueens                    | 80.1 ms                                                | 96.0 ms: 1.20x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 197 us: 1.20x slower                                                  |
| meteor_contest             | 104 ms                                                 | 126 ms: 1.22x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 12.7 ms: 1.22x slower                                                 |
| fannkuch                   | 372 ms                                                 | 465 ms: 1.25x slower                                                  |
| telco                      | 6.53 ms                                                | 8.41 ms: 1.29x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 88.4 ms: 1.29x slower                                                 |
| scimark_fft                | 342 ms                                                 | 450 ms: 1.32x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 153 ms: 1.34x slower                                                  |
| coverage                   | 71.4 ms                                                | 95.7 ms: 1.34x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 9.61 ms: 1.34x slower                                                 |
| nbody                      | 89.3 ms                                                | 121 ms: 1.36x slower                                                  |
| mako                       | 11.0 ms                                                | 15.6 ms: 1.41x slower                                                 |
| python_startup             | 9.93 ms                                                | 15.6 ms: 1.57x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 7.45 ms: 1.70x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.28 ms: 3.48x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 94.7 ms: 8.77x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.06x slower                                                          |

Benchmark hidden because not significant (5): pylint, json, pycparser, deepcopy_reduce, raytrace
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250227-3.14.0a5+-0d98b60-NOGIL/bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-0d98b60.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.024x slower

# HPT report

- Reliability score: 99.89% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.36x