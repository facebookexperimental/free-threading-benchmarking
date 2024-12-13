# Results vs. 3.13.0rc2

- fork: python
- ref: ba2d2fda93a03a91ac6c
- machine: linux-x86_64
- commit hash: ba2d2fd
- commit date: 2024-12-13
- overall geometric mean: 1.252x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.20x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 369 ms: 1.42x slower                                                   |
| docutils       | 2.62 sec                                                     | 3.11 sec: 1.19x slower                                                 |
| html5lib       | 67.0 ms                                                      | 99.2 ms: 1.48x slower                                                  |
| Geometric mean | (ref)                                                        | 1.36x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 822 ms: 1.11x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 636 ms: 1.05x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 614 ms: 1.04x faster                                                   |
| async_tree_io              | 876 ms                                                       | 850 ms: 1.03x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 357 ms: 1.06x slower                                                   |
| coroutines                 | 23.6 ms                                                      | 25.2 ms: 1.07x slower                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 447 ms: 1.08x slower                                                   |
| async_tree_none            | 354 ms                                                       | 387 ms: 1.09x slower                                                   |
| async_generators           | 377 ms                                                       | 466 ms: 1.23x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.03x slower                                                           |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 181 ms: 1.19x faster                                                   |
| nbody          | 85.1 ms                                                      | 131 ms: 1.54x slower                                                   |
| float          | 77.5 ms                                                      | 140 ms: 1.81x slower                                                   |
| Geometric mean | (ref)                                                        | 1.33x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.83 ms: 1.09x faster                                                  |
| regex_dna      | 180 ms                                                       | 188 ms: 1.04x slower                                                   |
| regex_v8       | 22.7 ms                                                      | 25.3 ms: 1.11x slower                                                  |
| regex_compile  | 132 ms                                                       | 181 ms: 1.37x slower                                                   |
| Geometric mean | (ref)                                                        | 1.10x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 89.5 ms: 1.06x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| json_loads           | 27.0 us                                                      | 28.5 us: 1.05x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 98.3 ms: 1.15x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 78.6 ms: 1.32x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.69 sec: 1.34x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 14.4 ms: 1.37x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 339 us: 1.61x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 509 us: 1.73x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.25x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                  |
| python_startup         | 11.0 ms                                                      | 17.4 ms: 1.59x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.48x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 63.6 ms: 1.30x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 31.4 ms: 1.46x slower                                                  |
| django_template | 34.1 ms                                                      | 51.0 ms: 1.49x slower                                                  |
| mako            | 11.3 ms                                                      | 17.8 ms: 1.57x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.45x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits                   | 217 ms                                                       | 181 ms: 1.19x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 822 ms: 1.11x faster                                                   |
| deepcopy                   | 355 us                                                       | 325 us: 1.09x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.83 ms: 1.09x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 89.5 ms: 1.06x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 636 ms: 1.05x faster                                                   |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 614 ms: 1.04x faster                                                   |
| async_tree_io              | 876 ms                                                       | 850 ms: 1.03x faster                                                   |
| gc_traversal               | 3.14 ms                                                      | 3.17 ms: 1.01x slower                                                  |
| deepcopy_memo              | 39.1 us                                                      | 39.9 us: 1.02x slower                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.27 us: 1.03x slower                                                  |
| json                       | 4.93 ms                                                      | 5.08 ms: 1.03x slower                                                  |
| regex_dna                  | 180 ms                                                       | 188 ms: 1.04x slower                                                   |
| pathlib                    | 19.2 ms                                                      | 20.1 ms: 1.05x slower                                                  |
| json_loads                 | 27.0 us                                                      | 28.5 us: 1.05x slower                                                  |
| async_tree_none_tg         | 336 ms                                                       | 357 ms: 1.06x slower                                                   |
| coroutines                 | 23.6 ms                                                      | 25.2 ms: 1.07x slower                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 447 ms: 1.08x slower                                                   |
| async_tree_none            | 354 ms                                                       | 387 ms: 1.09x slower                                                   |
| telco                      | 7.82 ms                                                      | 8.62 ms: 1.10x slower                                                  |
| regex_v8                   | 22.7 ms                                                      | 25.3 ms: 1.11x slower                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.98 sec: 1.12x slower                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 3.49 us: 1.12x slower                                                  |
| spectral_norm              | 111 ms                                                       | 126 ms: 1.13x slower                                                   |
| xml_etree_generate         | 85.4 ms                                                      | 98.3 ms: 1.15x slower                                                  |
| scimark_fft                | 349 ms                                                       | 403 ms: 1.15x slower                                                   |
| docutils                   | 2.62 sec                                                     | 3.11 sec: 1.19x slower                                                 |
| coverage                   | 83.0 ms                                                      | 99.7 ms: 1.20x slower                                                  |
| pylint                     | 317 ms                                                       | 383 ms: 1.21x slower                                                   |
| async_generators           | 377 ms                                                       | 466 ms: 1.23x slower                                                   |
| nqueens                    | 78.6 ms                                                      | 98.4 ms: 1.25x slower                                                  |
| mdp                        | 2.36 sec                                                     | 2.97 sec: 1.26x slower                                                 |
| sqlglot_normalize          | 106 ms                                                       | 134 ms: 1.26x slower                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.95 ms: 1.26x slower                                                  |
| dulwich_log                | 74.8 ms                                                      | 96.0 ms: 1.28x slower                                                  |
| meteor_contest             | 102 ms                                                       | 131 ms: 1.29x slower                                                   |
| sqlglot_optimize           | 52.7 ms                                                      | 68.1 ms: 1.29x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 63.6 ms: 1.30x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 204 us: 1.32x slower                                                   |
| xml_etree_process          | 59.3 ms                                                      | 78.6 ms: 1.32x slower                                                  |
| generators                 | 28.8 ms                                                      | 38.4 ms: 1.33x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.79 ms: 1.34x slower                                                  |
| tomli_loads                | 2.01 sec                                                     | 2.69 sec: 1.34x slower                                                 |
| pprint_safe_repr           | 738 ms                                                       | 991 ms: 1.34x slower                                                   |
| fannkuch                   | 370 ms                                                       | 499 ms: 1.35x slower                                                   |
| regex_compile              | 132 ms                                                       | 181 ms: 1.37x slower                                                   |
| json_dumps                 | 10.5 ms                                                      | 14.4 ms: 1.37x slower                                                  |
| pprint_pformat             | 1.50 sec                                                     | 2.05 sec: 1.37x slower                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 93.5 ms: 1.38x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.56 sec: 1.40x slower                                                 |
| 2to3                       | 260 ms                                                       | 369 ms: 1.42x slower                                                   |
| genshi_text                | 21.5 ms                                                      | 31.4 ms: 1.46x slower                                                  |
| html5lib                   | 67.0 ms                                                      | 99.2 ms: 1.48x slower                                                  |
| django_template            | 34.1 ms                                                      | 51.0 ms: 1.49x slower                                                  |
| thrift                     | 778 us                                                       | 1.17 ms: 1.50x slower                                                  |
| sympy_integrate            | 19.8 ms                                                      | 29.7 ms: 1.50x slower                                                  |
| nbody                      | 85.1 ms                                                      | 131 ms: 1.54x slower                                                   |
| pyflate                    | 449 ms                                                       | 692 ms: 1.54x slower                                                   |
| mako                       | 11.3 ms                                                      | 17.8 ms: 1.57x slower                                                  |
| python_startup             | 11.0 ms                                                      | 17.4 ms: 1.59x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 339 us: 1.61x slower                                                   |
| scimark_lu                 | 113 ms                                                       | 185 ms: 1.64x slower                                                   |
| hexiom                     | 5.99 ms                                                      | 10.0 ms: 1.67x slower                                                  |
| comprehensions             | 16.5 us                                                      | 27.6 us: 1.67x slower                                                  |
| richards_super             | 51.6 ms                                                      | 87.4 ms: 1.69x slower                                                  |
| richards                   | 45.2 ms                                                      | 78.2 ms: 1.73x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 509 us: 1.73x slower                                                   |
| sympy_str                  | 275 ms                                                       | 479 ms: 1.74x slower                                                   |
| logging_simple             | 6.16 us                                                      | 10.9 us: 1.77x slower                                                  |
| logging_format             | 6.84 us                                                      | 12.1 us: 1.77x slower                                                  |
| scimark_sor                | 134 ms                                                       | 239 ms: 1.78x slower                                                   |
| float                      | 77.5 ms                                                      | 140 ms: 1.81x slower                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 120 ms: 1.83x slower                                                   |
| logging_silent             | 103 ns                                                       | 188 ns: 1.84x slower                                                   |
| chaos                      | 57.3 ms                                                      | 106 ms: 1.85x slower                                                   |
| sqlglot_transpile          | 1.56 ms                                                      | 2.98 ms: 1.91x slower                                                  |
| go                         | 141 ms                                                       | 276 ms: 1.96x slower                                                   |
| sqlglot_parse              | 1.25 ms                                                      | 2.61 ms: 2.09x slower                                                  |
| sympy_expand               | 457 ms                                                       | 959 ms: 2.10x slower                                                   |
| raytrace                   | 253 ms                                                       | 566 ms: 2.24x slower                                                   |
| sympy_sum                  | 156 ms                                                       | 352 ms: 2.26x slower                                                   |
| deltablue                  | 3.12 ms                                                      | 8.33 ms: 2.67x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 3.43 ms: 3.74x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 109 ms: 9.90x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.39x slower                                                           |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_memoization
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241213-3.14.0a2+-ba2d2fd-NOGIL/bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.252x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.25x
- 95% likely to have a slowdown of 1.24x
- 99% likely to have a slowdown of 1.20x

# Memory
- memory change: 1.31x