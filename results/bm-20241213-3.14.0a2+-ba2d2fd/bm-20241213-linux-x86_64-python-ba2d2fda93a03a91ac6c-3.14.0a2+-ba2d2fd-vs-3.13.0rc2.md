# Results vs. 3.13.0rc2

- fork: python
- ref: ba2d2fda93a03a91ac6c
- machine: linux-x86_64
- commit hash: ba2d2fd
- commit date: 2024-12-13
- overall geometric mean: 1.061x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 4.01 sec                                                     | 3.67 sec: 1.09x faster                                                 |
| html5lib       | 92.6 ms                                                      | 82.9 ms: 1.12x faster                                                  |
| Geometric mean | (ref)                                                        | 1.08x faster                                                           |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 864 ms: 1.62x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 894 ms: 1.55x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 471 ms: 1.51x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 452 ms: 1.48x faster                                                   |
| async_tree_none            | 572 ms                                                       | 387 ms: 1.48x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 373 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 662 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 674 ms: 1.26x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.31x faster                                                           |

Benchmark hidden because not significant (3): async_generators, asyncio_websockets, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 240 ms: 1.05x faster                                                   |
| float          | 116 ms                                                       | 111 ms: 1.05x faster                                                   |
| nbody          | 119 ms                                                       | 127 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                        | 1.01x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 182 ms                                                       | 165 ms: 1.10x faster                                                   |
| regex_effbot   | 4.74 ms                                                      | 4.43 ms: 1.07x faster                                                  |
| regex_dna      | 282 ms                                                       | 271 ms: 1.04x faster                                                   |
| regex_v8       | 32.8 ms                                                      | 34.7 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 145 ms: 1.22x faster                                                   |
| xml_etree_parse      | 231 ms                                                       | 196 ms: 1.18x faster                                                   |
| unpickle_pure_python | 290 us                                                       | 274 us: 1.06x faster                                                   |
| tomli_loads          | 2.78 sec                                                     | 2.72 sec: 1.02x faster                                                 |
| pickle_pure_python   | 416 us                                                       | 437 us: 1.05x slower                                                   |
| json_dumps           | 14.1 ms                                                      | 15.2 ms: 1.08x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.04x faster                                                           |

