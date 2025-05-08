# Results vs. 3.12.6

- fork: nascheme
- ref: mcache_str_hash
- machine: linux-x86_64
- commit hash: b6bca55
- commit date: 2025-05-08
- overall geometric mean: 1.011x faster
- HPT reliability: 90.96%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.44x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-b6bca55 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 285 ms: 1.08x slower                                               |
| docutils       | 2.64 sec                                               | 2.71 sec: 1.03x slower                                             |
| html5lib       | 63.6 ms                                                | 67.4 ms: 1.06x slower                                              |
| Geometric mean | (ref)                                                  | 1.06x slower                                                       |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-b6bca55 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 523 ms: 2.12x faster                                               |
| async_tree_none_tg         | 446 ms                                                 | 224 ms: 1.99x faster                                               |
| async_tree_memoization_tg  | 560 ms                                                 | 284 ms: 1.97x faster                                               |
| async_tree_io              | 1.08 sec                                               | 552 ms: 1.96x faster                                               |
| async_tree_none            | 464 ms                                                 | 259 ms: 1.79x faster                                               |
| async_tree_memoization     | 555 ms                                                 | 312 ms: 1.78x faster                                               |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 483 ms: 1.50x faster                                               |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 512 ms: 1.40x faster                                               |
| async_generators           | 384 ms                                                 | 365 ms: 1.05x faster                                               |
| coroutines                 | 23.9 ms                                                | 23.3 ms: 1.03x faster                                              |
| asyncio_websockets         | 517 ms                                                 | 515 ms: 1.00x faster                                               |
| Geometric mean             | (ref)                                                  | 1.54x faster                                                       |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-b6bca55 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 69.9 ms: 1.16x faster                                              |
| pidigits       | 184 ms                                                 | 191 ms: 1.04x slower                                               |
| nbody          | 89.3 ms                                                | 121 ms: 1.35x slower                                               |
| Geometric mean | (ref)                                                  | 1.07x slower                                                       |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-b6bca55 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.84 ms: 1.12x faster                                              |
| regex_v8       | 20.6 ms                                                | 20.9 ms: 1.02x slower                                              |
| regex_compile  | 142 ms                                                 | 145 ms: 1.02x slower                                               |
| regex_dna      | 168 ms                                                 | 181 ms: 1.08x slower                                               |
| Geometric mean | (ref)                                                  | 1.00x faster                                                       |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-b6bca55 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.4 ms: 1.11x faster                                              |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.08x faster                                               |
| tomli_loads          | 2.11 sec                                               | 2.13 sec: 1.01x slower                                             |
| unpickle_pure_python | 221 us                                                 | 226 us: 1.02x slower                                               |
| pickle_pure_python   | 308 us                                                 | 328 us: 1.07x slower                                               |
| xml_etree_generate   | 85.2 ms                                                | 94.4 ms: 1.11x slower                                              |
| xml_etree_process    | 59.0 ms                                                | 67.3 ms: 1.14x slower                                              |
| json_loads           | 26.5 us                                                | 30.6 us: 1.15x slower                                              |
| json_dumps           | 10.4 ms                                                | 13.4 ms: 1.29x slower                                              |
| Geometric mean       | (ref)                                                  | 1.06x slower                                                       |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-b6bca55 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.61 ms: 1.34x slower                                              |
| python_startup         | 9.93 ms                                                | 16.0 ms: 1.61x slower                                              |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                       |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-b6bca55 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 55.9 ms: 1.11x slower                                              |
| django_template | 34.7 ms                                                | 39.8 ms: 1.15x slower                                              |
| genshi_text     | 22.8 ms                                                | 26.5 ms: 1.16x slower                                              |
| mako            | 11.0 ms                                                | 16.0 ms: 1.46x slower                                              |
| Geometric mean  | (ref)                                                  | 1.21x slower                                                       |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-b6bca55 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 523 ms: 2.12x faster                                               |
| async_tree_none_tg         | 446 ms                                                 | 224 ms: 1.99x faster                                               |
| async_tree_memoization_tg  | 560 ms                                                 | 284 ms: 1.97x faster                                               |
| async_tree_io              | 1.08 sec                                               | 552 ms: 1.96x faster                                               |
| gc_traversal               | 3.46 ms                                                | 1.91 ms: 1.81x faster                                              |
| mdp                        | 2.42 sec                                               | 1.34 sec: 1.81x faster                                             |
| async_tree_none            | 464 ms                                                 | 259 ms: 1.79x faster                                               |
| async_tree_memoization     | 555 ms                                                 | 312 ms: 1.78x faster                                               |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 483 ms: 1.50x faster                                               |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 512 ms: 1.40x faster                                               |
| deepcopy                   | 352 us                                                 | 294 us: 1.20x faster                                               |
| float                      | 80.8 ms                                                | 69.9 ms: 1.16x faster                                              |
| deepcopy_memo              | 40.3 us                                                | 35.4 us: 1.14x faster                                              |
| go                         | 139 ms                                                 | 124 ms: 1.13x faster                                               |
| regex_effbot               | 3.17 ms                                                | 2.84 ms: 1.12x faster                                              |
| dulwich_log                | 78.9 ms                                                | 71.1 ms: 1.11x faster                                              |
| xml_etree_iterparse        | 96.7 ms                                                | 87.4 ms: 1.11x faster                                              |
| generators                 | 32.2 ms                                                | 29.3 ms: 1.10x faster                                              |
| pathlib                    | 21.5 ms                                                | 19.7 ms: 1.09x faster                                              |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.08x faster                                               |
| logging_silent             | 109 ns                                                 | 101 ns: 1.08x faster                                               |
| scimark_sor                | 130 ms                                                 | 122 ms: 1.07x faster                                               |
| bpe_tokeniser              | 4.74 sec                                               | 4.45 sec: 1.06x faster                                             |
| async_generators           | 384 ms                                                 | 365 ms: 1.05x faster                                               |
| sqlite_synth               | 2.20 us                                                | 2.10 us: 1.05x faster                                              |
| pylint                     | 319 ms                                                 | 306 ms: 1.04x faster                                               |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.04x faster                                             |
| coroutines                 | 23.9 ms                                                | 23.3 ms: 1.03x faster                                              |
| comprehensions             | 19.8 us                                                | 19.4 us: 1.02x faster                                              |
| spectral_norm              | 110 ms                                                 | 109 ms: 1.01x faster                                               |
| deepcopy_reduce            | 3.08 us                                                | 3.05 us: 1.01x faster                                              |
| asyncio_websockets         | 517 ms                                                 | 515 ms: 1.00x faster                                               |
| raytrace                   | 299 ms                                                 | 301 ms: 1.01x slower                                               |
| tomli_loads                | 2.11 sec                                               | 2.13 sec: 1.01x slower                                             |
| chaos                      | 62.8 ms                                                | 63.7 ms: 1.01x slower                                              |
| regex_v8                   | 20.6 ms                                                | 20.9 ms: 1.02x slower                                              |
| regex_compile              | 142 ms                                                 | 145 ms: 1.02x slower                                               |
| unpickle_pure_python       | 221 us                                                 | 226 us: 1.02x slower                                               |
| docutils                   | 2.64 sec                                               | 2.71 sec: 1.03x slower                                             |
| deltablue                  | 3.45 ms                                                | 3.54 ms: 1.03x slower                                              |
| json                       | 5.02 ms                                                | 5.18 ms: 1.03x slower                                              |
| pidigits                   | 184 ms                                                 | 191 ms: 1.04x slower                                               |
| pprint_safe_repr           | 743 ms                                                 | 779 ms: 1.05x slower                                               |
| pprint_pformat             | 1.52 sec                                               | 1.61 sec: 1.06x slower                                             |
| html5lib                   | 63.6 ms                                                | 67.4 ms: 1.06x slower                                              |
| pickle_pure_python         | 308 us                                                 | 328 us: 1.07x slower                                               |
| scimark_fft                | 342 ms                                                 | 366 ms: 1.07x slower                                               |
| logging_simple             | 6.63 us                                                | 7.13 us: 1.07x slower                                              |
| regex_dna                  | 168 ms                                                 | 181 ms: 1.08x slower                                               |
| hexiom                     | 6.17 ms                                                | 6.64 ms: 1.08x slower                                              |
| 2to3                       | 264 ms                                                 | 285 ms: 1.08x slower                                               |
| logging_format             | 7.35 us                                                | 7.96 us: 1.08x slower                                              |
| pyflate                    | 448 ms                                                 | 486 ms: 1.09x slower                                               |
| sympy_integrate            | 20.5 ms                                                | 22.3 ms: 1.09x slower                                              |
| sympy_sum                  | 166 ms                                                 | 182 ms: 1.09x slower                                               |
| sympy_str                  | 292 ms                                                 | 320 ms: 1.10x slower                                               |
| nqueens                    | 80.1 ms                                                | 88.4 ms: 1.10x slower                                              |
| thrift                     | 791 us                                                 | 875 us: 1.11x slower                                               |
| xml_etree_generate         | 85.2 ms                                                | 94.4 ms: 1.11x slower                                              |
| genshi_xml                 | 50.2 ms                                                | 55.9 ms: 1.11x slower                                              |
| richards                   | 45.9 ms                                                | 51.3 ms: 1.12x slower                                              |
| scimark_monte_carlo        | 68.4 ms                                                | 77.0 ms: 1.13x slower                                              |
| richards_super             | 51.9 ms                                                | 58.4 ms: 1.13x slower                                              |
| crypto_pyaes               | 76.6 ms                                                | 86.4 ms: 1.13x slower                                              |
| xml_etree_process          | 59.0 ms                                                | 67.3 ms: 1.14x slower                                              |
| django_template            | 34.7 ms                                                | 39.8 ms: 1.15x slower                                              |
| sympy_expand               | 468 ms                                                 | 537 ms: 1.15x slower                                               |
| json_loads                 | 26.5 us                                                | 30.6 us: 1.15x slower                                              |
| scimark_lu                 | 114 ms                                                 | 132 ms: 1.15x slower                                               |
| genshi_text                | 22.8 ms                                                | 26.5 ms: 1.16x slower                                              |
| typing_runtime_protocols   | 163 us                                                 | 193 us: 1.18x slower                                               |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.53 ms: 1.26x slower                                              |
| meteor_contest             | 104 ms                                                 | 131 ms: 1.27x slower                                               |
| fannkuch                   | 372 ms                                                 | 476 ms: 1.28x slower                                               |
| json_dumps                 | 10.4 ms                                                | 13.4 ms: 1.29x slower                                              |
| telco                      | 6.53 ms                                                | 8.72 ms: 1.34x slower                                              |
| python_startup_no_site     | 7.16 ms                                                | 9.61 ms: 1.34x slower                                              |
| nbody                      | 89.3 ms                                                | 121 ms: 1.35x slower                                               |
| create_gc_cycles           | 1.09 ms                                                | 1.49 ms: 1.36x slower                                              |
| mako                       | 11.0 ms                                                | 16.0 ms: 1.46x slower                                              |
| coverage                   | 71.4 ms                                                | 109 ms: 1.53x slower                                               |
| python_startup             | 9.93 ms                                                | 16.0 ms: 1.61x slower                                              |
| bench_thread_pool          | 941 us                                                 | 3.13 ms: 3.32x slower                                              |
| bench_mp_pool              | 10.8 ms                                                | 103 ms: 9.54x slower                                               |
| Geometric mean             | (ref)                                                  | 1.03x slower                                                       |
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250508-3.15.0a0-b6bca55-NOGIL/bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-b6bca55.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.011x faster

# HPT report

- Reliability score: 90.96% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.44x