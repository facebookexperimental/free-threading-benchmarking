# Results vs. 3.12.6

- fork: python
- ref: ba2d2fda93a03a91ac6c
- machine: linux-x86_64
- commit hash: ba2d2fd
- commit date: 2024-12-13
- overall geometric mean: 1.102x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 4.00 sec                                               | 3.67 sec: 1.09x faster                                                 |
| html5lib       | 88.9 ms                                                | 82.9 ms: 1.07x faster                                                  |
| Geometric mean | (ref)                                                  | 1.07x faster                                                           |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 864 ms: 2.24x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 471 ms: 2.08x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 894 ms: 2.07x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 452 ms: 2.06x faster                                                   |
| async_tree_none            | 741 ms                                                 | 387 ms: 1.92x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 373 ms: 1.89x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 674 ms: 1.63x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 662 ms: 1.63x faster                                                   |
| async_generators           | 589 ms                                                 | 552 ms: 1.07x faster                                                   |
| coroutines                 | 29.5 ms                                                | 31.0 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.61x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 111 ms: 1.11x faster                                                   |
| pidigits       | 250 ms                                                 | 240 ms: 1.04x faster                                                   |
| nbody          | 119 ms                                                 | 127 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.43 ms: 1.16x faster                                                  |
| regex_compile  | 187 ms                                                 | 165 ms: 1.13x faster                                                   |
| regex_v8       | 32.5 ms                                                | 34.7 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                  | 1.06x faster                                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 241 ms                                                 | 196 ms: 1.23x faster                                                   |
| xml_etree_iterparse  | 169 ms                                                 | 145 ms: 1.17x faster                                                   |
| json_loads           | 37.9 us                                                | 33.8 us: 1.12x faster                                                  |
| unpickle_pure_python | 300 us                                                 | 274 us: 1.09x faster                                                   |
| tomli_loads          | 2.88 sec                                               | 2.72 sec: 1.06x faster                                                 |
| json_dumps           | 14.3 ms                                                | 15.2 ms: 1.06x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.07x faster                                                           |

