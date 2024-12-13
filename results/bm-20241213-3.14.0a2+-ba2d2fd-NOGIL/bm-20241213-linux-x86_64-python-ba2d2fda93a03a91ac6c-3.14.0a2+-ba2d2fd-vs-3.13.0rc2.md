# Results vs. 3.13.0rc2

- fork: python
- ref: ba2d2fda93a03a91ac6c
- machine: linux-x86_64
- commit hash: ba2d2fd
- commit date: 2024-12-13
- overall geometric mean: 1.203x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 595 ms: 1.34x slower                                                   |
| docutils       | 4.01 sec                                                     | 4.43 sec: 1.10x slower                                                 |
| html5lib       | 92.6 ms                                                      | 124 ms: 1.34x slower                                                   |
| Geometric mean | (ref)                                                        | 1.25x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 1.06 sec: 1.32x faster                                                 |
| async_tree_io              | 1.39 sec                                                     | 1.14 sec: 1.22x faster                                                 |
| async_tree_none_tg         | 504 ms                                                       | 440 ms: 1.14x faster                                                   |
| async_tree_none            | 572 ms                                                       | 533 ms: 1.07x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 799 ms: 1.07x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 634 ms: 1.06x faster                                                   |
| coroutines                 | 30.9 ms                                                      | 33.6 ms: 1.09x slower                                                  |
| async_generators           | 567 ms                                                       | 653 ms: 1.15x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.06x faster                                                           |

