# Results vs. 3.12.6

- fork: colesbury
- ref: gh_127582_resurrecti
- machine: linux-x86_64
- commit hash: a7b41c8
- commit date: 2024-12-04
- overall geometric mean: 1.225x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-colesbury-gh_127582_resurrecti-3.14.0a2+-a7b41c8 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 367 ms: 1.39x slower                                                      |
| docutils       | 2.64 sec                                               | 3.10 sec: 1.18x slower                                                    |
| html5lib       | 63.6 ms                                                | 99.6 ms: 1.57x slower                                                     |
| Geometric mean | (ref)                                                  | 1.37x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-colesbury-gh_127582_resurrecti-3.14.0a2+-a7b41c8 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 831 ms: 1.34x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 853 ms: 1.27x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 355 ms: 1.26x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 450 ms: 1.24x faster                                                      |
| async_tree_none            | 464 ms                                                 | 390 ms: 1.19x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 473 ms: 1.17x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 619 ms: 1.17x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 647 ms: 1.11x faster                                                      |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                                      |
| coroutines                 | 23.9 ms                                                | 24.7 ms: 1.03x slower                                                     |
| async_generators           | 384 ms                                                 | 447 ms: 1.16x slower                                                      |
| Geometric mean             | (ref)                                                  | 1.13x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-colesbury-gh_127582_resurrecti-3.14.0a2+-a7b41c8 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 181 ms: 1.02x faster                                                      |
| nbody          | 89.3 ms                                                | 133 ms: 1.49x slower                                                      |
| float          | 80.8 ms                                                | 137 ms: 1.70x slower                                                      |
| Geometric mean | (ref)                                                  | 1.35x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-colesbury-gh_127582_resurrecti-3.14.0a2+-a7b41c8 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.84 ms: 1.12x faster                                                     |
| regex_dna      | 168 ms                                                 | 185 ms: 1.10x slower                                                      |
| regex_v8       | 20.6 ms                                                | 23.9 ms: 1.16x slower                                                     |
| regex_compile  | 142 ms                                                 | 180 ms: 1.26x slower                                                      |
| Geometric mean | (ref)                                                  | 1.10x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-colesbury-gh_127582_resurrecti-3.14.0a2+-a7b41c8 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                      |
| xml_etree_iterparse  | 96.7 ms                                                | 91.6 ms: 1.06x faster                                                     |
| json_loads           | 26.5 us                                                | 28.3 us: 1.07x slower                                                     |
| xml_etree_generate   | 85.2 ms                                                | 97.3 ms: 1.14x slower                                                     |
| tomli_loads          | 2.11 sec                                               | 2.66 sec: 1.26x slower                                                    |
| xml_etree_process    | 59.0 ms                                                | 77.9 ms: 1.32x slower                                                     |
| json_dumps           | 10.4 ms                                                | 14.2 ms: 1.37x slower                                                     |
| unpickle_pure_python | 221 us                                                 | 333 us: 1.51x slower                                                      |
| pickle_pure_python   | 308 us                                                 | 510 us: 1.66x slower                                                      |
| Geometric mean       | (ref)                                                  | 1.23x slower                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-colesbury-gh_127582_resurrecti-3.14.0a2+-a7b41c8 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.2 ms: 1.42x slower                                                     |
| python_startup         | 9.93 ms                                                | 17.4 ms: 1.75x slower                                                     |
| Geometric mean         | (ref)                                                  | 1.58x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-colesbury-gh_127582_resurrecti-3.14.0a2+-a7b41c8 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 63.8 ms: 1.27x slower                                                     |
| genshi_text     | 22.8 ms                                                | 31.6 ms: 1.39x slower                                                     |
| django_template | 34.7 ms                                                | 51.9 ms: 1.50x slower                                                     |
| mako            | 11.0 ms                                                | 17.8 ms: 1.62x slower                                                     |
| Geometric mean  | (ref)                                                  | 1.44x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-colesbury-gh_127582_resurrecti-3.14.0a2+-a7b41c8 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 831 ms: 1.34x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 853 ms: 1.27x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 355 ms: 1.26x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 450 ms: 1.24x faster                                                      |
| async_tree_none            | 464 ms                                                 | 390 ms: 1.19x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 473 ms: 1.17x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 619 ms: 1.17x faster                                                      |
| regex_effbot               | 3.17 ms                                                | 2.84 ms: 1.12x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 647 ms: 1.11x faster                                                      |
| deepcopy                   | 352 us                                                 | 331 us: 1.06x faster                                                      |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                      |
| gc_traversal               | 3.46 ms                                                | 3.26 ms: 1.06x faster                                                     |
| pathlib                    | 21.5 ms                                                | 20.4 ms: 1.06x faster                                                     |
| xml_etree_iterparse        | 96.7 ms                                                | 91.6 ms: 1.06x faster                                                     |
| pidigits                   | 184 ms                                                 | 181 ms: 1.02x faster                                                      |
| deepcopy_memo              | 40.3 us                                                | 40.0 us: 1.01x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                                      |
| json                       | 5.02 ms                                                | 5.11 ms: 1.02x slower                                                     |
| coroutines                 | 23.9 ms                                                | 24.7 ms: 1.03x slower                                                     |
| sqlite_synth               | 2.20 us                                                | 2.27 us: 1.03x slower                                                     |
| bpe_tokeniser              | 4.74 sec                                               | 5.04 sec: 1.07x slower                                                    |
| json_loads                 | 26.5 us                                                | 28.3 us: 1.07x slower                                                     |
| regex_dna                  | 168 ms                                                 | 185 ms: 1.10x slower                                                      |
| spectral_norm              | 110 ms                                                 | 123 ms: 1.12x slower                                                      |
| deepcopy_reduce            | 3.08 us                                                | 3.50 us: 1.14x slower                                                     |
| xml_etree_generate         | 85.2 ms                                                | 97.3 ms: 1.14x slower                                                     |
| regex_v8                   | 20.6 ms                                                | 23.9 ms: 1.16x slower                                                     |
| async_generators           | 384 ms                                                 | 447 ms: 1.16x slower                                                      |
| scimark_fft                | 342 ms                                                 | 402 ms: 1.18x slower                                                      |
| generators                 | 32.2 ms                                                | 37.9 ms: 1.18x slower                                                     |
| docutils                   | 2.64 sec                                               | 3.10 sec: 1.18x slower                                                    |
| pylint                     | 319 ms                                                 | 382 ms: 1.20x slower                                                      |
| crypto_pyaes               | 76.6 ms                                                | 91.9 ms: 1.20x slower                                                     |
| mdp                        | 2.42 sec                                               | 2.90 sec: 1.20x slower                                                    |
| nqueens                    | 80.1 ms                                                | 97.0 ms: 1.21x slower                                                     |
| dulwich_log                | 78.9 ms                                                | 96.0 ms: 1.22x slower                                                     |
| typing_runtime_protocols   | 163 us                                                 | 204 us: 1.25x slower                                                      |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.25x slower                                                      |
| regex_compile              | 142 ms                                                 | 180 ms: 1.26x slower                                                      |
| tomli_loads                | 2.11 sec                                               | 2.66 sec: 1.26x slower                                                    |
| genshi_xml                 | 50.2 ms                                                | 63.8 ms: 1.27x slower                                                     |
| sqlglot_normalize          | 107 ms                                                 | 137 ms: 1.28x slower                                                      |
| sqlglot_optimize           | 53.3 ms                                                | 69.0 ms: 1.29x slower                                                     |
| pycparser                  | 1.17 sec                                               | 1.54 sec: 1.32x slower                                                    |
| xml_etree_process          | 59.0 ms                                                | 77.9 ms: 1.32x slower                                                     |
| pprint_safe_repr           | 743 ms                                                 | 985 ms: 1.33x slower                                                      |
| fannkuch                   | 372 ms                                                 | 495 ms: 1.33x slower                                                      |
| pprint_pformat             | 1.52 sec                                               | 2.04 sec: 1.34x slower                                                    |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.91 ms: 1.35x slower                                                     |
| telco                      | 6.53 ms                                                | 8.80 ms: 1.35x slower                                                     |
| sqlalchemy_imperative      | 21.8 ms                                                | 29.6 ms: 1.36x slower                                                     |
| comprehensions             | 19.8 us                                                | 27.0 us: 1.36x slower                                                     |
| json_dumps                 | 10.4 ms                                                | 14.2 ms: 1.37x slower                                                     |
| genshi_text                | 22.8 ms                                                | 31.6 ms: 1.39x slower                                                     |
| 2to3                       | 264 ms                                                 | 367 ms: 1.39x slower                                                      |
| coverage                   | 71.4 ms                                                | 99.5 ms: 1.39x slower                                                     |
| python_startup_no_site     | 7.16 ms                                                | 10.2 ms: 1.42x slower                                                     |
| sqlalchemy_declarative     | 143 ms                                                 | 204 ms: 1.43x slower                                                      |
| sympy_integrate            | 20.5 ms                                                | 29.6 ms: 1.44x slower                                                     |
| thrift                     | 791 us                                                 | 1.18 ms: 1.49x slower                                                     |
| nbody                      | 89.3 ms                                                | 133 ms: 1.49x slower                                                      |
| django_template            | 34.7 ms                                                | 51.9 ms: 1.50x slower                                                     |
| unpickle_pure_python       | 221 us                                                 | 333 us: 1.51x slower                                                      |
| pyflate                    | 448 ms                                                 | 681 ms: 1.52x slower                                                      |
| html5lib                   | 63.6 ms                                                | 99.6 ms: 1.57x slower                                                     |
| hexiom                     | 6.17 ms                                                | 9.75 ms: 1.58x slower                                                     |
| scimark_lu                 | 114 ms                                                 | 183 ms: 1.60x slower                                                      |
| mako                       | 11.0 ms                                                | 17.8 ms: 1.62x slower                                                     |
| create_gc_cycles           | 1.09 ms                                                | 1.79 ms: 1.64x slower                                                     |
| sympy_str                  | 292 ms                                                 | 478 ms: 1.64x slower                                                      |
| logging_format             | 7.35 us                                                | 12.1 us: 1.65x slower                                                     |
| logging_simple             | 6.63 us                                                | 10.9 us: 1.65x slower                                                     |
| pickle_pure_python         | 308 us                                                 | 510 us: 1.66x slower                                                      |
| chaos                      | 62.8 ms                                                | 105 ms: 1.67x slower                                                      |
| richards_super             | 51.9 ms                                                | 86.7 ms: 1.67x slower                                                     |
| logging_silent             | 109 ns                                                 | 183 ns: 1.68x slower                                                      |
| richards                   | 45.9 ms                                                | 77.7 ms: 1.69x slower                                                     |
| float                      | 80.8 ms                                                | 137 ms: 1.70x slower                                                      |
| python_startup             | 9.93 ms                                                | 17.4 ms: 1.75x slower                                                     |
| scimark_monte_carlo        | 68.4 ms                                                | 120 ms: 1.75x slower                                                      |
| sqlglot_transpile          | 1.67 ms                                                | 2.98 ms: 1.78x slower                                                     |
| scimark_sor                | 130 ms                                                 | 237 ms: 1.83x slower                                                      |
| raytrace                   | 299 ms                                                 | 547 ms: 1.83x slower                                                      |
| sqlglot_parse              | 1.36 ms                                                | 2.58 ms: 1.90x slower                                                     |
| go                         | 139 ms                                                 | 269 ms: 1.93x slower                                                      |
| sympy_expand               | 468 ms                                                 | 955 ms: 2.04x slower                                                      |
| sympy_sum                  | 166 ms                                                 | 350 ms: 2.11x slower                                                      |
| deltablue                  | 3.45 ms                                                | 7.85 ms: 2.28x slower                                                     |
| bench_thread_pool          | 941 us                                                 | 3.36 ms: 3.57x slower                                                     |
| bench_mp_pool              | 10.8 ms                                                | 109 ms: 10.05x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.34x slower                                                              |
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241204-3.14.0a2+-a7b41c8-NOGIL/bm-20241204-vultr-x86_64-colesbury-gh_127582_resurrecti-3.14.0a2+-a7b41c8.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.225x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.21x
- 95% likely to have a slowdown of 1.20x
- 99% likely to have a slowdown of 1.17x

# Memory
- memory change: 1.33x