# Results vs. 3.13.0rc2

- fork: python
- ref: 0ac40acec045c4ce780c
- machine: linux-x86_64
- commit hash: 0ac40ac
- commit date: 2024-12-14
- overall geometric mean: 1.045x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 255 ms: 1.02x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.54 sec: 1.03x faster                                                 |
| Geometric mean | (ref)                                                        | 1.02x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 606 ms: 1.51x faster                                                   |
| async_tree_io              | 876 ms                                                       | 623 ms: 1.41x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 335 ms: 1.38x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 307 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 496 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 480 ms: 1.33x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 257 ms: 1.31x faster                                                   |
| async_tree_none            | 354 ms                                                       | 276 ms: 1.28x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 22.1 ms: 1.06x faster                                                  |
| async_generators           | 377 ms                                                       | 358 ms: 1.05x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.00x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.26x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 186 ms: 1.17x faster                                                   |
| float          | 77.5 ms                                                      | 76.8 ms: 1.01x faster                                                  |
| nbody          | 85.1 ms                                                      | 90.7 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.72 ms: 1.13x faster                                                  |
| regex_dna      | 180 ms                                                       | 167 ms: 1.08x faster                                                   |
| regex_compile  | 132 ms                                                       | 127 ms: 1.04x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 23.2 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                        | 1.06x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.06x faster                                                   |
| xml_etree_iterparse  | 94.9 ms                                                      | 90.8 ms: 1.05x faster                                                  |
| json_loads           | 27.0 us                                                      | 26.4 us: 1.02x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 83.8 ms: 1.02x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 58.6 ms: 1.01x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 1.99 sec: 1.01x faster                                                 |
| unpickle_pure_python | 210 us                                                       | 212 us: 1.01x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 319 us: 1.08x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 11.4 ms: 1.08x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.00x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.46 ms: 1.01x slower                                                  |
| python_startup         | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.16x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 11.5 ms: 1.01x slower                                                  |
| genshi_xml      | 48.8 ms                                                      | 50.6 ms: 1.04x slower                                                  |
| django_template | 34.1 ms                                                      | 35.5 ms: 1.04x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                           |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 606 ms: 1.51x faster                                                   |
| async_tree_io              | 876 ms                                                       | 623 ms: 1.41x faster                                                   |
| deepcopy                   | 355 us                                                       | 255 us: 1.39x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 335 ms: 1.38x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 307 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 496 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 480 ms: 1.33x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 257 ms: 1.31x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 30.2 us: 1.29x faster                                                  |
| async_tree_none            | 354 ms                                                       | 276 ms: 1.28x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.57 us: 1.21x faster                                                  |
| go                         | 141 ms                                                       | 117 ms: 1.21x faster                                                   |
| pidigits                   | 217 ms                                                       | 186 ms: 1.17x faster                                                   |
| pylint                     | 317 ms                                                       | 280 ms: 1.13x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.72 ms: 1.13x faster                                                  |
| spectral_norm              | 111 ms                                                       | 98.7 ms: 1.12x faster                                                  |
| telco                      | 7.82 ms                                                      | 7.15 ms: 1.09x faster                                                  |
| scimark_fft                | 349 ms                                                       | 320 ms: 1.09x faster                                                   |
| regex_dna                  | 180 ms                                                       | 167 ms: 1.08x faster                                                   |
| scimark_sor                | 134 ms                                                       | 125 ms: 1.08x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 22.1 ms: 1.06x faster                                                  |
| pyflate                    | 449 ms                                                       | 422 ms: 1.06x faster                                                   |
| thrift                     | 778 us                                                       | 732 us: 1.06x faster                                                   |
| pathlib                    | 19.2 ms                                                      | 18.1 ms: 1.06x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.06x faster                                                   |
| async_generators           | 377 ms                                                       | 358 ms: 1.05x faster                                                   |
| coverage                   | 83.0 ms                                                      | 78.8 ms: 1.05x faster                                                  |
| generators                 | 28.8 ms                                                      | 27.4 ms: 1.05x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.8 ms: 1.05x faster                                                  |
| regex_compile              | 132 ms                                                       | 127 ms: 1.04x faster                                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 4.27 sec: 1.04x faster                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.54 ms: 1.04x faster                                                  |
| pprint_safe_repr           | 738 ms                                                       | 711 ms: 1.04x faster                                                   |
| docutils                   | 2.62 sec                                                     | 2.54 sec: 1.03x faster                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.46 sec: 1.03x faster                                                 |
| scimark_lu                 | 113 ms                                                       | 110 ms: 1.03x faster                                                   |
| json_loads                 | 27.0 us                                                      | 26.4 us: 1.02x faster                                                  |
| sympy_sum                  | 156 ms                                                       | 152 ms: 1.02x faster                                                   |
| meteor_contest             | 102 ms                                                       | 99.3 ms: 1.02x faster                                                  |
| json                       | 4.93 ms                                                      | 4.82 ms: 1.02x faster                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 66.4 ms: 1.02x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 83.8 ms: 1.02x faster                                                  |
| sqlglot_normalize          | 106 ms                                                       | 104 ms: 1.02x faster                                                   |
| richards_super             | 51.6 ms                                                      | 50.7 ms: 1.02x faster                                                  |
| 2to3                       | 260 ms                                                       | 255 ms: 1.02x faster                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 64.3 ms: 1.02x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 58.6 ms: 1.01x faster                                                  |
| richards                   | 45.2 ms                                                      | 44.7 ms: 1.01x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.18 us: 1.01x faster                                                  |
| sympy_str                  | 275 ms                                                       | 272 ms: 1.01x faster                                                   |
| logging_simple             | 6.16 us                                                      | 6.10 us: 1.01x faster                                                  |
| hexiom                     | 5.99 ms                                                      | 5.94 ms: 1.01x faster                                                  |
| float                      | 77.5 ms                                                      | 76.8 ms: 1.01x faster                                                  |
| sqlglot_optimize           | 52.7 ms                                                      | 52.3 ms: 1.01x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.99 sec: 1.01x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.00x slower                                                   |
| deltablue                  | 3.12 ms                                                      | 3.14 ms: 1.01x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.46 ms: 1.01x slower                                                  |
| fannkuch                   | 370 ms                                                       | 373 ms: 1.01x slower                                                   |
| typing_runtime_protocols   | 155 us                                                       | 156 us: 1.01x slower                                                   |
| unpickle_pure_python       | 210 us                                                       | 212 us: 1.01x slower                                                   |
| mako                       | 11.3 ms                                                      | 11.5 ms: 1.01x slower                                                  |
| chaos                      | 57.3 ms                                                      | 58.2 ms: 1.02x slower                                                  |
| nqueens                    | 78.6 ms                                                      | 79.9 ms: 1.02x slower                                                  |
| sqlglot_transpile          | 1.56 ms                                                      | 1.59 ms: 1.02x slower                                                  |
| dulwich_log                | 74.8 ms                                                      | 76.3 ms: 1.02x slower                                                  |
| regex_v8                   | 22.7 ms                                                      | 23.2 ms: 1.02x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 1.28 ms: 1.02x slower                                                  |
| raytrace                   | 253 ms                                                       | 261 ms: 1.03x slower                                                   |
| genshi_xml                 | 48.8 ms                                                      | 50.6 ms: 1.04x slower                                                  |
| logging_silent             | 103 ns                                                       | 107 ns: 1.04x slower                                                   |
| django_template            | 34.1 ms                                                      | 35.5 ms: 1.04x slower                                                  |
| mdp                        | 2.36 sec                                                     | 2.46 sec: 1.05x slower                                                 |
| comprehensions             | 16.5 us                                                      | 17.5 us: 1.07x slower                                                  |
| nbody                      | 85.1 ms                                                      | 90.7 ms: 1.07x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 319 us: 1.08x slower                                                   |
| json_dumps                 | 10.5 ms                                                      | 11.4 ms: 1.08x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.03 ms: 1.13x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.16 ms: 1.33x slower                                                  |
| python_startup             | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.82 ms: 1.36x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 88.3 ms: 8.03x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.02x faster                                                           |

Benchmark hidden because not significant (5): pycparser, sympy_integrate, genshi_text, sympy_expand, logging_format
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241214-3.14.0a2+-0ac40ac/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.045x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.09x