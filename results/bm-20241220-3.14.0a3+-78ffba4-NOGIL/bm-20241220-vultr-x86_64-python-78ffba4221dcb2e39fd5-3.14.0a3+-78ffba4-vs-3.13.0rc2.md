# Results vs. 3.13.0rc2

- fork: python
- ref: 78ffba4221dcb2e39fd5
- machine: linux-x86_64
- commit hash: 78ffba4
- commit date: 2024-12-20
- overall geometric mean: 1.217x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 359 ms: 1.38x slower                                                   |
| docutils       | 2.62 sec                                                     | 3.02 sec: 1.15x slower                                                 |
| html5lib       | 67.0 ms                                                      | 93.4 ms: 1.39x slower                                                  |
| Geometric mean | (ref)                                                        | 1.30x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 729 ms: 1.25x faster                                                   |
| async_tree_io              | 876 ms                                                       | 753 ms: 1.16x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 311 ms: 1.08x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 428 ms: 1.08x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 600 ms: 1.06x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 631 ms: 1.06x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 400 ms: 1.04x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 25.2 ms: 1.07x slower                                                  |
| async_generators           | 377 ms                                                       | 446 ms: 1.18x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                           |

Benchmark hidden because not significant (2): async_tree_none, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 197 ms: 1.10x faster                                                   |
| float          | 77.5 ms                                                      | 113 ms: 1.45x slower                                                   |
| nbody          | 85.1 ms                                                      | 131 ms: 1.54x slower                                                   |
| Geometric mean | (ref)                                                        | 1.27x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.79 ms: 1.11x faster                                                  |
| regex_dna      | 180 ms                                                       | 186 ms: 1.03x slower                                                   |
| regex_v8       | 22.7 ms                                                      | 24.9 ms: 1.10x slower                                                  |
| regex_compile  | 132 ms                                                       | 168 ms: 1.27x slower                                                   |
| Geometric mean | (ref)                                                        | 1.07x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 90.2 ms: 1.05x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                                   |
| json_loads           | 27.0 us                                                      | 28.4 us: 1.05x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 96.9 ms: 1.13x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 73.0 ms: 1.23x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.54 sec: 1.27x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 14.1 ms: 1.34x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 328 us: 1.56x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 506 us: 1.72x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.22x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.2 ms: 1.39x slower                                                  |
| python_startup         | 11.0 ms                                                      | 17.2 ms: 1.57x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.47x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 63.8 ms: 1.31x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 30.9 ms: 1.44x slower                                                  |
| django_template | 34.1 ms                                                      | 50.7 ms: 1.49x slower                                                  |
| mako            | 11.3 ms                                                      | 17.3 ms: 1.52x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.44x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 729 ms: 1.25x faster                                                   |
| async_tree_io              | 876 ms                                                       | 753 ms: 1.16x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.79 ms: 1.11x faster                                                  |
| pidigits                   | 217 ms                                                       | 197 ms: 1.10x faster                                                   |
| deepcopy                   | 355 us                                                       | 325 us: 1.10x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 311 ms: 1.08x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 428 ms: 1.08x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 600 ms: 1.06x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 631 ms: 1.06x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.2 ms: 1.05x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.05x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 400 ms: 1.04x faster                                                   |
| sqlite_synth               | 2.21 us                                                      | 2.15 us: 1.03x faster                                                  |
| gc_traversal               | 3.14 ms                                                      | 3.16 ms: 1.01x slower                                                  |
| json                       | 4.93 ms                                                      | 5.06 ms: 1.03x slower                                                  |
| regex_dna                  | 180 ms                                                       | 186 ms: 1.03x slower                                                   |
| deepcopy_memo              | 39.1 us                                                      | 40.6 us: 1.04x slower                                                  |
| pathlib                    | 19.2 ms                                                      | 20.0 ms: 1.04x slower                                                  |
| spectral_norm              | 111 ms                                                       | 117 ms: 1.05x slower                                                   |
| json_loads                 | 27.0 us                                                      | 28.4 us: 1.05x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 25.2 ms: 1.07x slower                                                  |
| regex_v8                   | 22.7 ms                                                      | 24.9 ms: 1.10x slower                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 3.43 us: 1.10x slower                                                  |
| scimark_fft                | 349 ms                                                       | 386 ms: 1.11x slower                                                   |
| telco                      | 7.82 ms                                                      | 8.74 ms: 1.12x slower                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 5.04 sec: 1.13x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 96.9 ms: 1.13x slower                                                  |
| pylint                     | 317 ms                                                       | 364 ms: 1.15x slower                                                   |
| docutils                   | 2.62 sec                                                     | 3.02 sec: 1.15x slower                                                 |
| async_generators           | 377 ms                                                       | 446 ms: 1.18x slower                                                   |
| coverage                   | 83.0 ms                                                      | 99.4 ms: 1.20x slower                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.64 ms: 1.20x slower                                                  |
| dulwich_log                | 74.8 ms                                                      | 90.5 ms: 1.21x slower                                                  |
| mdp                        | 2.36 sec                                                     | 2.88 sec: 1.22x slower                                                 |
| xml_etree_process          | 59.3 ms                                                      | 73.0 ms: 1.23x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.38 sec: 1.24x slower                                                 |
| sqlglot_optimize           | 52.7 ms                                                      | 65.9 ms: 1.25x slower                                                  |
| meteor_contest             | 102 ms                                                       | 128 ms: 1.26x slower                                                   |
| sqlglot_normalize          | 106 ms                                                       | 134 ms: 1.26x slower                                                   |
| thrift                     | 778 us                                                       | 986 us: 1.27x slower                                                   |
| tomli_loads                | 2.01 sec                                                     | 2.54 sec: 1.27x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 99.7 ms: 1.27x slower                                                  |
| regex_compile              | 132 ms                                                       | 168 ms: 1.27x slower                                                   |
| pprint_safe_repr           | 738 ms                                                       | 961 ms: 1.30x slower                                                   |
| genshi_xml                 | 48.8 ms                                                      | 63.8 ms: 1.31x slower                                                  |
| generators                 | 28.8 ms                                                      | 38.0 ms: 1.32x slower                                                  |
| fannkuch                   | 370 ms                                                       | 488 ms: 1.32x slower                                                   |
| typing_runtime_protocols   | 155 us                                                       | 206 us: 1.33x slower                                                   |
| crypto_pyaes               | 67.9 ms                                                      | 90.7 ms: 1.34x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 14.1 ms: 1.34x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.79 ms: 1.34x slower                                                  |
| pprint_pformat             | 1.50 sec                                                     | 2.01 sec: 1.34x slower                                                 |
| 2to3                       | 260 ms                                                       | 359 ms: 1.38x slower                                                   |
| python_startup_no_site     | 7.39 ms                                                      | 10.2 ms: 1.39x slower                                                  |
| html5lib                   | 67.0 ms                                                      | 93.4 ms: 1.39x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 160 ms: 1.42x slower                                                   |
| genshi_text                | 21.5 ms                                                      | 30.9 ms: 1.44x slower                                                  |
| pyflate                    | 449 ms                                                       | 648 ms: 1.45x slower                                                   |
| float                      | 77.5 ms                                                      | 113 ms: 1.45x slower                                                   |
| logging_format             | 6.84 us                                                      | 10.1 us: 1.48x slower                                                  |
| logging_simple             | 6.16 us                                                      | 9.11 us: 1.48x slower                                                  |
| richards_super             | 51.6 ms                                                      | 76.5 ms: 1.48x slower                                                  |
| django_template            | 34.1 ms                                                      | 50.7 ms: 1.49x slower                                                  |
| sympy_integrate            | 19.8 ms                                                      | 29.5 ms: 1.49x slower                                                  |
| richards                   | 45.2 ms                                                      | 67.6 ms: 1.50x slower                                                  |
| mako                       | 11.3 ms                                                      | 17.3 ms: 1.52x slower                                                  |
| nbody                      | 85.1 ms                                                      | 131 ms: 1.54x slower                                                   |
| unpickle_pure_python       | 210 us                                                       | 328 us: 1.56x slower                                                   |
| python_startup             | 11.0 ms                                                      | 17.2 ms: 1.57x slower                                                  |
| scimark_sor                | 134 ms                                                       | 216 ms: 1.61x slower                                                   |
| hexiom                     | 5.99 ms                                                      | 9.69 ms: 1.62x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 106 ms: 1.63x slower                                                   |
| chaos                      | 57.3 ms                                                      | 94.9 ms: 1.66x slower                                                  |
| comprehensions             | 16.5 us                                                      | 27.6 us: 1.68x slower                                                  |
| go                         | 141 ms                                                       | 241 ms: 1.71x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 506 us: 1.72x slower                                                   |
| sqlglot_transpile          | 1.56 ms                                                      | 2.69 ms: 1.73x slower                                                  |
| sympy_str                  | 275 ms                                                       | 475 ms: 1.73x slower                                                   |
| logging_silent             | 103 ns                                                       | 184 ns: 1.79x slower                                                   |
| sqlglot_parse              | 1.25 ms                                                      | 2.33 ms: 1.87x slower                                                  |
| raytrace                   | 253 ms                                                       | 490 ms: 1.94x slower                                                   |
| sympy_expand               | 457 ms                                                       | 952 ms: 2.08x slower                                                   |
| sympy_sum                  | 156 ms                                                       | 348 ms: 2.24x slower                                                   |
| deltablue                  | 3.12 ms                                                      | 7.53 ms: 2.41x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 3.38 ms: 3.68x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 108 ms: 9.82x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.32x slower                                                           |

Benchmark hidden because not significant (2): async_tree_none, asyncio_websockets
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241220-3.14.0a3+-78ffba4-NOGIL/bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.217x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.21x
- 95% likely to have a slowdown of 1.19x
- 99% likely to have a slowdown of 1.16x

# Memory
- memory change: 1.32x