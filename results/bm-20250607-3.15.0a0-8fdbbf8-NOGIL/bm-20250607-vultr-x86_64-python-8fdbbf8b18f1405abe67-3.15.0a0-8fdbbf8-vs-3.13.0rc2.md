# Results vs. 3.13.0rc2

- fork: python
- ref: 8fdbbf8b18f1405abe67
- machine: linux-x86_64
- commit hash: 8fdbbf8
- commit date: 2025-06-07
- overall geometric mean: 1.024x slower
- HPT reliability: 96.40%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.41x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 280 ms: 1.08x slower                                                  |
| docutils       | 2.63 sec                                                               | 2.69 sec: 1.02x slower                                                |
| html5lib       | 68.6 ms                                                                | 65.7 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 528 ms: 1.71x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 554 ms: 1.59x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 229 ms: 1.46x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 318 ms: 1.45x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 287 ms: 1.43x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 260 ms: 1.36x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 476 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 506 ms: 1.32x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.0 ms: 1.01x faster                                                 |
| async_generators           | 375 ms                                                                 | 370 ms: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 516 ms: 1.00x faster                                                  |
| asyncio_tcp                | 502 ms                                                                 | 533 ms: 1.06x slower                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                                               | 1.79 sec: 1.18x slower                                                |
| Geometric mean             | (ref)                                                                  | 1.24x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 69.7 ms: 1.10x faster                                                 |
| pidigits       | 216 ms                                                                 | 214 ms: 1.01x faster                                                  |
| nbody          | 85.3 ms                                                                | 123 ms: 1.44x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.09x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.61 ms: 1.23x faster                                                 |
| regex_v8       | 23.2 ms                                                                | 20.2 ms: 1.15x faster                                                 |
| regex_dna      | 189 ms                                                                 | 170 ms: 1.11x faster                                                  |
| regex_compile  | 131 ms                                                                 | 144 ms: 1.10x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.09x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 87.6 ms: 1.08x faster                                                 |
| xml_etree_parse      | 136 ms                                                                 | 130 ms: 1.04x faster                                                  |
| pickle_dict          | 32.7 us                                                                | 31.6 us: 1.04x faster                                                 |
| unpickle             | 14.6 us                                                                | 15.0 us: 1.03x slower                                                 |
| pickle_list          | 4.81 us                                                                | 4.99 us: 1.04x slower                                                 |
| tomli_loads          | 2.01 sec                                                               | 2.12 sec: 1.06x slower                                                |
| pickle               | 11.4 us                                                                | 12.1 us: 1.06x slower                                                 |
| unpickle_pure_python | 208 us                                                                 | 232 us: 1.12x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 95.5 ms: 1.12x slower                                                 |
| json_dumps           | 10.6 ms                                                                | 12.0 ms: 1.13x slower                                                 |
| json_loads           | 27.3 us                                                                | 31.0 us: 1.13x slower                                                 |
| xml_etree_process    | 59.2 ms                                                                | 69.3 ms: 1.17x slower                                                 |
| unpickle_list        | 4.60 us                                                                | 5.42 us: 1.18x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 347 us: 1.19x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.07x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.56 ms: 1.29x slower                                                 |
| python_startup         | 11.0 ms                                                                | 16.0 ms: 1.45x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.37x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 39.5 ms: 1.16x slower                                                 |
| genshi_xml      | 49.1 ms                                                                | 57.7 ms: 1.18x slower                                                 |
| genshi_text     | 21.7 ms                                                                | 26.7 ms: 1.23x slower                                                 |
| mako            | 11.2 ms                                                                | 15.9 ms: 1.41x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.24x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.34 sec                                                               | 1.32 sec: 1.78x faster                                                |
| gc_traversal               | 3.32 ms                                                                | 1.89 ms: 1.76x faster                                                 |
| async_tree_io_tg           | 901 ms                                                                 | 528 ms: 1.71x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 554 ms: 1.59x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 229 ms: 1.46x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 318 ms: 1.45x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 287 ms: 1.43x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 260 ms: 1.36x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 476 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 506 ms: 1.32x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.61 ms: 1.23x faster                                                 |
| deepcopy                   | 357 us                                                                 | 291 us: 1.23x faster                                                  |
| go                         | 141 ms                                                                 | 122 ms: 1.15x faster                                                  |
| regex_v8                   | 23.2 ms                                                                | 20.2 ms: 1.15x faster                                                 |
| sqlite_synth               | 2.25 us                                                                | 2.02 us: 1.11x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 170 ms: 1.11x faster                                                  |
| float                      | 76.7 ms                                                                | 69.7 ms: 1.10x faster                                                 |
| deepcopy_memo              | 38.1 us                                                                | 34.8 us: 1.09x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 87.6 ms: 1.08x faster                                                 |
| scimark_sor                | 134 ms                                                                 | 124 ms: 1.08x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 2.98 us: 1.05x faster                                                 |
| html5lib                   | 68.6 ms                                                                | 65.7 ms: 1.04x faster                                                 |
| xml_etree_parse            | 136 ms                                                                 | 130 ms: 1.04x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 71.5 ms: 1.04x faster                                                 |
| pickle_dict                | 32.7 us                                                                | 31.6 us: 1.04x faster                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.39 sec: 1.01x faster                                                |
| pidigits                   | 216 ms                                                                 | 214 ms: 1.01x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.0 ms: 1.01x faster                                                 |
| async_generators           | 375 ms                                                                 | 370 ms: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 516 ms: 1.00x faster                                                  |
| pathlib                    | 19.3 ms                                                                | 19.4 ms: 1.01x slower                                                 |
| pycparser                  | 1.12 sec                                                               | 1.13 sec: 1.01x slower                                                |
| docutils                   | 2.63 sec                                                               | 2.69 sec: 1.02x slower                                                |
| unpickle                   | 14.6 us                                                                | 15.0 us: 1.03x slower                                                 |
| spectral_norm              | 108 ms                                                                 | 111 ms: 1.04x slower                                                  |
| pickle_list                | 4.81 us                                                                | 4.99 us: 1.04x slower                                                 |
| pyflate                    | 449 ms                                                                 | 466 ms: 1.04x slower                                                  |
| scimark_fft                | 348 ms                                                                 | 365 ms: 1.05x slower                                                  |
| tomli_loads                | 2.01 sec                                                               | 2.12 sec: 1.06x slower                                                |
| generators                 | 28.5 ms                                                                | 30.2 ms: 1.06x slower                                                 |
| asyncio_tcp                | 502 ms                                                                 | 533 ms: 1.06x slower                                                  |
| comprehensions             | 16.6 us                                                                | 17.6 us: 1.06x slower                                                 |
| pickle                     | 11.4 us                                                                | 12.1 us: 1.06x slower                                                 |
| json                       | 4.98 ms                                                                | 5.31 ms: 1.07x slower                                                 |
| 2to3                       | 259 ms                                                                 | 280 ms: 1.08x slower                                                  |
| hexiom                     | 5.95 ms                                                                | 6.44 ms: 1.08x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.45 ms: 1.09x slower                                                 |
| regex_compile              | 131 ms                                                                 | 144 ms: 1.10x slower                                                  |
| telco                      | 7.77 ms                                                                | 8.59 ms: 1.11x slower                                                 |
| nqueens                    | 77.7 ms                                                                | 86.3 ms: 1.11x slower                                                 |
| thrift                     | 772 us                                                                 | 860 us: 1.12x slower                                                  |
| unpickle_pure_python       | 208 us                                                                 | 232 us: 1.12x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 95.5 ms: 1.12x slower                                                 |
| sympy_integrate            | 19.7 ms                                                                | 22.1 ms: 1.12x slower                                                 |
| chaos                      | 56.3 ms                                                                | 63.2 ms: 1.12x slower                                                 |
| json_dumps                 | 10.6 ms                                                                | 12.0 ms: 1.13x slower                                                 |
| json_loads                 | 27.3 us                                                                | 31.0 us: 1.13x slower                                                 |
| sympy_str                  | 274 ms                                                                 | 315 ms: 1.15x slower                                                  |
| django_template            | 34.2 ms                                                                | 39.5 ms: 1.16x slower                                                 |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.49 ms: 1.16x slower                                                 |
| richards                   | 44.4 ms                                                                | 51.4 ms: 1.16x slower                                                 |
| scimark_lu                 | 112 ms                                                                 | 131 ms: 1.16x slower                                                  |
| sympy_expand               | 454 ms                                                                 | 528 ms: 1.16x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 180 ms: 1.17x slower                                                  |
| xml_etree_process          | 59.2 ms                                                                | 69.3 ms: 1.17x slower                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 77.0 ms: 1.17x slower                                                 |
| richards_super             | 50.4 ms                                                                | 59.0 ms: 1.17x slower                                                 |
| genshi_xml                 | 49.1 ms                                                                | 57.7 ms: 1.18x slower                                                 |
| unpickle_list              | 4.60 us                                                                | 5.42 us: 1.18x slower                                                 |
| meteor_contest             | 101 ms                                                                 | 120 ms: 1.18x slower                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                                               | 1.79 sec: 1.18x slower                                                |
| deltablue                  | 3.10 ms                                                                | 3.68 ms: 1.19x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 347 us: 1.19x slower                                                  |
| raytrace                   | 250 ms                                                                 | 303 ms: 1.21x slower                                                  |
| fannkuch                   | 376 ms                                                                 | 458 ms: 1.22x slower                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 191 us: 1.23x slower                                                  |
| genshi_text                | 21.7 ms                                                                | 26.7 ms: 1.23x slower                                                 |
| pprint_safe_repr           | 719 ms                                                                 | 884 ms: 1.23x slower                                                  |
| logging_format             | 6.92 us                                                                | 8.55 us: 1.24x slower                                                 |
| logging_simple             | 6.14 us                                                                | 7.63 us: 1.24x slower                                                 |
| pprint_pformat             | 1.46 sec                                                               | 1.82 sec: 1.25x slower                                                |
| crypto_pyaes               | 68.2 ms                                                                | 86.5 ms: 1.27x slower                                                 |
| python_startup_no_site     | 7.41 ms                                                                | 9.56 ms: 1.29x slower                                                 |
| coverage                   | 82.5 ms                                                                | 111 ms: 1.34x slower                                                  |
| mako                       | 11.2 ms                                                                | 15.9 ms: 1.41x slower                                                 |
| unpack_sequence            | 39.3 ns                                                                | 56.4 ns: 1.43x slower                                                 |
| nbody                      | 85.3 ms                                                                | 123 ms: 1.44x slower                                                  |
| python_startup             | 11.0 ms                                                                | 16.0 ms: 1.45x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 3.11 ms: 3.37x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 529 ns: 5.38x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 103 ms: 9.33x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.09x slower                                                          |

Benchmark hidden because not significant (1): pylint
Ignored benchmarks (10) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20250607-3.15.0a0-8fdbbf8-NOGIL/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.024x slower

# HPT report

- Reliability score: 96.40% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.41x