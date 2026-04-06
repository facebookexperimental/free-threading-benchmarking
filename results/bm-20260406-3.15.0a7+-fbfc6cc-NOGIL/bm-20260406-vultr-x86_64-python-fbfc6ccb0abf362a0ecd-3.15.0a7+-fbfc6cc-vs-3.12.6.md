# Results vs. 3.12.6

- fork: python
- ref: fbfc6ccb0abf362a0ecd
- machine: linux-x86_64
- commit hash: fbfc6cc
- commit date: 2026-04-06
- overall geometric mean: 1.026x slower
- HPT reliability: 72.56%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.44x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 283 ms: 1.07x slower                                                   |
| docutils       | 2.64 sec                                               | 2.65 sec: 1.00x slower                                                 |
| html5lib       | 63.6 ms                                                | 65.5 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 614 ms: 1.81x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 327 ms: 1.71x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 642 ms: 1.69x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 265 ms: 1.68x faster                                                   |
| async_tree_none            | 464 ms                                                 | 292 ms: 1.59x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 358 ms: 1.55x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 509 ms: 1.42x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 536 ms: 1.33x faster                                                   |
| async_generators           | 384 ms                                                 | 375 ms: 1.03x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 514 ms: 1.01x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.41x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 74.5 ms: 1.08x faster                                                  |
| pidigits       | 184 ms                                                 | 181 ms: 1.02x faster                                                   |
| nbody          | 89.3 ms                                                | 125 ms: 1.40x slower                                                   |
| Geometric mean | (ref)                                                  | 1.08x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.73 ms: 1.16x faster                                                  |
| regex_compile  | 142 ms                                                 | 142 ms: 1.01x faster                                                   |
| regex_v8       | 20.6 ms                                                | 20.5 ms: 1.01x faster                                                  |
| regex_dna      | 168 ms                                                 | 169 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 86.8 ms: 1.11x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 1.96 sec: 1.08x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.05x faster                                                   |
| json_dumps           | 10.4 ms                                                | 11.0 ms: 1.07x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 236 us: 1.07x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 336 us: 1.09x slower                                                   |
| json_loads           | 26.5 us                                                | 29.5 us: 1.11x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 96.7 ms: 1.14x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 69.1 ms: 1.17x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.04x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.86 ms: 1.38x slower                                                  |
| python_startup         | 9.93 ms                                                | 16.1 ms: 1.62x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.50x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 55.1 ms: 1.10x slower                                                  |
| genshi_text     | 22.8 ms                                                | 25.7 ms: 1.13x slower                                                  |
| django_template | 34.7 ms                                                | 39.8 ms: 1.15x slower                                                  |
| mako            | 11.0 ms                                                | 15.9 ms: 1.45x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.20x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.31 sec: 1.85x faster                                                 |
| async_tree_io_tg           | 1.11 sec                                               | 614 ms: 1.81x faster                                                   |
| gc_traversal               | 3.46 ms                                                | 1.93 ms: 1.79x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 327 ms: 1.71x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 642 ms: 1.69x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 265 ms: 1.68x faster                                                   |
| async_tree_none            | 464 ms                                                 | 292 ms: 1.59x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 358 ms: 1.55x faster                                                   |
| bench_mp_pool              | 10.8 ms                                                | 7.03 ms: 1.54x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 509 ms: 1.42x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 536 ms: 1.33x faster                                                   |
| deepcopy                   | 352 us                                                 | 267 us: 1.32x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 31.6 us: 1.27x faster                                                  |
| pathlib                    | 21.5 ms                                                | 17.4 ms: 1.24x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.73 ms: 1.16x faster                                                  |
| go                         | 139 ms                                                 | 121 ms: 1.15x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 1.93 us: 1.14x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 86.8 ms: 1.11x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 71.1 ms: 1.11x faster                                                  |
| float                      | 80.8 ms                                                | 74.5 ms: 1.08x faster                                                  |
| comprehensions             | 19.8 us                                                | 18.4 us: 1.08x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.39 sec: 1.08x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.96 sec: 1.08x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.90 us: 1.06x faster                                                  |
| pylint                     | 319 ms                                                 | 300 ms: 1.06x faster                                                   |
| scimark_sor                | 130 ms                                                 | 122 ms: 1.06x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.05x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.12 sec: 1.04x faster                                                 |
| async_generators           | 384 ms                                                 | 375 ms: 1.03x faster                                                   |
| logging_silent             | 109 ns                                                 | 107 ns: 1.02x faster                                                   |
| pidigits                   | 184 ms                                                 | 181 ms: 1.02x faster                                                   |
| chaos                      | 62.8 ms                                                | 61.7 ms: 1.02x faster                                                  |
| regex_compile              | 142 ms                                                 | 142 ms: 1.01x faster                                                   |
| regex_v8                   | 20.6 ms                                                | 20.5 ms: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 514 ms: 1.01x faster                                                   |
| docutils                   | 2.64 sec                                               | 2.65 sec: 1.00x slower                                                 |
| regex_dna                  | 168 ms                                                 | 169 ms: 1.01x slower                                                   |
| raytrace                   | 299 ms                                                 | 302 ms: 1.01x slower                                                   |
| logging_simple             | 6.63 us                                                | 6.72 us: 1.01x slower                                                  |
| deltablue                  | 3.45 ms                                                | 3.49 ms: 1.01x slower                                                  |
| json                       | 5.02 ms                                                | 5.12 ms: 1.02x slower                                                  |
| spectral_norm              | 110 ms                                                 | 113 ms: 1.02x slower                                                   |
| scimark_fft                | 342 ms                                                 | 350 ms: 1.02x slower                                                   |
| html5lib                   | 63.6 ms                                                | 65.5 ms: 1.03x slower                                                  |
| logging_format             | 7.35 us                                                | 7.64 us: 1.04x slower                                                  |
| pyflate                    | 448 ms                                                 | 469 ms: 1.05x slower                                                   |
| sympy_integrate            | 20.5 ms                                                | 21.9 ms: 1.06x slower                                                  |
| sympy_str                  | 292 ms                                                 | 311 ms: 1.07x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 11.0 ms: 1.07x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 794 ms: 1.07x slower                                                   |
| sympy_sum                  | 166 ms                                                 | 178 ms: 1.07x slower                                                   |
| unpickle_pure_python       | 221 us                                                 | 236 us: 1.07x slower                                                   |
| 2to3                       | 264 ms                                                 | 283 ms: 1.07x slower                                                   |
| hexiom                     | 6.17 ms                                                | 6.66 ms: 1.08x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.65 sec: 1.09x slower                                                 |
| nqueens                    | 80.1 ms                                                | 87.3 ms: 1.09x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 336 us: 1.09x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 55.1 ms: 1.10x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 126 ms: 1.11x slower                                                   |
| json_loads                 | 26.5 us                                                | 29.5 us: 1.11x slower                                                  |
| sympy_expand               | 468 ms                                                 | 522 ms: 1.12x slower                                                   |
| genshi_text                | 22.8 ms                                                | 25.7 ms: 1.13x slower                                                  |
| richards                   | 45.9 ms                                                | 52.1 ms: 1.13x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 96.7 ms: 1.14x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 78.4 ms: 1.15x slower                                                  |
| richards_super             | 51.9 ms                                                | 59.4 ms: 1.15x slower                                                  |
| django_template            | 34.7 ms                                                | 39.8 ms: 1.15x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 88.2 ms: 1.15x slower                                                  |
| thrift                     | 791 us                                                 | 924 us: 1.17x slower                                                   |
| typing_runtime_protocols   | 163 us                                                 | 191 us: 1.17x slower                                                   |
| xml_etree_process          | 59.0 ms                                                | 69.1 ms: 1.17x slower                                                  |
| meteor_contest             | 104 ms                                                 | 123 ms: 1.18x slower                                                   |
| fannkuch                   | 372 ms                                                 | 458 ms: 1.23x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.55 ms: 1.26x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.50 ms: 1.37x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 9.86 ms: 1.38x slower                                                  |
| nbody                      | 89.3 ms                                                | 125 ms: 1.40x slower                                                   |
| mako                       | 11.0 ms                                                | 15.9 ms: 1.45x slower                                                  |
| coverage                   | 71.4 ms                                                | 110 ms: 1.54x slower                                                   |
| bench_thread_pool          | 941 us                                                 | 1.46 ms: 1.55x slower                                                  |
| python_startup             | 9.93 ms                                                | 16.1 ms: 1.62x slower                                                  |
| telco                      | 6.53 ms                                                | 172 ms: 26.42x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.02x slower                                                           |

Benchmark hidden because not significant (2): coroutines, generators
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260406-3.15.0a7+-fbfc6cc-NOGIL/bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.026x slower

# HPT report

- Reliability score: 72.56% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.44x