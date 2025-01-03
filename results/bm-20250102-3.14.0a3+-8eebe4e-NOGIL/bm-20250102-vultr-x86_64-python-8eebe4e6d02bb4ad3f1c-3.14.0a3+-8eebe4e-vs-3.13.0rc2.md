# Results vs. 3.13.0rc2

- fork: python
- ref: 8eebe4e6d02bb4ad3f1c
- machine: linux-x86_64
- commit hash: 8eebe4e
- commit date: 2025-01-02
- overall geometric mean: 1.194x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.14x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 351 ms: 1.35x slower                                                   |
| docutils       | 2.62 sec                                                     | 3.00 sec: 1.15x slower                                                 |
| html5lib       | 67.0 ms                                                      | 93.4 ms: 1.39x slower                                                  |
| Geometric mean | (ref)                                                        | 1.29x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 719 ms: 1.27x faster                                                   |
| async_tree_io              | 876 ms                                                       | 749 ms: 1.17x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 563 ms: 1.13x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 592 ms: 1.12x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 422 ms: 1.09x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 309 ms: 1.09x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 391 ms: 1.06x faster                                                   |
| async_tree_none            | 354 ms                                                       | 348 ms: 1.02x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 24.4 ms: 1.04x slower                                                  |
| async_generators           | 377 ms                                                       | 451 ms: 1.20x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.06x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 193 ms: 1.12x faster                                                   |
| float          | 77.5 ms                                                      | 108 ms: 1.40x slower                                                   |
| nbody          | 85.1 ms                                                      | 129 ms: 1.52x slower                                                   |
| Geometric mean | (ref)                                                        | 1.24x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.71 ms: 1.14x faster                                                  |
| regex_dna      | 180 ms                                                       | 178 ms: 1.01x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 23.3 ms: 1.03x slower                                                  |
| regex_compile  | 132 ms                                                       | 170 ms: 1.28x slower                                                   |
| Geometric mean | (ref)                                                        | 1.03x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 89.5 ms: 1.06x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.05x faster                                                   |
| json_loads           | 27.0 us                                                      | 28.1 us: 1.04x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 97.7 ms: 1.14x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 74.0 ms: 1.25x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.55 sec: 1.27x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 13.9 ms: 1.32x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 327 us: 1.56x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 499 us: 1.70x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.22x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.76 ms: 1.32x slower                                                  |
| python_startup         | 11.0 ms                                                      | 15.6 ms: 1.42x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 63.9 ms: 1.31x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 31.0 ms: 1.44x slower                                                  |
| django_template | 34.1 ms                                                      | 49.6 ms: 1.45x slower                                                  |
| mako            | 11.3 ms                                                      | 17.2 ms: 1.52x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.43x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 719 ms: 1.27x faster                                                   |
| async_tree_io              | 876 ms                                                       | 749 ms: 1.17x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.71 ms: 1.14x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 563 ms: 1.13x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 592 ms: 1.12x faster                                                   |
| pidigits                   | 217 ms                                                       | 193 ms: 1.12x faster                                                   |
| deepcopy                   | 355 us                                                       | 324 us: 1.10x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 422 ms: 1.09x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 309 ms: 1.09x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 89.5 ms: 1.06x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 391 ms: 1.06x faster                                                   |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.05x faster                                                   |
| sqlite_synth               | 2.21 us                                                      | 2.11 us: 1.04x faster                                                  |
| async_tree_none            | 354 ms                                                       | 348 ms: 1.02x faster                                                   |
| regex_dna                  | 180 ms                                                       | 178 ms: 1.01x faster                                                   |
| pathlib                    | 19.2 ms                                                      | 19.3 ms: 1.01x slower                                                  |
| json                       | 4.93 ms                                                      | 5.00 ms: 1.01x slower                                                  |
| spectral_norm              | 111 ms                                                       | 113 ms: 1.02x slower                                                   |
| regex_v8                   | 22.7 ms                                                      | 23.3 ms: 1.03x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 24.4 ms: 1.04x slower                                                  |
| json_loads                 | 27.0 us                                                      | 28.1 us: 1.04x slower                                                  |
| deepcopy_memo              | 39.1 us                                                      | 40.8 us: 1.05x slower                                                  |
| scimark_fft                | 349 ms                                                       | 377 ms: 1.08x slower                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 3.40 us: 1.09x slower                                                  |
| pylint                     | 317 ms                                                       | 347 ms: 1.09x slower                                                   |
| telco                      | 7.82 ms                                                      | 8.66 ms: 1.11x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 3.52 ms: 1.12x slower                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 5.04 sec: 1.13x slower                                                 |
| mdp                        | 2.36 sec                                                     | 2.69 sec: 1.14x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 97.7 ms: 1.14x slower                                                  |
| docutils                   | 2.62 sec                                                     | 3.00 sec: 1.15x slower                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.58 ms: 1.19x slower                                                  |
| coverage                   | 83.0 ms                                                      | 98.7 ms: 1.19x slower                                                  |
| async_generators           | 377 ms                                                       | 451 ms: 1.20x slower                                                   |
| dulwich_log                | 74.8 ms                                                      | 90.0 ms: 1.20x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.37 sec: 1.22x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 97.9 ms: 1.25x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 74.0 ms: 1.25x slower                                                  |
| sqlglot_normalize          | 106 ms                                                       | 133 ms: 1.25x slower                                                   |
| sympy_sum                  | 156 ms                                                       | 195 ms: 1.26x slower                                                   |
| sqlglot_optimize           | 52.7 ms                                                      | 66.6 ms: 1.26x slower                                                  |
| tomli_loads                | 2.01 sec                                                     | 2.55 sec: 1.27x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 25.2 ms: 1.27x slower                                                  |
| pprint_safe_repr           | 738 ms                                                       | 943 ms: 1.28x slower                                                   |
| sympy_expand               | 457 ms                                                       | 584 ms: 1.28x slower                                                   |
| regex_compile              | 132 ms                                                       | 170 ms: 1.28x slower                                                   |
| sympy_str                  | 275 ms                                                       | 355 ms: 1.29x slower                                                   |
| thrift                     | 778 us                                                       | 1.01 ms: 1.29x slower                                                  |
| meteor_contest             | 102 ms                                                       | 132 ms: 1.30x slower                                                   |
| genshi_xml                 | 48.8 ms                                                      | 63.9 ms: 1.31x slower                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.97 sec: 1.32x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 13.9 ms: 1.32x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 9.76 ms: 1.32x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 90.1 ms: 1.33x slower                                                  |
| generators                 | 28.8 ms                                                      | 38.3 ms: 1.33x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 207 us: 1.34x slower                                                   |
| fannkuch                   | 370 ms                                                       | 495 ms: 1.34x slower                                                   |
| 2to3                       | 260 ms                                                       | 351 ms: 1.35x slower                                                   |
| scimark_lu                 | 113 ms                                                       | 155 ms: 1.37x slower                                                   |
| create_gc_cycles           | 1.34 ms                                                      | 1.85 ms: 1.38x slower                                                  |
| html5lib                   | 67.0 ms                                                      | 93.4 ms: 1.39x slower                                                  |
| float                      | 77.5 ms                                                      | 108 ms: 1.40x slower                                                   |
| python_startup             | 11.0 ms                                                      | 15.6 ms: 1.42x slower                                                  |
| genshi_text                | 21.5 ms                                                      | 31.0 ms: 1.44x slower                                                  |
| django_template            | 34.1 ms                                                      | 49.6 ms: 1.45x slower                                                  |
| logging_simple             | 6.16 us                                                      | 9.10 us: 1.48x slower                                                  |
| richards_super             | 51.6 ms                                                      | 76.5 ms: 1.48x slower                                                  |
| pyflate                    | 449 ms                                                       | 665 ms: 1.48x slower                                                   |
| richards                   | 45.2 ms                                                      | 67.6 ms: 1.49x slower                                                  |
| logging_format             | 6.84 us                                                      | 10.3 us: 1.51x slower                                                  |
| nbody                      | 85.1 ms                                                      | 129 ms: 1.52x slower                                                   |
| mako                       | 11.3 ms                                                      | 17.2 ms: 1.52x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 327 us: 1.56x slower                                                   |
| scimark_sor                | 134 ms                                                       | 216 ms: 1.60x slower                                                   |
| hexiom                     | 5.99 ms                                                      | 9.62 ms: 1.61x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 106 ms: 1.62x slower                                                   |
| comprehensions             | 16.5 us                                                      | 27.2 us: 1.65x slower                                                  |
| chaos                      | 57.3 ms                                                      | 96.0 ms: 1.68x slower                                                  |
| go                         | 141 ms                                                       | 238 ms: 1.69x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 499 us: 1.70x slower                                                   |
| sqlglot_transpile          | 1.56 ms                                                      | 2.69 ms: 1.72x slower                                                  |
| logging_silent             | 103 ns                                                       | 181 ns: 1.77x slower                                                   |
| sqlglot_parse              | 1.25 ms                                                      | 2.32 ms: 1.86x slower                                                  |
| raytrace                   | 253 ms                                                       | 489 ms: 1.94x slower                                                   |
| deltablue                  | 3.12 ms                                                      | 7.39 ms: 2.37x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 3.37 ms: 3.67x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 100 ms: 9.10x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.29x slower                                                           |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250102-3.14.0a3+-8eebe4e-NOGIL/bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.194x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.19x
- 95% likely to have a slowdown of 1.16x
- 99% likely to have a slowdown of 1.14x

# Memory
- memory change: 1.32x