Benchmark hidden because not significant (3): xml_etree_process, json_loads, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup | 22.4 ms                                                      | 25.9 ms: 1.16x slower                                                  |
| Geometric mean | (ref)                                                        | 1.09x slower                                                           |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text    | 31.7 ms                                                      | 29.3 ms: 1.08x faster                                                  |
| genshi_xml     | 72.1 ms                                                      | 67.9 ms: 1.06x faster                                                  |
| mako           | 15.9 ms                                                      | 16.8 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                        | 1.01x faster                                                           |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 864 ms: 1.62x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 894 ms: 1.55x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 471 ms: 1.51x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 452 ms: 1.48x faster                                                   |
| async_tree_none            | 572 ms                                                       | 387 ms: 1.48x faster                                                   |
| deepcopy                   | 498 us                                                       | 347 us: 1.43x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 373 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 662 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 674 ms: 1.26x faster                                                   |
| telco                      | 12.2 ms                                                      | 9.74 ms: 1.25x faster                                                  |
| deepcopy_memo              | 50.1 us                                                      | 40.6 us: 1.24x faster                                                  |
| xml_etree_iterparse        | 177 ms                                                       | 145 ms: 1.22x faster                                                   |
| pylint                     | 470 ms                                                       | 394 ms: 1.19x faster                                                   |
| go                         | 191 ms                                                       | 160 ms: 1.19x faster                                                   |
| xml_etree_parse            | 231 ms                                                       | 196 ms: 1.18x faster                                                   |
| deepcopy_reduce            | 4.10 us                                                      | 3.62 us: 1.13x faster                                                  |
| meteor_contest             | 150 ms                                                       | 133 ms: 1.13x faster                                                   |
| pathlib                    | 29.9 ms                                                      | 26.6 ms: 1.12x faster                                                  |
| nqueens                    | 112 ms                                                       | 99.9 ms: 1.12x faster                                                  |
| html5lib                   | 92.6 ms                                                      | 82.9 ms: 1.12x faster                                                  |
| sympy_integrate            | 30.2 ms                                                      | 27.3 ms: 1.11x faster                                                  |
| regex_compile              | 182 ms                                                       | 165 ms: 1.10x faster                                                   |
| scimark_sor                | 179 ms                                                       | 163 ms: 1.10x faster                                                   |
| docutils                   | 4.01 sec                                                     | 3.67 sec: 1.09x faster                                                 |
| richards_super             | 73.2 ms                                                      | 67.3 ms: 1.09x faster                                                  |
| genshi_text                | 31.7 ms                                                      | 29.3 ms: 1.08x faster                                                  |
| bpe_tokeniser              | 6.28 sec                                                     | 5.82 sec: 1.08x faster                                                 |
| spectral_norm              | 157 ms                                                       | 145 ms: 1.08x faster                                                   |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 6.29 ms: 1.07x faster                                                  |
| richards                   | 65.5 ms                                                      | 61.0 ms: 1.07x faster                                                  |
| sqlglot_optimize           | 74.7 ms                                                      | 69.8 ms: 1.07x faster                                                  |
| regex_effbot               | 4.74 ms                                                      | 4.43 ms: 1.07x faster                                                  |
| genshi_xml                 | 72.1 ms                                                      | 67.9 ms: 1.06x faster                                                  |
| unpickle_pure_python       | 290 us                                                       | 274 us: 1.06x faster                                                   |
| fannkuch                   | 547 ms                                                       | 516 ms: 1.06x faster                                                   |
| pprint_safe_repr           | 987 ms                                                       | 935 ms: 1.06x faster                                                   |
| crypto_pyaes               | 100 ms                                                       | 95.2 ms: 1.05x faster                                                  |
| pidigits                   | 251 ms                                                       | 240 ms: 1.05x faster                                                   |
| float                      | 116 ms                                                       | 111 ms: 1.05x faster                                                   |
| regex_dna                  | 282 ms                                                       | 271 ms: 1.04x faster                                                   |
| pyflate                    | 664 ms                                                       | 644 ms: 1.03x faster                                                   |
| scimark_fft                | 473 ms                                                       | 460 ms: 1.03x faster                                                   |
| tomli_loads                | 2.78 sec                                                     | 2.72 sec: 1.02x faster                                                 |
| mdp                        | 3.80 sec                                                     | 3.91 sec: 1.03x slower                                                 |
| pickle_pure_python         | 416 us                                                       | 437 us: 1.05x slower                                                   |
| mako                       | 15.9 ms                                                      | 16.8 ms: 1.06x slower                                                  |
| regex_v8                   | 32.8 ms                                                      | 34.7 ms: 1.06x slower                                                  |
| nbody                      | 119 ms                                                       | 127 ms: 1.07x slower                                                   |
| logging_simple             | 8.56 us                                                      | 9.12 us: 1.07x slower                                                  |
| scimark_lu                 | 146 ms                                                       | 156 ms: 1.07x slower                                                   |
| json_dumps                 | 14.1 ms                                                      | 15.2 ms: 1.08x slower                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 3.17 ms: 1.10x slower                                                  |
| logging_silent             | 130 ns                                                       | 144 ns: 1.11x slower                                                   |
| python_startup             | 22.4 ms                                                      | 25.9 ms: 1.16x slower                                                  |
| dulwich_log                | 93.7 ms                                                      | 112 ms: 1.20x slower                                                   |
| gc_traversal               | 5.70 ms                                                      | 8.42 ms: 1.48x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 3.65 ms: 1.51x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 90.6 ms: 4.85x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                           |

Benchmark hidden because not significant (30): chaos, xml_etree_process, async_generators, asyncio_websockets, 2to3, sqlglot_normalize, pprint_pformat, sympy_expand, scimark_monte_carlo, sympy_str, json_loads, sqlite_synth, json, xml_etree_generate, generators, coverage, coroutines, comprehensions, typing_runtime_protocols, raytrace, sqlglot_parse, thrift, logging_format, hexiom, pycparser, sympy_sum, django_template, python_startup_no_site, sqlglot_transpile, deltablue
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241213-3.14.0a2+-ba2d2fd/bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.061x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.12x