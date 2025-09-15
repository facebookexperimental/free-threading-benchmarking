# Results vs. 3.12.6

- fork: DinoV
- ref: heap_ast_types
- machine: linux-x86_64
- commit hash: f1e05f7
- commit date: 2025-09-15
- overall geometric mean: 1.068x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250915-vultr-x86_64-DinoV-heap_ast_types-3.15.0a0-f1e05f7 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 250 ms: 1.05x faster                                           |
| docutils       | 2.64 sec                                               | 2.54 sec: 1.04x faster                                         |
| html5lib       | 63.6 ms                                                | 61.2 ms: 1.04x faster                                          |
| Geometric mean | (ref)                                                  | 1.04x faster                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250915-vultr-x86_64-DinoV-heap_ast_types-3.15.0a0-f1e05f7 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 608 ms: 1.78x faster                                           |
| async_tree_memoization     | 555 ms                                                 | 313 ms: 1.77x faster                                           |
| async_tree_memoization_tg  | 560 ms                                                 | 316 ms: 1.77x faster                                           |
| async_tree_none_tg         | 446 ms                                                 | 253 ms: 1.77x faster                                           |
| async_tree_none            | 464 ms                                                 | 264 ms: 1.76x faster                                           |
| async_tree_io_tg           | 1.11 sec                                               | 633 ms: 1.75x faster                                           |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 497 ms: 1.44x faster                                           |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 502 ms: 1.44x faster                                           |
| async_generators           | 384 ms                                                 | 347 ms: 1.11x faster                                           |
| Geometric mean             | (ref)                                                  | 1.47x faster                                                   |

