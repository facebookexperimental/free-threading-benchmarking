# Results vs. 3.12.6

- fork: python
- ref: cebae977a63f32c3c03d
- machine: linux-x86_64
- commit hash: cebae97
- commit date: 2025-06-01
- overall geometric mean: 1.153x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 244 ms: 1.08x faster                                                  |
| docutils       | 2.64 sec                                               | 2.51 sec: 1.05x faster                                                |
| html5lib       | 63.6 ms                                                | 57.7 ms: 1.10x faster                                                 |
| Geometric mean | (ref)                                                  | 1.08x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 576 ms: 1.88x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 300 ms: 1.86x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 600 ms: 1.85x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 301 ms: 1.84x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 244 ms: 1.83x faster                                                  |
| async_tree_none            | 464 ms                                                 | 260 ms: 1.78x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 472 ms: 1.53x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 479 ms: 1.49x faster                                                  |
| async_generators           | 384 ms                                                 | 315 ms: 1.22x faster                                                  |
| coroutines                 | 23.9 ms                                                | 22.2 ms: 1.08x faster                                                 |
| asyncio_tcp                | 519 ms                                                 | 494 ms: 1.05x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 518 ms: 1.00x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.45x faster                                                          |

Benchmark hidden because not significant (1): asyncio_tcp_ssl

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 67.6 ms: 1.20x faster                                                 |
| nbody          | 89.3 ms                                                | 79.6 ms: 1.12x faster                                                 |
| pidigits       | 184 ms                                                 | 192 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                  | 1.09x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 120 ms: 1.19x faster                                                  |
| regex_effbot   | 3.17 ms                                                | 3.14 ms: 1.01x faster                                                 |
| regex_dna      | 168 ms                                                 | 189 ms: 1.13x slower                                                  |
| regex_v8       | 20.6 ms                                                | 23.4 ms: 1.14x slower                                                 |
| Geometric mean | (ref)                                                  | 1.02x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.82 sec: 1.16x faster                                                |
| unpickle_pure_python | 221 us                                                 | 199 us: 1.11x faster                                                  |
| unpickle_list        | 4.67 us                                                | 4.25 us: 1.10x faster                                                 |
| unpickle             | 14.1 us                                                | 13.2 us: 1.07x faster                                                 |
| json_loads           | 26.5 us                                                | 25.0 us: 1.06x faster                                                 |
| xml_etree_generate   | 85.2 ms                                                | 81.4 ms: 1.05x faster                                                 |
| pickle_pure_python   | 308 us                                                 | 294 us: 1.05x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 56.5 ms: 1.04x faster                                                 |
| pickle_dict          | 31.8 us                                                | 30.5 us: 1.04x faster                                                 |
| xml_etree_iterparse  | 96.7 ms                                                | 94.9 ms: 1.02x faster                                                 |
| pickle_list          | 4.77 us                                                | 4.70 us: 1.01x faster                                                 |
| json_dumps           | 10.4 ms                                                | 10.8 ms: 1.04x slower                                                 |
| xml_etree_parse      | 139 ms                                                 | 146 ms: 1.05x slower                                                  |
| pickle               | 10.9 us                                                | 12.7 us: 1.16x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.39 ms: 1.03x slower                                                 |
| python_startup         | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 19.3 ms: 1.18x faster                                                 |
| genshi_xml      | 50.2 ms                                                | 45.7 ms: 1.10x faster                                                 |
| django_template | 34.7 ms                                                | 32.8 ms: 1.06x faster                                                 |
| mako            | 11.0 ms                                                | 11.2 ms: 1.02x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.08x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.08 sec: 2.23x faster                                                |
| async_tree_io              | 1.08 sec                                               | 576 ms: 1.88x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 300 ms: 1.86x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 600 ms: 1.85x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 301 ms: 1.84x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 244 ms: 1.83x faster                                                  |
| async_tree_none            | 464 ms                                                 | 260 ms: 1.78x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 26.1 us: 1.54x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 472 ms: 1.53x faster                                                  |
| deepcopy                   | 352 us                                                 | 231 us: 1.52x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 479 ms: 1.49x faster                                                  |
| go                         | 139 ms                                                 | 96.7 ms: 1.44x faster                                                 |
| comprehensions             | 19.8 us                                                | 13.9 us: 1.43x faster                                                 |
| scimark_sor                | 130 ms                                                 | 100 ms: 1.30x faster                                                  |
| raytrace                   | 299 ms                                                 | 231 ms: 1.29x faster                                                  |
| spectral_norm              | 110 ms                                                 | 86.1 ms: 1.28x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.41 us: 1.28x faster                                                 |
| chaos                      | 62.8 ms                                                | 49.5 ms: 1.27x faster                                                 |
| richards                   | 45.9 ms                                                | 36.8 ms: 1.25x faster                                                 |
| scimark_fft                | 342 ms                                                 | 275 ms: 1.24x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 55.1 ms: 1.24x faster                                                 |
| async_generators           | 384 ms                                                 | 315 ms: 1.22x faster                                                  |
| richards_super             | 51.9 ms                                                | 42.8 ms: 1.21x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 65.7 ms: 1.20x faster                                                 |
| float                      | 80.8 ms                                                | 67.6 ms: 1.20x faster                                                 |
| deltablue                  | 3.45 ms                                                | 2.89 ms: 1.19x faster                                                 |
| regex_compile              | 142 ms                                                 | 120 ms: 1.19x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 3.98 sec: 1.19x faster                                                |
| hexiom                     | 6.17 ms                                                | 5.21 ms: 1.19x faster                                                 |
| genshi_text                | 22.8 ms                                                | 19.3 ms: 1.18x faster                                                 |
| pylint                     | 319 ms                                                 | 273 ms: 1.17x faster                                                  |
| pathlib                    | 21.5 ms                                                | 18.5 ms: 1.16x faster                                                 |
| generators                 | 32.2 ms                                                | 27.8 ms: 1.16x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.82 sec: 1.16x faster                                                |
| pyflate                    | 448 ms                                                 | 391 ms: 1.15x faster                                                  |
| crypto_pyaes               | 76.6 ms                                                | 66.9 ms: 1.15x faster                                                 |
| scimark_lu                 | 114 ms                                                 | 100 ms: 1.14x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 18.1 ms: 1.14x faster                                                 |
| typing_runtime_protocols   | 163 us                                                 | 144 us: 1.13x faster                                                  |
| sympy_str                  | 292 ms                                                 | 258 ms: 1.13x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 148 ms: 1.12x faster                                                  |
| nbody                      | 89.3 ms                                                | 79.6 ms: 1.12x faster                                                 |
| unpickle_pure_python       | 221 us                                                 | 199 us: 1.11x faster                                                  |
| html5lib                   | 63.6 ms                                                | 57.7 ms: 1.10x faster                                                 |
| unpickle_list              | 4.67 us                                                | 4.25 us: 1.10x faster                                                 |
| genshi_xml                 | 50.2 ms                                                | 45.7 ms: 1.10x faster                                                 |
| thrift                     | 791 us                                                 | 728 us: 1.09x faster                                                  |
| unpack_sequence            | 52.1 ns                                                | 47.9 ns: 1.09x faster                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.05 ms: 1.08x faster                                                 |
| nqueens                    | 80.1 ms                                                | 74.2 ms: 1.08x faster                                                 |
| sympy_expand               | 468 ms                                                 | 434 ms: 1.08x faster                                                  |
| 2to3                       | 264 ms                                                 | 244 ms: 1.08x faster                                                  |
| coroutines                 | 23.9 ms                                                | 22.2 ms: 1.08x faster                                                 |
| unpickle                   | 14.1 us                                                | 13.2 us: 1.07x faster                                                 |
| logging_simple             | 6.63 us                                                | 6.24 us: 1.06x faster                                                 |
| json_loads                 | 26.5 us                                                | 25.0 us: 1.06x faster                                                 |
| django_template            | 34.7 ms                                                | 32.8 ms: 1.06x faster                                                 |
| docutils                   | 2.64 sec                                               | 2.51 sec: 1.05x faster                                                |
| asyncio_tcp                | 519 ms                                                 | 494 ms: 1.05x faster                                                  |
| xml_etree_generate         | 85.2 ms                                                | 81.4 ms: 1.05x faster                                                 |
| pickle_pure_python         | 308 us                                                 | 294 us: 1.05x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.12 sec: 1.04x faster                                                |
| xml_etree_process          | 59.0 ms                                                | 56.5 ms: 1.04x faster                                                 |
| pickle_dict                | 31.8 us                                                | 30.5 us: 1.04x faster                                                 |
| logging_format             | 7.35 us                                                | 7.12 us: 1.03x faster                                                 |
| json                       | 5.02 ms                                                | 4.92 ms: 1.02x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 94.9 ms: 1.02x faster                                                 |
| fannkuch                   | 372 ms                                                 | 367 ms: 1.02x faster                                                  |
| meteor_contest             | 104 ms                                                 | 102 ms: 1.01x faster                                                  |
| pickle_list                | 4.77 us                                                | 4.70 us: 1.01x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 3.14 ms: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 518 ms: 1.00x slower                                                  |
| mako                       | 11.0 ms                                                | 11.2 ms: 1.02x slower                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.55 sec: 1.02x slower                                                |
| pprint_safe_repr           | 743 ms                                                 | 760 ms: 1.02x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.39 ms: 1.03x slower                                                 |
| telco                      | 6.53 ms                                                | 6.75 ms: 1.03x slower                                                 |
| pidigits                   | 184 ms                                                 | 192 ms: 1.04x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 10.8 ms: 1.04x slower                                                 |
| xml_etree_parse            | 139 ms                                                 | 146 ms: 1.05x slower                                                  |
| coverage                   | 71.4 ms                                                | 76.2 ms: 1.07x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.01 ms: 1.07x slower                                                 |
| regex_dna                  | 168 ms                                                 | 189 ms: 1.13x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 23.4 ms: 1.14x slower                                                 |
| pickle                     | 10.9 us                                                | 12.7 us: 1.16x slower                                                 |
| python_startup             | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.38 ms: 1.27x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.99 ms: 1.82x slower                                                 |
| logging_silent             | 109 ns                                                 | 476 ns: 4.37x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 97.3 ms: 9.01x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.09x faster                                                          |

Benchmark hidden because not significant (2): asyncio_tcp_ssl, sqlite_synth
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20250601-3.15.0a0-cebae97-CLANG/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.153x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.11x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.20x