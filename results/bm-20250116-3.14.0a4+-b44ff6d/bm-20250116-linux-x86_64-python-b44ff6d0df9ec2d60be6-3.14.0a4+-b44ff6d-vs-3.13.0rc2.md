# Results vs. 3.13.0rc2

- fork: python
- ref: b44ff6d0df9ec2d60be6
- machine: linux-x86_64
- commit hash: b44ff6d
- commit date: 2025-01-16
- overall geometric mean: 1.038x faster
- HPT reliability: 99.92%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 479 ms: 1.08x slower                                                   |
| docutils       | 4.01 sec                                                     | 3.60 sec: 1.11x faster                                                 |
| html5lib       | 92.6 ms                                                      | 87.3 ms: 1.06x faster                                                  |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 572 ms                                                       | 375 ms: 1.53x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 921 ms: 1.51x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 939 ms: 1.49x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 492 ms: 1.44x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 474 ms: 1.41x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 392 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 731 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 727 ms: 1.17x faster                                                   |
| async_generators           | 567 ms                                                       | 544 ms: 1.04x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.26x faster                                                           |

Benchmark hidden because not significant (2): asyncio_websockets, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 101 ms: 1.14x faster                                                   |
| pidigits       | 251 ms                                                       | 229 ms: 1.10x faster                                                   |
| nbody          | 119 ms                                                       | 129 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                        | 1.05x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.23 ms: 1.12x faster                                                  |
| regex_v8       | 32.8 ms                                                      | 30.6 ms: 1.07x faster                                                  |
| regex_dna      | 282 ms                                                       | 270 ms: 1.04x faster                                                   |
| Geometric mean | (ref)                                                        | 1.06x faster                                                           |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 231 ms                                                       | 206 ms: 1.12x faster                                                   |
| xml_etree_iterparse  | 177 ms                                                       | 162 ms: 1.09x faster                                                   |
| tomli_loads          | 2.78 sec                                                     | 2.64 sec: 1.05x faster                                                 |
| unpickle_pure_python | 290 us                                                       | 308 us: 1.06x slower                                                   |
| json_loads           | 34.3 us                                                      | 36.6 us: 1.07x slower                                                  |
| json_dumps           | 14.1 ms                                                      | 16.3 ms: 1.16x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (3): xml_etree_generate, xml_etree_process, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 16.7 ms: 1.09x slower                                                  |
| python_startup         | 22.4 ms                                                      | 28.2 ms: 1.26x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.17x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 67.8 ms: 1.06x faster                                                  |
| mako            | 15.9 ms                                                      | 17.7 ms: 1.11x slower                                                  |
| django_template | 44.3 ms                                                      | 49.3 ms: 1.11x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.03x slower                                                           |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 572 ms                                                       | 375 ms: 1.53x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 921 ms: 1.51x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 939 ms: 1.49x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 492 ms: 1.44x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 474 ms: 1.41x faster                                                   |
| deepcopy                   | 498 us                                                       | 353 us: 1.41x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 392 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 731 ms: 1.22x faster                                                   |
| deepcopy_reduce            | 4.10 us                                                      | 3.39 us: 1.21x faster                                                  |
| deepcopy_memo              | 50.1 us                                                      | 41.9 us: 1.20x faster                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 727 ms: 1.17x faster                                                   |
| go                         | 191 ms                                                       | 164 ms: 1.17x faster                                                   |
| pylint                     | 470 ms                                                       | 408 ms: 1.15x faster                                                   |
| float                      | 116 ms                                                       | 101 ms: 1.14x faster                                                   |
| telco                      | 12.2 ms                                                      | 10.8 ms: 1.13x faster                                                  |
| regex_effbot               | 4.74 ms                                                      | 4.23 ms: 1.12x faster                                                  |
| xml_etree_parse            | 231 ms                                                       | 206 ms: 1.12x faster                                                   |
| docutils                   | 4.01 sec                                                     | 3.60 sec: 1.11x faster                                                 |
| spectral_norm              | 157 ms                                                       | 142 ms: 1.10x faster                                                   |
| pidigits                   | 251 ms                                                       | 229 ms: 1.10x faster                                                   |
| fannkuch                   | 547 ms                                                       | 499 ms: 1.10x faster                                                   |
| xml_etree_iterparse        | 177 ms                                                       | 162 ms: 1.09x faster                                                   |
| scimark_fft                | 473 ms                                                       | 434 ms: 1.09x faster                                                   |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 6.28 ms: 1.08x faster                                                  |
| pathlib                    | 29.9 ms                                                      | 27.8 ms: 1.07x faster                                                  |
| mdp                        | 3.80 sec                                                     | 3.54 sec: 1.07x faster                                                 |
| regex_v8                   | 32.8 ms                                                      | 30.6 ms: 1.07x faster                                                  |
| richards                   | 65.5 ms                                                      | 61.4 ms: 1.07x faster                                                  |
| logging_simple             | 8.56 us                                                      | 8.03 us: 1.07x faster                                                  |
| genshi_xml                 | 72.1 ms                                                      | 67.8 ms: 1.06x faster                                                  |
| html5lib                   | 92.6 ms                                                      | 87.3 ms: 1.06x faster                                                  |
| scimark_monte_carlo        | 90.6 ms                                                      | 85.6 ms: 1.06x faster                                                  |
| tomli_loads                | 2.78 sec                                                     | 2.64 sec: 1.05x faster                                                 |
| typing_runtime_protocols   | 226 us                                                       | 215 us: 1.05x faster                                                   |
| hexiom                     | 8.11 ms                                                      | 7.73 ms: 1.05x faster                                                  |
| pprint_safe_repr           | 987 ms                                                       | 945 ms: 1.04x faster                                                   |
| regex_dna                  | 282 ms                                                       | 270 ms: 1.04x faster                                                   |
| async_generators           | 567 ms                                                       | 544 ms: 1.04x faster                                                   |
| pprint_pformat             | 1.94 sec                                                     | 1.89 sec: 1.03x faster                                                 |
| coverage                   | 107 ms                                                       | 113 ms: 1.06x slower                                                   |
| unpickle_pure_python       | 290 us                                                       | 308 us: 1.06x slower                                                   |
| logging_silent             | 130 ns                                                       | 139 ns: 1.07x slower                                                   |
| json_loads                 | 34.3 us                                                      | 36.6 us: 1.07x slower                                                  |
| dulwich_log                | 93.7 ms                                                      | 101 ms: 1.07x slower                                                   |
| 2to3                       | 445 ms                                                       | 479 ms: 1.08x slower                                                   |
| comprehensions             | 22.2 us                                                      | 24.0 us: 1.08x slower                                                  |
| nbody                      | 119 ms                                                       | 129 ms: 1.08x slower                                                   |
| python_startup_no_site     | 15.3 ms                                                      | 16.7 ms: 1.09x slower                                                  |
| sympy_str                  | 379 ms                                                       | 419 ms: 1.10x slower                                                   |
| mako                       | 15.9 ms                                                      | 17.7 ms: 1.11x slower                                                  |
| django_template            | 44.3 ms                                                      | 49.3 ms: 1.11x slower                                                  |
| raytrace                   | 344 ms                                                       | 386 ms: 1.12x slower                                                   |
| logging_format             | 9.24 us                                                      | 10.4 us: 1.12x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 16.3 ms: 1.16x slower                                                  |
| json                       | 6.51 ms                                                      | 7.84 ms: 1.20x slower                                                  |
| python_startup             | 22.4 ms                                                      | 28.2 ms: 1.26x slower                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 3.92 ms: 1.36x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 9.29 ms: 1.63x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 4.11 ms: 1.70x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 100 ms: 5.36x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.01x faster                                                           |

Benchmark hidden because not significant (28): deltablue, thrift, crypto_pyaes, xml_etree_generate, regex_compile, sqlglot_parse, generators, genshi_text, scimark_sor, sqlglot_transpile, sympy_integrate, sqlglot_normalize, bpe_tokeniser, pyflate, chaos, meteor_contest, sqlglot_optimize, nqueens, sqlite_synth, asyncio_websockets, pycparser, scimark_lu, sympy_expand, coroutines, xml_etree_process, richards_super, pickle_pure_python, sympy_sum
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250116-3.14.0a4+-b44ff6d/bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.038x faster

# HPT report

- Reliability score: 99.92% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.13x