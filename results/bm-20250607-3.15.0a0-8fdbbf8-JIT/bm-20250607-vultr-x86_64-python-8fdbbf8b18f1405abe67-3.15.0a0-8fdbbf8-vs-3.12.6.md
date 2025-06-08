# Results vs. 3.12.6

- fork: python
- ref: 8fdbbf8b18f1405abe67
- machine: linux-x86_64
- commit hash: 8fdbbf8
- commit date: 2025-06-07
- overall geometric mean: 1.117x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 255 ms: 1.03x faster                                                  |
| docutils       | 2.64 sec                                               | 2.58 sec: 1.02x faster                                                |
| html5lib       | 63.6 ms                                                | 61.3 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                  | 1.03x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 312 ms: 1.79x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 311 ms: 1.78x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 629 ms: 1.76x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 614 ms: 1.76x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 254 ms: 1.76x faster                                                  |
| async_tree_none            | 464 ms                                                 | 269 ms: 1.72x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 506 ms: 1.43x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 502 ms: 1.42x faster                                                  |
| async_generators           | 384 ms                                                 | 349 ms: 1.10x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.0 ms: 1.04x faster                                                 |
| asyncio_tcp                | 519 ms                                                 | 500 ms: 1.04x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 518 ms: 1.00x slower                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.51 sec: 1.00x slower                                                |
| Geometric mean             | (ref)                                                  | 1.39x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 64.2 ms: 1.26x faster                                                 |
| nbody          | 89.3 ms                                                | 85.1 ms: 1.05x faster                                                 |
| pidigits       | 184 ms                                                 | 208 ms: 1.13x slower                                                  |
| Geometric mean | (ref)                                                  | 1.05x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.60 ms: 1.22x faster                                                 |
| regex_compile  | 142 ms                                                 | 123 ms: 1.16x faster                                                  |
| regex_dna      | 168 ms                                                 | 168 ms: 1.00x slower                                                  |
| regex_v8       | 20.6 ms                                                | 21.5 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                  | 1.08x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.81 sec: 1.17x faster                                                |
| unpickle_pure_python | 221 us                                                 | 191 us: 1.15x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 78.4 ms: 1.09x faster                                                 |
| xml_etree_process    | 59.0 ms                                                | 54.5 ms: 1.08x faster                                                 |
| pickle_dict          | 31.8 us                                                | 29.9 us: 1.06x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 132 ms: 1.05x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 92.6 ms: 1.04x faster                                                 |
| unpickle_list        | 4.67 us                                                | 4.76 us: 1.02x slower                                                 |
| pickle_list          | 4.77 us                                                | 4.91 us: 1.03x slower                                                 |
| json_dumps           | 10.4 ms                                                | 10.8 ms: 1.04x slower                                                 |
| json_loads           | 26.5 us                                                | 28.1 us: 1.06x slower                                                 |
| pickle               | 10.9 us                                                | 12.0 us: 1.10x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (2): unpickle, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.34 ms: 1.02x slower                                                 |
| python_startup         | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.4 ms: 1.12x faster                                                 |
| genshi_xml      | 50.2 ms                                                | 48.2 ms: 1.04x faster                                                 |
| django_template | 34.7 ms                                                | 34.5 ms: 1.01x faster                                                 |
| mako            | 11.0 ms                                                | 11.1 ms: 1.01x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.04x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.16 sec: 2.09x faster                                                |
| async_tree_memoization_tg  | 560 ms                                                 | 312 ms: 1.79x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 311 ms: 1.78x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 629 ms: 1.76x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 614 ms: 1.76x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 254 ms: 1.76x faster                                                  |
| async_tree_none            | 464 ms                                                 | 269 ms: 1.72x faster                                                  |
| richards                   | 45.9 ms                                                | 31.8 ms: 1.45x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 506 ms: 1.43x faster                                                  |
| richards_super             | 51.9 ms                                                | 36.4 ms: 1.43x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 502 ms: 1.42x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 28.9 us: 1.40x faster                                                 |
| deepcopy                   | 352 us                                                 | 253 us: 1.39x faster                                                  |
| float                      | 80.8 ms                                                | 64.2 ms: 1.26x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.60 ms: 1.22x faster                                                 |
| scimark_sor                | 130 ms                                                 | 108 ms: 1.20x faster                                                  |
| deltablue                  | 3.45 ms                                                | 2.87 ms: 1.20x faster                                                 |
| spectral_norm              | 110 ms                                                 | 92.1 ms: 1.20x faster                                                 |
| raytrace                   | 299 ms                                                 | 251 ms: 1.19x faster                                                  |
| comprehensions             | 19.8 us                                                | 16.7 us: 1.19x faster                                                 |
| go                         | 139 ms                                                 | 118 ms: 1.18x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.03 sec: 1.17x faster                                                |
| scimark_fft                | 342 ms                                                 | 292 ms: 1.17x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.64 us: 1.17x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.81 sec: 1.17x faster                                                |
| dulwich_log                | 78.9 ms                                                | 67.7 ms: 1.16x faster                                                 |
| regex_compile              | 142 ms                                                 | 123 ms: 1.16x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 191 us: 1.15x faster                                                  |
| generators                 | 32.2 ms                                                | 28.3 ms: 1.14x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 60.1 ms: 1.14x faster                                                 |
| pyflate                    | 448 ms                                                 | 395 ms: 1.13x faster                                                  |
| pylint                     | 319 ms                                                 | 282 ms: 1.13x faster                                                  |
| genshi_text                | 22.8 ms                                                | 20.4 ms: 1.12x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 68.6 ms: 1.12x faster                                                 |
| chaos                      | 62.8 ms                                                | 56.4 ms: 1.11x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.5 ms: 1.11x faster                                                 |
| async_generators           | 384 ms                                                 | 349 ms: 1.10x faster                                                  |
| xml_etree_generate         | 85.2 ms                                                | 78.4 ms: 1.09x faster                                                 |
| xml_etree_process          | 59.0 ms                                                | 54.5 ms: 1.08x faster                                                 |
| sympy_sum                  | 166 ms                                                 | 154 ms: 1.08x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 19.1 ms: 1.08x faster                                                 |
| thrift                     | 791 us                                                 | 738 us: 1.07x faster                                                  |
| sympy_str                  | 292 ms                                                 | 274 ms: 1.07x faster                                                  |
| pickle_dict                | 31.8 us                                                | 29.9 us: 1.06x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 132 ms: 1.05x faster                                                  |
| scimark_lu                 | 114 ms                                                 | 109 ms: 1.05x faster                                                  |
| nbody                      | 89.3 ms                                                | 85.1 ms: 1.05x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 92.6 ms: 1.04x faster                                                 |
| genshi_xml                 | 50.2 ms                                                | 48.2 ms: 1.04x faster                                                 |
| coroutines                 | 23.9 ms                                                | 23.0 ms: 1.04x faster                                                 |
| html5lib                   | 63.6 ms                                                | 61.3 ms: 1.04x faster                                                 |
| typing_runtime_protocols   | 163 us                                                 | 158 us: 1.04x faster                                                  |
| asyncio_tcp                | 519 ms                                                 | 500 ms: 1.04x faster                                                  |
| 2to3                       | 264 ms                                                 | 255 ms: 1.03x faster                                                  |
| logging_simple             | 6.63 us                                                | 6.42 us: 1.03x faster                                                 |
| nqueens                    | 80.1 ms                                                | 77.7 ms: 1.03x faster                                                 |
| pycparser                  | 1.17 sec                                               | 1.14 sec: 1.03x faster                                                |
| meteor_contest             | 104 ms                                                 | 101 ms: 1.03x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.58 sec: 1.02x faster                                                |
| hexiom                     | 6.17 ms                                                | 6.07 ms: 1.02x faster                                                 |
| logging_format             | 7.35 us                                                | 7.23 us: 1.02x faster                                                 |
| fannkuch                   | 372 ms                                                 | 367 ms: 1.01x faster                                                  |
| django_template            | 34.7 ms                                                | 34.5 ms: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 518 ms: 1.00x slower                                                  |
| regex_dna                  | 168 ms                                                 | 168 ms: 1.00x slower                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.51 sec: 1.00x slower                                                |
| mako                       | 11.0 ms                                                | 11.1 ms: 1.01x slower                                                 |
| json                       | 5.02 ms                                                | 5.11 ms: 1.02x slower                                                 |
| unpickle_list              | 4.67 us                                                | 4.76 us: 1.02x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.48 ms: 1.02x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 7.34 ms: 1.02x slower                                                 |
| pickle_list                | 4.77 us                                                | 4.91 us: 1.03x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 10.8 ms: 1.04x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 21.5 ms: 1.04x slower                                                 |
| json_loads                 | 26.5 us                                                | 28.1 us: 1.06x slower                                                 |
| telco                      | 6.53 ms                                                | 6.98 ms: 1.07x slower                                                 |
| pickle                     | 10.9 us                                                | 12.0 us: 1.10x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.04 ms: 1.11x slower                                                 |
| pidigits                   | 184 ms                                                 | 208 ms: 1.13x slower                                                  |
| coverage                   | 71.4 ms                                                | 81.6 ms: 1.14x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 853 ms: 1.15x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.76 sec: 1.16x slower                                                |
| unpack_sequence            | 52.1 ns                                                | 60.6 ns: 1.16x slower                                                 |
| python_startup             | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.50 ms: 1.30x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.92 ms: 1.76x slower                                                 |
| logging_silent             | 109 ns                                                 | 468 ns: 4.29x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 98.4 ms: 9.11x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                          |

Benchmark hidden because not significant (4): unpickle, sympy_expand, pickle_pure_python, sqlite_synth
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20250607-3.15.0a0-8fdbbf8-JIT/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.117x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.17x