Benchmark hidden because not significant (3): xml_etree_generate, xml_etree_process, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 15.7 ms: 1.12x faster                                                  |
| python_startup         | 23.7 ms                                                | 25.9 ms: 1.09x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako           | 15.7 ms                                                | 16.8 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (3): genshi_text, genshi_xml, django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 864 ms: 2.24x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 471 ms: 2.08x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 894 ms: 2.07x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 452 ms: 2.06x faster                                                   |
| async_tree_none            | 741 ms                                                 | 387 ms: 1.92x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 373 ms: 1.89x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 674 ms: 1.63x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 662 ms: 1.63x faster                                                   |
| deepcopy                   | 468 us                                                 | 347 us: 1.35x faster                                                   |
| deepcopy_memo              | 52.4 us                                                | 40.6 us: 1.29x faster                                                  |
| sqlalchemy_declarative     | 218 ms                                                 | 173 ms: 1.26x faster                                                   |
| xml_etree_parse            | 241 ms                                                 | 196 ms: 1.23x faster                                                   |
| comprehensions             | 27.1 us                                                | 22.4 us: 1.21x faster                                                  |
| pathlib                    | 31.6 ms                                                | 26.6 ms: 1.19x faster                                                  |
| pylint                     | 465 ms                                                 | 394 ms: 1.18x faster                                                   |
| raytrace                   | 408 ms                                                 | 347 ms: 1.18x faster                                                   |
| nqueens                    | 117 ms                                                 | 99.9 ms: 1.17x faster                                                  |
| sqlalchemy_imperative      | 24.7 ms                                                | 21.2 ms: 1.17x faster                                                  |
| xml_etree_iterparse        | 169 ms                                                 | 145 ms: 1.17x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.43 ms: 1.16x faster                                                  |
| sqlglot_normalize          | 157 ms                                                 | 137 ms: 1.15x faster                                                   |
| bpe_tokeniser              | 6.59 sec                                               | 5.82 sec: 1.13x faster                                                 |
| regex_compile              | 187 ms                                                 | 165 ms: 1.13x faster                                                   |
| pyflate                    | 727 ms                                                 | 644 ms: 1.13x faster                                                   |
| crypto_pyaes               | 107 ms                                                 | 95.2 ms: 1.13x faster                                                  |
| python_startup_no_site     | 17.6 ms                                                | 15.7 ms: 1.12x faster                                                  |
| json_loads                 | 37.9 us                                                | 33.8 us: 1.12x faster                                                  |
| pycparser                  | 1.79 sec                                               | 1.60 sec: 1.12x faster                                                 |
| deepcopy_reduce            | 4.04 us                                                | 3.62 us: 1.11x faster                                                  |
| float                      | 123 ms                                                 | 111 ms: 1.11x faster                                                   |
| meteor_contest             | 146 ms                                                 | 133 ms: 1.10x faster                                                   |
| bench_thread_pool          | 3.48 ms                                                | 3.17 ms: 1.10x faster                                                  |
| unpickle_pure_python       | 300 us                                                 | 274 us: 1.09x faster                                                   |
| sqlglot_optimize           | 76.0 ms                                                | 69.8 ms: 1.09x faster                                                  |
| sympy_integrate            | 29.8 ms                                                | 27.3 ms: 1.09x faster                                                  |
| scimark_fft                | 500 ms                                                 | 460 ms: 1.09x faster                                                   |
| docutils                   | 4.00 sec                                               | 3.67 sec: 1.09x faster                                                 |
| richards_super             | 72.8 ms                                                | 67.3 ms: 1.08x faster                                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 89.1 ms: 1.08x faster                                                  |
| html5lib                   | 88.9 ms                                                | 82.9 ms: 1.07x faster                                                  |
| go                         | 172 ms                                                 | 160 ms: 1.07x faster                                                   |
| spectral_norm              | 156 ms                                                 | 145 ms: 1.07x faster                                                   |
| async_generators           | 589 ms                                                 | 552 ms: 1.07x faster                                                   |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 6.29 ms: 1.06x faster                                                  |
| json                       | 6.85 ms                                                | 6.44 ms: 1.06x faster                                                  |
| tomli_loads                | 2.88 sec                                               | 2.72 sec: 1.06x faster                                                 |
| chaos                      | 84.9 ms                                                | 80.9 ms: 1.05x faster                                                  |
| fannkuch                   | 540 ms                                                 | 516 ms: 1.05x faster                                                   |
| pidigits                   | 250 ms                                                 | 240 ms: 1.04x faster                                                   |
| pprint_pformat             | 1.98 sec                                               | 1.90 sec: 1.04x faster                                                 |
| pprint_safe_repr           | 967 ms                                                 | 935 ms: 1.03x faster                                                   |
| coroutines                 | 29.5 ms                                                | 31.0 ms: 1.05x slower                                                  |
| nbody                      | 119 ms                                                 | 127 ms: 1.06x slower                                                   |
| json_dumps                 | 14.3 ms                                                | 15.2 ms: 1.06x slower                                                  |
| regex_v8                   | 32.5 ms                                                | 34.7 ms: 1.07x slower                                                  |
| mako                       | 15.7 ms                                                | 16.8 ms: 1.07x slower                                                  |
| deltablue                  | 4.27 ms                                                | 4.62 ms: 1.08x slower                                                  |
| python_startup             | 23.7 ms                                                | 25.9 ms: 1.09x slower                                                  |
| dulwich_log                | 100 ms                                                 | 112 ms: 1.12x slower                                                   |
| coverage                   | 95.4 ms                                                | 108 ms: 1.13x slower                                                   |
| gc_traversal               | 5.86 ms                                                | 8.42 ms: 1.44x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 3.65 ms: 1.88x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 90.6 ms: 4.38x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.08x faster                                                           |

Benchmark hidden because not significant (27): 2to3, xml_etree_generate, logging_simple, sympy_sum, sqlglot_transpile, sympy_str, genshi_text, logging_format, generators, regex_dna, scimark_sor, mdp, sqlglot_parse, hexiom, xml_etree_process, asyncio_websockets, pickle_pure_python, genshi_xml, django_template, richards, typing_runtime_protocols, sympy_expand, telco, sqlite_synth, scimark_lu, logging_silent, thrift
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241213-3.14.0a2+-ba2d2fd/bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.102x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.13x