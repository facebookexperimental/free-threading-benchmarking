# Results vs. 3.13.0rc2

- fork: python
- ref: c3ae5c9e4ad121f8ba60
- machine: linux-x86_64
- commit hash: c3ae5c9
- commit date: 2025-01-31
- overall geometric mean: 1.078x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250131-linux-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 542 ms: 1.22x slower                                                   |
| docutils       | 4.01 sec                                                     | 4.13 sec: 1.03x slower                                                 |
| html5lib       | 92.6 ms                                                      | 104 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                        | 1.12x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250131-linux-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 742 ms: 1.89x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 826 ms: 1.68x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 453 ms: 1.48x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 343 ms: 1.47x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 498 ms: 1.42x faster                                                   |
| async_tree_none            | 572 ms                                                       | 413 ms: 1.38x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 641 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 769 ms: 1.15x faster                                                   |
| coroutines                 | 30.9 ms                                                      | 35.2 ms: 1.14x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.30x faster                                                           |

Benchmark hidden because not significant (2): asyncio_websockets, async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250131-linux-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 103 ms: 1.13x faster                                                   |
| pidigits       | 251 ms                                                       | 235 ms: 1.07x faster                                                   |
| nbody          | 119 ms                                                       | 185 ms: 1.56x slower                                                   |
| Geometric mean | (ref)                                                        | 1.09x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250131-linux-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.42 ms: 1.07x faster                                                  |
| regex_v8       | 32.8 ms                                                      | 34.2 ms: 1.04x slower                                                  |
| regex_dna      | 282 ms                                                       | 308 ms: 1.09x slower                                                   |
| regex_compile  | 182 ms                                                       | 205 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                        | 1.05x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250131-linux-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 164 ms: 1.08x faster                                                   |
| tomli_loads          | 2.78 sec                                                     | 3.27 sec: 1.18x slower                                                 |
| json_loads           | 34.3 us                                                      | 41.9 us: 1.22x slower                                                  |
| unpickle_pure_python | 290 us                                                       | 356 us: 1.23x slower                                                   |
| xml_etree_generate   | 122 ms                                                       | 152 ms: 1.24x slower                                                   |
| json_dumps           | 14.1 ms                                                      | 18.3 ms: 1.29x slower                                                  |
| pickle_pure_python   | 416 us                                                       | 598 us: 1.44x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.16x slower                                                           |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250131-linux-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 21.2 ms: 1.39x slower                                                  |
| python_startup         | 22.4 ms                                                      | 33.3 ms: 1.49x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.44x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250131-linux-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 44.3 ms                                                      | 51.3 ms: 1.16x slower                                                  |
| genshi_xml      | 72.1 ms                                                      | 87.2 ms: 1.21x slower                                                  |
| genshi_text     | 31.7 ms                                                      | 38.4 ms: 1.21x slower                                                  |
| mako            | 15.9 ms                                                      | 24.2 ms: 1.52x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.27x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250131-linux-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 742 ms: 1.89x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 826 ms: 1.68x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 453 ms: 1.48x faster                                                   |
| gc_traversal               | 5.70 ms                                                      | 3.88 ms: 1.47x faster                                                  |
| async_tree_none_tg         | 504 ms                                                       | 343 ms: 1.47x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 498 ms: 1.42x faster                                                   |
| async_tree_none            | 572 ms                                                       | 413 ms: 1.38x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 641 ms: 1.33x faster                                                   |
| deepcopy                   | 498 us                                                       | 415 us: 1.20x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 769 ms: 1.15x faster                                                   |
| float                      | 116 ms                                                       | 103 ms: 1.13x faster                                                   |
| xml_etree_iterparse        | 177 ms                                                       | 164 ms: 1.08x faster                                                   |
| regex_effbot               | 4.74 ms                                                      | 4.42 ms: 1.07x faster                                                  |
| go                         | 191 ms                                                       | 179 ms: 1.07x faster                                                   |
| pidigits                   | 251 ms                                                       | 235 ms: 1.07x faster                                                   |
| sqlite_synth               | 3.99 us                                                      | 3.79 us: 1.05x faster                                                  |
| docutils                   | 4.01 sec                                                     | 4.13 sec: 1.03x slower                                                 |
| regex_v8                   | 32.8 ms                                                      | 34.2 ms: 1.04x slower                                                  |
| spectral_norm              | 157 ms                                                       | 165 ms: 1.05x slower                                                   |
| richards                   | 65.5 ms                                                      | 70.2 ms: 1.07x slower                                                  |
| deepcopy_memo              | 50.1 us                                                      | 54.0 us: 1.08x slower                                                  |
| sqlglot_normalize          | 140 ms                                                       | 151 ms: 1.08x slower                                                   |
| deepcopy_reduce            | 4.10 us                                                      | 4.43 us: 1.08x slower                                                  |
| scimark_sor                | 179 ms                                                       | 194 ms: 1.09x slower                                                   |
| dulwich_log                | 93.7 ms                                                      | 102 ms: 1.09x slower                                                   |
| regex_dna                  | 282 ms                                                       | 308 ms: 1.09x slower                                                   |
| pycparser                  | 1.57 sec                                                     | 1.72 sec: 1.10x slower                                                 |
| generators                 | 40.0 ms                                                      | 44.4 ms: 1.11x slower                                                  |
| sympy_str                  | 379 ms                                                       | 424 ms: 1.12x slower                                                   |
| html5lib                   | 92.6 ms                                                      | 104 ms: 1.12x slower                                                   |
| regex_compile              | 182 ms                                                       | 205 ms: 1.12x slower                                                   |
| sympy_expand               | 601 ms                                                       | 678 ms: 1.13x slower                                                   |
| pprint_safe_repr           | 987 ms                                                       | 1.12 sec: 1.13x slower                                                 |
| sqlglot_transpile          | 2.20 ms                                                      | 2.50 ms: 1.14x slower                                                  |
| coroutines                 | 30.9 ms                                                      | 35.2 ms: 1.14x slower                                                  |
| pprint_pformat             | 1.94 sec                                                     | 2.22 sec: 1.14x slower                                                 |
| mdp                        | 3.80 sec                                                     | 4.39 sec: 1.15x slower                                                 |
| logging_silent             | 130 ns                                                       | 150 ns: 1.16x slower                                                   |
| richards_super             | 73.2 ms                                                      | 84.8 ms: 1.16x slower                                                  |
| django_template            | 44.3 ms                                                      | 51.3 ms: 1.16x slower                                                  |
| sqlglot_optimize           | 74.7 ms                                                      | 86.9 ms: 1.16x slower                                                  |
| pyflate                    | 664 ms                                                       | 777 ms: 1.17x slower                                                   |
| logging_simple             | 8.56 us                                                      | 10.0 us: 1.17x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 2.84 ms: 1.18x slower                                                  |
| tomli_loads                | 2.78 sec                                                     | 3.27 sec: 1.18x slower                                                 |
| bpe_tokeniser              | 6.28 sec                                                     | 7.43 sec: 1.18x slower                                                 |
| json                       | 6.51 ms                                                      | 7.77 ms: 1.19x slower                                                  |
| scimark_fft                | 473 ms                                                       | 565 ms: 1.19x slower                                                   |
| logging_format             | 9.24 us                                                      | 11.1 us: 1.20x slower                                                  |
| sympy_integrate            | 30.2 ms                                                      | 36.2 ms: 1.20x slower                                                  |
| genshi_xml                 | 72.1 ms                                                      | 87.2 ms: 1.21x slower                                                  |
| comprehensions             | 22.2 us                                                      | 27.0 us: 1.21x slower                                                  |
| fannkuch                   | 547 ms                                                       | 664 ms: 1.21x slower                                                   |
| genshi_text                | 31.7 ms                                                      | 38.4 ms: 1.21x slower                                                  |
| 2to3                       | 445 ms                                                       | 542 ms: 1.22x slower                                                   |
| thrift                     | 1.10 ms                                                      | 1.34 ms: 1.22x slower                                                  |
| sqlglot_parse              | 1.76 ms                                                      | 2.14 ms: 1.22x slower                                                  |
| json_loads                 | 34.3 us                                                      | 41.9 us: 1.22x slower                                                  |
| meteor_contest             | 150 ms                                                       | 184 ms: 1.23x slower                                                   |
| unpickle_pure_python       | 290 us                                                       | 356 us: 1.23x slower                                                   |
| xml_etree_generate         | 122 ms                                                       | 152 ms: 1.24x slower                                                   |
| sympy_sum                  | 210 ms                                                       | 261 ms: 1.24x slower                                                   |
| crypto_pyaes               | 100 ms                                                       | 125 ms: 1.25x slower                                                   |
| scimark_lu                 | 146 ms                                                       | 184 ms: 1.26x slower                                                   |
| chaos                      | 83.6 ms                                                      | 107 ms: 1.28x slower                                                   |
| json_dumps                 | 14.1 ms                                                      | 18.3 ms: 1.29x slower                                                  |
| nqueens                    | 112 ms                                                       | 145 ms: 1.29x slower                                                   |
| scimark_monte_carlo        | 90.6 ms                                                      | 118 ms: 1.30x slower                                                   |
| hexiom                     | 8.11 ms                                                      | 10.7 ms: 1.32x slower                                                  |
| typing_runtime_protocols   | 226 us                                                       | 298 us: 1.32x slower                                                   |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 9.10 ms: 1.35x slower                                                  |
| raytrace                   | 344 ms                                                       | 464 ms: 1.35x slower                                                   |
| coverage                   | 107 ms                                                       | 145 ms: 1.35x slower                                                   |
| bench_thread_pool          | 2.89 ms                                                      | 3.93 ms: 1.36x slower                                                  |
| python_startup_no_site     | 15.3 ms                                                      | 21.2 ms: 1.39x slower                                                  |
| pickle_pure_python         | 416 us                                                       | 598 us: 1.44x slower                                                   |
| deltablue                  | 4.44 ms                                                      | 6.60 ms: 1.49x slower                                                  |
| python_startup             | 22.4 ms                                                      | 33.3 ms: 1.49x slower                                                  |
| mako                       | 15.9 ms                                                      | 24.2 ms: 1.52x slower                                                  |
| nbody                      | 119 ms                                                       | 185 ms: 1.56x slower                                                   |
| bench_mp_pool              | 18.7 ms                                                      | 87.6 ms: 4.69x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.11x slower                                                           |

Benchmark hidden because not significant (7): pylint, xml_etree_parse, asyncio_websockets, pathlib, telco, async_generators, xml_etree_process
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250131-3.14.0a4+-c3ae5c9-NOGIL/bm-20250131-linux-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.078x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.35x