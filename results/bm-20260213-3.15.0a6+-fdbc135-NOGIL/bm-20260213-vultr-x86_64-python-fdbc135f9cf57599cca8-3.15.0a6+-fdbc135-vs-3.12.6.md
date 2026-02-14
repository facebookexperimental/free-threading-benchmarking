# Results vs. 3.12.6

- fork: python
- ref: fdbc135f9cf57599cca8
- machine: linux-x86_64
- commit hash: fdbc135
- commit date: 2026-02-13
- overall geometric mean: 1.025x slower
- HPT reliability: 68.43%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.42x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260213-vultr-x86_64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 277 ms: 1.05x slower                                                   |
| docutils       | 2.64 sec                                               | 2.74 sec: 1.04x slower                                                 |
| html5lib       | 63.6 ms                                                | 65.6 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260213-vultr-x86_64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 596 ms: 1.86x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 324 ms: 1.73x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 626 ms: 1.73x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 262 ms: 1.71x faster                                                   |
| async_tree_none            | 464 ms                                                 | 286 ms: 1.62x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 353 ms: 1.57x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 516 ms: 1.40x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 543 ms: 1.32x faster                                                   |
| async_generators           | 384 ms                                                 | 371 ms: 1.03x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 509 ms: 1.01x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.42x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260213-vultr-x86_64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 73.8 ms: 1.09x faster                                                  |
| pidigits       | 184 ms                                                 | 191 ms: 1.04x slower                                                   |
| nbody          | 89.3 ms                                                | 121 ms: 1.36x slower                                                   |
| Geometric mean | (ref)                                                  | 1.09x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260213-vultr-x86_64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.80 ms: 1.13x faster                                                  |
| regex_compile  | 142 ms                                                 | 141 ms: 1.01x faster                                                   |
| regex_v8       | 20.6 ms                                                | 20.5 ms: 1.00x faster                                                  |
| regex_dna      | 168 ms                                                 | 171 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260213-vultr-x86_64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.92 sec: 1.10x faster                                                 |
| xml_etree_iterparse  | 96.7 ms                                                | 89.2 ms: 1.08x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 133 ms: 1.04x faster                                                   |
| json_dumps           | 10.4 ms                                                | 11.1 ms: 1.07x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 330 us: 1.07x slower                                                   |
| unpickle_pure_python | 221 us                                                 | 237 us: 1.08x slower                                                   |
| xml_etree_generate   | 85.2 ms                                                | 96.2 ms: 1.13x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 69.1 ms: 1.17x slower                                                  |
| json_loads           | 26.5 us                                                | 32.2 us: 1.21x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260213-vultr-x86_64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.79 ms: 1.37x slower                                                  |
| python_startup         | 9.93 ms                                                | 16.0 ms: 1.61x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.49x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260213-vultr-x86_64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 53.6 ms: 1.07x slower                                                  |
| genshi_text     | 22.8 ms                                                | 25.6 ms: 1.12x slower                                                  |
| django_template | 34.7 ms                                                | 39.6 ms: 1.14x slower                                                  |
| mako            | 11.0 ms                                                | 16.0 ms: 1.46x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.19x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260213-vultr-x86_64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 596 ms: 1.86x faster                                                   |
| mdp                        | 2.42 sec                                               | 1.31 sec: 1.84x faster                                                 |
| gc_traversal               | 3.46 ms                                                | 1.97 ms: 1.76x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 324 ms: 1.73x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 626 ms: 1.73x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 262 ms: 1.71x faster                                                   |
| async_tree_none            | 464 ms                                                 | 286 ms: 1.62x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 353 ms: 1.57x faster                                                   |
| bench_mp_pool              | 10.8 ms                                                | 7.08 ms: 1.53x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 516 ms: 1.40x faster                                                   |
| deepcopy                   | 352 us                                                 | 263 us: 1.34x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 543 ms: 1.32x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 31.0 us: 1.30x faster                                                  |
| pathlib                    | 21.5 ms                                                | 17.5 ms: 1.23x faster                                                  |
| go                         | 139 ms                                                 | 119 ms: 1.17x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 1.93 us: 1.14x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.80 ms: 1.13x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 69.9 ms: 1.13x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.92 sec: 1.10x faster                                                 |
| float                      | 80.8 ms                                                | 73.8 ms: 1.09x faster                                                  |
| logging_silent             | 109 ns                                                 | 100 ns: 1.09x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 89.2 ms: 1.08x faster                                                  |
| comprehensions             | 19.8 us                                                | 18.3 us: 1.08x faster                                                  |
| scimark_sor                | 130 ms                                                 | 121 ms: 1.07x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.42 sec: 1.07x faster                                                 |
| pylint                     | 319 ms                                                 | 298 ms: 1.07x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.90 us: 1.06x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 133 ms: 1.04x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.12 sec: 1.04x faster                                                 |
| async_generators           | 384 ms                                                 | 371 ms: 1.03x faster                                                   |
| spectral_norm              | 110 ms                                                 | 107 ms: 1.03x faster                                                   |
| scimark_fft                | 342 ms                                                 | 336 ms: 1.02x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 509 ms: 1.01x faster                                                   |
| raytrace                   | 299 ms                                                 | 295 ms: 1.01x faster                                                   |
| regex_compile              | 142 ms                                                 | 141 ms: 1.01x faster                                                   |
| regex_v8                   | 20.6 ms                                                | 20.5 ms: 1.00x faster                                                  |
| logging_simple             | 6.63 us                                                | 6.67 us: 1.01x slower                                                  |
| generators                 | 32.2 ms                                                | 32.5 ms: 1.01x slower                                                  |
| regex_dna                  | 168 ms                                                 | 171 ms: 1.02x slower                                                   |
| pyflate                    | 448 ms                                                 | 458 ms: 1.02x slower                                                   |
| chaos                      | 62.8 ms                                                | 64.7 ms: 1.03x slower                                                  |
| html5lib                   | 63.6 ms                                                | 65.6 ms: 1.03x slower                                                  |
| logging_format             | 7.35 us                                                | 7.58 us: 1.03x slower                                                  |
| pidigits                   | 184 ms                                                 | 191 ms: 1.04x slower                                                   |
| docutils                   | 2.64 sec                                               | 2.74 sec: 1.04x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 772 ms: 1.04x slower                                                   |
| deltablue                  | 3.45 ms                                                | 3.61 ms: 1.05x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.60 sec: 1.05x slower                                                 |
| 2to3                       | 264 ms                                                 | 277 ms: 1.05x slower                                                   |
| hexiom                     | 6.17 ms                                                | 6.51 ms: 1.06x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 21.7 ms: 1.06x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 176 ms: 1.06x slower                                                   |
| sympy_str                  | 292 ms                                                 | 309 ms: 1.06x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 53.6 ms: 1.07x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 11.1 ms: 1.07x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 330 us: 1.07x slower                                                   |
| unpickle_pure_python       | 221 us                                                 | 237 us: 1.08x slower                                                   |
| json                       | 5.02 ms                                                | 5.43 ms: 1.08x slower                                                  |
| sympy_expand               | 468 ms                                                 | 515 ms: 1.10x slower                                                   |
| scimark_lu                 | 114 ms                                                 | 126 ms: 1.10x slower                                                   |
| genshi_text                | 22.8 ms                                                | 25.6 ms: 1.12x slower                                                  |
| nqueens                    | 80.1 ms                                                | 90.3 ms: 1.13x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 96.2 ms: 1.13x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 86.6 ms: 1.13x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 77.6 ms: 1.13x slower                                                  |
| thrift                     | 791 us                                                 | 901 us: 1.14x slower                                                   |
| django_template            | 34.7 ms                                                | 39.6 ms: 1.14x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 69.1 ms: 1.17x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.18 ms: 1.18x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 195 us: 1.19x slower                                                   |
| richards                   | 45.9 ms                                                | 55.1 ms: 1.20x slower                                                  |
| richards_super             | 51.9 ms                                                | 62.4 ms: 1.20x slower                                                  |
| meteor_contest             | 104 ms                                                 | 125 ms: 1.21x slower                                                   |
| json_loads                 | 26.5 us                                                | 32.2 us: 1.21x slower                                                  |
| fannkuch                   | 372 ms                                                 | 459 ms: 1.23x slower                                                   |
| nbody                      | 89.3 ms                                                | 121 ms: 1.36x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 9.79 ms: 1.37x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.51 ms: 1.39x slower                                                  |
| mako                       | 11.0 ms                                                | 16.0 ms: 1.46x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.48 ms: 1.57x slower                                                  |
| coverage                   | 71.4 ms                                                | 113 ms: 1.59x slower                                                   |
| python_startup             | 9.93 ms                                                | 16.0 ms: 1.61x slower                                                  |
| telco                      | 6.53 ms                                                | 174 ms: 26.67x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.02x slower                                                           |

Benchmark hidden because not significant (1): coroutines
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260213-3.15.0a6+-fdbc135-NOGIL/bm-20260213-vultr-x86_64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.025x slower

# HPT report

- Reliability score: 68.43% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.42x