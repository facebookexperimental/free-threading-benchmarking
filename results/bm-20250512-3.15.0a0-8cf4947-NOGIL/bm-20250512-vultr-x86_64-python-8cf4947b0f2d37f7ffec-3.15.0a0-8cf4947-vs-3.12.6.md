# Results vs. 3.12.6

- fork: python
- ref: 8cf4947b0f2d37f7ffec
- machine: linux-x86_64
- commit hash: 8cf4947
- commit date: 2025-05-12
- overall geometric mean: 1.010x faster
- HPT reliability: 86.29%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.43x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 285 ms: 1.08x slower                                                  |
| docutils       | 2.64 sec                                               | 2.70 sec: 1.02x slower                                                |
| html5lib       | 63.6 ms                                                | 67.0 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                  | 1.05x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 523 ms: 2.12x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 227 ms: 1.97x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 284 ms: 1.97x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 551 ms: 1.96x faster                                                  |
| async_tree_none            | 464 ms                                                 | 258 ms: 1.80x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 311 ms: 1.78x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 485 ms: 1.49x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 509 ms: 1.41x faster                                                  |
| async_generators           | 384 ms                                                 | 371 ms: 1.04x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 515 ms: 1.00x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.54x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.8 ms: 1.14x faster                                                 |
| pidigits       | 184 ms                                                 | 200 ms: 1.09x slower                                                  |
| nbody          | 89.3 ms                                                | 120 ms: 1.35x slower                                                  |
| Geometric mean | (ref)                                                  | 1.09x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.83 ms: 1.12x faster                                                 |
| regex_compile  | 142 ms                                                 | 144 ms: 1.01x slower                                                  |
| regex_v8       | 20.6 ms                                                | 21.0 ms: 1.02x slower                                                 |
| regex_dna      | 168 ms                                                 | 182 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                  | 1.00x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 86.8 ms: 1.11x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.12 sec: 1.01x slower                                                |
| unpickle_pure_python | 221 us                                                 | 230 us: 1.04x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 333 us: 1.08x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 96.0 ms: 1.13x slower                                                 |
| json_loads           | 26.5 us                                                | 30.4 us: 1.15x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 68.3 ms: 1.16x slower                                                 |
| json_dumps           | 10.4 ms                                                | 13.3 ms: 1.28x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.07x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.61 ms: 1.34x slower                                                 |
| python_startup         | 9.93 ms                                                | 16.0 ms: 1.62x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 55.3 ms: 1.10x slower                                                 |
| genshi_text     | 22.8 ms                                                | 25.6 ms: 1.12x slower                                                 |
| django_template | 34.7 ms                                                | 40.7 ms: 1.17x slower                                                 |
| mako            | 11.0 ms                                                | 15.4 ms: 1.40x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.19x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 523 ms: 2.12x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 227 ms: 1.97x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 284 ms: 1.97x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 551 ms: 1.96x faster                                                  |
| mdp                        | 2.42 sec                                               | 1.33 sec: 1.82x faster                                                |
| async_tree_none            | 464 ms                                                 | 258 ms: 1.80x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 1.93 ms: 1.79x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 311 ms: 1.78x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 485 ms: 1.49x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 509 ms: 1.41x faster                                                  |
| deepcopy                   | 352 us                                                 | 291 us: 1.21x faster                                                  |
| float                      | 80.8 ms                                                | 70.8 ms: 1.14x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 35.6 us: 1.13x faster                                                 |
| go                         | 139 ms                                                 | 123 ms: 1.13x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.83 ms: 1.12x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 86.8 ms: 1.11x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 71.2 ms: 1.11x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.6 ms: 1.10x faster                                                 |
| generators                 | 32.2 ms                                                | 29.4 ms: 1.10x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.39 sec: 1.08x faster                                                |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                  |
| scimark_sor                | 130 ms                                                 | 122 ms: 1.06x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.08 us: 1.06x faster                                                 |
| pylint                     | 319 ms                                                 | 306 ms: 1.04x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.04x faster                                                |
| async_generators           | 384 ms                                                 | 371 ms: 1.04x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 3.00 us: 1.03x faster                                                 |
| chaos                      | 62.8 ms                                                | 61.7 ms: 1.02x faster                                                 |
| comprehensions             | 19.8 us                                                | 19.5 us: 1.02x faster                                                 |
| spectral_norm              | 110 ms                                                 | 109 ms: 1.01x faster                                                  |
| raytrace                   | 299 ms                                                 | 297 ms: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 515 ms: 1.00x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 2.12 sec: 1.01x slower                                                |
| regex_compile              | 142 ms                                                 | 144 ms: 1.01x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 21.0 ms: 1.02x slower                                                 |
| json                       | 5.02 ms                                                | 5.14 ms: 1.02x slower                                                 |
| docutils                   | 2.64 sec                                               | 2.70 sec: 1.02x slower                                                |
| deltablue                  | 3.45 ms                                                | 3.54 ms: 1.03x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 773 ms: 1.04x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 230 us: 1.04x slower                                                  |
| html5lib                   | 63.6 ms                                                | 67.0 ms: 1.05x slower                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.61 sec: 1.06x slower                                                |
| hexiom                     | 6.17 ms                                                | 6.58 ms: 1.07x slower                                                 |
| scimark_fft                | 342 ms                                                 | 365 ms: 1.07x slower                                                  |
| pyflate                    | 448 ms                                                 | 481 ms: 1.07x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 22.2 ms: 1.08x slower                                                 |
| 2to3                       | 264 ms                                                 | 285 ms: 1.08x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 333 us: 1.08x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 180 ms: 1.08x slower                                                  |
| nqueens                    | 80.1 ms                                                | 86.9 ms: 1.08x slower                                                 |
| regex_dna                  | 168 ms                                                 | 182 ms: 1.09x slower                                                  |
| pidigits                   | 184 ms                                                 | 200 ms: 1.09x slower                                                  |
| sympy_str                  | 292 ms                                                 | 317 ms: 1.09x slower                                                  |
| thrift                     | 791 us                                                 | 871 us: 1.10x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 55.3 ms: 1.10x slower                                                 |
| richards                   | 45.9 ms                                                | 50.7 ms: 1.10x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 84.7 ms: 1.11x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 76.5 ms: 1.12x slower                                                 |
| richards_super             | 51.9 ms                                                | 58.0 ms: 1.12x slower                                                 |
| genshi_text                | 22.8 ms                                                | 25.6 ms: 1.12x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 96.0 ms: 1.13x slower                                                 |
| sympy_expand               | 468 ms                                                 | 536 ms: 1.15x slower                                                  |
| json_loads                 | 26.5 us                                                | 30.4 us: 1.15x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 132 ms: 1.15x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 68.3 ms: 1.16x slower                                                 |
| django_template            | 34.7 ms                                                | 40.7 ms: 1.17x slower                                                 |
| logging_simple             | 6.63 us                                                | 7.81 us: 1.18x slower                                                 |
| logging_format             | 7.35 us                                                | 8.78 us: 1.20x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 196 us: 1.20x slower                                                  |
| meteor_contest             | 104 ms                                                 | 129 ms: 1.25x slower                                                  |
| fannkuch                   | 372 ms                                                 | 467 ms: 1.25x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.53 ms: 1.26x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 13.3 ms: 1.28x slower                                                 |
| telco                      | 6.53 ms                                                | 8.66 ms: 1.33x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 9.61 ms: 1.34x slower                                                 |
| nbody                      | 89.3 ms                                                | 120 ms: 1.35x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.51 ms: 1.38x slower                                                 |
| mako                       | 11.0 ms                                                | 15.4 ms: 1.40x slower                                                 |
| coverage                   | 71.4 ms                                                | 109 ms: 1.52x slower                                                  |
| python_startup             | 9.93 ms                                                | 16.0 ms: 1.62x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.12 ms: 3.31x slower                                                 |
| logging_silent             | 109 ns                                                 | 541 ns: 4.97x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 103 ms: 9.55x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.05x slower                                                          |
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250512-3.15.0a0-8cf4947-NOGIL/bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.010x faster

# HPT report

- Reliability score: 86.29% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.43x