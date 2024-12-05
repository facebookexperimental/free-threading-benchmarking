# Results vs. 3.13.0rc2

- fork: colesbury
- ref: gh_127582_resurrecti
- machine: linux-x86_64
- commit hash: a7b41c8
- commit date: 2024-12-04
- overall geometric mean: 1.249x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.19x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-colesbury-gh_127582_resurrecti-3.14.0a2+-a7b41c8 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 367 ms: 1.41x slower                                                      |
| docutils       | 2.62 sec                                                     | 3.10 sec: 1.19x slower                                                    |
| html5lib       | 67.0 ms                                                      | 99.6 ms: 1.49x slower                                                     |
| Geometric mean | (ref)                                                        | 1.36x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-colesbury-gh_127582_resurrecti-3.14.0a2+-a7b41c8 |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 831 ms: 1.10x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 647 ms: 1.03x faster                                                      |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 619 ms: 1.03x faster                                                      |
| async_tree_io              | 876 ms                                                       | 853 ms: 1.03x faster                                                      |
| async_tree_memoization     | 461 ms                                                       | 473 ms: 1.03x slower                                                      |
| coroutines                 | 23.6 ms                                                      | 24.7 ms: 1.05x slower                                                     |
| async_tree_none_tg         | 336 ms                                                       | 355 ms: 1.06x slower                                                      |
| async_tree_memoization_tg  | 414 ms                                                       | 450 ms: 1.09x slower                                                      |
| async_tree_none            | 354 ms                                                       | 390 ms: 1.10x slower                                                      |
| async_generators           | 377 ms                                                       | 447 ms: 1.18x slower                                                      |
| Geometric mean             | (ref)                                                        | 1.03x slower                                                              |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-colesbury-gh_127582_resurrecti-3.14.0a2+-a7b41c8 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 181 ms: 1.20x faster                                                      |
| nbody          | 85.1 ms                                                      | 133 ms: 1.56x slower                                                      |
| float          | 77.5 ms                                                      | 137 ms: 1.77x slower                                                      |
| Geometric mean | (ref)                                                        | 1.32x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-colesbury-gh_127582_resurrecti-3.14.0a2+-a7b41c8 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.84 ms: 1.09x faster                                                     |
| regex_dna      | 180 ms                                                       | 185 ms: 1.02x slower                                                      |
| regex_v8       | 22.7 ms                                                      | 23.9 ms: 1.05x slower                                                     |
| regex_compile  | 132 ms                                                       | 180 ms: 1.36x slower                                                      |
| Geometric mean | (ref)                                                        | 1.08x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-colesbury-gh_127582_resurrecti-3.14.0a2+-a7b41c8 |
|----------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                      |
| xml_etree_iterparse  | 94.9 ms                                                      | 91.6 ms: 1.04x faster                                                     |
| json_loads           | 27.0 us                                                      | 28.3 us: 1.05x slower                                                     |
| xml_etree_generate   | 85.4 ms                                                      | 97.3 ms: 1.14x slower                                                     |
| xml_etree_process    | 59.3 ms                                                      | 77.9 ms: 1.31x slower                                                     |
| tomli_loads          | 2.01 sec                                                     | 2.66 sec: 1.33x slower                                                    |
| json_dumps           | 10.5 ms                                                      | 14.2 ms: 1.34x slower                                                     |
| unpickle_pure_python | 210 us                                                       | 333 us: 1.59x slower                                                      |
| pickle_pure_python   | 294 us                                                       | 510 us: 1.73x slower                                                      |
| Geometric mean       | (ref)                                                        | 1.24x slower                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-colesbury-gh_127582_resurrecti-3.14.0a2+-a7b41c8 |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                     |
| python_startup         | 11.0 ms                                                      | 17.4 ms: 1.58x slower                                                     |
| Geometric mean         | (ref)                                                        | 1.48x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-colesbury-gh_127582_resurrecti-3.14.0a2+-a7b41c8 |
|-----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 63.8 ms: 1.31x slower                                                     |
| genshi_text     | 21.5 ms                                                      | 31.6 ms: 1.47x slower                                                     |
| django_template | 34.1 ms                                                      | 51.9 ms: 1.52x slower                                                     |
| mako            | 11.3 ms                                                      | 17.8 ms: 1.57x slower                                                     |
| Geometric mean  | (ref)                                                        | 1.46x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-colesbury-gh_127582_resurrecti-3.14.0a2+-a7b41c8 |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits                   | 217 ms                                                       | 181 ms: 1.20x faster                                                      |
| async_tree_io_tg           | 913 ms                                                       | 831 ms: 1.10x faster                                                      |
| regex_effbot               | 3.08 ms                                                      | 2.84 ms: 1.09x faster                                                     |
| deepcopy                   | 355 us                                                       | 331 us: 1.08x faster                                                      |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                      |
| xml_etree_iterparse        | 94.9 ms                                                      | 91.6 ms: 1.04x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 647 ms: 1.03x faster                                                      |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 619 ms: 1.03x faster                                                      |
| async_tree_io              | 876 ms                                                       | 853 ms: 1.03x faster                                                      |
| deepcopy_memo              | 39.1 us                                                      | 40.0 us: 1.02x slower                                                     |
| regex_dna                  | 180 ms                                                       | 185 ms: 1.02x slower                                                      |
| async_tree_memoization     | 461 ms                                                       | 473 ms: 1.03x slower                                                      |
| sqlite_synth               | 2.21 us                                                      | 2.27 us: 1.03x slower                                                     |
| json                       | 4.93 ms                                                      | 5.11 ms: 1.04x slower                                                     |
| gc_traversal               | 3.14 ms                                                      | 3.26 ms: 1.04x slower                                                     |
| coroutines                 | 23.6 ms                                                      | 24.7 ms: 1.05x slower                                                     |
| json_loads                 | 27.0 us                                                      | 28.3 us: 1.05x slower                                                     |
| regex_v8                   | 22.7 ms                                                      | 23.9 ms: 1.05x slower                                                     |
| async_tree_none_tg         | 336 ms                                                       | 355 ms: 1.06x slower                                                      |
| pathlib                    | 19.2 ms                                                      | 20.4 ms: 1.06x slower                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 450 ms: 1.09x slower                                                      |
| async_tree_none            | 354 ms                                                       | 390 ms: 1.10x slower                                                      |
| spectral_norm              | 111 ms                                                       | 123 ms: 1.11x slower                                                      |
| deepcopy_reduce            | 3.11 us                                                      | 3.50 us: 1.12x slower                                                     |
| telco                      | 7.82 ms                                                      | 8.80 ms: 1.12x slower                                                     |
| bpe_tokeniser              | 4.45 sec                                                     | 5.04 sec: 1.13x slower                                                    |
| xml_etree_generate         | 85.4 ms                                                      | 97.3 ms: 1.14x slower                                                     |
| scimark_fft                | 349 ms                                                       | 402 ms: 1.15x slower                                                      |
| async_generators           | 377 ms                                                       | 447 ms: 1.18x slower                                                      |
| docutils                   | 2.62 sec                                                     | 3.10 sec: 1.19x slower                                                    |
| coverage                   | 83.0 ms                                                      | 99.5 ms: 1.20x slower                                                     |
| pylint                     | 317 ms                                                       | 382 ms: 1.20x slower                                                      |
| mdp                        | 2.36 sec                                                     | 2.90 sec: 1.23x slower                                                    |
| nqueens                    | 78.6 ms                                                      | 97.0 ms: 1.23x slower                                                     |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.91 ms: 1.26x slower                                                     |
| meteor_contest             | 102 ms                                                       | 130 ms: 1.28x slower                                                      |
| dulwich_log                | 74.8 ms                                                      | 96.0 ms: 1.28x slower                                                     |
| sqlglot_normalize          | 106 ms                                                       | 137 ms: 1.29x slower                                                      |
| genshi_xml                 | 48.8 ms                                                      | 63.8 ms: 1.31x slower                                                     |
| sqlglot_optimize           | 52.7 ms                                                      | 69.0 ms: 1.31x slower                                                     |
| xml_etree_process          | 59.3 ms                                                      | 77.9 ms: 1.31x slower                                                     |
| generators                 | 28.8 ms                                                      | 37.9 ms: 1.32x slower                                                     |
| typing_runtime_protocols   | 155 us                                                       | 204 us: 1.32x slower                                                      |
| tomli_loads                | 2.01 sec                                                     | 2.66 sec: 1.33x slower                                                    |
| pprint_safe_repr           | 738 ms                                                       | 985 ms: 1.34x slower                                                      |
| create_gc_cycles           | 1.34 ms                                                      | 1.79 ms: 1.34x slower                                                     |
| fannkuch                   | 370 ms                                                       | 495 ms: 1.34x slower                                                      |
| json_dumps                 | 10.5 ms                                                      | 14.2 ms: 1.34x slower                                                     |
| crypto_pyaes               | 67.9 ms                                                      | 91.9 ms: 1.35x slower                                                     |
| regex_compile              | 132 ms                                                       | 180 ms: 1.36x slower                                                      |
| pprint_pformat             | 1.50 sec                                                     | 2.04 sec: 1.37x slower                                                    |
| pycparser                  | 1.12 sec                                                     | 1.54 sec: 1.38x slower                                                    |
| python_startup_no_site     | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                     |
| 2to3                       | 260 ms                                                       | 367 ms: 1.41x slower                                                      |
| genshi_text                | 21.5 ms                                                      | 31.6 ms: 1.47x slower                                                     |
| html5lib                   | 67.0 ms                                                      | 99.6 ms: 1.49x slower                                                     |
| sympy_integrate            | 19.8 ms                                                      | 29.6 ms: 1.49x slower                                                     |
| thrift                     | 778 us                                                       | 1.18 ms: 1.51x slower                                                     |
| pyflate                    | 449 ms                                                       | 681 ms: 1.52x slower                                                      |
| django_template            | 34.1 ms                                                      | 51.9 ms: 1.52x slower                                                     |
| nbody                      | 85.1 ms                                                      | 133 ms: 1.56x slower                                                      |
| mako                       | 11.3 ms                                                      | 17.8 ms: 1.57x slower                                                     |
| python_startup             | 11.0 ms                                                      | 17.4 ms: 1.58x slower                                                     |
| unpickle_pure_python       | 210 us                                                       | 333 us: 1.59x slower                                                      |
| scimark_lu                 | 113 ms                                                       | 183 ms: 1.62x slower                                                      |
| hexiom                     | 5.99 ms                                                      | 9.75 ms: 1.63x slower                                                     |
| comprehensions             | 16.5 us                                                      | 27.0 us: 1.64x slower                                                     |
| richards_super             | 51.6 ms                                                      | 86.7 ms: 1.68x slower                                                     |
| richards                   | 45.2 ms                                                      | 77.7 ms: 1.72x slower                                                     |
| pickle_pure_python         | 294 us                                                       | 510 us: 1.73x slower                                                      |
| sympy_str                  | 275 ms                                                       | 478 ms: 1.74x slower                                                      |
| scimark_sor                | 134 ms                                                       | 237 ms: 1.76x slower                                                      |
| logging_format             | 6.84 us                                                      | 12.1 us: 1.77x slower                                                     |
| logging_simple             | 6.16 us                                                      | 10.9 us: 1.77x slower                                                     |
| float                      | 77.5 ms                                                      | 137 ms: 1.77x slower                                                      |
| logging_silent             | 103 ns                                                       | 183 ns: 1.78x slower                                                      |
| chaos                      | 57.3 ms                                                      | 105 ms: 1.83x slower                                                      |
| scimark_monte_carlo        | 65.4 ms                                                      | 120 ms: 1.84x slower                                                      |
| sqlglot_transpile          | 1.56 ms                                                      | 2.98 ms: 1.91x slower                                                     |
| go                         | 141 ms                                                       | 269 ms: 1.91x slower                                                      |
| sqlglot_parse              | 1.25 ms                                                      | 2.58 ms: 2.07x slower                                                     |
| sympy_expand               | 457 ms                                                       | 955 ms: 2.09x slower                                                      |
| raytrace                   | 253 ms                                                       | 547 ms: 2.17x slower                                                      |
| sympy_sum                  | 156 ms                                                       | 350 ms: 2.25x slower                                                      |
| deltablue                  | 3.12 ms                                                      | 7.85 ms: 2.51x slower                                                     |
| bench_thread_pool          | 919 us                                                       | 3.36 ms: 3.65x slower                                                     |
| bench_mp_pool              | 11.0 ms                                                      | 109 ms: 9.87x slower                                                      |
| Geometric mean             | (ref)                                                        | 1.38x slower                                                              |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241204-3.14.0a2+-a7b41c8-NOGIL/bm-20241204-vultr-x86_64-colesbury-gh_127582_resurrecti-3.14.0a2+-a7b41c8.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.249x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.24x
- 95% likely to have a slowdown of 1.23x
- 99% likely to have a slowdown of 1.19x

# Memory
- memory change: 1.31x