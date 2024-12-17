# Results vs. 3.12.6

- fork: python
- ref: cfeaa992ba9bad9be268
- machine: linux-x86_64
- commit hash: cfeaa99
- commit date: 2024-12-16
- overall geometric mean: 1.212x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241216-vultr-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 364 ms: 1.38x slower                                                   |
| docutils       | 2.64 sec                                               | 3.09 sec: 1.17x slower                                                 |
| html5lib       | 63.6 ms                                                | 98.6 ms: 1.55x slower                                                  |
| Geometric mean | (ref)                                                  | 1.36x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241216-vultr-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 790 ms: 1.41x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 807 ms: 1.34x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 431 ms: 1.30x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 345 ms: 1.29x faster                                                   |
| async_tree_none            | 464 ms                                                 | 375 ms: 1.24x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 459 ms: 1.21x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 604 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 628 ms: 1.14x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 521 ms: 1.01x slower                                                   |
| coroutines                 | 23.9 ms                                                | 24.7 ms: 1.03x slower                                                  |
| async_generators           | 384 ms                                                 | 456 ms: 1.19x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.16x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241216-vultr-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 184 ms: 1.00x faster                                                   |
| nbody          | 89.3 ms                                                | 133 ms: 1.49x slower                                                   |
| float          | 80.8 ms                                                | 134 ms: 1.66x slower                                                   |
| Geometric mean | (ref)                                                  | 1.35x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241216-vultr-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                  |
| regex_dna      | 168 ms                                                 | 179 ms: 1.06x slower                                                   |
| regex_v8       | 20.6 ms                                                | 23.8 ms: 1.16x slower                                                  |
| regex_compile  | 142 ms                                                 | 177 ms: 1.24x slower                                                   |
| Geometric mean | (ref)                                                  | 1.07x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241216-vultr-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 89.7 ms: 1.08x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| json_loads           | 26.5 us                                                | 28.6 us: 1.08x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 97.6 ms: 1.15x slower                                                  |
| tomli_loads          | 2.11 sec                                               | 2.58 sec: 1.23x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 78.4 ms: 1.33x slower                                                  |
| json_dumps           | 10.4 ms                                                | 14.1 ms: 1.36x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 333 us: 1.51x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 510 us: 1.66x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.22x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241216-vultr-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                  |
| python_startup         | 9.93 ms                                                | 17.2 ms: 1.73x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.57x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241216-vultr-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 63.5 ms: 1.26x slower                                                  |
| genshi_text     | 22.8 ms                                                | 30.3 ms: 1.33x slower                                                  |
| django_template | 34.7 ms                                                | 50.0 ms: 1.44x slower                                                  |
| mako            | 11.0 ms                                                | 17.3 ms: 1.57x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.40x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241216-vultr-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 790 ms: 1.41x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 807 ms: 1.34x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 431 ms: 1.30x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 345 ms: 1.29x faster                                                   |
| async_tree_none            | 464 ms                                                 | 375 ms: 1.24x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 459 ms: 1.21x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 604 ms: 1.20x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 628 ms: 1.14x faster                                                   |
| pathlib                    | 21.5 ms                                                | 19.7 ms: 1.09x faster                                                  |
| deepcopy                   | 352 us                                                 | 322 us: 1.09x faster                                                   |
| gc_traversal               | 3.46 ms                                                | 3.17 ms: 1.09x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 89.7 ms: 1.08x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 40.0 us: 1.01x faster                                                  |
| pidigits                   | 184 ms                                                 | 184 ms: 1.00x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 521 ms: 1.01x slower                                                   |
| spectral_norm              | 110 ms                                                 | 111 ms: 1.01x slower                                                   |
| json                       | 5.02 ms                                                | 5.09 ms: 1.01x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.7 ms: 1.03x slower                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 5.01 sec: 1.06x slower                                                 |
| regex_dna                  | 168 ms                                                 | 179 ms: 1.06x slower                                                   |
| json_loads                 | 26.5 us                                                | 28.6 us: 1.08x slower                                                  |
| scimark_fft                | 342 ms                                                 | 377 ms: 1.10x slower                                                   |
| mdp                        | 2.42 sec                                               | 2.72 sec: 1.12x slower                                                 |
| deepcopy_reduce            | 3.08 us                                                | 3.47 us: 1.13x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 97.6 ms: 1.15x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 23.8 ms: 1.16x slower                                                  |
| pylint                     | 319 ms                                                 | 371 ms: 1.16x slower                                                   |
| docutils                   | 2.64 sec                                               | 3.09 sec: 1.17x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 90.7 ms: 1.18x slower                                                  |
| async_generators           | 384 ms                                                 | 456 ms: 1.19x slower                                                   |
| generators                 | 32.2 ms                                                | 38.4 ms: 1.19x slower                                                  |
| dulwich_log                | 78.9 ms                                                | 94.3 ms: 1.20x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.35 ms: 1.22x slower                                                  |
| nqueens                    | 80.1 ms                                                | 98.1 ms: 1.23x slower                                                  |
| tomli_loads                | 2.11 sec                                               | 2.58 sec: 1.23x slower                                                 |
| regex_compile              | 142 ms                                                 | 177 ms: 1.24x slower                                                   |
| sqlglot_optimize           | 53.3 ms                                                | 66.1 ms: 1.24x slower                                                  |
| sqlglot_normalize          | 107 ms                                                 | 133 ms: 1.25x slower                                                   |
| typing_runtime_protocols   | 163 us                                                 | 206 us: 1.26x slower                                                   |
| meteor_contest             | 104 ms                                                 | 131 ms: 1.26x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 63.5 ms: 1.26x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.52 sec: 1.30x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 971 ms: 1.31x slower                                                   |
| telco                      | 6.53 ms                                                | 8.62 ms: 1.32x slower                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 28.8 ms: 1.32x slower                                                  |
| fannkuch                   | 372 ms                                                 | 493 ms: 1.32x slower                                                   |
| xml_etree_process          | 59.0 ms                                                | 78.4 ms: 1.33x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 2.02 sec: 1.33x slower                                                 |
| genshi_text                | 22.8 ms                                                | 30.3 ms: 1.33x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 14.1 ms: 1.36x slower                                                  |
| 2to3                       | 264 ms                                                 | 364 ms: 1.38x slower                                                   |
| comprehensions             | 19.8 us                                                | 27.6 us: 1.39x slower                                                  |
| thrift                     | 791 us                                                 | 1.10 ms: 1.39x slower                                                  |
| coverage                   | 71.4 ms                                                | 99.5 ms: 1.39x slower                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 201 ms: 1.41x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 29.6 ms: 1.44x slower                                                  |
| django_template            | 34.7 ms                                                | 50.0 ms: 1.44x slower                                                  |
| pyflate                    | 448 ms                                                 | 669 ms: 1.49x slower                                                   |
| nbody                      | 89.3 ms                                                | 133 ms: 1.49x slower                                                   |
| unpickle_pure_python       | 221 us                                                 | 333 us: 1.51x slower                                                   |
| logging_simple             | 6.63 us                                                | 10.0 us: 1.51x slower                                                  |
| logging_format             | 7.35 us                                                | 11.2 us: 1.52x slower                                                  |
| html5lib                   | 63.6 ms                                                | 98.6 ms: 1.55x slower                                                  |
| mako                       | 11.0 ms                                                | 17.3 ms: 1.57x slower                                                  |
| hexiom                     | 6.17 ms                                                | 9.82 ms: 1.59x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 183 ms: 1.60x slower                                                   |
| chaos                      | 62.8 ms                                                | 103 ms: 1.64x slower                                                   |
| sympy_str                  | 292 ms                                                 | 478 ms: 1.64x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.80 ms: 1.65x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 510 us: 1.66x slower                                                   |
| float                      | 80.8 ms                                                | 134 ms: 1.66x slower                                                   |
| richards_super             | 51.9 ms                                                | 86.5 ms: 1.67x slower                                                  |
| logging_silent             | 109 ns                                                 | 182 ns: 1.67x slower                                                   |
| richards                   | 45.9 ms                                                | 77.9 ms: 1.70x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 117 ms: 1.71x slower                                                   |
| python_startup             | 9.93 ms                                                | 17.2 ms: 1.73x slower                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 2.93 ms: 1.75x slower                                                  |
| scimark_sor                | 130 ms                                                 | 230 ms: 1.77x slower                                                   |
| raytrace                   | 299 ms                                                 | 551 ms: 1.84x slower                                                   |
| sqlglot_parse              | 1.36 ms                                                | 2.57 ms: 1.90x slower                                                  |
| go                         | 139 ms                                                 | 268 ms: 1.93x slower                                                   |
| sympy_expand               | 468 ms                                                 | 962 ms: 2.06x slower                                                   |
| sympy_sum                  | 166 ms                                                 | 351 ms: 2.11x slower                                                   |
| deltablue                  | 3.45 ms                                                | 8.10 ms: 2.35x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.39 ms: 3.60x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 108 ms: 9.99x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.32x slower                                                           |

Benchmark hidden because not significant (1): sqlite_synth
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241216-3.14.0a2+-cfeaa99-NOGIL/bm-20241216-vultr-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.212x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.19x
- 95% likely to have a slowdown of 1.18x
- 99% likely to have a slowdown of 1.16x

# Memory
- memory change: 1.33x