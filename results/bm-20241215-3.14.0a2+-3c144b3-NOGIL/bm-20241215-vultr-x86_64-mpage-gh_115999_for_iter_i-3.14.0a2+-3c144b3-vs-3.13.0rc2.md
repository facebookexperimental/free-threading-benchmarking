# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_for_iter_i
- machine: linux-x86_64
- commit hash: 3c144b3
- commit date: 2024-12-15
- overall geometric mean: 1.109x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 316 ms: 1.22x slower                                                  |
| docutils       | 2.62 sec                                                     | 2.85 sec: 1.09x slower                                                |
| html5lib       | 67.0 ms                                                      | 75.2 ms: 1.12x slower                                                 |
| Geometric mean | (ref)                                                        | 1.14x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 586 ms: 1.56x faster                                                  |
| async_tree_io              | 876 ms                                                       | 600 ms: 1.46x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 238 ms: 1.41x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 309 ms: 1.34x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 476 ms: 1.34x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 347 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 511 ms: 1.30x faster                                                  |
| async_tree_none            | 354 ms                                                       | 281 ms: 1.26x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.8 ms: 1.01x slower                                                 |
| async_generators           | 377 ms                                                       | 411 ms: 1.09x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.25x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 181 ms: 1.20x faster                                                  |
| float          | 77.5 ms                                                      | 80.7 ms: 1.04x slower                                                 |
| nbody          | 85.1 ms                                                      | 130 ms: 1.53x slower                                                  |
| Geometric mean | (ref)                                                        | 1.10x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.93 ms: 1.05x faster                                                 |
| regex_dna      | 180 ms                                                       | 182 ms: 1.01x slower                                                  |
| regex_v8       | 22.7 ms                                                      | 24.0 ms: 1.06x slower                                                 |
| regex_compile  | 132 ms                                                       | 150 ms: 1.13x slower                                                  |
| Geometric mean | (ref)                                                        | 1.04x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 88.7 ms: 1.07x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.04x faster                                                  |
| json_loads           | 27.0 us                                                      | 28.0 us: 1.04x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 95.6 ms: 1.12x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 67.8 ms: 1.14x slower                                                 |
| tomli_loads          | 2.01 sec                                                     | 2.33 sec: 1.16x slower                                                |
| unpickle_pure_python | 210 us                                                       | 250 us: 1.19x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 366 us: 1.24x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 13.2 ms: 1.25x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.11x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                 |
| python_startup         | 11.0 ms                                                      | 17.1 ms: 1.55x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.47x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 58.7 ms: 1.20x slower                                                 |
| genshi_text     | 21.5 ms                                                      | 27.0 ms: 1.26x slower                                                 |
| django_template | 34.1 ms                                                      | 43.3 ms: 1.27x slower                                                 |
| mako            | 11.3 ms                                                      | 15.5 ms: 1.37x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.27x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 586 ms: 1.56x faster                                                  |
| async_tree_io              | 876 ms                                                       | 600 ms: 1.46x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 238 ms: 1.41x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 309 ms: 1.34x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 476 ms: 1.34x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 347 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 511 ms: 1.30x faster                                                  |
| async_tree_none            | 354 ms                                                       | 281 ms: 1.26x faster                                                  |
| pidigits                   | 217 ms                                                       | 181 ms: 1.20x faster                                                  |
| deepcopy                   | 355 us                                                       | 314 us: 1.13x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.06 us: 1.07x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 88.7 ms: 1.07x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.93 ms: 1.05x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.04x faster                                                  |
| go                         | 141 ms                                                       | 138 ms: 1.02x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 18.8 ms: 1.02x faster                                                 |
| deepcopy_memo              | 39.1 us                                                      | 38.4 us: 1.02x faster                                                 |
| coroutines                 | 23.6 ms                                                      | 23.8 ms: 1.01x slower                                                 |
| regex_dna                  | 180 ms                                                       | 182 ms: 1.01x slower                                                  |
| json_loads                 | 27.0 us                                                      | 28.0 us: 1.04x slower                                                 |
| spectral_norm              | 111 ms                                                       | 116 ms: 1.04x slower                                                  |
| float                      | 77.5 ms                                                      | 80.7 ms: 1.04x slower                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 3.26 us: 1.05x slower                                                 |
| regex_v8                   | 22.7 ms                                                      | 24.0 ms: 1.06x slower                                                 |
| generators                 | 28.8 ms                                                      | 30.5 ms: 1.06x slower                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.71 sec: 1.06x slower                                                |
| pyflate                    | 449 ms                                                       | 477 ms: 1.06x slower                                                  |
| telco                      | 7.82 ms                                                      | 8.36 ms: 1.07x slower                                                 |
| scimark_fft                | 349 ms                                                       | 374 ms: 1.07x slower                                                  |
| pylint                     | 317 ms                                                       | 342 ms: 1.08x slower                                                  |
| async_generators           | 377 ms                                                       | 411 ms: 1.09x slower                                                  |
| docutils                   | 2.62 sec                                                     | 2.85 sec: 1.09x slower                                                |
| pycparser                  | 1.12 sec                                                     | 1.23 sec: 1.10x slower                                                |
| dulwich_log                | 74.8 ms                                                      | 82.7 ms: 1.11x slower                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.24 ms: 1.11x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 95.6 ms: 1.12x slower                                                 |
| scimark_sor                | 134 ms                                                       | 151 ms: 1.12x slower                                                  |
| html5lib                   | 67.0 ms                                                      | 75.2 ms: 1.12x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 3.54 ms: 1.13x slower                                                 |
| regex_compile              | 132 ms                                                       | 150 ms: 1.13x slower                                                  |
| pprint_safe_repr           | 738 ms                                                       | 836 ms: 1.13x slower                                                  |
| logging_silent             | 103 ns                                                       | 117 ns: 1.14x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 67.8 ms: 1.14x slower                                                 |
| sqlglot_normalize          | 106 ms                                                       | 121 ms: 1.14x slower                                                  |
| mdp                        | 2.36 sec                                                     | 2.70 sec: 1.15x slower                                                |
| pprint_pformat             | 1.50 sec                                                     | 1.72 sec: 1.15x slower                                                |
| sqlglot_optimize           | 52.7 ms                                                      | 61.0 ms: 1.16x slower                                                 |
| tomli_loads                | 2.01 sec                                                     | 2.33 sec: 1.16x slower                                                |
| logging_simple             | 6.16 us                                                      | 7.27 us: 1.18x slower                                                 |
| thrift                     | 778 us                                                       | 920 us: 1.18x slower                                                  |
| coverage                   | 83.0 ms                                                      | 98.6 ms: 1.19x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 93.7 ms: 1.19x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 250 us: 1.19x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 58.7 ms: 1.20x slower                                                 |
| comprehensions             | 16.5 us                                                      | 19.9 us: 1.21x slower                                                 |
| 2to3                       | 260 ms                                                       | 316 ms: 1.22x slower                                                  |
| logging_format             | 6.84 us                                                      | 8.36 us: 1.22x slower                                                 |
| chaos                      | 57.3 ms                                                      | 70.3 ms: 1.23x slower                                                 |
| sqlglot_transpile          | 1.56 ms                                                      | 1.93 ms: 1.24x slower                                                 |
| hexiom                     | 5.99 ms                                                      | 7.43 ms: 1.24x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 366 us: 1.24x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 81.5 ms: 1.25x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 13.2 ms: 1.25x slower                                                 |
| genshi_text                | 21.5 ms                                                      | 27.0 ms: 1.26x slower                                                 |
| richards                   | 45.2 ms                                                      | 56.9 ms: 1.26x slower                                                 |
| meteor_contest             | 102 ms                                                       | 128 ms: 1.26x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 85.9 ms: 1.26x slower                                                 |
| typing_runtime_protocols   | 155 us                                                       | 196 us: 1.27x slower                                                  |
| django_template            | 34.1 ms                                                      | 43.3 ms: 1.27x slower                                                 |
| richards_super             | 51.6 ms                                                      | 65.6 ms: 1.27x slower                                                 |
| sqlglot_parse              | 1.25 ms                                                      | 1.60 ms: 1.28x slower                                                 |
| raytrace                   | 253 ms                                                       | 326 ms: 1.29x slower                                                  |
| fannkuch                   | 370 ms                                                       | 479 ms: 1.30x slower                                                  |
| mako                       | 11.3 ms                                                      | 15.5 ms: 1.37x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.85 ms: 1.38x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 28.4 ms: 1.43x slower                                                 |
| scimark_lu                 | 113 ms                                                       | 164 ms: 1.46x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 4.61 ms: 1.47x slower                                                 |
| nbody                      | 85.1 ms                                                      | 130 ms: 1.53x slower                                                  |
| python_startup             | 11.0 ms                                                      | 17.1 ms: 1.55x slower                                                 |
| sympy_str                  | 275 ms                                                       | 454 ms: 1.65x slower                                                  |
| sympy_expand               | 457 ms                                                       | 920 ms: 2.01x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 341 ms: 2.19x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 3.32 ms: 3.61x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 106 ms: 9.62x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.17x slower                                                          |

Benchmark hidden because not significant (2): json, asyncio_websockets
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241215-3.14.0a2+-3c144b3-NOGIL/bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.109x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.33x