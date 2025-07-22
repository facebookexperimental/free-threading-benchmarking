# Results vs. 3.12.6

- fork: python
- ref: bbe589f93ccaf32eb95f
- machine: linux-x86_64
- commit hash: bbe589f
- commit date: 2025-07-22
- overall geometric mean: 1.023x slower
- HPT reliability: 94.16%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 284 ms: 1.08x slower                                                  |
| docutils       | 2.64 sec                                               | 2.70 sec: 1.02x slower                                                |
| html5lib       | 63.6 ms                                                | 66.8 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                  | 1.05x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 510 ms: 2.18x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 536 ms: 2.02x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 223 ms: 2.00x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 281 ms: 1.99x faster                                                  |
| async_tree_none            | 464 ms                                                 | 253 ms: 1.83x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 308 ms: 1.80x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 485 ms: 1.49x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 509 ms: 1.40x faster                                                  |
| async_generators           | 384 ms                                                 | 375 ms: 1.03x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 513 ms: 1.01x faster                                                  |
| coroutines                 | 23.9 ms                                                | 24.7 ms: 1.03x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.55x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 69.1 ms: 1.17x faster                                                 |
| pidigits       | 184 ms                                                 | 192 ms: 1.04x slower                                                  |
| nbody          | 89.3 ms                                                | 126 ms: 1.41x slower                                                  |
| Geometric mean | (ref)                                                  | 1.08x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.71 ms: 1.17x faster                                                 |
| regex_compile  | 142 ms                                                 | 143 ms: 1.00x slower                                                  |
| regex_v8       | 20.6 ms                                                | 20.7 ms: 1.00x slower                                                 |
| regex_dna      | 168 ms                                                 | 175 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.1 ms: 1.11x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.16 sec: 1.02x slower                                                |
| unpickle_pure_python | 221 us                                                 | 233 us: 1.06x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 341 us: 1.11x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 96.5 ms: 1.13x slower                                                 |
| json_dumps           | 10.4 ms                                                | 12.1 ms: 1.17x slower                                                 |
| json_loads           | 26.5 us                                                | 31.5 us: 1.19x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 70.1 ms: 1.19x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.07x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.55 ms: 1.33x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.45x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 57.4 ms: 1.14x slower                                                 |
| django_template | 34.7 ms                                                | 40.2 ms: 1.16x slower                                                 |
| genshi_text     | 22.8 ms                                                | 26.7 ms: 1.17x slower                                                 |
| mako            | 11.0 ms                                                | 15.7 ms: 1.42x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.22x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 510 ms: 2.18x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 536 ms: 2.02x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 223 ms: 2.00x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 281 ms: 1.99x faster                                                  |
| mdp                        | 2.42 sec                                               | 1.31 sec: 1.85x faster                                                |
| async_tree_none            | 464 ms                                                 | 253 ms: 1.83x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 308 ms: 1.80x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 1.95 ms: 1.77x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 485 ms: 1.49x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 509 ms: 1.40x faster                                                  |
| deepcopy                   | 352 us                                                 | 298 us: 1.18x faster                                                  |
| float                      | 80.8 ms                                                | 69.1 ms: 1.17x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.71 ms: 1.17x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 34.9 us: 1.15x faster                                                 |
| go                         | 139 ms                                                 | 121 ms: 1.15x faster                                                  |
| comprehensions             | 19.8 us                                                | 17.6 us: 1.13x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.4 ms: 1.11x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 87.1 ms: 1.11x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 71.5 ms: 1.10x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.37 sec: 1.08x faster                                                |
| sqlite_synth               | 2.20 us                                                | 2.06 us: 1.07x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                  |
| generators                 | 32.2 ms                                                | 30.5 ms: 1.06x faster                                                 |
| logging_silent             | 109 ns                                                 | 104 ns: 1.05x faster                                                  |
| scimark_sor                | 130 ms                                                 | 124 ms: 1.05x faster                                                  |
| pylint                     | 319 ms                                                 | 308 ms: 1.03x faster                                                  |
| async_generators           | 384 ms                                                 | 375 ms: 1.03x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.14 sec: 1.02x faster                                                |
| deepcopy_reduce            | 3.08 us                                                | 3.05 us: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 513 ms: 1.01x faster                                                  |
| regex_compile              | 142 ms                                                 | 143 ms: 1.00x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 20.7 ms: 1.00x slower                                                 |
| chaos                      | 62.8 ms                                                | 63.5 ms: 1.01x slower                                                 |
| docutils                   | 2.64 sec                                               | 2.70 sec: 1.02x slower                                                |
| tomli_loads                | 2.11 sec                                               | 2.16 sec: 1.02x slower                                                |
| spectral_norm              | 110 ms                                                 | 113 ms: 1.03x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.7 ms: 1.03x slower                                                 |
| hexiom                     | 6.17 ms                                                | 6.38 ms: 1.03x slower                                                 |
| pyflate                    | 448 ms                                                 | 464 ms: 1.04x slower                                                  |
| pidigits                   | 184 ms                                                 | 192 ms: 1.04x slower                                                  |
| regex_dna                  | 168 ms                                                 | 175 ms: 1.04x slower                                                  |
| logging_simple             | 6.63 us                                                | 6.94 us: 1.05x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 781 ms: 1.05x slower                                                  |
| html5lib                   | 63.6 ms                                                | 66.8 ms: 1.05x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 233 us: 1.06x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.62 sec: 1.06x slower                                                |
| deltablue                  | 3.45 ms                                                | 3.67 ms: 1.07x slower                                                 |
| json                       | 5.02 ms                                                | 5.37 ms: 1.07x slower                                                 |
| sympy_str                  | 292 ms                                                 | 312 ms: 1.07x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 22.1 ms: 1.07x slower                                                 |
| scimark_fft                | 342 ms                                                 | 368 ms: 1.08x slower                                                  |
| 2to3                       | 264 ms                                                 | 284 ms: 1.08x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 180 ms: 1.09x slower                                                  |
| nqueens                    | 80.1 ms                                                | 87.6 ms: 1.09x slower                                                 |
| logging_format             | 7.35 us                                                | 8.10 us: 1.10x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 341 us: 1.11x slower                                                  |
| richards                   | 45.9 ms                                                | 51.1 ms: 1.11x slower                                                 |
| thrift                     | 791 us                                                 | 881 us: 1.11x slower                                                  |
| sympy_expand               | 468 ms                                                 | 522 ms: 1.12x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 86.4 ms: 1.13x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 96.5 ms: 1.13x slower                                                 |
| richards_super             | 51.9 ms                                                | 58.9 ms: 1.14x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 130 ms: 1.14x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 57.4 ms: 1.14x slower                                                 |
| meteor_contest             | 104 ms                                                 | 119 ms: 1.15x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 78.8 ms: 1.15x slower                                                 |
| django_template            | 34.7 ms                                                | 40.2 ms: 1.16x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 12.1 ms: 1.17x slower                                                 |
| genshi_text                | 22.8 ms                                                | 26.7 ms: 1.17x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 192 us: 1.17x slower                                                  |
| json_loads                 | 26.5 us                                                | 31.5 us: 1.19x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 70.1 ms: 1.19x slower                                                 |
| fannkuch                   | 372 ms                                                 | 455 ms: 1.22x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.62 ms: 1.28x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 9.55 ms: 1.33x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.53 ms: 1.40x slower                                                 |
| nbody                      | 89.3 ms                                                | 126 ms: 1.41x slower                                                  |
| mako                       | 11.0 ms                                                | 15.7 ms: 1.42x slower                                                 |
| coverage                   | 71.4 ms                                                | 111 ms: 1.56x slower                                                  |
| python_startup             | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.16 ms: 3.36x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 108 ms: 10.00x slower                                                 |
| telco                      | 6.53 ms                                                | 176 ms: 26.89x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.07x slower                                                          |

Benchmark hidden because not significant (1): raytrace
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250722-3.15.0a0-bbe589f-NOGIL/bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.023x slower

# HPT report

- Reliability score: 94.16% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.40x