# Results vs. 3.13.0rc2

- fork: python
- ref: bfb0788bfcaab7474c1b
- machine: linux-x86_64
- commit hash: bfb0788
- commit date: 2024-12-03
- overall geometric mean: 1.021x faster
- HPT reliability: 70.24%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 259 ms: 1.00x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.58 sec: 1.01x faster                                                 |
| Geometric mean | (ref)                                                        | 1.01x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 629 ms: 1.45x faster                                                   |
| async_tree_io              | 876 ms                                                       | 629 ms: 1.39x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 341 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 503 ms: 1.32x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 314 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 487 ms: 1.31x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 264 ms: 1.27x faster                                                   |
| async_tree_none            | 354 ms                                                       | 278 ms: 1.27x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 22.5 ms: 1.05x faster                                                  |
| async_generators           | 377 ms                                                       | 366 ms: 1.03x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.00x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.24x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 185 ms: 1.17x faster                                                   |
| float          | 77.5 ms                                                      | 79.2 ms: 1.02x slower                                                  |
| nbody          | 85.1 ms                                                      | 95.5 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                        | 1.01x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.79 ms: 1.11x faster                                                  |
| regex_dna      | 180 ms                                                       | 171 ms: 1.05x faster                                                   |
| regex_compile  | 132 ms                                                       | 131 ms: 1.01x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 23.7 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_loads           | 27.0 us                                                      | 25.4 us: 1.06x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                                   |
| xml_etree_iterparse  | 94.9 ms                                                      | 92.3 ms: 1.03x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 85.8 ms: 1.00x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 60.1 ms: 1.01x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.10 sec: 1.05x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 222 us: 1.06x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 11.4 ms: 1.08x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 322 us: 1.09x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.02x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.50 ms: 1.01x slower                                                  |
| python_startup         | 11.0 ms                                                      | 14.7 ms: 1.33x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.16x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 22.1 ms: 1.02x slower                                                  |
| mako            | 11.3 ms                                                      | 11.6 ms: 1.03x slower                                                  |
| genshi_xml      | 48.8 ms                                                      | 50.5 ms: 1.04x slower                                                  |
| django_template | 34.1 ms                                                      | 36.3 ms: 1.06x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.04x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 629 ms: 1.45x faster                                                   |
| async_tree_io              | 876 ms                                                       | 629 ms: 1.39x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 341 ms: 1.35x faster                                                   |
| deepcopy                   | 355 us                                                       | 266 us: 1.34x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 503 ms: 1.32x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 314 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 487 ms: 1.31x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 264 ms: 1.27x faster                                                   |
| async_tree_none            | 354 ms                                                       | 278 ms: 1.27x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 31.1 us: 1.26x faster                                                  |
| pidigits                   | 217 ms                                                       | 185 ms: 1.17x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.68 us: 1.16x faster                                                  |
| go                         | 141 ms                                                       | 124 ms: 1.14x faster                                                   |
| pylint                     | 317 ms                                                       | 285 ms: 1.11x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.79 ms: 1.11x faster                                                  |
| json                       | 4.93 ms                                                      | 4.56 ms: 1.08x faster                                                  |
| json_loads                 | 27.0 us                                                      | 25.4 us: 1.06x faster                                                  |
| telco                      | 7.82 ms                                                      | 7.37 ms: 1.06x faster                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.47 ms: 1.05x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 18.2 ms: 1.05x faster                                                  |
| regex_dna                  | 180 ms                                                       | 171 ms: 1.05x faster                                                   |
| coverage                   | 83.0 ms                                                      | 78.9 ms: 1.05x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.05x faster                                                   |
| thrift                     | 778 us                                                       | 744 us: 1.05x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 22.5 ms: 1.05x faster                                                  |
| scimark_fft                | 349 ms                                                       | 338 ms: 1.03x faster                                                   |
| async_generators           | 377 ms                                                       | 366 ms: 1.03x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 92.3 ms: 1.03x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.34 sec: 1.03x faster                                                 |
| docutils                   | 2.62 sec                                                     | 2.58 sec: 1.01x faster                                                 |
| meteor_contest             | 102 ms                                                       | 100 ms: 1.01x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.48 sec: 1.01x faster                                                 |
| regex_compile              | 132 ms                                                       | 131 ms: 1.01x faster                                                   |
| pprint_safe_repr           | 738 ms                                                       | 729 ms: 1.01x faster                                                   |
| sympy_sum                  | 156 ms                                                       | 154 ms: 1.01x faster                                                   |
| mdp                        | 2.36 sec                                                     | 2.34 sec: 1.00x faster                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 67.6 ms: 1.00x faster                                                  |
| 2to3                       | 260 ms                                                       | 259 ms: 1.00x faster                                                   |
| xml_etree_generate         | 85.4 ms                                                      | 85.8 ms: 1.00x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.00x slower                                                   |
| sympy_str                  | 275 ms                                                       | 277 ms: 1.01x slower                                                   |
| generators                 | 28.8 ms                                                      | 29.1 ms: 1.01x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.13 sec: 1.01x slower                                                 |
| xml_etree_process          | 59.3 ms                                                      | 60.1 ms: 1.01x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 114 ms: 1.01x slower                                                   |
| python_startup_no_site     | 7.39 ms                                                      | 7.50 ms: 1.01x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 66.4 ms: 1.02x slower                                                  |
| sqlglot_normalize          | 106 ms                                                       | 107 ms: 1.02x slower                                                   |
| nqueens                    | 78.6 ms                                                      | 79.8 ms: 1.02x slower                                                  |
| spectral_norm              | 111 ms                                                       | 113 ms: 1.02x slower                                                   |
| sympy_integrate            | 19.8 ms                                                      | 20.2 ms: 1.02x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 157 us: 1.02x slower                                                   |
| pyflate                    | 449 ms                                                       | 457 ms: 1.02x slower                                                   |
| hexiom                     | 5.99 ms                                                      | 6.10 ms: 1.02x slower                                                  |
| dulwich_log                | 74.8 ms                                                      | 76.2 ms: 1.02x slower                                                  |
| sympy_expand               | 457 ms                                                       | 466 ms: 1.02x slower                                                   |
| fannkuch                   | 370 ms                                                       | 378 ms: 1.02x slower                                                   |
| float                      | 77.5 ms                                                      | 79.2 ms: 1.02x slower                                                  |
| scimark_sor                | 134 ms                                                       | 137 ms: 1.02x slower                                                   |
| genshi_text                | 21.5 ms                                                      | 22.1 ms: 1.02x slower                                                  |
| sqlglot_optimize           | 52.7 ms                                                      | 54.1 ms: 1.03x slower                                                  |
| mako                       | 11.3 ms                                                      | 11.6 ms: 1.03x slower                                                  |
| logging_simple             | 6.16 us                                                      | 6.36 us: 1.03x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 50.5 ms: 1.04x slower                                                  |
| logging_format             | 6.84 us                                                      | 7.12 us: 1.04x slower                                                  |
| regex_v8                   | 22.7 ms                                                      | 23.7 ms: 1.04x slower                                                  |
| richards_super             | 51.6 ms                                                      | 54.0 ms: 1.05x slower                                                  |
| chaos                      | 57.3 ms                                                      | 60.0 ms: 1.05x slower                                                  |
| tomli_loads                | 2.01 sec                                                     | 2.10 sec: 1.05x slower                                                 |
| sqlglot_transpile          | 1.56 ms                                                      | 1.64 ms: 1.05x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 1.32 ms: 1.06x slower                                                  |
| richards                   | 45.2 ms                                                      | 47.9 ms: 1.06x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 222 us: 1.06x slower                                                   |
| django_template            | 34.1 ms                                                      | 36.3 ms: 1.06x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.36 ms: 1.08x slower                                                  |
| raytrace                   | 253 ms                                                       | 272 ms: 1.08x slower                                                   |
| comprehensions             | 16.5 us                                                      | 17.8 us: 1.08x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 11.4 ms: 1.08x slower                                                  |
| logging_silent             | 103 ns                                                       | 112 ns: 1.09x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 322 us: 1.09x slower                                                   |
| bench_thread_pool          | 919 us                                                       | 1.02 ms: 1.11x slower                                                  |
| nbody                      | 85.1 ms                                                      | 95.5 ms: 1.12x slower                                                  |
| python_startup             | 11.0 ms                                                      | 14.7 ms: 1.33x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.82 ms: 1.36x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.28 ms: 1.36x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 89.6 ms: 8.15x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (1): sqlite_synth
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241203-3.14.0a2+-bfb0788/bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.021x faster

# HPT report

- Reliability score: 70.24% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.09x