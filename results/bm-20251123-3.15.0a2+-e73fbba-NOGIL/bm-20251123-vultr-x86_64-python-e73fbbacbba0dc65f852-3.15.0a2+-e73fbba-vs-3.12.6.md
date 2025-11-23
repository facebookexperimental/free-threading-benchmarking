# Results vs. 3.12.6

- fork: python
- ref: e73fbbacbba0dc65f852
- machine: linux-x86_64
- commit hash: e73fbba
- commit date: 2025-11-23
- overall geometric mean: 1.015x slower
- HPT reliability: 80.73%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.41x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 281 ms: 1.07x slower                                                   |
| docutils       | 2.64 sec                                               | 2.69 sec: 1.02x slower                                                 |
| Geometric mean | (ref)                                                  | 1.03x slower                                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 519 ms: 2.14x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 544 ms: 1.99x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 228 ms: 1.95x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 286 ms: 1.95x faster                                                   |
| async_tree_none            | 464 ms                                                 | 258 ms: 1.80x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 311 ms: 1.78x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 488 ms: 1.48x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 512 ms: 1.40x faster                                                   |
| async_generators           | 384 ms                                                 | 376 ms: 1.02x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 509 ms: 1.01x faster                                                   |
| coroutines                 | 23.9 ms                                                | 25.1 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.53x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.1 ms: 1.15x faster                                                  |
| pidigits       | 184 ms                                                 | 192 ms: 1.04x slower                                                   |
| nbody          | 89.3 ms                                                | 124 ms: 1.39x slower                                                   |
| Geometric mean | (ref)                                                  | 1.08x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.66 ms: 1.19x faster                                                  |
| regex_dna      | 168 ms                                                 | 164 ms: 1.02x faster                                                   |
| regex_v8       | 20.6 ms                                                | 20.3 ms: 1.01x faster                                                  |
| regex_compile  | 142 ms                                                 | 143 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                  | 1.05x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.7 ms: 1.09x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 132 ms: 1.05x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 2.04 sec: 1.04x faster                                                 |
| json_dumps           | 10.4 ms                                                | 10.9 ms: 1.05x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 233 us: 1.06x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 337 us: 1.09x slower                                                   |
| xml_etree_generate   | 85.2 ms                                                | 95.7 ms: 1.12x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 69.0 ms: 1.17x slower                                                  |
| json_loads           | 26.5 us                                                | 31.8 us: 1.20x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.57 ms: 1.34x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.46x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 40.2 ms: 1.16x slower                                                  |
| genshi_xml      | 50.2 ms                                                | 58.1 ms: 1.16x slower                                                  |
| genshi_text     | 22.8 ms                                                | 26.7 ms: 1.17x slower                                                  |
| mako            | 11.0 ms                                                | 15.8 ms: 1.44x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.23x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 519 ms: 2.14x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 544 ms: 1.99x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 228 ms: 1.95x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 286 ms: 1.95x faster                                                   |
| mdp                        | 2.42 sec                                               | 1.31 sec: 1.84x faster                                                 |
| async_tree_none            | 464 ms                                                 | 258 ms: 1.80x faster                                                   |
| gc_traversal               | 3.46 ms                                                | 1.93 ms: 1.79x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 311 ms: 1.78x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 488 ms: 1.48x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 512 ms: 1.40x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 30.9 us: 1.30x faster                                                  |
| deepcopy                   | 352 us                                                 | 279 us: 1.26x faster                                                   |
| pathlib                    | 21.5 ms                                                | 17.7 ms: 1.22x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.66 ms: 1.19x faster                                                  |
| float                      | 80.8 ms                                                | 70.1 ms: 1.15x faster                                                  |
| go                         | 139 ms                                                 | 121 ms: 1.15x faster                                                   |
| comprehensions             | 19.8 us                                                | 17.9 us: 1.11x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 71.9 ms: 1.10x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 88.7 ms: 1.09x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.03 us: 1.08x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.41 sec: 1.07x faster                                                 |
| generators                 | 32.2 ms                                                | 30.4 ms: 1.06x faster                                                  |
| scimark_sor                | 130 ms                                                 | 123 ms: 1.06x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 132 ms: 1.05x faster                                                   |
| pylint                     | 319 ms                                                 | 305 ms: 1.04x faster                                                   |
| tomli_loads                | 2.11 sec                                               | 2.04 sec: 1.04x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 3.00 us: 1.03x faster                                                  |
| async_generators           | 384 ms                                                 | 376 ms: 1.02x faster                                                   |
| regex_dna                  | 168 ms                                                 | 164 ms: 1.02x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 509 ms: 1.01x faster                                                   |
| regex_v8                   | 20.6 ms                                                | 20.3 ms: 1.01x faster                                                  |
| logging_silent             | 109 ns                                                 | 108 ns: 1.01x faster                                                   |
| raytrace                   | 299 ms                                                 | 296 ms: 1.01x faster                                                   |
| regex_compile              | 142 ms                                                 | 143 ms: 1.01x slower                                                   |
| scimark_fft                | 342 ms                                                 | 345 ms: 1.01x slower                                                   |
| spectral_norm              | 110 ms                                                 | 112 ms: 1.02x slower                                                   |
| docutils                   | 2.64 sec                                               | 2.69 sec: 1.02x slower                                                 |
| logging_simple             | 6.63 us                                                | 6.83 us: 1.03x slower                                                  |
| pidigits                   | 184 ms                                                 | 192 ms: 1.04x slower                                                   |
| pyflate                    | 448 ms                                                 | 467 ms: 1.04x slower                                                   |
| hexiom                     | 6.17 ms                                                | 6.44 ms: 1.04x slower                                                  |
| coroutines                 | 23.9 ms                                                | 25.1 ms: 1.05x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 779 ms: 1.05x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 10.9 ms: 1.05x slower                                                  |
| deltablue                  | 3.45 ms                                                | 3.63 ms: 1.05x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 233 us: 1.06x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.61 sec: 1.06x slower                                                 |
| sympy_str                  | 292 ms                                                 | 309 ms: 1.06x slower                                                   |
| sympy_integrate            | 20.5 ms                                                | 21.8 ms: 1.06x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 176 ms: 1.06x slower                                                   |
| logging_format             | 7.35 us                                                | 7.83 us: 1.07x slower                                                  |
| 2to3                       | 264 ms                                                 | 281 ms: 1.07x slower                                                   |
| json                       | 5.02 ms                                                | 5.39 ms: 1.07x slower                                                  |
| thrift                     | 791 us                                                 | 852 us: 1.08x slower                                                   |
| pickle_pure_python         | 308 us                                                 | 337 us: 1.09x slower                                                   |
| sympy_expand               | 468 ms                                                 | 518 ms: 1.11x slower                                                   |
| nqueens                    | 80.1 ms                                                | 88.8 ms: 1.11x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 95.7 ms: 1.12x slower                                                  |
| richards                   | 45.9 ms                                                | 51.7 ms: 1.12x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 86.3 ms: 1.13x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 186 us: 1.14x slower                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 78.6 ms: 1.15x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 131 ms: 1.15x slower                                                   |
| richards_super             | 51.9 ms                                                | 59.8 ms: 1.15x slower                                                  |
| django_template            | 34.7 ms                                                | 40.2 ms: 1.16x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 58.1 ms: 1.16x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 69.0 ms: 1.17x slower                                                  |
| genshi_text                | 22.8 ms                                                | 26.7 ms: 1.17x slower                                                  |
| meteor_contest             | 104 ms                                                 | 121 ms: 1.17x slower                                                   |
| json_loads                 | 26.5 us                                                | 31.8 us: 1.20x slower                                                  |
| fannkuch                   | 372 ms                                                 | 458 ms: 1.23x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.50 ms: 1.25x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 9.57 ms: 1.34x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.50 ms: 1.37x slower                                                  |
| nbody                      | 89.3 ms                                                | 124 ms: 1.39x slower                                                   |
| mako                       | 11.0 ms                                                | 15.8 ms: 1.44x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 15.6 ms: 1.44x slower                                                  |
| coverage                   | 71.4 ms                                                | 110 ms: 1.54x slower                                                   |
| python_startup             | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.17 ms: 3.37x slower                                                  |
| telco                      | 6.53 ms                                                | 173 ms: 26.54x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.03x slower                                                           |

Benchmark hidden because not significant (3): pycparser, chaos, html5lib
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (7) of results/bm-20251123-3.15.0a2+-e73fbba-NOGIL/bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba.json: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.015x slower

# HPT report

- Reliability score: 80.73% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.41x