# Results vs. 3.12.6

- fork: python
- ref: 3945eaf2fcd9cbc3f306
- machine: linux-x86_64
- commit hash: 3945eaf
- commit date: 2026-11-03
- overall geometric mean: 1.035x slower
- HPT reliability: 77.92%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261103-vultr-x86_64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 291 ms: 1.10x slower                                                      |
| docutils       | 2.64 sec                                               | 2.83 sec: 1.07x slower                                                    |
| html5lib       | 63.6 ms                                                | 65.1 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                  | 1.07x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261103-vultr-x86_64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 705 ms: 1.57x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 715 ms: 1.51x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 399 ms: 1.40x faster                                                      |
| async_tree_none            | 464 ms                                                 | 339 ms: 1.37x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 333 ms: 1.34x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 419 ms: 1.32x faster                                                      |
| async_generators           | 384 ms                                                 | 295 ms: 1.30x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 571 ms: 1.27x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 574 ms: 1.25x faster                                                      |
| asyncio_websockets         | 517 ms                                                 | 502 ms: 1.03x faster                                                      |
| coroutines                 | 23.9 ms                                                | 26.0 ms: 1.09x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.29x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261103-vultr-x86_64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 190 ms: 1.03x slower                                                      |
| float          | 80.8 ms                                                | 84.0 ms: 1.04x slower                                                     |
| nbody          | 89.3 ms                                                | 117 ms: 1.31x slower                                                      |
| Geometric mean | (ref)                                                  | 1.12x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261103-vultr-x86_64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.99 ms: 1.06x faster                                                     |
| regex_v8       | 20.6 ms                                                | 21.0 ms: 1.02x slower                                                     |
| regex_dna      | 168 ms                                                 | 180 ms: 1.07x slower                                                      |
| regex_compile  | 142 ms                                                 | 171 ms: 1.20x slower                                                      |
| Geometric mean | (ref)                                                  | 1.05x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261103-vultr-x86_64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.95 sec: 1.08x faster                                                    |
| json_dumps           | 10.4 ms                                                | 10.1 ms: 1.03x faster                                                     |
| xml_etree_iterparse  | 96.7 ms                                                | 96.2 ms: 1.00x faster                                                     |
| xml_etree_parse      | 139 ms                                                 | 145 ms: 1.05x slower                                                      |
| unpickle_pure_python | 221 us                                                 | 240 us: 1.09x slower                                                      |
| pickle_pure_python   | 308 us                                                 | 352 us: 1.15x slower                                                      |
| json_loads           | 26.5 us                                                | 30.7 us: 1.16x slower                                                     |
| xml_etree_generate   | 85.2 ms                                                | 101 ms: 1.19x slower                                                      |
| xml_etree_process    | 59.0 ms                                                | 75.7 ms: 1.28x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.08x slower                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261103-vultr-x86_64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 8.93 ms: 1.25x slower                                                     |
| python_startup         | 9.93 ms                                                | 13.4 ms: 1.35x slower                                                     |
| Geometric mean         | (ref)                                                  | 1.30x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261103-vultr-x86_64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 41.1 ms: 1.19x slower                                                     |
| mako            | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                     |
| Geometric mean  | (ref)                                                  | 1.30x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261103-vultr-x86_64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 128 ms: 2.48x faster                                                      |
| gc_traversal               | 3.46 ms                                                | 1.82 ms: 1.90x faster                                                     |
| mdp                        | 2.42 sec                                               | 1.30 sec: 1.87x faster                                                    |
| bench_mp_pool              | 10.8 ms                                                | 6.65 ms: 1.62x faster                                                     |
| async_tree_io_tg           | 1.11 sec                                               | 705 ms: 1.57x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 715 ms: 1.51x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 399 ms: 1.40x faster                                                      |
| async_tree_none            | 464 ms                                                 | 339 ms: 1.37x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 333 ms: 1.34x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 419 ms: 1.32x faster                                                      |
| async_generators           | 384 ms                                                 | 295 ms: 1.30x faster                                                      |
| deepcopy                   | 352 us                                                 | 274 us: 1.28x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 571 ms: 1.27x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 574 ms: 1.25x faster                                                      |
| deepcopy_memo              | 40.3 us                                                | 33.3 us: 1.21x faster                                                     |
| pathlib                    | 21.5 ms                                                | 18.2 ms: 1.19x faster                                                     |
| typing_runtime_protocols   | 163 us                                                 | 139 us: 1.18x faster                                                      |
| go                         | 139 ms                                                 | 122 ms: 1.15x faster                                                      |
| comprehensions             | 19.8 us                                                | 18.0 us: 1.10x faster                                                     |
| dulwich_log                | 78.9 ms                                                | 72.5 ms: 1.09x faster                                                     |
| bpe_tokeniser              | 4.74 sec                                               | 4.36 sec: 1.09x faster                                                    |
| sqlite_synth               | 2.20 us                                                | 2.03 us: 1.08x faster                                                     |
| tomli_loads                | 2.11 sec                                               | 1.95 sec: 1.08x faster                                                    |
| scimark_sor                | 130 ms                                                 | 121 ms: 1.07x faster                                                      |
| regex_effbot               | 3.17 ms                                                | 2.99 ms: 1.06x faster                                                     |
| spectral_norm              | 110 ms                                                 | 105 ms: 1.05x faster                                                      |
| json_dumps                 | 10.4 ms                                                | 10.1 ms: 1.03x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 502 ms: 1.03x faster                                                      |
| chaos                      | 62.8 ms                                                | 61.2 ms: 1.03x faster                                                     |
| deepcopy_reduce            | 3.08 us                                                | 3.00 us: 1.02x faster                                                     |
| scimark_fft                | 342 ms                                                 | 334 ms: 1.02x faster                                                      |
| pyflate                    | 448 ms                                                 | 441 ms: 1.02x faster                                                      |
| raytrace                   | 299 ms                                                 | 296 ms: 1.01x faster                                                      |
| xml_etree_iterparse        | 96.7 ms                                                | 96.2 ms: 1.00x faster                                                     |
| regex_v8                   | 20.6 ms                                                | 21.0 ms: 1.02x slower                                                     |
| html5lib                   | 63.6 ms                                                | 65.1 ms: 1.02x slower                                                     |
| pidigits                   | 184 ms                                                 | 190 ms: 1.03x slower                                                      |
| float                      | 80.8 ms                                                | 84.0 ms: 1.04x slower                                                     |
| xml_etree_parse            | 139 ms                                                 | 145 ms: 1.05x slower                                                      |
| generators                 | 32.2 ms                                                | 34.1 ms: 1.06x slower                                                     |
| logging_simple             | 6.63 us                                                | 7.10 us: 1.07x slower                                                     |
| regex_dna                  | 168 ms                                                 | 180 ms: 1.07x slower                                                      |
| docutils                   | 2.64 sec                                               | 2.83 sec: 1.07x slower                                                    |
| hexiom                     | 6.17 ms                                                | 6.65 ms: 1.08x slower                                                     |
| sympy_integrate            | 20.5 ms                                                | 22.2 ms: 1.08x slower                                                     |
| unpickle_pure_python       | 221 us                                                 | 240 us: 1.09x slower                                                      |
| coroutines                 | 23.9 ms                                                | 26.0 ms: 1.09x slower                                                     |
| pprint_safe_repr           | 743 ms                                                 | 809 ms: 1.09x slower                                                      |
| json                       | 5.02 ms                                                | 5.48 ms: 1.09x slower                                                     |
| logging_format             | 7.35 us                                                | 8.03 us: 1.09x slower                                                     |
| nqueens                    | 80.1 ms                                                | 88.0 ms: 1.10x slower                                                     |
| pprint_pformat             | 1.52 sec                                               | 1.67 sec: 1.10x slower                                                    |
| deltablue                  | 3.45 ms                                                | 3.80 ms: 1.10x slower                                                     |
| 2to3                       | 264 ms                                                 | 291 ms: 1.10x slower                                                      |
| sympy_str                  | 292 ms                                                 | 325 ms: 1.12x slower                                                      |
| sympy_sum                  | 166 ms                                                 | 186 ms: 1.12x slower                                                      |
| scimark_monte_carlo        | 68.4 ms                                                | 77.1 ms: 1.13x slower                                                     |
| scimark_lu                 | 114 ms                                                 | 129 ms: 1.13x slower                                                      |
| pickle_pure_python         | 308 us                                                 | 352 us: 1.15x slower                                                      |
| richards                   | 45.9 ms                                                | 52.9 ms: 1.15x slower                                                     |
| crypto_pyaes               | 76.6 ms                                                | 88.5 ms: 1.15x slower                                                     |
| sympy_expand               | 468 ms                                                 | 541 ms: 1.16x slower                                                      |
| json_loads                 | 26.5 us                                                | 30.7 us: 1.16x slower                                                     |
| richards_super             | 51.9 ms                                                | 60.7 ms: 1.17x slower                                                     |
| thrift                     | 791 us                                                 | 927 us: 1.17x slower                                                      |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.16 ms: 1.17x slower                                                     |
| xml_etree_generate         | 85.2 ms                                                | 101 ms: 1.19x slower                                                      |
| django_template            | 34.7 ms                                                | 41.1 ms: 1.19x slower                                                     |
| regex_compile              | 142 ms                                                 | 171 ms: 1.20x slower                                                      |
| meteor_contest             | 104 ms                                                 | 126 ms: 1.22x slower                                                      |
| create_gc_cycles           | 1.09 ms                                                | 1.35 ms: 1.24x slower                                                     |
| python_startup_no_site     | 7.16 ms                                                | 8.93 ms: 1.25x slower                                                     |
| fannkuch                   | 372 ms                                                 | 468 ms: 1.26x slower                                                      |
| xml_etree_process          | 59.0 ms                                                | 75.7 ms: 1.28x slower                                                     |
| nbody                      | 89.3 ms                                                | 117 ms: 1.31x slower                                                      |
| python_startup             | 9.93 ms                                                | 13.4 ms: 1.35x slower                                                     |
| mako                       | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                     |
| bench_thread_pool          | 941 us                                                 | 1.40 ms: 1.49x slower                                                     |
| coverage                   | 71.4 ms                                                | 119 ms: 1.67x slower                                                      |
| telco                      | 6.53 ms                                                | 176 ms: 26.92x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.03x slower                                                              |

Benchmark hidden because not significant (2): logging_silent, pycparser
Ignored benchmarks (23) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20261103-3.16.0a1+dev-3945eaf-NOGIL/bm-20261103-vultr-x86_64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.035x slower

# HPT report

- Reliability score: 77.92% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.31x