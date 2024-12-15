# Results vs. 3.12.6

- fork: python
- ref: 0ac40acec045c4ce780c
- machine: linux-x86_64
- commit hash: 0ac40ac
- commit date: 2024-12-14
- overall geometric mean: 1.211x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 363 ms: 1.38x slower                                                   |
| docutils       | 2.64 sec                                               | 3.06 sec: 1.16x slower                                                 |
| html5lib       | 63.6 ms                                                | 96.7 ms: 1.52x slower                                                  |
| Geometric mean | (ref)                                                  | 1.34x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 791 ms: 1.40x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 807 ms: 1.34x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 431 ms: 1.30x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 345 ms: 1.29x faster                                                   |
| async_tree_none            | 464 ms                                                 | 374 ms: 1.24x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 457 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 604 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 625 ms: 1.14x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 521 ms: 1.01x slower                                                   |
| coroutines                 | 23.9 ms                                                | 24.4 ms: 1.02x slower                                                  |
| async_generators           | 384 ms                                                 | 455 ms: 1.18x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.16x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 181 ms: 1.02x faster                                                   |
| nbody          | 89.3 ms                                                | 131 ms: 1.47x slower                                                   |
| float          | 80.8 ms                                                | 134 ms: 1.66x slower                                                   |
| Geometric mean | (ref)                                                  | 1.34x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.86 ms: 1.11x faster                                                  |
| regex_dna      | 168 ms                                                 | 187 ms: 1.12x slower                                                   |
| regex_v8       | 20.6 ms                                                | 25.2 ms: 1.22x slower                                                  |
| regex_compile  | 142 ms                                                 | 175 ms: 1.23x slower                                                   |
| Geometric mean | (ref)                                                  | 1.11x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 89.6 ms: 1.08x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| json_loads           | 26.5 us                                                | 28.5 us: 1.07x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 97.0 ms: 1.14x slower                                                  |
| tomli_loads          | 2.11 sec                                               | 2.60 sec: 1.23x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 78.8 ms: 1.34x slower                                                  |
| json_dumps           | 10.4 ms                                                | 14.0 ms: 1.35x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 335 us: 1.52x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 501 us: 1.63x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.22x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                  |
| python_startup         | 9.93 ms                                                | 17.1 ms: 1.73x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.57x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 63.1 ms: 1.26x slower                                                  |
| genshi_text     | 22.8 ms                                                | 31.0 ms: 1.36x slower                                                  |
| django_template | 34.7 ms                                                | 49.3 ms: 1.42x slower                                                  |
| mako            | 11.0 ms                                                | 16.9 ms: 1.54x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.39x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 791 ms: 1.40x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 807 ms: 1.34x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 431 ms: 1.30x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 345 ms: 1.29x faster                                                   |
| async_tree_none            | 464 ms                                                 | 374 ms: 1.24x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 457 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 604 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 625 ms: 1.14x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.86 ms: 1.11x faster                                                  |
| deepcopy                   | 352 us                                                 | 318 us: 1.11x faster                                                   |
| gc_traversal               | 3.46 ms                                                | 3.15 ms: 1.10x faster                                                  |
| pathlib                    | 21.5 ms                                                | 19.8 ms: 1.09x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 89.6 ms: 1.08x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 39.4 us: 1.02x faster                                                  |
| pidigits                   | 184 ms                                                 | 181 ms: 1.02x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 521 ms: 1.01x slower                                                   |
| coroutines                 | 23.9 ms                                                | 24.4 ms: 1.02x slower                                                  |
| spectral_norm              | 110 ms                                                 | 114 ms: 1.03x slower                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 5.00 sec: 1.06x slower                                                 |
| json_loads                 | 26.5 us                                                | 28.5 us: 1.07x slower                                                  |
| scimark_fft                | 342 ms                                                 | 378 ms: 1.11x slower                                                   |
| regex_dna                  | 168 ms                                                 | 187 ms: 1.12x slower                                                   |
| deepcopy_reduce            | 3.08 us                                                | 3.46 us: 1.12x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 97.0 ms: 1.14x slower                                                  |
| pylint                     | 319 ms                                                 | 369 ms: 1.16x slower                                                   |
| docutils                   | 2.64 sec                                               | 3.06 sec: 1.16x slower                                                 |
| mdp                        | 2.42 sec                                               | 2.83 sec: 1.17x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 89.8 ms: 1.17x slower                                                  |
| async_generators           | 384 ms                                                 | 455 ms: 1.18x slower                                                   |
| generators                 | 32.2 ms                                                | 38.2 ms: 1.19x slower                                                  |
| dulwich_log                | 78.9 ms                                                | 94.0 ms: 1.19x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 25.2 ms: 1.22x slower                                                  |
| regex_compile              | 142 ms                                                 | 175 ms: 1.23x slower                                                   |
| tomli_loads                | 2.11 sec                                               | 2.60 sec: 1.23x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 202 us: 1.24x slower                                                   |
| sqlglot_optimize           | 53.3 ms                                                | 65.9 ms: 1.24x slower                                                  |
| sqlglot_normalize          | 107 ms                                                 | 132 ms: 1.24x slower                                                   |
| meteor_contest             | 104 ms                                                 | 129 ms: 1.25x slower                                                   |
| nqueens                    | 80.1 ms                                                | 99.9 ms: 1.25x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.51 ms: 1.25x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 63.1 ms: 1.26x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.52 sec: 1.30x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 973 ms: 1.31x slower                                                   |
| telco                      | 6.53 ms                                                | 8.58 ms: 1.31x slower                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 28.9 ms: 1.32x slower                                                  |
| fannkuch                   | 372 ms                                                 | 493 ms: 1.32x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 2.02 sec: 1.33x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 78.8 ms: 1.34x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 14.0 ms: 1.35x slower                                                  |
| genshi_text                | 22.8 ms                                                | 31.0 ms: 1.36x slower                                                  |
| 2to3                       | 264 ms                                                 | 363 ms: 1.38x slower                                                   |
| comprehensions             | 19.8 us                                                | 27.6 us: 1.39x slower                                                  |
| thrift                     | 791 us                                                 | 1.11 ms: 1.40x slower                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 200 ms: 1.40x slower                                                   |
| coverage                   | 71.4 ms                                                | 101 ms: 1.41x slower                                                   |
| django_template            | 34.7 ms                                                | 49.3 ms: 1.42x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 29.4 ms: 1.43x slower                                                  |
| nbody                      | 89.3 ms                                                | 131 ms: 1.47x slower                                                   |
| pyflate                    | 448 ms                                                 | 668 ms: 1.49x slower                                                   |
| logging_simple             | 6.63 us                                                | 9.93 us: 1.50x slower                                                  |
| logging_format             | 7.35 us                                                | 11.1 us: 1.50x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 335 us: 1.52x slower                                                   |
| html5lib                   | 63.6 ms                                                | 96.7 ms: 1.52x slower                                                  |
| mako                       | 11.0 ms                                                | 16.9 ms: 1.54x slower                                                  |
| hexiom                     | 6.17 ms                                                | 9.82 ms: 1.59x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 183 ms: 1.60x slower                                                   |
| pickle_pure_python         | 308 us                                                 | 501 us: 1.63x slower                                                   |
| sympy_str                  | 292 ms                                                 | 475 ms: 1.63x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.80 ms: 1.64x slower                                                  |
| richards_super             | 51.9 ms                                                | 85.4 ms: 1.65x slower                                                  |
| chaos                      | 62.8 ms                                                | 104 ms: 1.65x slower                                                   |
| float                      | 80.8 ms                                                | 134 ms: 1.66x slower                                                   |
| richards                   | 45.9 ms                                                | 77.3 ms: 1.68x slower                                                  |
| logging_silent             | 109 ns                                                 | 183 ns: 1.68x slower                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 118 ms: 1.73x slower                                                   |
| python_startup             | 9.93 ms                                                | 17.1 ms: 1.73x slower                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 2.91 ms: 1.74x slower                                                  |
| scimark_sor                | 130 ms                                                 | 234 ms: 1.80x slower                                                   |
| raytrace                   | 299 ms                                                 | 552 ms: 1.85x slower                                                   |
| sqlglot_parse              | 1.36 ms                                                | 2.56 ms: 1.89x slower                                                  |
| go                         | 139 ms                                                 | 268 ms: 1.93x slower                                                   |
| sympy_expand               | 468 ms                                                 | 951 ms: 2.03x slower                                                   |
| sympy_sum                  | 166 ms                                                 | 348 ms: 2.10x slower                                                   |
| deltablue                  | 3.45 ms                                                | 8.25 ms: 2.39x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.40 ms: 3.61x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 108 ms: 9.99x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.32x slower                                                           |

Benchmark hidden because not significant (2): sqlite_synth, json
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241214-3.14.0a2+-0ac40ac-NOGIL/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.211x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.19x
- 95% likely to have a slowdown of 1.18x
- 99% likely to have a slowdown of 1.17x

# Memory
- memory change: 1.33x