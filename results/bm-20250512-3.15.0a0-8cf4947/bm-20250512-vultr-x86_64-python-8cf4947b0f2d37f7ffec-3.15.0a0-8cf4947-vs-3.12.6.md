# Results vs. 3.12.6

- fork: python
- ref: 8cf4947b0f2d37f7ffec
- machine: linux-x86_64
- commit hash: 8cf4947
- commit date: 2025-05-12
- overall geometric mean: 1.109x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 249 ms: 1.06x faster                                                  |
| docutils       | 2.64 sec                                               | 2.52 sec: 1.05x faster                                                |
| html5lib       | 63.6 ms                                                | 61.2 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                  | 1.05x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 309 ms: 1.81x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 599 ms: 1.81x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 311 ms: 1.79x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 626 ms: 1.77x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 254 ms: 1.76x faster                                                  |
| async_tree_none            | 464 ms                                                 | 271 ms: 1.72x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 498 ms: 1.45x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 506 ms: 1.41x faster                                                  |
| async_generators           | 384 ms                                                 | 328 ms: 1.17x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 518 ms: 1.00x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.48x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.3 ms: 1.15x faster                                                 |
| nbody          | 89.3 ms                                                | 87.9 ms: 1.02x faster                                                 |
| pidigits       | 184 ms                                                 | 193 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.72 ms: 1.17x faster                                                 |
| regex_compile  | 142 ms                                                 | 123 ms: 1.16x faster                                                  |
| regex_dna      | 168 ms                                                 | 174 ms: 1.04x slower                                                  |
| regex_v8       | 20.6 ms                                                | 22.4 ms: 1.09x slower                                                 |
| Geometric mean | (ref)                                                  | 1.05x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.92 sec: 1.10x faster                                                |
| unpickle_pure_python | 221 us                                                 | 207 us: 1.07x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 91.4 ms: 1.06x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 132 ms: 1.05x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 82.4 ms: 1.03x faster                                                 |
| xml_etree_process    | 59.0 ms                                                | 57.6 ms: 1.02x faster                                                 |
| pickle_pure_python   | 308 us                                                 | 306 us: 1.01x faster                                                  |
| json_loads           | 26.5 us                                                | 28.9 us: 1.09x slower                                                 |
| json_dumps           | 10.4 ms                                                | 12.1 ms: 1.17x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.33 ms: 1.02x slower                                                 |
| python_startup         | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.4 ms: 1.12x faster                                                 |
| genshi_xml      | 50.2 ms                                                | 47.8 ms: 1.05x faster                                                 |
| django_template | 34.7 ms                                                | 34.2 ms: 1.01x faster                                                 |
| mako            | 11.0 ms                                                | 11.9 ms: 1.08x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.02x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.14 sec: 2.12x faster                                                |
| async_tree_memoization_tg  | 560 ms                                                 | 309 ms: 1.81x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 599 ms: 1.81x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 311 ms: 1.79x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 626 ms: 1.77x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 254 ms: 1.76x faster                                                  |
| async_tree_none            | 464 ms                                                 | 271 ms: 1.72x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 498 ms: 1.45x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 28.5 us: 1.41x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 506 ms: 1.41x faster                                                  |
| deepcopy                   | 352 us                                                 | 250 us: 1.41x faster                                                  |
| go                         | 139 ms                                                 | 107 ms: 1.30x faster                                                  |
| generators                 | 32.2 ms                                                | 26.8 ms: 1.20x faster                                                 |
| comprehensions             | 19.8 us                                                | 16.5 us: 1.20x faster                                                 |
| raytrace                   | 299 ms                                                 | 251 ms: 1.19x faster                                                  |
| scimark_sor                | 130 ms                                                 | 110 ms: 1.18x faster                                                  |
| async_generators           | 384 ms                                                 | 328 ms: 1.17x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.72 ms: 1.17x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 67.8 ms: 1.16x faster                                                 |
| regex_compile              | 142 ms                                                 | 123 ms: 1.16x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.65 us: 1.16x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.08 sec: 1.16x faster                                                |
| richards                   | 45.9 ms                                                | 39.8 ms: 1.15x faster                                                 |
| float                      | 80.8 ms                                                | 70.3 ms: 1.15x faster                                                 |
| pylint                     | 319 ms                                                 | 278 ms: 1.14x faster                                                  |
| spectral_norm              | 110 ms                                                 | 96.3 ms: 1.14x faster                                                 |
| richards_super             | 51.9 ms                                                | 45.7 ms: 1.14x faster                                                 |
| chaos                      | 62.8 ms                                                | 55.3 ms: 1.14x faster                                                 |
| pyflate                    | 448 ms                                                 | 398 ms: 1.13x faster                                                  |
| genshi_text                | 22.8 ms                                                | 20.4 ms: 1.12x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.5 ms: 1.10x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 69.5 ms: 1.10x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 62.2 ms: 1.10x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.92 sec: 1.10x faster                                                |
| sympy_integrate            | 20.5 ms                                                | 18.8 ms: 1.10x faster                                                 |
| hexiom                     | 6.17 ms                                                | 5.67 ms: 1.09x faster                                                 |
| sympy_str                  | 292 ms                                                 | 268 ms: 1.09x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 153 ms: 1.08x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.21 ms: 1.07x faster                                                 |
| thrift                     | 791 us                                                 | 737 us: 1.07x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.09 sec: 1.07x faster                                                |
| unpickle_pure_python       | 221 us                                                 | 207 us: 1.07x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 154 us: 1.06x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 91.4 ms: 1.06x faster                                                 |
| scimark_lu                 | 114 ms                                                 | 108 ms: 1.06x faster                                                  |
| 2to3                       | 264 ms                                                 | 249 ms: 1.06x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 708 ms: 1.05x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 132 ms: 1.05x faster                                                  |
| genshi_xml                 | 50.2 ms                                                | 47.8 ms: 1.05x faster                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.45 sec: 1.05x faster                                                |
| scimark_fft                | 342 ms                                                 | 326 ms: 1.05x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.52 sec: 1.05x faster                                                |
| html5lib                   | 63.6 ms                                                | 61.2 ms: 1.04x faster                                                 |
| meteor_contest             | 104 ms                                                 | 99.7 ms: 1.04x faster                                                 |
| xml_etree_generate         | 85.2 ms                                                | 82.4 ms: 1.03x faster                                                 |
| sympy_expand               | 468 ms                                                 | 455 ms: 1.03x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                                 |
| xml_etree_process          | 59.0 ms                                                | 57.6 ms: 1.02x faster                                                 |
| nqueens                    | 80.1 ms                                                | 78.6 ms: 1.02x faster                                                 |
| nbody                      | 89.3 ms                                                | 87.9 ms: 1.02x faster                                                 |
| django_template            | 34.7 ms                                                | 34.2 ms: 1.01x faster                                                 |
| logging_simple             | 6.63 us                                                | 6.54 us: 1.01x faster                                                 |
| pickle_pure_python         | 308 us                                                 | 306 us: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 518 ms: 1.00x slower                                                  |
| logging_format             | 7.35 us                                                | 7.44 us: 1.01x slower                                                 |
| sqlite_synth               | 2.20 us                                                | 2.25 us: 1.02x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 7.33 ms: 1.02x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.52 ms: 1.03x slower                                                 |
| json                       | 5.02 ms                                                | 5.19 ms: 1.03x slower                                                 |
| fannkuch                   | 372 ms                                                 | 385 ms: 1.04x slower                                                  |
| regex_dna                  | 168 ms                                                 | 174 ms: 1.04x slower                                                  |
| pidigits                   | 184 ms                                                 | 193 ms: 1.05x slower                                                  |
| mako                       | 11.0 ms                                                | 11.9 ms: 1.08x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 22.4 ms: 1.09x slower                                                 |
| json_loads                 | 26.5 us                                                | 28.9 us: 1.09x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.05 ms: 1.12x slower                                                 |
| telco                      | 6.53 ms                                                | 7.49 ms: 1.15x slower                                                 |
| coverage                   | 71.4 ms                                                | 82.0 ms: 1.15x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 12.1 ms: 1.17x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.07 ms: 1.18x slower                                                 |
| python_startup             | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.93 ms: 1.77x slower                                                 |
| logging_silent             | 109 ns                                                 | 465 ns: 4.26x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 98.7 ms: 9.14x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                          |
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250512-3.15.0a0-8cf4947/bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.109x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.15x