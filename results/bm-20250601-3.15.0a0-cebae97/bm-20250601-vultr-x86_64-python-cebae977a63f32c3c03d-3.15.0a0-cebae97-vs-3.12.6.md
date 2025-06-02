# Results vs. 3.12.6

- fork: python
- ref: cebae977a63f32c3c03d
- machine: linux-x86_64
- commit hash: cebae97
- commit date: 2025-06-01
- overall geometric mean: 1.096x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 254 ms: 1.04x faster                                                  |
| docutils       | 2.64 sec                                               | 2.56 sec: 1.03x faster                                                |
| html5lib       | 63.6 ms                                                | 61.7 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                  | 1.03x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 603 ms: 1.80x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 313 ms: 1.79x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 628 ms: 1.77x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 316 ms: 1.76x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 255 ms: 1.75x faster                                                  |
| async_tree_none            | 464 ms                                                 | 275 ms: 1.69x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 507 ms: 1.42x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 518 ms: 1.38x faster                                                  |
| async_generators           | 384 ms                                                 | 342 ms: 1.12x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 519 ms: 1.00x slower                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.54 sec: 1.02x slower                                                |
| Geometric mean             | (ref)                                                  | 1.38x faster                                                          |

Benchmark hidden because not significant (2): asyncio_tcp, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 72.4 ms: 1.12x faster                                                 |
| nbody          | 89.3 ms                                                | 88.3 ms: 1.01x faster                                                 |
| pidigits       | 184 ms                                                 | 199 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.55 ms: 1.24x faster                                                 |
| regex_compile  | 142 ms                                                 | 124 ms: 1.15x faster                                                  |
| regex_dna      | 168 ms                                                 | 166 ms: 1.01x faster                                                  |
| regex_v8       | 20.6 ms                                                | 21.0 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                  | 1.09x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.95 sec: 1.08x faster                                                |
| unpickle_pure_python | 221 us                                                 | 209 us: 1.05x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 134 ms: 1.03x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 83.6 ms: 1.02x faster                                                 |
| pickle_dict          | 31.8 us                                                | 31.5 us: 1.01x faster                                                 |
| xml_etree_process    | 59.0 ms                                                | 58.7 ms: 1.01x faster                                                 |
| pickle_pure_python   | 308 us                                                 | 308 us: 1.00x slower                                                  |
| unpickle             | 14.1 us                                                | 14.2 us: 1.01x slower                                                 |
| pickle_list          | 4.77 us                                                | 4.93 us: 1.03x slower                                                 |
| json_dumps           | 10.4 ms                                                | 10.7 ms: 1.04x slower                                                 |
| unpickle_list        | 4.67 us                                                | 5.03 us: 1.08x slower                                                 |
| json_loads           | 26.5 us                                                | 29.2 us: 1.10x slower                                                 |
| pickle               | 10.9 us                                                | 12.5 us: 1.14x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.54 ms: 1.05x slower                                                 |
| python_startup         | 9.93 ms                                                | 12.8 ms: 1.29x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.17x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text    | 22.8 ms                                                | 20.8 ms: 1.10x faster                                                 |
| genshi_xml     | 50.2 ms                                                | 48.0 ms: 1.04x faster                                                 |
| mako           | 11.0 ms                                                | 11.9 ms: 1.08x slower                                                 |
| Geometric mean | (ref)                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.20 sec: 2.01x faster                                                |
| async_tree_io              | 1.08 sec                                               | 603 ms: 1.80x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 313 ms: 1.79x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 628 ms: 1.77x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 316 ms: 1.76x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 255 ms: 1.75x faster                                                  |
| async_tree_none            | 464 ms                                                 | 275 ms: 1.69x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 507 ms: 1.42x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 28.9 us: 1.39x faster                                                 |
| deepcopy                   | 352 us                                                 | 253 us: 1.39x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 518 ms: 1.38x faster                                                  |
| go                         | 139 ms                                                 | 105 ms: 1.32x faster                                                  |
| comprehensions             | 19.8 us                                                | 15.7 us: 1.26x faster                                                 |
| unpack_sequence            | 52.1 ns                                                | 41.3 ns: 1.26x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.55 ms: 1.24x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 66.5 ms: 1.19x faster                                                 |
| raytrace                   | 299 ms                                                 | 253 ms: 1.18x faster                                                  |
| scimark_sor                | 130 ms                                                 | 111 ms: 1.16x faster                                                  |
| regex_compile              | 142 ms                                                 | 124 ms: 1.15x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.69 us: 1.14x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.19 sec: 1.13x faster                                                |
| async_generators           | 384 ms                                                 | 342 ms: 1.12x faster                                                  |
| crypto_pyaes               | 76.6 ms                                                | 68.2 ms: 1.12x faster                                                 |
| richards                   | 45.9 ms                                                | 40.9 ms: 1.12x faster                                                 |
| pylint                     | 319 ms                                                 | 285 ms: 1.12x faster                                                  |
| float                      | 80.8 ms                                                | 72.4 ms: 1.12x faster                                                 |
| richards_super             | 51.9 ms                                                | 46.5 ms: 1.12x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 61.4 ms: 1.12x faster                                                 |
| chaos                      | 62.8 ms                                                | 56.6 ms: 1.11x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.6 ms: 1.10x faster                                                 |
| hexiom                     | 6.17 ms                                                | 5.63 ms: 1.10x faster                                                 |
| genshi_text                | 22.8 ms                                                | 20.8 ms: 1.10x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 18.9 ms: 1.09x faster                                                 |
| sympy_str                  | 292 ms                                                 | 268 ms: 1.09x faster                                                  |
| pyflate                    | 448 ms                                                 | 413 ms: 1.09x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.95 sec: 1.08x faster                                                |
| spectral_norm              | 110 ms                                                 | 102 ms: 1.08x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 154 ms: 1.07x faster                                                  |
| generators                 | 32.2 ms                                                | 30.1 ms: 1.07x faster                                                 |
| typing_runtime_protocols   | 163 us                                                 | 154 us: 1.06x faster                                                  |
| thrift                     | 791 us                                                 | 745 us: 1.06x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 209 us: 1.05x faster                                                  |
| nqueens                    | 80.1 ms                                                | 75.9 ms: 1.05x faster                                                 |
| meteor_contest             | 104 ms                                                 | 98.6 ms: 1.05x faster                                                 |
| genshi_xml                 | 50.2 ms                                                | 48.0 ms: 1.04x faster                                                 |
| deltablue                  | 3.45 ms                                                | 3.31 ms: 1.04x faster                                                 |
| sympy_expand               | 468 ms                                                 | 450 ms: 1.04x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.04x faster                                                |
| 2to3                       | 264 ms                                                 | 254 ms: 1.04x faster                                                  |
| scimark_lu                 | 114 ms                                                 | 110 ms: 1.03x faster                                                  |
| html5lib                   | 63.6 ms                                                | 61.7 ms: 1.03x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 134 ms: 1.03x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.56 sec: 1.03x faster                                                |
| xml_etree_generate         | 85.2 ms                                                | 83.6 ms: 1.02x faster                                                 |
| regex_dna                  | 168 ms                                                 | 166 ms: 1.01x faster                                                  |
| nbody                      | 89.3 ms                                                | 88.3 ms: 1.01x faster                                                 |
| pickle_dict                | 31.8 us                                                | 31.5 us: 1.01x faster                                                 |
| xml_etree_process          | 59.0 ms                                                | 58.7 ms: 1.01x faster                                                 |
| pickle_pure_python         | 308 us                                                 | 308 us: 1.00x slower                                                  |
| asyncio_websockets         | 517 ms                                                 | 519 ms: 1.00x slower                                                  |
| logging_format             | 7.35 us                                                | 7.39 us: 1.01x slower                                                 |
| fannkuch                   | 372 ms                                                 | 375 ms: 1.01x slower                                                  |
| unpickle                   | 14.1 us                                                | 14.2 us: 1.01x slower                                                 |
| sqlite_synth               | 2.20 us                                                | 2.23 us: 1.02x slower                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.54 sec: 1.02x slower                                                |
| regex_v8                   | 20.6 ms                                                | 21.0 ms: 1.02x slower                                                 |
| pickle_list                | 4.77 us                                                | 4.93 us: 1.03x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 10.7 ms: 1.04x slower                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.58 sec: 1.04x slower                                                |
| json                       | 5.02 ms                                                | 5.22 ms: 1.04x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 773 ms: 1.04x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.54 ms: 1.05x slower                                                 |
| unpickle_list              | 4.67 us                                                | 5.03 us: 1.08x slower                                                 |
| pidigits                   | 184 ms                                                 | 199 ms: 1.08x slower                                                  |
| mako                       | 11.0 ms                                                | 11.9 ms: 1.08x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.80 ms: 1.09x slower                                                 |
| json_loads                 | 26.5 us                                                | 29.2 us: 1.10x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.05 ms: 1.11x slower                                                 |
| telco                      | 6.53 ms                                                | 7.31 ms: 1.12x slower                                                 |
| pickle                     | 10.9 us                                                | 12.5 us: 1.14x slower                                                 |
| coverage                   | 71.4 ms                                                | 82.7 ms: 1.16x slower                                                 |
| python_startup             | 9.93 ms                                                | 12.8 ms: 1.29x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.56 ms: 1.32x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 2.03 ms: 1.86x slower                                                 |
| logging_silent             | 109 ns                                                 | 469 ns: 4.30x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 101 ms: 9.36x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (6): asyncio_tcp, scimark_fft, xml_etree_iterparse, logging_simple, django_template, coroutines
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20250601-3.15.0a0-cebae97/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.096x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.15x