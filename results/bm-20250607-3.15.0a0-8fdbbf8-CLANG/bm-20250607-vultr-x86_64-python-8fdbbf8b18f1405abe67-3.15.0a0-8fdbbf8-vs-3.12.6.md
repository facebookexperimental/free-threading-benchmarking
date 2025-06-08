# Results vs. 3.12.6

- fork: python
- ref: 8fdbbf8b18f1405abe67
- machine: linux-x86_64
- commit hash: 8fdbbf8
- commit date: 2025-06-07
- overall geometric mean: 1.159x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 242 ms: 1.09x faster                                                  |
| docutils       | 2.64 sec                                               | 2.50 sec: 1.05x faster                                                |
| html5lib       | 63.6 ms                                                | 59.9 ms: 1.06x faster                                                 |
| Geometric mean | (ref)                                                  | 1.07x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 577 ms: 1.88x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 598 ms: 1.86x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 302 ms: 1.85x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 300 ms: 1.85x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 244 ms: 1.83x faster                                                  |
| async_tree_none            | 464 ms                                                 | 260 ms: 1.79x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 479 ms: 1.51x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 484 ms: 1.48x faster                                                  |
| async_generators           | 384 ms                                                 | 315 ms: 1.22x faster                                                  |
| coroutines                 | 23.9 ms                                                | 21.6 ms: 1.11x faster                                                 |
| asyncio_tcp                | 519 ms                                                 | 496 ms: 1.05x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.45x faster                                                          |

