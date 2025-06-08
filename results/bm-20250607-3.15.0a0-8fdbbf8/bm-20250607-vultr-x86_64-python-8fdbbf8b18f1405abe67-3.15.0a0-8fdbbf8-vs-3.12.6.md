# Results vs. 3.12.6

- fork: python
- ref: 8fdbbf8b18f1405abe67
- machine: linux-x86_64
- commit hash: 8fdbbf8
- commit date: 2025-06-07
- overall geometric mean: 1.102x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 250 ms: 1.05x faster                                                  |
| docutils       | 2.64 sec                                               | 2.54 sec: 1.04x faster                                                |
| html5lib       | 63.6 ms                                                | 61.1 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                  | 1.04x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 306 ms: 1.83x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 593 ms: 1.83x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 307 ms: 1.81x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 623 ms: 1.78x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 251 ms: 1.77x faster                                                  |
| async_tree_none            | 464 ms                                                 | 270 ms: 1.72x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 514 ms: 1.41x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 521 ms: 1.37x faster                                                  |
| async_generators           | 384 ms                                                 | 340 ms: 1.13x faster                                                  |
| asyncio_tcp                | 519 ms                                                 | 500 ms: 1.04x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.1 ms: 1.04x faster                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.51 sec: 1.00x slower                                                |
| Geometric mean             | (ref)                                                  | 1.40x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 71.8 ms: 1.13x faster                                                 |
| nbody          | 89.3 ms                                                | 87.5 ms: 1.02x faster                                                 |
| pidigits       | 184 ms                                                 | 197 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 124 ms: 1.15x faster                                                  |
| regex_effbot   | 3.17 ms                                                | 2.88 ms: 1.10x faster                                                 |
| regex_dna      | 168 ms                                                 | 176 ms: 1.05x slower                                                  |
| regex_v8       | 20.6 ms                                                | 23.0 ms: 1.12x slower                                                 |
| Geometric mean | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.95 sec: 1.08x faster                                                |
| unpickle_pure_python | 221 us                                                 | 208 us: 1.06x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 92.4 ms: 1.05x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 133 ms: 1.04x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 83.3 ms: 1.02x faster                                                 |
| unpickle             | 14.1 us                                                | 13.8 us: 1.02x faster                                                 |
| xml_etree_process    | 59.0 ms                                                | 58.5 ms: 1.01x faster                                                 |
| pickle_dict          | 31.8 us                                                | 32.4 us: 1.02x slower                                                 |
| json_dumps           | 10.4 ms                                                | 10.9 ms: 1.05x slower                                                 |
| unpickle_list        | 4.67 us                                                | 5.00 us: 1.07x slower                                                 |
| pickle_list          | 4.77 us                                                | 5.14 us: 1.08x slower                                                 |
| json_loads           | 26.5 us                                                | 29.1 us: 1.10x slower                                                 |
| pickle               | 10.9 us                                                | 12.2 us: 1.11x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.33 ms: 1.02x slower                                                 |
| python_startup         | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text    | 22.8 ms                                                | 20.5 ms: 1.11x faster                                                 |
| genshi_xml     | 50.2 ms                                                | 48.4 ms: 1.04x faster                                                 |
| mako           | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                 |
| Geometric mean | (ref)                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.15 sec: 2.10x faster                                                |
| async_tree_memoization_tg  | 560 ms                                                 | 306 ms: 1.83x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 593 ms: 1.83x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 307 ms: 1.81x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 623 ms: 1.78x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 251 ms: 1.77x faster                                                  |
| async_tree_none            | 464 ms                                                 | 270 ms: 1.72x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 514 ms: 1.41x faster                                                  |
| deepcopy                   | 352 us                                                 | 252 us: 1.39x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 28.9 us: 1.39x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 521 ms: 1.37x faster                                                  |
| go                         | 139 ms                                                 | 105 ms: 1.32x faster                                                  |
| comprehensions             | 19.8 us                                                | 15.7 us: 1.26x faster                                                 |
| unpack_sequence            | 52.1 ns                                                | 41.8 ns: 1.24x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 66.4 ms: 1.19x faster                                                 |
| raytrace                   | 299 ms                                                 | 253 ms: 1.18x faster                                                  |
| scimark_sor                | 130 ms                                                 | 111 ms: 1.17x faster                                                  |
| generators                 | 32.2 ms                                                | 27.7 ms: 1.16x faster                                                 |
| regex_compile              | 142 ms                                                 | 124 ms: 1.15x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.67 us: 1.15x faster                                                 |
| pylint                     | 319 ms                                                 | 278 ms: 1.15x faster                                                  |
| crypto_pyaes               | 76.6 ms                                                | 67.3 ms: 1.14x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.16 sec: 1.14x faster                                                |
| async_generators           | 384 ms                                                 | 340 ms: 1.13x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.46 ms: 1.13x faster                                                 |
| float                      | 80.8 ms                                                | 71.8 ms: 1.13x faster                                                 |
| richards_super             | 51.9 ms                                                | 46.3 ms: 1.12x faster                                                 |
| richards                   | 45.9 ms                                                | 41.1 ms: 1.12x faster                                                 |
| genshi_text                | 22.8 ms                                                | 20.5 ms: 1.11x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.5 ms: 1.11x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 62.0 ms: 1.10x faster                                                 |
| pyflate                    | 448 ms                                                 | 406 ms: 1.10x faster                                                  |
| chaos                      | 62.8 ms                                                | 57.0 ms: 1.10x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.88 ms: 1.10x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 18.8 ms: 1.09x faster                                                 |
| sympy_str                  | 292 ms                                                 | 267 ms: 1.09x faster                                                  |
| spectral_norm              | 110 ms                                                 | 101 ms: 1.09x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 153 ms: 1.08x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.95 sec: 1.08x faster                                                |
| thrift                     | 791 us                                                 | 735 us: 1.08x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.23 ms: 1.07x faster                                                 |
| typing_runtime_protocols   | 163 us                                                 | 153 us: 1.07x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 208 us: 1.06x faster                                                  |
| nqueens                    | 80.1 ms                                                | 75.8 ms: 1.06x faster                                                 |
| 2to3                       | 264 ms                                                 | 250 ms: 1.05x faster                                                  |
| meteor_contest             | 104 ms                                                 | 98.7 ms: 1.05x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 92.4 ms: 1.05x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 133 ms: 1.04x faster                                                  |
| html5lib                   | 63.6 ms                                                | 61.1 ms: 1.04x faster                                                 |
| scimark_lu                 | 114 ms                                                 | 110 ms: 1.04x faster                                                  |
| sympy_expand               | 468 ms                                                 | 450 ms: 1.04x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.54 sec: 1.04x faster                                                |
| asyncio_tcp                | 519 ms                                                 | 500 ms: 1.04x faster                                                  |
| genshi_xml                 | 50.2 ms                                                | 48.4 ms: 1.04x faster                                                 |
| coroutines                 | 23.9 ms                                                | 23.1 ms: 1.04x faster                                                 |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.03x faster                                                |
| xml_etree_generate         | 85.2 ms                                                | 83.3 ms: 1.02x faster                                                 |
| nbody                      | 89.3 ms                                                | 87.5 ms: 1.02x faster                                                 |
| unpickle                   | 14.1 us                                                | 13.8 us: 1.02x faster                                                 |
| logging_simple             | 6.63 us                                                | 6.53 us: 1.02x faster                                                 |
| xml_etree_process          | 59.0 ms                                                | 58.5 ms: 1.01x faster                                                 |
| scimark_fft                | 342 ms                                                 | 340 ms: 1.00x faster                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.51 sec: 1.00x slower                                                |
| fannkuch                   | 372 ms                                                 | 378 ms: 1.01x slower                                                  |
| pickle_dict                | 31.8 us                                                | 32.4 us: 1.02x slower                                                 |
| sqlite_synth               | 2.20 us                                                | 2.25 us: 1.02x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 7.33 ms: 1.02x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 763 ms: 1.03x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.57 sec: 1.03x slower                                                |
| regex_dna                  | 168 ms                                                 | 176 ms: 1.05x slower                                                  |
| json                       | 5.02 ms                                                | 5.26 ms: 1.05x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 10.9 ms: 1.05x slower                                                 |
| unpickle_list              | 4.67 us                                                | 5.00 us: 1.07x slower                                                 |
| mako                       | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                 |
| pidigits                   | 184 ms                                                 | 197 ms: 1.07x slower                                                  |
| pickle_list                | 4.77 us                                                | 5.14 us: 1.08x slower                                                 |
| json_loads                 | 26.5 us                                                | 29.1 us: 1.10x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.83 ms: 1.10x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.04 ms: 1.11x slower                                                 |
| telco                      | 6.53 ms                                                | 7.24 ms: 1.11x slower                                                 |
| pickle                     | 10.9 us                                                | 12.2 us: 1.11x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 23.0 ms: 1.12x slower                                                 |
| coverage                   | 71.4 ms                                                | 82.8 ms: 1.16x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.26 ms: 1.23x slower                                                 |
| python_startup             | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.89 ms: 1.74x slower                                                 |
| logging_silent             | 109 ns                                                 | 470 ns: 4.32x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 98.9 ms: 9.16x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.05x faster                                                          |

Benchmark hidden because not significant (4): logging_format, pickle_pure_python, asyncio_websockets, django_template
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20250607-3.15.0a0-8fdbbf8/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.102x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.15x