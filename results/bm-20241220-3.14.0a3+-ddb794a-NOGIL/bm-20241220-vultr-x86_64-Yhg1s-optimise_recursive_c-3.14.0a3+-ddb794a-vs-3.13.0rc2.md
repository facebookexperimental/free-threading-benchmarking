# Results vs. 3.13.0rc2

- fork: Yhg1s
- ref: optimise_recursive_c
- machine: linux-x86_64
- commit hash: ddb794a
- commit date: 2024-12-20
- overall geometric mean: 1.212x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-ddb794a |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 358 ms: 1.38x slower                                                  |
| docutils       | 2.62 sec                                                     | 3.05 sec: 1.16x slower                                                |
| html5lib       | 67.0 ms                                                      | 94.1 ms: 1.40x slower                                                 |
| Geometric mean | (ref)                                                        | 1.31x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-ddb794a |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 751 ms: 1.22x faster                                                  |
| async_tree_io              | 876 ms                                                       | 774 ms: 1.13x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 573 ms: 1.11x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 602 ms: 1.11x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 436 ms: 1.06x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 322 ms: 1.04x faster                                                  |
| async_tree_none            | 354 ms                                                       | 359 ms: 1.02x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 25.5 ms: 1.08x slower                                                 |
| async_generators           | 377 ms                                                       | 462 ms: 1.22x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.03x faster                                                          |

