# Results vs. 3.12.6

- fork: python
- ref: aa8578dc54df2af9daa3
- machine: linux-x86_64
- commit hash: aa8578d
- commit date: 2026-01-10
- overall geometric mean: 1.136x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 244 ms: 1.08x faster                                                   |
| docutils       | 2.64 sec                                               | 2.47 sec: 1.07x faster                                                 |
| html5lib       | 63.6 ms                                                | 56.6 ms: 1.12x faster                                                  |
| Geometric mean | (ref)                                                  | 1.09x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 519 ms: 2.08x faster                                                   |
| async_tree_none            | 464 ms                                                 | 229 ms: 2.03x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 279 ms: 1.99x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 557 ms: 1.99x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 230 ms: 1.94x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 289 ms: 1.93x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 456 ms: 1.59x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 457 ms: 1.57x faster                                                   |
| async_generators           | 384 ms                                                 | 317 ms: 1.21x faster                                                   |
| asyncio_tcp                | 519 ms                                                 | 449 ms: 1.15x faster                                                   |
| coroutines                 | 23.9 ms                                                | 22.6 ms: 1.06x faster                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.47 sec: 1.03x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.52x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 65.4 ms: 1.24x faster                                                  |
| nbody          | 89.3 ms                                                | 81.1 ms: 1.10x faster                                                  |
| pidigits       | 184 ms                                                 | 198 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                  | 1.08x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 117 ms: 1.21x faster                                                   |
| regex_effbot   | 3.17 ms                                                | 2.99 ms: 1.06x faster                                                  |
| regex_dna      | 168 ms                                                 | 182 ms: 1.09x slower                                                   |
| regex_v8       | 20.6 ms                                                | 22.9 ms: 1.11x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.74 sec: 1.21x faster                                                 |
| json_dumps           | 10.4 ms                                                | 9.04 ms: 1.15x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 88.0 ms: 1.10x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 201 us: 1.10x faster                                                   |
| xml_etree_process    | 59.0 ms                                                | 54.5 ms: 1.08x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 79.0 ms: 1.08x faster                                                  |
| unpickle_list        | 4.67 us                                                | 4.42 us: 1.06x faster                                                  |
| pickle_pure_python   | 308 us                                                 | 295 us: 1.04x faster                                                   |
| json_loads           | 26.5 us                                                | 26.0 us: 1.02x faster                                                  |
| pickle_dict          | 31.8 us                                                | 33.1 us: 1.04x slower                                                  |
| pickle_list          | 4.77 us                                                | 5.03 us: 1.06x slower                                                  |
| unpickle             | 14.1 us                                                | 15.0 us: 1.07x slower                                                  |
| xml_etree_parse      | 139 ms                                                 | 148 ms: 1.07x slower                                                   |
| pickle               | 10.9 us                                                | 12.9 us: 1.18x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.34 ms: 1.02x slower                                                  |
| python_startup         | 9.93 ms                                                | 12.4 ms: 1.25x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 19.3 ms: 1.18x faster                                                  |
| django_template | 34.7 ms                                                | 31.7 ms: 1.09x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 45.9 ms: 1.09x faster                                                  |
| mako            | 11.0 ms                                                | 11.4 ms: 1.03x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.08x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.09 sec: 2.22x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 519 ms: 2.08x faster                                                   |
| async_tree_none            | 464 ms                                                 | 229 ms: 2.03x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 279 ms: 1.99x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 557 ms: 1.99x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 230 ms: 1.94x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 289 ms: 1.93x faster                                                   |
| deepcopy                   | 352 us                                                 | 210 us: 1.68x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 24.6 us: 1.64x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 456 ms: 1.59x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 457 ms: 1.57x faster                                                   |
| go                         | 139 ms                                                 | 97.2 ms: 1.43x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.27 us: 1.35x faster                                                  |
| spectral_norm              | 110 ms                                                 | 81.6 ms: 1.35x faster                                                  |
| comprehensions             | 19.8 us                                                | 14.8 us: 1.34x faster                                                  |
| logging_silent             | 109 ns                                                 | 81.2 ns: 1.34x faster                                                  |
| scimark_fft                | 342 ms                                                 | 255 ms: 1.34x faster                                                   |
| scimark_sor                | 130 ms                                                 | 98.4 ms: 1.32x faster                                                  |
| pathlib                    | 21.5 ms                                                | 16.8 ms: 1.28x faster                                                  |
| raytrace                   | 299 ms                                                 | 234 ms: 1.28x faster                                                   |
| richards                   | 45.9 ms                                                | 36.4 ms: 1.26x faster                                                  |
| chaos                      | 62.8 ms                                                | 50.2 ms: 1.25x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 54.9 ms: 1.25x faster                                                  |
| richards_super             | 51.9 ms                                                | 41.7 ms: 1.24x faster                                                  |
| float                      | 80.8 ms                                                | 65.4 ms: 1.24x faster                                                  |
| deltablue                  | 3.45 ms                                                | 2.80 ms: 1.23x faster                                                  |
| async_generators           | 384 ms                                                 | 317 ms: 1.21x faster                                                   |
| regex_compile              | 142 ms                                                 | 117 ms: 1.21x faster                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 3.64 ms: 1.21x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.74 sec: 1.21x faster                                                 |
| logging_simple             | 6.63 us                                                | 5.52 us: 1.20x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 66.1 ms: 1.19x faster                                                  |
| generators                 | 32.2 ms                                                | 27.2 ms: 1.19x faster                                                  |
| genshi_text                | 22.8 ms                                                | 19.3 ms: 1.18x faster                                                  |
| logging_format             | 7.35 us                                                | 6.24 us: 1.18x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.03 sec: 1.17x faster                                                 |
| pyflate                    | 448 ms                                                 | 383 ms: 1.17x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 66.3 ms: 1.16x faster                                                  |
| pylint                     | 319 ms                                                 | 276 ms: 1.16x faster                                                   |
| asyncio_tcp                | 519 ms                                                 | 449 ms: 1.15x faster                                                   |
| scimark_lu                 | 114 ms                                                 | 99.1 ms: 1.15x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.36 ms: 1.15x faster                                                  |
| json_dumps                 | 10.4 ms                                                | 9.04 ms: 1.15x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 143 us: 1.14x faster                                                   |
| sympy_integrate            | 20.5 ms                                                | 18.2 ms: 1.13x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 147 ms: 1.13x faster                                                   |
| html5lib                   | 63.6 ms                                                | 56.6 ms: 1.12x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.36 sec: 1.11x faster                                                 |
| pprint_safe_repr           | 743 ms                                                 | 668 ms: 1.11x faster                                                   |
| sympy_str                  | 292 ms                                                 | 263 ms: 1.11x faster                                                   |
| nbody                      | 89.3 ms                                                | 81.1 ms: 1.10x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 88.0 ms: 1.10x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 201 us: 1.10x faster                                                   |
| django_template            | 34.7 ms                                                | 31.7 ms: 1.09x faster                                                  |
| genshi_xml                 | 50.2 ms                                                | 45.9 ms: 1.09x faster                                                  |
| xml_etree_process          | 59.0 ms                                                | 54.5 ms: 1.08x faster                                                  |
| thrift                     | 791 us                                                 | 733 us: 1.08x faster                                                   |
| 2to3                       | 264 ms                                                 | 244 ms: 1.08x faster                                                   |
| xml_etree_generate         | 85.2 ms                                                | 79.0 ms: 1.08x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.09 sec: 1.07x faster                                                 |
| docutils                   | 2.64 sec                                               | 2.47 sec: 1.07x faster                                                 |
| nqueens                    | 80.1 ms                                                | 75.3 ms: 1.06x faster                                                  |
| unpickle_list              | 4.67 us                                                | 4.42 us: 1.06x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.99 ms: 1.06x faster                                                  |
| coroutines                 | 23.9 ms                                                | 22.6 ms: 1.06x faster                                                  |
| sympy_expand               | 468 ms                                                 | 446 ms: 1.05x faster                                                   |
| pickle_pure_python         | 308 us                                                 | 295 us: 1.04x faster                                                   |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.47 sec: 1.03x faster                                                 |
| fannkuch                   | 372 ms                                                 | 364 ms: 1.02x faster                                                   |
| json_loads                 | 26.5 us                                                | 26.0 us: 1.02x faster                                                  |
| meteor_contest             | 104 ms                                                 | 102 ms: 1.01x faster                                                   |
| json                       | 5.02 ms                                                | 4.96 ms: 1.01x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.18 us: 1.01x faster                                                  |
| unpack_sequence            | 52.1 ns                                                | 52.4 ns: 1.01x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.34 ms: 1.02x slower                                                  |
| mako                       | 11.0 ms                                                | 11.4 ms: 1.03x slower                                                  |
| pickle_dict                | 31.8 us                                                | 33.1 us: 1.04x slower                                                  |
| coverage                   | 71.4 ms                                                | 74.7 ms: 1.05x slower                                                  |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                   |
| pickle_list                | 4.77 us                                                | 5.03 us: 1.06x slower                                                  |
| unpickle                   | 14.1 us                                                | 15.0 us: 1.07x slower                                                  |
| xml_etree_parse            | 139 ms                                                 | 148 ms: 1.07x slower                                                   |
| pidigits                   | 184 ms                                                 | 198 ms: 1.07x slower                                                   |
| regex_dna                  | 168 ms                                                 | 182 ms: 1.09x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 22.9 ms: 1.11x slower                                                  |
| pickle                     | 10.9 us                                                | 12.9 us: 1.18x slower                                                  |
| python_startup             | 9.93 ms                                                | 12.4 ms: 1.25x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.37 ms: 1.27x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.26 ms: 1.34x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 2.05 ms: 1.87x slower                                                  |
| telco                      | 6.53 ms                                                | 153 ms: 23.43x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 317 ms: 29.35x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.08x faster                                                           |
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20260110-3.15.0a3+-aa8578d-CLANG/bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.136x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.11x
- 95% likely to have a speedup of 1.11x
- 99% likely to have a speedup of 1.09x

# Memory
- memory change: 1.19x