Benchmark hidden because not significant (2): coroutines, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250915-vultr-x86_64-DinoV-heap_ast_types-3.15.0a0-f1e05f7 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| float          | 80.8 ms                                                | 72.0 ms: 1.12x faster                                          |
| nbody          | 89.3 ms                                                | 90.2 ms: 1.01x slower                                          |
| pidigits       | 184 ms                                                 | 200 ms: 1.08x slower                                           |
| Geometric mean | (ref)                                                  | 1.01x faster                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250915-vultr-x86_64-DinoV-heap_ast_types-3.15.0a0-f1e05f7 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 123 ms: 1.16x faster                                           |
| regex_effbot   | 3.17 ms                                                | 2.74 ms: 1.16x faster                                          |
| regex_dna      | 168 ms                                                 | 175 ms: 1.04x slower                                           |
| regex_v8       | 20.6 ms                                                | 22.2 ms: 1.08x slower                                          |
| Geometric mean | (ref)                                                  | 1.05x faster                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250915-vultr-x86_64-DinoV-heap_ast_types-3.15.0a0-f1e05f7 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.90 sec: 1.11x faster                                         |
| json_dumps           | 10.4 ms                                                | 9.67 ms: 1.07x faster                                          |
| xml_etree_parse      | 139 ms                                                 | 133 ms: 1.04x faster                                           |
| unpickle_pure_python | 221 us                                                 | 213 us: 1.04x faster                                           |
| xml_etree_iterparse  | 96.7 ms                                                | 93.5 ms: 1.03x faster                                          |
| xml_etree_generate   | 85.2 ms                                                | 83.6 ms: 1.02x faster                                          |
| xml_etree_process    | 59.0 ms                                                | 58.1 ms: 1.01x faster                                          |
| pickle_pure_python   | 308 us                                                 | 305 us: 1.01x faster                                           |
| json_loads           | 26.5 us                                                | 28.3 us: 1.07x slower                                          |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250915-vultr-x86_64-DinoV-heap_ast_types-3.15.0a0-f1e05f7 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.26 ms: 1.01x slower                                          |
| python_startup         | 9.93 ms                                                | 12.6 ms: 1.26x slower                                          |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250915-vultr-x86_64-DinoV-heap_ast_types-3.15.0a0-f1e05f7 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.2 ms: 1.13x faster                                          |
| genshi_xml      | 50.2 ms                                                | 47.9 ms: 1.05x faster                                          |
| django_template | 34.7 ms                                                | 34.2 ms: 1.01x faster                                          |
| mako            | 11.0 ms                                                | 12.0 ms: 1.09x slower                                          |
| Geometric mean  | (ref)                                                  | 1.02x faster                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250915-vultr-x86_64-DinoV-heap_ast_types-3.15.0a0-f1e05f7 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.16 sec: 2.08x faster                                         |
| async_tree_io              | 1.08 sec                                               | 608 ms: 1.78x faster                                           |
| async_tree_memoization     | 555 ms                                                 | 313 ms: 1.77x faster                                           |
| async_tree_memoization_tg  | 560 ms                                                 | 316 ms: 1.77x faster                                           |
| async_tree_none_tg         | 446 ms                                                 | 253 ms: 1.77x faster                                           |
| async_tree_none            | 464 ms                                                 | 264 ms: 1.76x faster                                           |
| async_tree_io_tg           | 1.11 sec                                               | 633 ms: 1.75x faster                                           |
| deepcopy_memo              | 40.3 us                                                | 26.8 us: 1.51x faster                                          |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 497 ms: 1.44x faster                                           |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 502 ms: 1.44x faster                                           |
| deepcopy                   | 352 us                                                 | 245 us: 1.43x faster                                           |
| go                         | 139 ms                                                 | 105 ms: 1.32x faster                                           |
| comprehensions             | 19.8 us                                                | 15.9 us: 1.25x faster                                          |
| pathlib                    | 21.5 ms                                                | 18.1 ms: 1.19x faster                                          |
| dulwich_log                | 78.9 ms                                                | 66.5 ms: 1.19x faster                                          |
| scimark_sor                | 130 ms                                                 | 111 ms: 1.17x faster                                           |
| raytrace                   | 299 ms                                                 | 255 ms: 1.17x faster                                           |
| deepcopy_reduce            | 3.08 us                                                | 2.65 us: 1.16x faster                                          |
| regex_compile              | 142 ms                                                 | 123 ms: 1.16x faster                                           |
| regex_effbot               | 3.17 ms                                                | 2.74 ms: 1.16x faster                                          |
| generators                 | 32.2 ms                                                | 28.2 ms: 1.15x faster                                          |
| pylint                     | 319 ms                                                 | 280 ms: 1.14x faster                                           |
| spectral_norm              | 110 ms                                                 | 97.0 ms: 1.14x faster                                          |
| logging_simple             | 6.63 us                                                | 5.85 us: 1.13x faster                                          |
| genshi_text                | 22.8 ms                                                | 20.2 ms: 1.13x faster                                          |
| logging_format             | 7.35 us                                                | 6.53 us: 1.12x faster                                          |
| float                      | 80.8 ms                                                | 72.0 ms: 1.12x faster                                          |
| richards                   | 45.9 ms                                                | 41.1 ms: 1.12x faster                                          |
| logging_silent             | 109 ns                                                 | 97.4 ns: 1.12x faster                                          |
| bpe_tokeniser              | 4.74 sec                                               | 4.26 sec: 1.11x faster                                         |
| crypto_pyaes               | 76.6 ms                                                | 68.8 ms: 1.11x faster                                          |
| chaos                      | 62.8 ms                                                | 56.7 ms: 1.11x faster                                          |
| tomli_loads                | 2.11 sec                                               | 1.90 sec: 1.11x faster                                         |
| richards_super             | 51.9 ms                                                | 46.8 ms: 1.11x faster                                          |
| async_generators           | 384 ms                                                 | 347 ms: 1.11x faster                                           |
| scimark_monte_carlo        | 68.4 ms                                                | 61.9 ms: 1.10x faster                                          |
| sympy_integrate            | 20.5 ms                                                | 18.8 ms: 1.09x faster                                          |
| pyflate                    | 448 ms                                                 | 412 ms: 1.09x faster                                           |
| hexiom                     | 6.17 ms                                                | 5.69 ms: 1.09x faster                                          |
| sympy_str                  | 292 ms                                                 | 270 ms: 1.08x faster                                           |
| typing_runtime_protocols   | 163 us                                                 | 152 us: 1.08x faster                                           |
| sympy_sum                  | 166 ms                                                 | 154 ms: 1.08x faster                                           |
| pycparser                  | 1.17 sec                                               | 1.09 sec: 1.07x faster                                         |
| json_dumps                 | 10.4 ms                                                | 9.67 ms: 1.07x faster                                          |
| pprint_pformat             | 1.52 sec                                               | 1.43 sec: 1.06x faster                                         |
| pprint_safe_repr           | 743 ms                                                 | 702 ms: 1.06x faster                                           |
| deltablue                  | 3.45 ms                                                | 3.27 ms: 1.05x faster                                          |
| 2to3                       | 264 ms                                                 | 250 ms: 1.05x faster                                           |
| meteor_contest             | 104 ms                                                 | 98.8 ms: 1.05x faster                                          |
| genshi_xml                 | 50.2 ms                                                | 47.9 ms: 1.05x faster                                          |
| xml_etree_parse            | 139 ms                                                 | 133 ms: 1.04x faster                                           |
| thrift                     | 791 us                                                 | 759 us: 1.04x faster                                           |
| html5lib                   | 63.6 ms                                                | 61.2 ms: 1.04x faster                                          |
| docutils                   | 2.64 sec                                               | 2.54 sec: 1.04x faster                                         |
| unpickle_pure_python       | 221 us                                                 | 213 us: 1.04x faster                                           |
| xml_etree_iterparse        | 96.7 ms                                                | 93.5 ms: 1.03x faster                                          |
| scimark_lu                 | 114 ms                                                 | 111 ms: 1.03x faster                                           |
| nqueens                    | 80.1 ms                                                | 77.9 ms: 1.03x faster                                          |
| xml_etree_generate         | 85.2 ms                                                | 83.6 ms: 1.02x faster                                          |
| xml_etree_process          | 59.0 ms                                                | 58.1 ms: 1.01x faster                                          |
| django_template            | 34.7 ms                                                | 34.2 ms: 1.01x faster                                          |
| sympy_expand               | 468 ms                                                 | 462 ms: 1.01x faster                                           |
| scimark_fft                | 342 ms                                                 | 338 ms: 1.01x faster                                           |
| pickle_pure_python         | 308 us                                                 | 305 us: 1.01x faster                                           |
| nbody                      | 89.3 ms                                                | 90.2 ms: 1.01x slower                                          |
| python_startup_no_site     | 7.16 ms                                                | 7.26 ms: 1.01x slower                                          |
| fannkuch                   | 372 ms                                                 | 379 ms: 1.02x slower                                           |
| json                       | 5.02 ms                                                | 5.15 ms: 1.03x slower                                          |
| regex_dna                  | 168 ms                                                 | 175 ms: 1.04x slower                                           |
| sqlite_synth               | 2.20 us                                                | 2.30 us: 1.05x slower                                          |
| json_loads                 | 26.5 us                                                | 28.3 us: 1.07x slower                                          |
| bench_thread_pool          | 941 us                                                 | 1.01 ms: 1.07x slower                                          |
| regex_v8                   | 20.6 ms                                                | 22.2 ms: 1.08x slower                                          |
| pidigits                   | 184 ms                                                 | 200 ms: 1.08x slower                                           |
| mako                       | 11.0 ms                                                | 12.0 ms: 1.09x slower                                          |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.85 ms: 1.10x slower                                          |
| coverage                   | 71.4 ms                                                | 81.5 ms: 1.14x slower                                          |
| bench_mp_pool              | 10.8 ms                                                | 12.5 ms: 1.16x slower                                          |
| gc_traversal               | 3.46 ms                                                | 4.32 ms: 1.25x slower                                          |
| python_startup             | 9.93 ms                                                | 12.6 ms: 1.26x slower                                          |
| create_gc_cycles           | 1.09 ms                                                | 1.93 ms: 1.77x slower                                          |
| telco                      | 6.53 ms                                                | 158 ms: 24.21x slower                                          |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                   |

Benchmark hidden because not significant (2): coroutines, asyncio_websockets
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250915-3.15.0a0-f1e05f7/bm-20250915-vultr-x86_64-DinoV-heap_ast_types-3.15.0a0-f1e05f7.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.068x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.16x