Benchmark hidden because not significant (2): async_tree_memoization_tg, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-ddb794a |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 181 ms: 1.20x faster                                                  |
| float          | 77.5 ms                                                      | 114 ms: 1.47x slower                                                  |
| nbody          | 85.1 ms                                                      | 133 ms: 1.57x slower                                                  |
| Geometric mean | (ref)                                                        | 1.24x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-ddb794a |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.91 ms: 1.06x faster                                                 |
| regex_dna      | 180 ms                                                       | 188 ms: 1.04x slower                                                  |
| regex_v8       | 22.7 ms                                                      | 25.0 ms: 1.10x slower                                                 |
| regex_compile  | 132 ms                                                       | 172 ms: 1.30x slower                                                  |
| Geometric mean | (ref)                                                        | 1.09x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-ddb794a |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 91.7 ms: 1.04x faster                                                 |
| json_loads           | 27.0 us                                                      | 28.3 us: 1.05x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 98.4 ms: 1.15x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 75.4 ms: 1.27x slower                                                 |
| tomli_loads          | 2.01 sec                                                     | 2.59 sec: 1.29x slower                                                |
| json_dumps           | 10.5 ms                                                      | 14.3 ms: 1.36x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 339 us: 1.61x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 511 us: 1.74x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.24x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-ddb794a |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.83 ms: 1.33x slower                                                 |
| python_startup         | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.38x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-ddb794a |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 64.5 ms: 1.32x slower                                                 |
| genshi_text     | 21.5 ms                                                      | 31.5 ms: 1.46x slower                                                 |
| django_template | 34.1 ms                                                      | 51.1 ms: 1.50x slower                                                 |
| mako            | 11.3 ms                                                      | 17.5 ms: 1.54x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.45x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-ddb794a |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 751 ms: 1.22x faster                                                  |
| pidigits                   | 217 ms                                                       | 181 ms: 1.20x faster                                                  |
| async_tree_io              | 876 ms                                                       | 774 ms: 1.13x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 573 ms: 1.11x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 602 ms: 1.11x faster                                                  |
| deepcopy                   | 355 us                                                       | 329 us: 1.08x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.91 ms: 1.06x faster                                                 |
| async_tree_memoization     | 461 ms                                                       | 436 ms: 1.06x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.05x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 322 ms: 1.04x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 91.7 ms: 1.04x faster                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.16 us: 1.02x faster                                                 |
| async_tree_none            | 354 ms                                                       | 359 ms: 1.02x slower                                                  |
| json                       | 4.93 ms                                                      | 5.02 ms: 1.02x slower                                                 |
| pathlib                    | 19.2 ms                                                      | 19.8 ms: 1.03x slower                                                 |
| regex_dna                  | 180 ms                                                       | 188 ms: 1.04x slower                                                  |
| json_loads                 | 27.0 us                                                      | 28.3 us: 1.05x slower                                                 |
| deepcopy_memo              | 39.1 us                                                      | 41.2 us: 1.05x slower                                                 |
| coroutines                 | 23.6 ms                                                      | 25.5 ms: 1.08x slower                                                 |
| spectral_norm              | 111 ms                                                       | 122 ms: 1.10x slower                                                  |
| regex_v8                   | 22.7 ms                                                      | 25.0 ms: 1.10x slower                                                 |
| scimark_fft                | 349 ms                                                       | 386 ms: 1.10x slower                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 3.46 us: 1.11x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 3.51 ms: 1.12x slower                                                 |
| telco                      | 7.82 ms                                                      | 8.76 ms: 1.12x slower                                                 |
| pylint                     | 317 ms                                                       | 356 ms: 1.12x slower                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 5.07 sec: 1.14x slower                                                |
| xml_etree_generate         | 85.4 ms                                                      | 98.4 ms: 1.15x slower                                                 |
| docutils                   | 2.62 sec                                                     | 3.05 sec: 1.16x slower                                                |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.58 ms: 1.19x slower                                                 |
| coverage                   | 83.0 ms                                                      | 101 ms: 1.22x slower                                                  |
| async_generators           | 377 ms                                                       | 462 ms: 1.22x slower                                                  |
| dulwich_log                | 74.8 ms                                                      | 91.8 ms: 1.23x slower                                                 |
| mdp                        | 2.36 sec                                                     | 2.90 sec: 1.23x slower                                                |
| pycparser                  | 1.12 sec                                                     | 1.39 sec: 1.25x slower                                                |
| xml_etree_process          | 59.3 ms                                                      | 75.4 ms: 1.27x slower                                                 |
| sqlglot_optimize           | 52.7 ms                                                      | 67.1 ms: 1.27x slower                                                 |
| meteor_contest             | 102 ms                                                       | 130 ms: 1.28x slower                                                  |
| thrift                     | 778 us                                                       | 998 us: 1.28x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 200 ms: 1.28x slower                                                  |
| nqueens                    | 78.6 ms                                                      | 101 ms: 1.28x slower                                                  |
| tomli_loads                | 2.01 sec                                                     | 2.59 sec: 1.29x slower                                                |
| sympy_integrate            | 19.8 ms                                                      | 25.7 ms: 1.30x slower                                                 |
| sqlglot_normalize          | 106 ms                                                       | 137 ms: 1.30x slower                                                  |
| regex_compile              | 132 ms                                                       | 172 ms: 1.30x slower                                                  |
| sympy_expand               | 457 ms                                                       | 595 ms: 1.30x slower                                                  |
| pprint_safe_repr           | 738 ms                                                       | 975 ms: 1.32x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 64.5 ms: 1.32x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 9.83 ms: 1.33x slower                                                 |
| sympy_str                  | 275 ms                                                       | 365 ms: 1.33x slower                                                  |
| fannkuch                   | 370 ms                                                       | 497 ms: 1.34x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 209 us: 1.35x slower                                                  |
| pprint_pformat             | 1.50 sec                                                     | 2.03 sec: 1.36x slower                                                |
| json_dumps                 | 10.5 ms                                                      | 14.3 ms: 1.36x slower                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 92.4 ms: 1.36x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.83 ms: 1.37x slower                                                 |
| 2to3                       | 260 ms                                                       | 358 ms: 1.38x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 158 ms: 1.40x slower                                                  |
| html5lib                   | 67.0 ms                                                      | 94.1 ms: 1.40x slower                                                 |
| python_startup             | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                 |
| pyflate                    | 449 ms                                                       | 653 ms: 1.46x slower                                                  |
| genshi_text                | 21.5 ms                                                      | 31.5 ms: 1.46x slower                                                 |
| generators                 | 28.8 ms                                                      | 42.3 ms: 1.47x slower                                                 |
| float                      | 77.5 ms                                                      | 114 ms: 1.47x slower                                                  |
| logging_simple             | 6.16 us                                                      | 9.18 us: 1.49x slower                                                 |
| django_template            | 34.1 ms                                                      | 51.1 ms: 1.50x slower                                                 |
| richards_super             | 51.6 ms                                                      | 78.5 ms: 1.52x slower                                                 |
| logging_format             | 6.84 us                                                      | 10.4 us: 1.53x slower                                                 |
| richards                   | 45.2 ms                                                      | 69.8 ms: 1.54x slower                                                 |
| mako                       | 11.3 ms                                                      | 17.5 ms: 1.54x slower                                                 |
| nbody                      | 85.1 ms                                                      | 133 ms: 1.57x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 339 us: 1.61x slower                                                  |
| scimark_sor                | 134 ms                                                       | 220 ms: 1.64x slower                                                  |
| hexiom                     | 5.99 ms                                                      | 9.85 ms: 1.64x slower                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 107 ms: 1.64x slower                                                  |
| chaos                      | 57.3 ms                                                      | 97.2 ms: 1.70x slower                                                 |
| comprehensions             | 16.5 us                                                      | 28.2 us: 1.71x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 511 us: 1.74x slower                                                  |
| go                         | 141 ms                                                       | 247 ms: 1.75x slower                                                  |
| sqlglot_transpile          | 1.56 ms                                                      | 2.75 ms: 1.77x slower                                                 |
| logging_silent             | 103 ns                                                       | 189 ns: 1.84x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 2.39 ms: 1.91x slower                                                 |
| raytrace                   | 253 ms                                                       | 503 ms: 1.99x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 7.73 ms: 2.47x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 3.40 ms: 3.70x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 101 ms: 9.17x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.32x slower                                                          |

Benchmark hidden because not significant (2): async_tree_memoization_tg, asyncio_websockets
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241220-3.14.0a3+-ddb794a-NOGIL/bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-ddb794a.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.212x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.22x
- 95% likely to have a slowdown of 1.21x
- 99% likely to have a slowdown of 1.16x

# Memory
- memory change: 1.32x