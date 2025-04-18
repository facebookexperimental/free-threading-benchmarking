# Results vs. 3.13.0rc2

- fork: Yhg1s
- ref: optimise_recursive_c
- machine: linux-x86_64
- commit hash: b28153d
- commit date: 2024-12-20
- overall geometric mean: 1.195x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 350 ms: 1.35x slower                                                  |
| docutils       | 2.62 sec                                                     | 3.00 sec: 1.15x slower                                                |
| html5lib       | 67.0 ms                                                      | 90.2 ms: 1.35x slower                                                 |
| Geometric mean | (ref)                                                        | 1.28x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 737 ms: 1.24x faster                                                  |
| async_tree_io              | 876 ms                                                       | 756 ms: 1.16x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 575 ms: 1.11x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 601 ms: 1.11x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 429 ms: 1.08x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 318 ms: 1.06x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 403 ms: 1.03x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 24.2 ms: 1.03x slower                                                 |
| async_generators           | 377 ms                                                       | 446 ms: 1.18x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                          |

Benchmark hidden because not significant (2): async_tree_none, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 181 ms: 1.20x faster                                                  |
| float          | 77.5 ms                                                      | 112 ms: 1.44x slower                                                  |
| nbody          | 85.1 ms                                                      | 133 ms: 1.56x slower                                                  |
| Geometric mean | (ref)                                                        | 1.23x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.89 ms: 1.07x faster                                                 |
| regex_dna      | 180 ms                                                       | 179 ms: 1.01x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 24.9 ms: 1.10x slower                                                 |
| regex_compile  | 132 ms                                                       | 169 ms: 1.28x slower                                                  |
| Geometric mean | (ref)                                                        | 1.07x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 90.1 ms: 1.05x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                                  |
| json_loads           | 27.0 us                                                      | 28.1 us: 1.04x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 97.0 ms: 1.14x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 73.0 ms: 1.23x slower                                                 |
| tomli_loads          | 2.01 sec                                                     | 2.52 sec: 1.26x slower                                                |
| json_dumps           | 10.5 ms                                                      | 14.0 ms: 1.32x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 330 us: 1.57x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 499 us: 1.69x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.22x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.79 ms: 1.32x slower                                                 |
| python_startup         | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 63.6 ms: 1.30x slower                                                 |
| genshi_text     | 21.5 ms                                                      | 30.6 ms: 1.42x slower                                                 |
| django_template | 34.1 ms                                                      | 48.6 ms: 1.42x slower                                                 |
| mako            | 11.3 ms                                                      | 17.0 ms: 1.50x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.41x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 737 ms: 1.24x faster                                                  |
| pidigits                   | 217 ms                                                       | 181 ms: 1.20x faster                                                  |
| async_tree_io              | 876 ms                                                       | 756 ms: 1.16x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 575 ms: 1.11x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 601 ms: 1.11x faster                                                  |
| deepcopy                   | 355 us                                                       | 323 us: 1.10x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 429 ms: 1.08x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.89 ms: 1.07x faster                                                 |
| async_tree_none_tg         | 336 ms                                                       | 318 ms: 1.06x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.1 ms: 1.05x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.05x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.12 us: 1.04x faster                                                 |
| async_tree_memoization_tg  | 414 ms                                                       | 403 ms: 1.03x faster                                                  |
| regex_dna                  | 180 ms                                                       | 179 ms: 1.01x faster                                                  |
| json                       | 4.93 ms                                                      | 4.98 ms: 1.01x slower                                                 |
| pathlib                    | 19.2 ms                                                      | 19.5 ms: 1.02x slower                                                 |
| coroutines                 | 23.6 ms                                                      | 24.2 ms: 1.03x slower                                                 |
| deepcopy_memo              | 39.1 us                                                      | 40.6 us: 1.04x slower                                                 |
| json_loads                 | 27.0 us                                                      | 28.1 us: 1.04x slower                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 3.38 us: 1.09x slower                                                 |
| scimark_fft                | 349 ms                                                       | 379 ms: 1.09x slower                                                  |
| regex_v8                   | 22.7 ms                                                      | 24.9 ms: 1.10x slower                                                 |
| pylint                     | 317 ms                                                       | 349 ms: 1.10x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 3.51 ms: 1.12x slower                                                 |
| telco                      | 7.82 ms                                                      | 8.82 ms: 1.13x slower                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 5.02 sec: 1.13x slower                                                |
| xml_etree_generate         | 85.4 ms                                                      | 97.0 ms: 1.14x slower                                                 |
| docutils                   | 2.62 sec                                                     | 3.00 sec: 1.15x slower                                                |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.53 ms: 1.18x slower                                                 |
| async_generators           | 377 ms                                                       | 446 ms: 1.18x slower                                                  |
| mdp                        | 2.36 sec                                                     | 2.81 sec: 1.19x slower                                                |
| coverage                   | 83.0 ms                                                      | 99.3 ms: 1.20x slower                                                 |
| dulwich_log                | 74.8 ms                                                      | 90.7 ms: 1.21x slower                                                 |
| xml_etree_process          | 59.3 ms                                                      | 73.0 ms: 1.23x slower                                                 |
| pycparser                  | 1.12 sec                                                     | 1.39 sec: 1.24x slower                                                |
| sqlglot_optimize           | 52.7 ms                                                      | 65.9 ms: 1.25x slower                                                 |
| tomli_loads                | 2.01 sec                                                     | 2.52 sec: 1.26x slower                                                |
| sympy_sum                  | 156 ms                                                       | 195 ms: 1.26x slower                                                  |
| sqlglot_normalize          | 106 ms                                                       | 133 ms: 1.26x slower                                                  |
| nqueens                    | 78.6 ms                                                      | 99.1 ms: 1.26x slower                                                 |
| thrift                     | 778 us                                                       | 990 us: 1.27x slower                                                  |
| regex_compile              | 132 ms                                                       | 169 ms: 1.28x slower                                                  |
| sympy_integrate            | 19.8 ms                                                      | 25.3 ms: 1.28x slower                                                 |
| sympy_expand               | 457 ms                                                       | 591 ms: 1.29x slower                                                  |
| meteor_contest             | 102 ms                                                       | 131 ms: 1.29x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 63.6 ms: 1.30x slower                                                 |
| pprint_safe_repr           | 738 ms                                                       | 963 ms: 1.31x slower                                                  |
| sympy_str                  | 275 ms                                                       | 359 ms: 1.31x slower                                                  |
| generators                 | 28.8 ms                                                      | 37.7 ms: 1.31x slower                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 89.7 ms: 1.32x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 9.79 ms: 1.32x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 14.0 ms: 1.32x slower                                                 |
| fannkuch                   | 370 ms                                                       | 493 ms: 1.33x slower                                                  |
| pprint_pformat             | 1.50 sec                                                     | 2.00 sec: 1.34x slower                                                |
| typing_runtime_protocols   | 155 us                                                       | 207 us: 1.34x slower                                                  |
| 2to3                       | 260 ms                                                       | 350 ms: 1.35x slower                                                  |
| html5lib                   | 67.0 ms                                                      | 90.2 ms: 1.35x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.84 ms: 1.38x slower                                                 |
| scimark_lu                 | 113 ms                                                       | 155 ms: 1.38x slower                                                  |
| genshi_text                | 21.5 ms                                                      | 30.6 ms: 1.42x slower                                                 |
| django_template            | 34.1 ms                                                      | 48.6 ms: 1.42x slower                                                 |
| python_startup             | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                 |
| float                      | 77.5 ms                                                      | 112 ms: 1.44x slower                                                  |
| pyflate                    | 449 ms                                                       | 648 ms: 1.44x slower                                                  |
| richards_super             | 51.6 ms                                                      | 74.7 ms: 1.45x slower                                                 |
| richards                   | 45.2 ms                                                      | 66.6 ms: 1.47x slower                                                 |
| logging_simple             | 6.16 us                                                      | 9.10 us: 1.48x slower                                                 |
| logging_format             | 6.84 us                                                      | 10.2 us: 1.49x slower                                                 |
| mako                       | 11.3 ms                                                      | 17.0 ms: 1.50x slower                                                 |
| nbody                      | 85.1 ms                                                      | 133 ms: 1.56x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 330 us: 1.57x slower                                                  |
| hexiom                     | 5.99 ms                                                      | 9.52 ms: 1.59x slower                                                 |
| scimark_sor                | 134 ms                                                       | 214 ms: 1.59x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 105 ms: 1.61x slower                                                  |
| chaos                      | 57.3 ms                                                      | 93.9 ms: 1.64x slower                                                 |
| comprehensions             | 16.5 us                                                      | 27.3 us: 1.66x slower                                                 |
| go                         | 141 ms                                                       | 236 ms: 1.68x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 499 us: 1.69x slower                                                  |
| sqlglot_transpile          | 1.56 ms                                                      | 2.69 ms: 1.73x slower                                                 |
| logging_silent             | 103 ns                                                       | 180 ns: 1.76x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 2.34 ms: 1.88x slower                                                 |
| raytrace                   | 253 ms                                                       | 483 ms: 1.91x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 7.31 ms: 2.34x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 3.39 ms: 3.69x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 100 ms: 9.11x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.29x slower                                                          |

Benchmark hidden because not significant (3): async_tree_none, asyncio_websockets, spectral_norm
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241220-3.14.0a3+-b28153d-NOGIL/bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.195x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.19x
- 95% likely to have a slowdown of 1.18x
- 99% likely to have a slowdown of 1.15x

# Memory
- memory change: 1.31x