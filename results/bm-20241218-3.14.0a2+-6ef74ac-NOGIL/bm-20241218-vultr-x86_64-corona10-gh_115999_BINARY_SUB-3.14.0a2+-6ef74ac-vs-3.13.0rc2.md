# Results vs. 3.13.0rc2

- fork: corona10
- ref: gh_115999_BINARY_SUB
- machine: linux-x86_64
- commit hash: 6ef74ac
- commit date: 2024-12-18
- overall geometric mean: 1.247x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.18x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 366 ms: 1.41x slower                                                     |
| docutils       | 2.62 sec                                                     | 3.10 sec: 1.18x slower                                                   |
| html5lib       | 67.0 ms                                                      | 98.1 ms: 1.46x slower                                                    |
| Geometric mean | (ref)                                                        | 1.35x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 827 ms: 1.10x faster                                                     |
| async_tree_io              | 876 ms                                                       | 849 ms: 1.03x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 620 ms: 1.03x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 649 ms: 1.03x faster                                                     |
| asyncio_websockets         | 520 ms                                                       | 518 ms: 1.00x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 473 ms: 1.03x slower                                                     |
| coroutines                 | 23.6 ms                                                      | 24.8 ms: 1.05x slower                                                    |
| async_tree_none_tg         | 336 ms                                                       | 356 ms: 1.06x slower                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 445 ms: 1.07x slower                                                     |
| async_tree_none            | 354 ms                                                       | 389 ms: 1.10x slower                                                     |
| async_generators           | 377 ms                                                       | 452 ms: 1.20x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.03x slower                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 184 ms: 1.18x faster                                                     |
| nbody          | 85.1 ms                                                      | 130 ms: 1.53x slower                                                     |
| float          | 77.5 ms                                                      | 138 ms: 1.79x slower                                                     |
| Geometric mean | (ref)                                                        | 1.32x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.92 ms: 1.06x faster                                                    |
| regex_dna      | 180 ms                                                       | 184 ms: 1.02x slower                                                     |
| regex_v8       | 22.7 ms                                                      | 25.5 ms: 1.13x slower                                                    |
| regex_compile  | 132 ms                                                       | 179 ms: 1.35x slower                                                     |
| Geometric mean | (ref)                                                        | 1.10x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 91.0 ms: 1.04x faster                                                    |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                     |
| json_loads           | 27.0 us                                                      | 28.1 us: 1.04x slower                                                    |
| xml_etree_generate   | 85.4 ms                                                      | 98.4 ms: 1.15x slower                                                    |
| xml_etree_process    | 59.3 ms                                                      | 78.3 ms: 1.32x slower                                                    |
| tomli_loads          | 2.01 sec                                                     | 2.69 sec: 1.34x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 14.2 ms: 1.34x slower                                                    |
| unpickle_pure_python | 210 us                                                       | 339 us: 1.61x slower                                                     |
| pickle_pure_python   | 294 us                                                       | 516 us: 1.75x slower                                                     |
| Geometric mean       | (ref)                                                        | 1.25x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                    |
| python_startup         | 11.0 ms                                                      | 17.4 ms: 1.59x slower                                                    |
| Geometric mean         | (ref)                                                        | 1.48x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 63.4 ms: 1.30x slower                                                    |
| genshi_text     | 21.5 ms                                                      | 31.4 ms: 1.46x slower                                                    |
| django_template | 34.1 ms                                                      | 50.7 ms: 1.49x slower                                                    |
| mako            | 11.3 ms                                                      | 17.8 ms: 1.57x slower                                                    |
| Geometric mean  | (ref)                                                        | 1.45x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits                   | 217 ms                                                       | 184 ms: 1.18x faster                                                     |
| async_tree_io_tg           | 913 ms                                                       | 827 ms: 1.10x faster                                                     |
| deepcopy                   | 355 us                                                       | 329 us: 1.08x faster                                                     |
| regex_effbot               | 3.08 ms                                                      | 2.92 ms: 1.06x faster                                                    |
| xml_etree_iterparse        | 94.9 ms                                                      | 91.0 ms: 1.04x faster                                                    |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                     |
| async_tree_io              | 876 ms                                                       | 849 ms: 1.03x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 620 ms: 1.03x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 649 ms: 1.03x faster                                                     |
| asyncio_websockets         | 520 ms                                                       | 518 ms: 1.00x faster                                                     |
| gc_traversal               | 3.14 ms                                                      | 3.17 ms: 1.01x slower                                                    |
| regex_dna                  | 180 ms                                                       | 184 ms: 1.02x slower                                                     |
| sqlite_synth               | 2.21 us                                                      | 2.26 us: 1.02x slower                                                    |
| json                       | 4.93 ms                                                      | 5.04 ms: 1.02x slower                                                    |
| async_tree_memoization     | 461 ms                                                       | 473 ms: 1.03x slower                                                     |
| deepcopy_memo              | 39.1 us                                                      | 40.2 us: 1.03x slower                                                    |
| json_loads                 | 27.0 us                                                      | 28.1 us: 1.04x slower                                                    |
| coroutines                 | 23.6 ms                                                      | 24.8 ms: 1.05x slower                                                    |
| async_tree_none_tg         | 336 ms                                                       | 356 ms: 1.06x slower                                                     |
| pathlib                    | 19.2 ms                                                      | 20.5 ms: 1.07x slower                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 445 ms: 1.07x slower                                                     |
| async_tree_none            | 354 ms                                                       | 389 ms: 1.10x slower                                                     |
| spectral_norm              | 111 ms                                                       | 124 ms: 1.11x slower                                                     |
| deepcopy_reduce            | 3.11 us                                                      | 3.49 us: 1.12x slower                                                    |
| regex_v8                   | 22.7 ms                                                      | 25.5 ms: 1.13x slower                                                    |
| telco                      | 7.82 ms                                                      | 8.81 ms: 1.13x slower                                                    |
| bpe_tokeniser              | 4.45 sec                                                     | 5.01 sec: 1.13x slower                                                   |
| scimark_fft                | 349 ms                                                       | 397 ms: 1.14x slower                                                     |
| xml_etree_generate         | 85.4 ms                                                      | 98.4 ms: 1.15x slower                                                    |
| mdp                        | 2.36 sec                                                     | 2.77 sec: 1.18x slower                                                   |
| docutils                   | 2.62 sec                                                     | 3.10 sec: 1.18x slower                                                   |
| coverage                   | 83.0 ms                                                      | 99.3 ms: 1.20x slower                                                    |
| async_generators           | 377 ms                                                       | 452 ms: 1.20x slower                                                     |
| pylint                     | 317 ms                                                       | 381 ms: 1.20x slower                                                     |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.68 ms: 1.21x slower                                                    |
| nqueens                    | 78.6 ms                                                      | 97.6 ms: 1.24x slower                                                    |
| dulwich_log                | 74.8 ms                                                      | 95.4 ms: 1.27x slower                                                    |
| meteor_contest             | 102 ms                                                       | 130 ms: 1.28x slower                                                     |
| sqlglot_normalize          | 106 ms                                                       | 136 ms: 1.29x slower                                                     |
| typing_runtime_protocols   | 155 us                                                       | 201 us: 1.30x slower                                                     |
| genshi_xml                 | 48.8 ms                                                      | 63.4 ms: 1.30x slower                                                    |
| pprint_safe_repr           | 738 ms                                                       | 964 ms: 1.31x slower                                                     |
| sqlglot_optimize           | 52.7 ms                                                      | 68.9 ms: 1.31x slower                                                    |
| xml_etree_process          | 59.3 ms                                                      | 78.3 ms: 1.32x slower                                                    |
| generators                 | 28.8 ms                                                      | 38.4 ms: 1.33x slower                                                    |
| pprint_pformat             | 1.50 sec                                                     | 2.00 sec: 1.34x slower                                                   |
| tomli_loads                | 2.01 sec                                                     | 2.69 sec: 1.34x slower                                                   |
| json_dumps                 | 10.5 ms                                                      | 14.2 ms: 1.34x slower                                                    |
| regex_compile              | 132 ms                                                       | 179 ms: 1.35x slower                                                     |
| create_gc_cycles           | 1.34 ms                                                      | 1.81 ms: 1.35x slower                                                    |
| fannkuch                   | 370 ms                                                       | 504 ms: 1.36x slower                                                     |
| crypto_pyaes               | 67.9 ms                                                      | 92.5 ms: 1.36x slower                                                    |
| pycparser                  | 1.12 sec                                                     | 1.53 sec: 1.37x slower                                                   |
| scimark_lu                 | 113 ms                                                       | 155 ms: 1.37x slower                                                     |
| python_startup_no_site     | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                    |
| 2to3                       | 260 ms                                                       | 366 ms: 1.41x slower                                                     |
| genshi_text                | 21.5 ms                                                      | 31.4 ms: 1.46x slower                                                    |
| html5lib                   | 67.0 ms                                                      | 98.1 ms: 1.46x slower                                                    |
| sympy_integrate            | 19.8 ms                                                      | 29.4 ms: 1.48x slower                                                    |
| django_template            | 34.1 ms                                                      | 50.7 ms: 1.49x slower                                                    |
| thrift                     | 778 us                                                       | 1.16 ms: 1.50x slower                                                    |
| nbody                      | 85.1 ms                                                      | 130 ms: 1.53x slower                                                     |
| pyflate                    | 449 ms                                                       | 693 ms: 1.54x slower                                                     |
| mako                       | 11.3 ms                                                      | 17.8 ms: 1.57x slower                                                    |
| python_startup             | 11.0 ms                                                      | 17.4 ms: 1.59x slower                                                    |
| unpickle_pure_python       | 210 us                                                       | 339 us: 1.61x slower                                                     |
| hexiom                     | 5.99 ms                                                      | 9.75 ms: 1.63x slower                                                    |
| comprehensions             | 16.5 us                                                      | 27.1 us: 1.65x slower                                                    |
| scimark_sor                | 134 ms                                                       | 226 ms: 1.68x slower                                                     |
| richards                   | 45.2 ms                                                      | 76.5 ms: 1.69x slower                                                    |
| richards_super             | 51.6 ms                                                      | 88.8 ms: 1.72x slower                                                    |
| sympy_str                  | 275 ms                                                       | 475 ms: 1.73x slower                                                     |
| pickle_pure_python         | 294 us                                                       | 516 us: 1.75x slower                                                     |
| logging_simple             | 6.16 us                                                      | 10.8 us: 1.76x slower                                                    |
| logging_format             | 6.84 us                                                      | 12.1 us: 1.76x slower                                                    |
| float                      | 77.5 ms                                                      | 138 ms: 1.79x slower                                                     |
| scimark_monte_carlo        | 65.4 ms                                                      | 118 ms: 1.81x slower                                                     |
| chaos                      | 57.3 ms                                                      | 104 ms: 1.81x slower                                                     |
| logging_silent             | 103 ns                                                       | 189 ns: 1.84x slower                                                     |
| sqlglot_transpile          | 1.56 ms                                                      | 2.96 ms: 1.90x slower                                                    |
| go                         | 141 ms                                                       | 269 ms: 1.91x slower                                                     |
| sqlglot_parse              | 1.25 ms                                                      | 2.55 ms: 2.04x slower                                                    |
| sympy_expand               | 457 ms                                                       | 953 ms: 2.09x slower                                                     |
| raytrace                   | 253 ms                                                       | 549 ms: 2.17x slower                                                     |
| sympy_sum                  | 156 ms                                                       | 350 ms: 2.25x slower                                                     |
| deltablue                  | 3.12 ms                                                      | 8.02 ms: 2.57x slower                                                    |
| bench_thread_pool          | 919 us                                                       | 3.43 ms: 3.73x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                      | 109 ms: 9.89x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.38x slower                                                             |
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241218-3.14.0a2+-6ef74ac-NOGIL/bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.247x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.23x
- 95% likely to have a slowdown of 1.20x
- 99% likely to have a slowdown of 1.18x

# Memory
- memory change: 1.31x