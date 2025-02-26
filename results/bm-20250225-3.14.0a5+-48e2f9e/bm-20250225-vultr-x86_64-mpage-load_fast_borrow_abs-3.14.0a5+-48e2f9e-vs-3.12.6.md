# Results vs. 3.12.6

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: 48e2f9e
- commit date: 2025-02-25
- overall geometric mean: 1.112x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 250 ms: 1.06x faster                                                  |
| docutils       | 2.64 sec                                               | 2.53 sec: 1.04x faster                                                |
| Geometric mean | (ref)                                                  | 1.05x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 596 ms: 1.86x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 305 ms: 1.83x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 598 ms: 1.81x faster                                                  |
| async_tree_none            | 464 ms                                                 | 257 ms: 1.80x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 309 ms: 1.79x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 252 ms: 1.77x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 472 ms: 1.53x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 484 ms: 1.48x faster                                                  |
| async_generators           | 384 ms                                                 | 316 ms: 1.22x faster                                                  |
| coroutines                 | 23.9 ms                                                | 21.7 ms: 1.10x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.53x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.2 ms: 1.15x faster                                                 |
| nbody          | 89.3 ms                                                | 87.5 ms: 1.02x faster                                                 |
| pidigits       | 184 ms                                                 | 197 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 125 ms: 1.14x faster                                                  |
| regex_effbot   | 3.17 ms                                                | 2.87 ms: 1.10x faster                                                 |
| regex_dna      | 168 ms                                                 | 176 ms: 1.05x slower                                                  |
| regex_v8       | 20.6 ms                                                | 25.1 ms: 1.22x slower                                                 |
| Geometric mean | (ref)                                                  | 1.00x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.88 sec: 1.12x faster                                                |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.08x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 89.9 ms: 1.08x faster                                                 |
| unpickle_pure_python | 221 us                                                 | 208 us: 1.06x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 81.8 ms: 1.04x faster                                                 |
| xml_etree_process    | 59.0 ms                                                | 57.3 ms: 1.03x faster                                                 |
| pickle_pure_python   | 308 us                                                 | 302 us: 1.02x faster                                                  |
| json_dumps           | 10.4 ms                                                | 11.1 ms: 1.07x slower                                                 |
| json_loads           | 26.5 us                                                | 28.6 us: 1.08x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.52 ms: 1.05x slower                                                 |
| python_startup         | 9.93 ms                                                | 14.8 ms: 1.49x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.25x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.4 ms: 1.12x faster                                                 |
| genshi_xml      | 50.2 ms                                                | 46.4 ms: 1.08x faster                                                 |
| django_template | 34.7 ms                                                | 32.8 ms: 1.06x faster                                                 |
| mako            | 11.0 ms                                                | 11.4 ms: 1.04x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.05x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 596 ms: 1.86x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 305 ms: 1.83x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 598 ms: 1.81x faster                                                  |
| async_tree_none            | 464 ms                                                 | 257 ms: 1.80x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 309 ms: 1.79x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 252 ms: 1.77x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 472 ms: 1.53x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 484 ms: 1.48x faster                                                  |
| deepcopy                   | 352 us                                                 | 246 us: 1.43x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 28.7 us: 1.40x faster                                                 |
| go                         | 139 ms                                                 | 110 ms: 1.27x faster                                                  |
| comprehensions             | 19.8 us                                                | 15.8 us: 1.25x faster                                                 |
| async_generators           | 384 ms                                                 | 316 ms: 1.22x faster                                                  |
| generators                 | 32.2 ms                                                | 26.5 ms: 1.22x faster                                                 |
| spectral_norm              | 110 ms                                                 | 90.6 ms: 1.22x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.56 us: 1.20x faster                                                 |
| raytrace                   | 299 ms                                                 | 254 ms: 1.18x faster                                                  |
| chaos                      | 62.8 ms                                                | 53.7 ms: 1.17x faster                                                 |
| pylint                     | 319 ms                                                 | 273 ms: 1.17x faster                                                  |
| scimark_sor                | 130 ms                                                 | 112 ms: 1.16x faster                                                  |
| float                      | 80.8 ms                                                | 70.2 ms: 1.15x faster                                                 |
| pathlib                    | 21.5 ms                                                | 18.7 ms: 1.15x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 66.8 ms: 1.15x faster                                                 |
| logging_simple             | 6.63 us                                                | 5.78 us: 1.15x faster                                                 |
| regex_compile              | 142 ms                                                 | 125 ms: 1.14x faster                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 126 ms: 1.14x faster                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.2 ms: 1.14x faster                                                 |
| deltablue                  | 3.45 ms                                                | 3.04 ms: 1.13x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.18 sec: 1.13x faster                                                |
| logging_format             | 7.35 us                                                | 6.52 us: 1.13x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.88 sec: 1.12x faster                                                |
| genshi_text                | 22.8 ms                                                | 20.4 ms: 1.12x faster                                                 |
| richards                   | 45.9 ms                                                | 41.3 ms: 1.11x faster                                                 |
| thrift                     | 791 us                                                 | 714 us: 1.11x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.37 sec: 1.11x faster                                                |
| scimark_monte_carlo        | 68.4 ms                                                | 61.9 ms: 1.11x faster                                                 |
| pprint_safe_repr           | 743 ms                                                 | 673 ms: 1.10x faster                                                  |
| pyflate                    | 448 ms                                                 | 406 ms: 1.10x faster                                                  |
| coroutines                 | 23.9 ms                                                | 21.7 ms: 1.10x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.87 ms: 1.10x faster                                                 |
| richards_super             | 51.9 ms                                                | 47.1 ms: 1.10x faster                                                 |
| sympy_sum                  | 166 ms                                                 | 151 ms: 1.10x faster                                                  |
| scimark_fft                | 342 ms                                                 | 312 ms: 1.09x faster                                                  |
| sympy_str                  | 292 ms                                                 | 267 ms: 1.09x faster                                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.24 ms: 1.09x faster                                                 |
| sqlglot_transpile          | 1.67 ms                                                | 1.54 ms: 1.09x faster                                                 |
| typing_runtime_protocols   | 163 us                                                 | 151 us: 1.08x faster                                                  |
| genshi_xml                 | 50.2 ms                                                | 46.4 ms: 1.08x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.08x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 89.9 ms: 1.08x faster                                                 |
| hexiom                     | 6.17 ms                                                | 5.74 ms: 1.07x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 19.2 ms: 1.07x faster                                                 |
| pycparser                  | 1.17 sec                                               | 1.10 sec: 1.06x faster                                                |
| unpickle_pure_python       | 221 us                                                 | 208 us: 1.06x faster                                                  |
| nqueens                    | 80.1 ms                                                | 75.6 ms: 1.06x faster                                                 |
| django_template            | 34.7 ms                                                | 32.8 ms: 1.06x faster                                                 |
| 2to3                       | 264 ms                                                 | 250 ms: 1.06x faster                                                  |
| logging_silent             | 109 ns                                                 | 103 ns: 1.05x faster                                                  |
| sqlglot_normalize          | 107 ms                                                 | 101 ms: 1.05x faster                                                  |
| mdp                        | 2.42 sec                                               | 2.30 sec: 1.05x faster                                                |
| sqlglot_optimize           | 53.3 ms                                                | 50.7 ms: 1.05x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 75.4 ms: 1.05x faster                                                 |
| sympy_expand               | 468 ms                                                 | 449 ms: 1.04x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.53 sec: 1.04x faster                                                |
| xml_etree_generate         | 85.2 ms                                                | 81.8 ms: 1.04x faster                                                 |
| meteor_contest             | 104 ms                                                 | 100 ms: 1.03x faster                                                  |
| scimark_lu                 | 114 ms                                                 | 111 ms: 1.03x faster                                                  |
| xml_etree_process          | 59.0 ms                                                | 57.3 ms: 1.03x faster                                                 |
| nbody                      | 89.3 ms                                                | 87.5 ms: 1.02x faster                                                 |
| pickle_pure_python         | 308 us                                                 | 302 us: 1.02x faster                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.34 ms: 1.01x faster                                                 |
| fannkuch                   | 372 ms                                                 | 369 ms: 1.01x faster                                                  |
| mako                       | 11.0 ms                                                | 11.4 ms: 1.04x slower                                                 |
| regex_dna                  | 168 ms                                                 | 176 ms: 1.05x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.52 ms: 1.05x slower                                                 |
| pidigits                   | 184 ms                                                 | 197 ms: 1.07x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 11.1 ms: 1.07x slower                                                 |
| json_loads                 | 26.5 us                                                | 28.6 us: 1.08x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.03 ms: 1.09x slower                                                 |
| telco                      | 6.53 ms                                                | 7.21 ms: 1.10x slower                                                 |
| coverage                   | 71.4 ms                                                | 79.2 ms: 1.11x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 25.1 ms: 1.22x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.22 ms: 1.22x slower                                                 |
| python_startup             | 9.93 ms                                                | 14.8 ms: 1.49x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.84 ms: 1.68x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 88.0 ms: 8.15x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.08x faster                                                          |

Benchmark hidden because not significant (3): asyncio_websockets, json, sqlite_synth
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250225-3.14.0a5+-48e2f9e/bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.112x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.12x