Benchmark hidden because not significant (2): asyncio_tcp_ssl, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 66.1 ms: 1.22x faster                                                 |
| nbody          | 89.3 ms                                                | 80.7 ms: 1.11x faster                                                 |
| pidigits       | 184 ms                                                 | 192 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                  | 1.09x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 117 ms: 1.21x faster                                                  |
| regex_effbot   | 3.17 ms                                                | 3.12 ms: 1.01x faster                                                 |
| regex_v8       | 20.6 ms                                                | 22.6 ms: 1.10x slower                                                 |
| regex_dna      | 168 ms                                                 | 195 ms: 1.16x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.79 sec: 1.18x faster                                                |
| unpickle_pure_python | 221 us                                                 | 195 us: 1.13x faster                                                  |
| unpickle_list        | 4.67 us                                                | 4.39 us: 1.07x faster                                                 |
| json_loads           | 26.5 us                                                | 25.1 us: 1.06x faster                                                 |
| xml_etree_generate   | 85.2 ms                                                | 80.8 ms: 1.06x faster                                                 |
| unpickle             | 14.1 us                                                | 13.3 us: 1.05x faster                                                 |
| xml_etree_process    | 59.0 ms                                                | 56.6 ms: 1.04x faster                                                 |
| pickle_pure_python   | 308 us                                                 | 296 us: 1.04x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 94.8 ms: 1.02x faster                                                 |
| pickle_dict          | 31.8 us                                                | 31.6 us: 1.00x faster                                                 |
| json_dumps           | 10.4 ms                                                | 10.8 ms: 1.04x slower                                                 |
| pickle_list          | 4.77 us                                                | 4.96 us: 1.04x slower                                                 |
| xml_etree_parse      | 139 ms                                                 | 146 ms: 1.05x slower                                                  |
| pickle               | 10.9 us                                                | 12.6 us: 1.15x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.39 ms: 1.03x slower                                                 |
| python_startup         | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 19.8 ms: 1.15x faster                                                 |
| genshi_xml      | 50.2 ms                                                | 46.1 ms: 1.09x faster                                                 |
| django_template | 34.7 ms                                                | 32.7 ms: 1.06x faster                                                 |
| mako            | 11.0 ms                                                | 11.5 ms: 1.04x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.06x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.08 sec: 2.24x faster                                                |
| async_tree_io              | 1.08 sec                                               | 577 ms: 1.88x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 598 ms: 1.86x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 302 ms: 1.85x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 300 ms: 1.85x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 244 ms: 1.83x faster                                                  |
| async_tree_none            | 464 ms                                                 | 260 ms: 1.79x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 25.9 us: 1.55x faster                                                 |
| deepcopy                   | 352 us                                                 | 228 us: 1.54x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 479 ms: 1.51x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 484 ms: 1.48x faster                                                  |
| go                         | 139 ms                                                 | 95.9 ms: 1.45x faster                                                 |
| comprehensions             | 19.8 us                                                | 14.0 us: 1.42x faster                                                 |
| spectral_norm              | 110 ms                                                 | 83.1 ms: 1.33x faster                                                 |
| scimark_sor                | 130 ms                                                 | 99.9 ms: 1.30x faster                                                 |
| raytrace                   | 299 ms                                                 | 231 ms: 1.30x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.39 us: 1.29x faster                                                 |
| chaos                      | 62.8 ms                                                | 49.0 ms: 1.28x faster                                                 |
| scimark_fft                | 342 ms                                                 | 268 ms: 1.27x faster                                                  |
| richards                   | 45.9 ms                                                | 36.5 ms: 1.26x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 54.4 ms: 1.26x faster                                                 |
| richards_super             | 51.9 ms                                                | 42.0 ms: 1.24x faster                                                 |
| float                      | 80.8 ms                                                | 66.1 ms: 1.22x faster                                                 |
| async_generators           | 384 ms                                                 | 315 ms: 1.22x faster                                                  |
| regex_compile              | 142 ms                                                 | 117 ms: 1.21x faster                                                  |
| deltablue                  | 3.45 ms                                                | 2.85 ms: 1.21x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 65.5 ms: 1.20x faster                                                 |
| hexiom                     | 6.17 ms                                                | 5.15 ms: 1.20x faster                                                 |
| generators                 | 32.2 ms                                                | 26.9 ms: 1.20x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 3.97 sec: 1.19x faster                                                |
| tomli_loads                | 2.11 sec                                               | 1.79 sec: 1.18x faster                                                |
| scimark_lu                 | 114 ms                                                 | 97.8 ms: 1.17x faster                                                 |
| pylint                     | 319 ms                                                 | 273 ms: 1.17x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 140 us: 1.16x faster                                                  |
| crypto_pyaes               | 76.6 ms                                                | 66.3 ms: 1.16x faster                                                 |
| pyflate                    | 448 ms                                                 | 388 ms: 1.15x faster                                                  |
| genshi_text                | 22.8 ms                                                | 19.8 ms: 1.15x faster                                                 |
| pathlib                    | 21.5 ms                                                | 18.7 ms: 1.15x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 18.0 ms: 1.14x faster                                                 |
| sympy_str                  | 292 ms                                                 | 257 ms: 1.14x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 195 us: 1.13x faster                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 3.89 ms: 1.13x faster                                                 |
| sympy_sum                  | 166 ms                                                 | 148 ms: 1.12x faster                                                  |
| coroutines                 | 23.9 ms                                                | 21.6 ms: 1.11x faster                                                 |
| nbody                      | 89.3 ms                                                | 80.7 ms: 1.11x faster                                                 |
| thrift                     | 791 us                                                 | 716 us: 1.11x faster                                                  |
| unpack_sequence            | 52.1 ns                                                | 47.3 ns: 1.10x faster                                                 |
| sympy_expand               | 468 ms                                                 | 428 ms: 1.09x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.07 sec: 1.09x faster                                                |
| genshi_xml                 | 50.2 ms                                                | 46.1 ms: 1.09x faster                                                 |
| 2to3                       | 264 ms                                                 | 242 ms: 1.09x faster                                                  |
| nqueens                    | 80.1 ms                                                | 74.3 ms: 1.08x faster                                                 |
| logging_simple             | 6.63 us                                                | 6.18 us: 1.07x faster                                                 |
| unpickle_list              | 4.67 us                                                | 4.39 us: 1.07x faster                                                 |
| html5lib                   | 63.6 ms                                                | 59.9 ms: 1.06x faster                                                 |
| django_template            | 34.7 ms                                                | 32.7 ms: 1.06x faster                                                 |
| json_loads                 | 26.5 us                                                | 25.1 us: 1.06x faster                                                 |
| xml_etree_generate         | 85.2 ms                                                | 80.8 ms: 1.06x faster                                                 |
| unpickle                   | 14.1 us                                                | 13.3 us: 1.05x faster                                                 |
| docutils                   | 2.64 sec                                               | 2.50 sec: 1.05x faster                                                |
| asyncio_tcp                | 519 ms                                                 | 496 ms: 1.05x faster                                                  |
| xml_etree_process          | 59.0 ms                                                | 56.6 ms: 1.04x faster                                                 |
| pickle_pure_python         | 308 us                                                 | 296 us: 1.04x faster                                                  |
| logging_format             | 7.35 us                                                | 7.12 us: 1.03x faster                                                 |
| json                       | 5.02 ms                                                | 4.91 ms: 1.02x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 94.8 ms: 1.02x faster                                                 |
| fannkuch                   | 372 ms                                                 | 366 ms: 1.02x faster                                                  |
| meteor_contest             | 104 ms                                                 | 102 ms: 1.02x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 3.12 ms: 1.01x faster                                                 |
| pickle_dict                | 31.8 us                                                | 31.6 us: 1.00x faster                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.53 sec: 1.01x slower                                                |
| pprint_safe_repr           | 743 ms                                                 | 749 ms: 1.01x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.39 ms: 1.03x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 10.8 ms: 1.04x slower                                                 |
| pickle_list                | 4.77 us                                                | 4.96 us: 1.04x slower                                                 |
| pidigits                   | 184 ms                                                 | 192 ms: 1.04x slower                                                  |
| mako                       | 11.0 ms                                                | 11.5 ms: 1.04x slower                                                 |
| xml_etree_parse            | 139 ms                                                 | 146 ms: 1.05x slower                                                  |
| telco                      | 6.53 ms                                                | 6.92 ms: 1.06x slower                                                 |
| coverage                   | 71.4 ms                                                | 76.0 ms: 1.06x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.01 ms: 1.07x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 22.6 ms: 1.10x slower                                                 |
| pickle                     | 10.9 us                                                | 12.6 us: 1.15x slower                                                 |
| regex_dna                  | 168 ms                                                 | 195 ms: 1.16x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.26 ms: 1.23x slower                                                 |
| python_startup             | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 2.00 ms: 1.84x slower                                                 |
| logging_silent             | 109 ns                                                 | 458 ns: 4.21x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 97.3 ms: 9.01x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.10x faster                                                          |

Benchmark hidden because not significant (3): asyncio_tcp_ssl, asyncio_websockets, sqlite_synth
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20250607-3.15.0a0-8fdbbf8-CLANG/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.159x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.11x
- 95% likely to have a speedup of 1.10x
- 99% likely to have a speedup of 1.09x

# Memory
- memory change: 1.20x