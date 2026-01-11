# Results vs. 3.12.6

- fork: python
- ref: aa8578dc54df2af9daa3
- machine: linux-x86_64
- commit hash: aa8578d
- commit date: 2026-01-10
- overall geometric mean: 1.129x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 249 ms: 1.06x faster                                                   |
| docutils       | 2.64 sec                                               | 2.66 sec: 1.01x slower                                                 |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 542 ms: 2.00x faster                                                   |
| async_tree_none            | 464 ms                                                 | 236 ms: 1.97x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 585 ms: 1.90x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 239 ms: 1.86x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 300 ms: 1.85x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 303 ms: 1.85x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 486 ms: 1.49x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 482 ms: 1.48x faster                                                   |
| asyncio_tcp                | 519 ms                                                 | 449 ms: 1.15x faster                                                   |
| async_generators           | 384 ms                                                 | 356 ms: 1.08x faster                                                   |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.47 sec: 1.03x faster                                                 |
| coroutines                 | 23.9 ms                                                | 23.7 ms: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.45x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 56.7 ms: 1.43x faster                                                  |
| nbody          | 89.3 ms                                                | 72.9 ms: 1.23x faster                                                  |
| pidigits       | 184 ms                                                 | 205 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                  | 1.16x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.67 ms: 1.18x faster                                                  |
| regex_compile  | 142 ms                                                 | 121 ms: 1.18x faster                                                   |
| regex_dna      | 168 ms                                                 | 170 ms: 1.01x slower                                                   |
| regex_v8       | 20.6 ms                                                | 22.1 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                  | 1.07x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.66 sec: 1.27x faster                                                 |
| unpickle_pure_python | 221 us                                                 | 177 us: 1.24x faster                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 83.1 ms: 1.16x faster                                                  |
| json_dumps           | 10.4 ms                                                | 9.36 ms: 1.11x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 77.7 ms: 1.10x faster                                                  |
| pickle_pure_python   | 308 us                                                 | 281 us: 1.10x faster                                                   |
| xml_etree_process    | 59.0 ms                                                | 54.3 ms: 1.09x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                                   |
| pickle_dict          | 31.8 us                                                | 31.7 us: 1.00x faster                                                  |
| unpickle             | 14.1 us                                                | 14.7 us: 1.05x slower                                                  |
| pickle_list          | 4.77 us                                                | 5.07 us: 1.06x slower                                                  |
| json_loads           | 26.5 us                                                | 28.2 us: 1.06x slower                                                  |
| unpickle_list        | 4.67 us                                                | 5.15 us: 1.10x slower                                                  |
| pickle               | 10.9 us                                                | 12.6 us: 1.15x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.05x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.36 ms: 1.03x slower                                                  |
| python_startup         | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text    | 22.8 ms                                                | 20.8 ms: 1.10x faster                                                  |
| mako           | 11.0 ms                                                | 10.4 ms: 1.06x faster                                                  |
| genshi_xml     | 50.2 ms                                                | 52.2 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| richards                   | 45.9 ms                                                | 17.7 ms: 2.59x faster                                                  |
| richards_super             | 51.9 ms                                                | 21.6 ms: 2.40x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 542 ms: 2.00x faster                                                   |
| async_tree_none            | 464 ms                                                 | 236 ms: 1.97x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 585 ms: 1.90x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 239 ms: 1.86x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 300 ms: 1.85x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 303 ms: 1.85x faster                                                   |
| mdp                        | 2.42 sec                                               | 1.35 sec: 1.80x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 24.6 us: 1.64x faster                                                  |
| deepcopy                   | 352 us                                                 | 223 us: 1.57x faster                                                   |
| go                         | 139 ms                                                 | 91.9 ms: 1.52x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 486 ms: 1.49x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 482 ms: 1.48x faster                                                   |
| float                      | 80.8 ms                                                | 56.7 ms: 1.43x faster                                                  |
| spectral_norm              | 110 ms                                                 | 84.0 ms: 1.31x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 52.2 ms: 1.31x faster                                                  |
| scimark_fft                | 342 ms                                                 | 262 ms: 1.30x faster                                                   |
| logging_silent             | 109 ns                                                 | 83.7 ns: 1.30x faster                                                  |
| scimark_sor                | 130 ms                                                 | 99.9 ms: 1.30x faster                                                  |
| deltablue                  | 3.45 ms                                                | 2.69 ms: 1.28x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.66 sec: 1.27x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.43 us: 1.26x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 177 us: 1.24x faster                                                   |
| pyflate                    | 448 ms                                                 | 362 ms: 1.24x faster                                                   |
| comprehensions             | 19.8 us                                                | 16.1 us: 1.23x faster                                                  |
| nbody                      | 89.3 ms                                                | 72.9 ms: 1.23x faster                                                  |
| pathlib                    | 21.5 ms                                                | 17.8 ms: 1.21x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.67 ms: 1.18x faster                                                  |
| chaos                      | 62.8 ms                                                | 53.2 ms: 1.18x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 630 ms: 1.18x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.01 sec: 1.18x faster                                                 |
| regex_compile              | 142 ms                                                 | 121 ms: 1.18x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 83.1 ms: 1.16x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.31 sec: 1.16x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 66.1 ms: 1.16x faster                                                  |
| asyncio_tcp                | 519 ms                                                 | 449 ms: 1.15x faster                                                   |
| scimark_lu                 | 114 ms                                                 | 100 ms: 1.14x faster                                                   |
| raytrace                   | 299 ms                                                 | 264 ms: 1.13x faster                                                   |
| logging_simple             | 6.63 us                                                | 5.91 us: 1.12x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 70.6 ms: 1.12x faster                                                  |
| json_dumps                 | 10.4 ms                                                | 9.36 ms: 1.11x faster                                                  |
| logging_format             | 7.35 us                                                | 6.67 us: 1.10x faster                                                  |
| genshi_text                | 22.8 ms                                                | 20.8 ms: 1.10x faster                                                  |
| xml_etree_generate         | 85.2 ms                                                | 77.7 ms: 1.10x faster                                                  |
| pickle_pure_python         | 308 us                                                 | 281 us: 1.10x faster                                                   |
| xml_etree_process          | 59.0 ms                                                | 54.3 ms: 1.09x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                   |
| async_generators           | 384 ms                                                 | 356 ms: 1.08x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.08 sec: 1.08x faster                                                 |
| generators                 | 32.2 ms                                                | 30.0 ms: 1.07x faster                                                  |
| fannkuch                   | 372 ms                                                 | 350 ms: 1.06x faster                                                   |
| 2to3                       | 264 ms                                                 | 249 ms: 1.06x faster                                                   |
| thrift                     | 791 us                                                 | 749 us: 1.06x faster                                                   |
| mako                       | 11.0 ms                                                | 10.4 ms: 1.06x faster                                                  |
| meteor_contest             | 104 ms                                                 | 98.9 ms: 1.05x faster                                                  |
| pylint                     | 319 ms                                                 | 306 ms: 1.04x faster                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.26 ms: 1.03x faster                                                  |
| json                       | 5.02 ms                                                | 4.87 ms: 1.03x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 159 us: 1.03x faster                                                   |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.47 sec: 1.03x faster                                                 |
| hexiom                     | 6.17 ms                                                | 6.03 ms: 1.02x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 20.2 ms: 1.02x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.7 ms: 1.01x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.18 us: 1.01x faster                                                  |
| pickle_dict                | 31.8 us                                                | 31.7 us: 1.00x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.66 sec: 1.01x slower                                                 |
| regex_dna                  | 168 ms                                                 | 170 ms: 1.01x slower                                                   |
| sympy_sum                  | 166 ms                                                 | 168 ms: 1.01x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 7.36 ms: 1.03x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 52.2 ms: 1.04x slower                                                  |
| unpickle                   | 14.1 us                                                | 14.7 us: 1.05x slower                                                  |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                   |
| sympy_str                  | 292 ms                                                 | 307 ms: 1.05x slower                                                   |
| pickle_list                | 4.77 us                                                | 5.07 us: 1.06x slower                                                  |
| json_loads                 | 26.5 us                                                | 28.2 us: 1.06x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 22.1 ms: 1.07x slower                                                  |
| sympy_expand               | 468 ms                                                 | 507 ms: 1.08x slower                                                   |
| unpickle_list              | 4.67 us                                                | 5.15 us: 1.10x slower                                                  |
| pidigits                   | 184 ms                                                 | 205 ms: 1.11x slower                                                   |
| coverage                   | 71.4 ms                                                | 81.0 ms: 1.13x slower                                                  |
| pickle                     | 10.9 us                                                | 12.6 us: 1.15x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.24 ms: 1.23x slower                                                  |
| python_startup             | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                  |
| unpack_sequence            | 52.1 ns                                                | 69.0 ns: 1.33x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.31 ms: 1.39x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.94 ms: 1.78x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 239 ms: 22.10x slower                                                  |
| telco                      | 6.53 ms                                                | 162 ms: 24.88x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                           |

Benchmark hidden because not significant (3): nqueens, django_template, html5lib
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20260110-3.15.0a3+-aa8578d-JIT/bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.129x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.19x