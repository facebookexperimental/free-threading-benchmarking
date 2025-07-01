# Results vs. 3.12.6

- fork: python
- ref: 23caccf74ce2c8dc5d9c
- machine: linux-x86_64
- commit hash: 23caccf
- commit date: 2025-06-30
- overall geometric mean: 1.014x faster
- HPT reliability: 90.96%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.41x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 284 ms: 1.08x slower                                                  |
| docutils       | 2.64 sec                                               | 2.70 sec: 1.02x slower                                                |
| html5lib       | 63.6 ms                                                | 65.0 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                  | 1.04x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 524 ms: 2.12x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 227 ms: 1.97x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 286 ms: 1.96x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 555 ms: 1.95x faster                                                  |
| async_tree_none            | 464 ms                                                 | 259 ms: 1.79x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 313 ms: 1.77x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 475 ms: 1.52x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 499 ms: 1.43x faster                                                  |
| async_generators           | 384 ms                                                 | 374 ms: 1.03x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 513 ms: 1.01x faster                                                  |
| coroutines                 | 23.9 ms                                                | 24.6 ms: 1.03x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.53x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 69.7 ms: 1.16x faster                                                 |
| pidigits       | 184 ms                                                 | 194 ms: 1.06x slower                                                  |
| nbody          | 89.3 ms                                                | 125 ms: 1.40x slower                                                  |
| Geometric mean | (ref)                                                  | 1.08x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.59 ms: 1.22x faster                                                 |
| regex_dna      | 168 ms                                                 | 163 ms: 1.03x faster                                                  |
| regex_v8       | 20.6 ms                                                | 20.1 ms: 1.03x faster                                                 |
| regex_compile  | 142 ms                                                 | 144 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                  | 1.06x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.1 ms: 1.11x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.15 sec: 1.02x slower                                                |
| unpickle_pure_python | 221 us                                                 | 234 us: 1.06x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 338 us: 1.10x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 95.5 ms: 1.12x slower                                                 |
| json_dumps           | 10.4 ms                                                | 12.0 ms: 1.16x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 69.1 ms: 1.17x slower                                                 |
| json_loads           | 26.5 us                                                | 31.9 us: 1.20x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.07x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.55 ms: 1.33x slower                                                 |
| python_startup         | 9.93 ms                                                | 16.0 ms: 1.61x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 39.9 ms: 1.15x slower                                                 |
| genshi_xml      | 50.2 ms                                                | 58.6 ms: 1.17x slower                                                 |
| genshi_text     | 22.8 ms                                                | 26.7 ms: 1.17x slower                                                 |
| mako            | 11.0 ms                                                | 15.8 ms: 1.43x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.22x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 524 ms: 2.12x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 227 ms: 1.97x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 286 ms: 1.96x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 555 ms: 1.95x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 1.87 ms: 1.85x faster                                                 |
| mdp                        | 2.42 sec                                               | 1.32 sec: 1.83x faster                                                |
| async_tree_none            | 464 ms                                                 | 259 ms: 1.79x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 313 ms: 1.77x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 475 ms: 1.52x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 499 ms: 1.43x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.59 ms: 1.22x faster                                                 |
| deepcopy                   | 352 us                                                 | 293 us: 1.20x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 34.7 us: 1.16x faster                                                 |
| float                      | 80.8 ms                                                | 69.7 ms: 1.16x faster                                                 |
| go                         | 139 ms                                                 | 121 ms: 1.15x faster                                                  |
| comprehensions             | 19.8 us                                                | 17.7 us: 1.12x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 87.1 ms: 1.11x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.5 ms: 1.10x faster                                                 |
| logging_silent             | 109 ns                                                 | 100 ns: 1.09x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 72.6 ms: 1.09x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.40 sec: 1.08x faster                                                |
| sqlite_synth               | 2.20 us                                                | 2.06 us: 1.07x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| generators                 | 32.2 ms                                                | 31.2 ms: 1.03x faster                                                 |
| scimark_sor                | 130 ms                                                 | 125 ms: 1.03x faster                                                  |
| async_generators           | 384 ms                                                 | 374 ms: 1.03x faster                                                  |
| regex_dna                  | 168 ms                                                 | 163 ms: 1.03x faster                                                  |
| regex_v8                   | 20.6 ms                                                | 20.1 ms: 1.03x faster                                                 |
| pycparser                  | 1.17 sec                                               | 1.14 sec: 1.03x faster                                                |
| asyncio_websockets         | 517 ms                                                 | 513 ms: 1.01x faster                                                  |
| regex_compile              | 142 ms                                                 | 144 ms: 1.01x slower                                                  |
| chaos                      | 62.8 ms                                                | 63.6 ms: 1.01x slower                                                 |
| raytrace                   | 299 ms                                                 | 304 ms: 1.02x slower                                                  |
| html5lib                   | 63.6 ms                                                | 65.0 ms: 1.02x slower                                                 |
| tomli_loads                | 2.11 sec                                               | 2.15 sec: 1.02x slower                                                |
| docutils                   | 2.64 sec                                               | 2.70 sec: 1.02x slower                                                |
| spectral_norm              | 110 ms                                                 | 113 ms: 1.03x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.6 ms: 1.03x slower                                                 |
| logging_simple             | 6.63 us                                                | 6.87 us: 1.04x slower                                                 |
| deltablue                  | 3.45 ms                                                | 3.59 ms: 1.04x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 775 ms: 1.04x slower                                                  |
| pyflate                    | 448 ms                                                 | 469 ms: 1.05x slower                                                  |
| hexiom                     | 6.17 ms                                                | 6.47 ms: 1.05x slower                                                 |
| pidigits                   | 184 ms                                                 | 194 ms: 1.06x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.61 sec: 1.06x slower                                                |
| logging_format             | 7.35 us                                                | 7.77 us: 1.06x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 234 us: 1.06x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 21.9 ms: 1.07x slower                                                 |
| sympy_str                  | 292 ms                                                 | 313 ms: 1.07x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 179 ms: 1.08x slower                                                  |
| json                       | 5.02 ms                                                | 5.41 ms: 1.08x slower                                                 |
| 2to3                       | 264 ms                                                 | 284 ms: 1.08x slower                                                  |
| scimark_fft                | 342 ms                                                 | 373 ms: 1.09x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 338 us: 1.10x slower                                                  |
| nqueens                    | 80.1 ms                                                | 88.7 ms: 1.11x slower                                                 |
| thrift                     | 791 us                                                 | 878 us: 1.11x slower                                                  |
| sympy_expand               | 468 ms                                                 | 520 ms: 1.11x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 95.5 ms: 1.12x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 86.7 ms: 1.13x slower                                                 |
| richards                   | 45.9 ms                                                | 52.0 ms: 1.13x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 131 ms: 1.14x slower                                                  |
| richards_super             | 51.9 ms                                                | 59.6 ms: 1.15x slower                                                 |
| django_template            | 34.7 ms                                                | 39.9 ms: 1.15x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 78.7 ms: 1.15x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 12.0 ms: 1.16x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 58.6 ms: 1.17x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 191 us: 1.17x slower                                                  |
| genshi_text                | 22.8 ms                                                | 26.7 ms: 1.17x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 69.1 ms: 1.17x slower                                                 |
| meteor_contest             | 104 ms                                                 | 122 ms: 1.17x slower                                                  |
| json_loads                 | 26.5 us                                                | 31.9 us: 1.20x slower                                                 |
| fannkuch                   | 372 ms                                                 | 464 ms: 1.25x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.54 ms: 1.26x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.44 ms: 1.32x slower                                                 |
| telco                      | 6.53 ms                                                | 8.67 ms: 1.33x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 9.55 ms: 1.33x slower                                                 |
| nbody                      | 89.3 ms                                                | 125 ms: 1.40x slower                                                  |
| mako                       | 11.0 ms                                                | 15.8 ms: 1.43x slower                                                 |
| coverage                   | 71.4 ms                                                | 112 ms: 1.57x slower                                                  |
| python_startup             | 9.93 ms                                                | 16.0 ms: 1.61x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.15 ms: 3.35x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 104 ms: 9.63x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.03x slower                                                          |

Benchmark hidden because not significant (2): pylint, deepcopy_reduce
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250630-3.15.0a0-23caccf-NOGIL/bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.014x faster

# HPT report

- Reliability score: 90.96% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.41x