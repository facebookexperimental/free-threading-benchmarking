# Results vs. 3.12.6

- fork: python
- ref: 4ddf505d9982dc8afead
- machine: linux-x86_64
- commit hash: 4ddf505
- commit date: 2025-06-20
- overall geometric mean: 1.019x faster
- HPT reliability: 78.56%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.44x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 282 ms: 1.07x slower                                                  |
| docutils       | 2.64 sec                                               | 2.67 sec: 1.01x slower                                                |
| html5lib       | 63.6 ms                                                | 66.1 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                  | 1.04x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 522 ms: 2.12x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 224 ms: 1.99x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 284 ms: 1.97x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 550 ms: 1.97x faster                                                  |
| async_tree_none            | 464 ms                                                 | 257 ms: 1.81x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 312 ms: 1.78x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 463 ms: 1.56x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 488 ms: 1.46x faster                                                  |
| async_generators           | 384 ms                                                 | 364 ms: 1.05x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.1 ms: 1.03x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.56x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 68.8 ms: 1.17x faster                                                 |
| pidigits       | 184 ms                                                 | 182 ms: 1.01x faster                                                  |
| nbody          | 89.3 ms                                                | 121 ms: 1.35x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.66 ms: 1.19x faster                                                 |
| regex_v8       | 20.6 ms                                                | 20.8 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (2): regex_compile, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 86.8 ms: 1.11x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.08x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.15 sec: 1.02x slower                                                |
| unpickle_pure_python | 221 us                                                 | 229 us: 1.04x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 337 us: 1.09x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 94.6 ms: 1.11x slower                                                 |
| json_dumps           | 10.4 ms                                                | 11.8 ms: 1.14x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 68.6 ms: 1.16x slower                                                 |
| json_loads           | 26.5 us                                                | 31.0 us: 1.17x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.06x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.61 ms: 1.34x slower                                                 |
| python_startup         | 9.93 ms                                                | 16.1 ms: 1.62x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 39.4 ms: 1.13x slower                                                 |
| genshi_xml      | 50.2 ms                                                | 58.2 ms: 1.16x slower                                                 |
| genshi_text     | 22.8 ms                                                | 26.5 ms: 1.16x slower                                                 |
| mako            | 11.0 ms                                                | 15.9 ms: 1.45x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.22x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 522 ms: 2.12x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 224 ms: 1.99x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 284 ms: 1.97x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 550 ms: 1.97x faster                                                  |
| mdp                        | 2.42 sec                                               | 1.31 sec: 1.84x faster                                                |
| async_tree_none            | 464 ms                                                 | 257 ms: 1.81x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 1.93 ms: 1.79x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 312 ms: 1.78x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 463 ms: 1.56x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 488 ms: 1.46x faster                                                  |
| deepcopy                   | 352 us                                                 | 286 us: 1.23x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.66 ms: 1.19x faster                                                 |
| float                      | 80.8 ms                                                | 68.8 ms: 1.17x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 34.4 us: 1.17x faster                                                 |
| go                         | 139 ms                                                 | 121 ms: 1.15x faster                                                  |
| comprehensions             | 19.8 us                                                | 17.6 us: 1.12x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 86.8 ms: 1.11x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 71.1 ms: 1.11x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.5 ms: 1.10x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.02 us: 1.09x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.34 sec: 1.09x faster                                                |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.08x faster                                                  |
| scimark_sor                | 130 ms                                                 | 122 ms: 1.06x faster                                                  |
| async_generators           | 384 ms                                                 | 364 ms: 1.05x faster                                                  |
| pylint                     | 319 ms                                                 | 306 ms: 1.04x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.1 ms: 1.03x faster                                                 |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.03x faster                                                |
| deepcopy_reduce            | 3.08 us                                                | 2.99 us: 1.03x faster                                                 |
| generators                 | 32.2 ms                                                | 31.7 ms: 1.02x faster                                                 |
| spectral_norm              | 110 ms                                                 | 108 ms: 1.02x faster                                                  |
| chaos                      | 62.8 ms                                                | 61.8 ms: 1.02x faster                                                 |
| pidigits                   | 184 ms                                                 | 182 ms: 1.01x faster                                                  |
| raytrace                   | 299 ms                                                 | 297 ms: 1.01x faster                                                  |
| regex_v8                   | 20.6 ms                                                | 20.8 ms: 1.01x slower                                                 |
| docutils                   | 2.64 sec                                               | 2.67 sec: 1.01x slower                                                |
| tomli_loads                | 2.11 sec                                               | 2.15 sec: 1.02x slower                                                |
| hexiom                     | 6.17 ms                                                | 6.33 ms: 1.03x slower                                                 |
| html5lib                   | 63.6 ms                                                | 66.1 ms: 1.04x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 229 us: 1.04x slower                                                  |
| scimark_fft                | 342 ms                                                 | 356 ms: 1.04x slower                                                  |
| json                       | 5.02 ms                                                | 5.25 ms: 1.04x slower                                                 |
| deltablue                  | 3.45 ms                                                | 3.60 ms: 1.04x slower                                                 |
| pyflate                    | 448 ms                                                 | 477 ms: 1.07x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 21.9 ms: 1.07x slower                                                 |
| 2to3                       | 264 ms                                                 | 282 ms: 1.07x slower                                                  |
| nqueens                    | 80.1 ms                                                | 85.8 ms: 1.07x slower                                                 |
| sympy_str                  | 292 ms                                                 | 314 ms: 1.08x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 179 ms: 1.08x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 337 us: 1.09x slower                                                  |
| thrift                     | 791 us                                                 | 876 us: 1.11x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 127 ms: 1.11x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 75.9 ms: 1.11x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 94.6 ms: 1.11x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 85.1 ms: 1.11x slower                                                 |
| sympy_expand               | 468 ms                                                 | 522 ms: 1.12x slower                                                  |
| django_template            | 34.7 ms                                                | 39.4 ms: 1.13x slower                                                 |
| richards                   | 45.9 ms                                                | 52.4 ms: 1.14x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 11.8 ms: 1.14x slower                                                 |
| logging_simple             | 6.63 us                                                | 7.60 us: 1.15x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 188 us: 1.15x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 58.2 ms: 1.16x slower                                                 |
| genshi_text                | 22.8 ms                                                | 26.5 ms: 1.16x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 68.6 ms: 1.16x slower                                                 |
| richards_super             | 51.9 ms                                                | 60.4 ms: 1.16x slower                                                 |
| json_loads                 | 26.5 us                                                | 31.0 us: 1.17x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 868 ms: 1.17x slower                                                  |
| meteor_contest             | 104 ms                                                 | 121 ms: 1.17x slower                                                  |
| logging_format             | 7.35 us                                                | 8.62 us: 1.17x slower                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.79 sec: 1.18x slower                                                |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.36 ms: 1.22x slower                                                 |
| fannkuch                   | 372 ms                                                 | 463 ms: 1.24x slower                                                  |
| telco                      | 6.53 ms                                                | 8.49 ms: 1.30x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 9.61 ms: 1.34x slower                                                 |
| nbody                      | 89.3 ms                                                | 121 ms: 1.35x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.50 ms: 1.37x slower                                                 |
| mako                       | 11.0 ms                                                | 15.9 ms: 1.45x slower                                                 |
| coverage                   | 71.4 ms                                                | 110 ms: 1.54x slower                                                  |
| python_startup             | 9.93 ms                                                | 16.1 ms: 1.62x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.11 ms: 3.30x slower                                                 |
| logging_silent             | 109 ns                                                 | 523 ns: 4.80x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 103 ms: 9.57x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.04x slower                                                          |

Benchmark hidden because not significant (3): asyncio_websockets, regex_compile, regex_dna
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250620-3.15.0a0-4ddf505-NOGIL/bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.019x faster

# HPT report

- Reliability score: 78.56% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.44x