Benchmark hidden because not significant (3): async_tree_memoization, async_tree_cpu_io_mixed, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 119 ms                                                       | 181 ms: 1.52x slower                                                   |
| float          | 116 ms                                                       | 181 ms: 1.56x slower                                                   |
| Geometric mean | (ref)                                                        | 1.32x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.47 ms: 1.06x faster                                                  |
| regex_dna      | 282 ms                                                       | 302 ms: 1.07x slower                                                   |
| regex_compile  | 182 ms                                                       | 231 ms: 1.27x slower                                                   |
| Geometric mean | (ref)                                                        | 1.07x slower                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 137 ms: 1.30x faster                                                   |
| xml_etree_parse      | 231 ms                                                       | 206 ms: 1.12x faster                                                   |
| xml_etree_generate   | 122 ms                                                       | 128 ms: 1.04x slower                                                   |
| json_loads           | 34.3 us                                                      | 38.3 us: 1.12x slower                                                  |
| xml_etree_process    | 85.9 ms                                                      | 107 ms: 1.24x slower                                                   |
| tomli_loads          | 2.78 sec                                                     | 3.50 sec: 1.26x slower                                                 |
| json_dumps           | 14.1 ms                                                      | 18.1 ms: 1.28x slower                                                  |
| unpickle_pure_python | 290 us                                                       | 406 us: 1.40x slower                                                   |
| pickle_pure_python   | 416 us                                                       | 664 us: 1.59x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.15x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 20.8 ms: 1.36x slower                                                  |
| python_startup         | 22.4 ms                                                      | 34.6 ms: 1.55x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.45x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 88.3 ms: 1.22x slower                                                  |
| genshi_text     | 31.7 ms                                                      | 42.1 ms: 1.33x slower                                                  |
| django_template | 44.3 ms                                                      | 63.3 ms: 1.43x slower                                                  |
| mako            | 15.9 ms                                                      | 27.5 ms: 1.73x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.42x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 1.06 sec: 1.32x faster                                                 |
| xml_etree_iterparse        | 177 ms                                                       | 137 ms: 1.30x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 1.14 sec: 1.22x faster                                                 |
| async_tree_none_tg         | 504 ms                                                       | 440 ms: 1.14x faster                                                   |
| xml_etree_parse            | 231 ms                                                       | 206 ms: 1.12x faster                                                   |
| deepcopy                   | 498 us                                                       | 458 us: 1.09x faster                                                   |
| async_tree_none            | 572 ms                                                       | 533 ms: 1.07x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 799 ms: 1.07x faster                                                   |
| regex_effbot               | 4.74 ms                                                      | 4.47 ms: 1.06x faster                                                  |
| async_tree_memoization_tg  | 670 ms                                                       | 634 ms: 1.06x faster                                                   |
| xml_etree_generate         | 122 ms                                                       | 128 ms: 1.04x slower                                                   |
| telco                      | 12.2 ms                                                      | 12.7 ms: 1.05x slower                                                  |
| regex_dna                  | 282 ms                                                       | 302 ms: 1.07x slower                                                   |
| json                       | 6.51 ms                                                      | 7.00 ms: 1.07x slower                                                  |
| coroutines                 | 30.9 ms                                                      | 33.6 ms: 1.09x slower                                                  |
| nqueens                    | 112 ms                                                       | 123 ms: 1.10x slower                                                   |
| docutils                   | 4.01 sec                                                     | 4.43 sec: 1.10x slower                                                 |
| deepcopy_reduce            | 4.10 us                                                      | 4.54 us: 1.11x slower                                                  |
| pylint                     | 470 ms                                                       | 524 ms: 1.11x slower                                                   |
| json_loads                 | 34.3 us                                                      | 38.3 us: 1.12x slower                                                  |
| spectral_norm              | 157 ms                                                       | 176 ms: 1.13x slower                                                   |
| async_generators           | 567 ms                                                       | 653 ms: 1.15x slower                                                   |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 7.85 ms: 1.16x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 6.65 ms: 1.17x slower                                                  |
| mdp                        | 3.80 sec                                                     | 4.48 sec: 1.18x slower                                                 |
| meteor_contest             | 150 ms                                                       | 180 ms: 1.20x slower                                                   |
| typing_runtime_protocols   | 226 us                                                       | 272 us: 1.20x slower                                                   |
| scimark_fft                | 473 ms                                                       | 574 ms: 1.21x slower                                                   |
| sqlglot_optimize           | 74.7 ms                                                      | 91.1 ms: 1.22x slower                                                  |
| genshi_xml                 | 72.1 ms                                                      | 88.3 ms: 1.22x slower                                                  |
| crypto_pyaes               | 100 ms                                                       | 123 ms: 1.23x slower                                                   |
| dulwich_log                | 93.7 ms                                                      | 115 ms: 1.23x slower                                                   |
| fannkuch                   | 547 ms                                                       | 672 ms: 1.23x slower                                                   |
| xml_etree_process          | 85.9 ms                                                      | 107 ms: 1.24x slower                                                   |
| bpe_tokeniser              | 6.28 sec                                                     | 7.82 sec: 1.24x slower                                                 |
| sqlglot_normalize          | 140 ms                                                       | 174 ms: 1.25x slower                                                   |
| pycparser                  | 1.57 sec                                                     | 1.97 sec: 1.25x slower                                                 |
| tomli_loads                | 2.78 sec                                                     | 3.50 sec: 1.26x slower                                                 |
| regex_compile              | 182 ms                                                       | 231 ms: 1.27x slower                                                   |
| json_dumps                 | 14.1 ms                                                      | 18.1 ms: 1.28x slower                                                  |
| coverage                   | 107 ms                                                       | 140 ms: 1.30x slower                                                   |
| pprint_safe_repr           | 987 ms                                                       | 1.29 sec: 1.31x slower                                                 |
| sympy_integrate            | 30.2 ms                                                      | 39.9 ms: 1.32x slower                                                  |
| generators                 | 40.0 ms                                                      | 52.9 ms: 1.32x slower                                                  |
| genshi_text                | 31.7 ms                                                      | 42.1 ms: 1.33x slower                                                  |
| html5lib                   | 92.6 ms                                                      | 124 ms: 1.34x slower                                                   |
| 2to3                       | 445 ms                                                       | 595 ms: 1.34x slower                                                   |
| python_startup_no_site     | 15.3 ms                                                      | 20.8 ms: 1.36x slower                                                  |
| pprint_pformat             | 1.94 sec                                                     | 2.65 sec: 1.36x slower                                                 |
| pyflate                    | 664 ms                                                       | 916 ms: 1.38x slower                                                   |
| richards                   | 65.5 ms                                                      | 91.1 ms: 1.39x slower                                                  |
| unpickle_pure_python       | 290 us                                                       | 406 us: 1.40x slower                                                   |
| bench_thread_pool          | 2.89 ms                                                      | 4.04 ms: 1.40x slower                                                  |
| richards_super             | 73.2 ms                                                      | 104 ms: 1.42x slower                                                   |
| django_template            | 44.3 ms                                                      | 63.3 ms: 1.43x slower                                                  |
| thrift                     | 1.10 ms                                                      | 1.58 ms: 1.44x slower                                                  |
| chaos                      | 83.6 ms                                                      | 121 ms: 1.45x slower                                                   |
| logging_format             | 9.24 us                                                      | 14.0 us: 1.51x slower                                                  |
| scimark_lu                 | 146 ms                                                       | 221 ms: 1.51x slower                                                   |
| create_gc_cycles           | 2.41 ms                                                      | 3.66 ms: 1.52x slower                                                  |
| nbody                      | 119 ms                                                       | 181 ms: 1.52x slower                                                   |
| logging_simple             | 8.56 us                                                      | 13.1 us: 1.53x slower                                                  |
| comprehensions             | 22.2 us                                                      | 34.1 us: 1.53x slower                                                  |
| python_startup             | 22.4 ms                                                      | 34.6 ms: 1.55x slower                                                  |
| float                      | 116 ms                                                       | 181 ms: 1.56x slower                                                   |
| scimark_monte_carlo        | 90.6 ms                                                      | 143 ms: 1.58x slower                                                   |
| sympy_str                  | 379 ms                                                       | 598 ms: 1.58x slower                                                   |
| pickle_pure_python         | 416 us                                                       | 664 us: 1.59x slower                                                   |
| hexiom                     | 8.11 ms                                                      | 13.3 ms: 1.63x slower                                                  |
| go                         | 191 ms                                                       | 314 ms: 1.64x slower                                                   |
| scimark_sor                | 179 ms                                                       | 297 ms: 1.66x slower                                                   |
| logging_silent             | 130 ns                                                       | 218 ns: 1.68x slower                                                   |
| sqlglot_transpile          | 2.20 ms                                                      | 3.79 ms: 1.73x slower                                                  |
| mako                       | 15.9 ms                                                      | 27.5 ms: 1.73x slower                                                  |
| sqlglot_parse              | 1.76 ms                                                      | 3.25 ms: 1.85x slower                                                  |
| raytrace                   | 344 ms                                                       | 645 ms: 1.87x slower                                                   |
| sympy_expand               | 601 ms                                                       | 1.16 sec: 1.94x slower                                                 |
| sympy_sum                  | 210 ms                                                       | 424 ms: 2.02x slower                                                   |
| deltablue                  | 4.44 ms                                                      | 11.1 ms: 2.51x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 94.3 ms: 5.04x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.28x slower                                                           |

Benchmark hidden because not significant (8): async_tree_memoization, pidigits, async_tree_cpu_io_mixed, asyncio_websockets, regex_v8, deepcopy_memo, sqlite_synth, pathlib
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241213-3.14.0a2+-ba2d2fd-NOGIL/bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.203x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.20x
- 95% likely to have a slowdown of 1.19x
- 99% likely to have a slowdown of 1.16x

# Memory
- memory change: 1.33x