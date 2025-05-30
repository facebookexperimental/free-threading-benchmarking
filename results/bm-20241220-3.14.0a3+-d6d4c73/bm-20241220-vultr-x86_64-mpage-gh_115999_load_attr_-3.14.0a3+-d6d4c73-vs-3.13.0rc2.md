# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: d6d4c73
- commit date: 2024-12-20
- overall geometric mean: 1.048x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 255 ms: 1.02x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.55 sec: 1.03x faster                                                |
| Geometric mean | (ref)                                                        | 1.02x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 610 ms: 1.50x faster                                                  |
| async_tree_io              | 876 ms                                                       | 619 ms: 1.41x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 329 ms: 1.40x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 302 ms: 1.37x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 253 ms: 1.33x faster                                                  |
| async_tree_none            | 354 ms                                                       | 273 ms: 1.29x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 565 ms: 1.18x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 546 ms: 1.17x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 21.3 ms: 1.11x faster                                                 |
| async_generators           | 377 ms                                                       | 358 ms: 1.05x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.00x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.25x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 75.7 ms: 1.02x faster                                                 |
| pidigits       | 217 ms                                                       | 217 ms: 1.00x slower                                                  |
| nbody          | 85.1 ms                                                      | 89.6 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                        | 1.01x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.76 ms: 1.12x faster                                                 |
| regex_dna      | 180 ms                                                       | 168 ms: 1.07x faster                                                  |
| regex_compile  | 132 ms                                                       | 126 ms: 1.05x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 23.5 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                        | 1.05x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.07x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 1.89 sec: 1.06x faster                                                |
| xml_etree_iterparse  | 94.9 ms                                                      | 90.9 ms: 1.04x faster                                                 |
| xml_etree_process    | 59.3 ms                                                      | 57.5 ms: 1.03x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 82.9 ms: 1.03x faster                                                 |
| json_loads           | 27.0 us                                                      | 26.3 us: 1.03x faster                                                 |
| unpickle_pure_python | 210 us                                                       | 209 us: 1.00x faster                                                  |
| pickle_pure_python   | 294 us                                                       | 306 us: 1.04x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 11.3 ms: 1.07x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.02x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.50 ms: 1.01x slower                                                 |
| python_startup         | 11.0 ms                                                      | 14.7 ms: 1.34x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.16x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.0 ms: 1.03x faster                                                 |
| django_template | 34.1 ms                                                      | 35.2 ms: 1.03x slower                                                 |
| mako            | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.01x slower                                                          |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 610 ms: 1.50x faster                                                  |
| async_tree_io              | 876 ms                                                       | 619 ms: 1.41x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 329 ms: 1.40x faster                                                  |
| deepcopy                   | 355 us                                                       | 255 us: 1.40x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 302 ms: 1.37x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 253 ms: 1.33x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 30.1 us: 1.30x faster                                                 |
| async_tree_none            | 354 ms                                                       | 273 ms: 1.29x faster                                                  |
| go                         | 141 ms                                                       | 114 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 565 ms: 1.18x faster                                                  |
| scimark_sor                | 134 ms                                                       | 114 ms: 1.18x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.65 us: 1.17x faster                                                 |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 546 ms: 1.17x faster                                                  |
| spectral_norm              | 111 ms                                                       | 95.9 ms: 1.16x faster                                                 |
| pylint                     | 317 ms                                                       | 279 ms: 1.14x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.76 ms: 1.12x faster                                                 |
| scimark_fft                | 349 ms                                                       | 315 ms: 1.11x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 21.3 ms: 1.11x faster                                                 |
| pyflate                    | 449 ms                                                       | 411 ms: 1.09x faster                                                  |
| regex_dna                  | 180 ms                                                       | 168 ms: 1.07x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.07x faster                                                  |
| telco                      | 7.82 ms                                                      | 7.37 ms: 1.06x faster                                                 |
| tomli_loads                | 2.01 sec                                                     | 1.89 sec: 1.06x faster                                                |
| pprint_safe_repr           | 738 ms                                                       | 696 ms: 1.06x faster                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.46 ms: 1.06x faster                                                 |
| coverage                   | 83.0 ms                                                      | 78.8 ms: 1.05x faster                                                 |
| async_generators           | 377 ms                                                       | 358 ms: 1.05x faster                                                  |
| richards                   | 45.2 ms                                                      | 43.0 ms: 1.05x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.23 sec: 1.05x faster                                                |
| thrift                     | 778 us                                                       | 741 us: 1.05x faster                                                  |
| regex_compile              | 132 ms                                                       | 126 ms: 1.05x faster                                                  |
| richards_super             | 51.6 ms                                                      | 49.2 ms: 1.05x faster                                                 |
| generators                 | 28.8 ms                                                      | 27.4 ms: 1.05x faster                                                 |
| pathlib                    | 19.2 ms                                                      | 18.3 ms: 1.05x faster                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.43 sec: 1.05x faster                                                |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.9 ms: 1.04x faster                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 62.6 ms: 1.04x faster                                                 |
| meteor_contest             | 102 ms                                                       | 98.1 ms: 1.04x faster                                                 |
| xml_etree_process          | 59.3 ms                                                      | 57.5 ms: 1.03x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 82.9 ms: 1.03x faster                                                 |
| sqlglot_normalize          | 106 ms                                                       | 103 ms: 1.03x faster                                                  |
| logging_simple             | 6.16 us                                                      | 5.99 us: 1.03x faster                                                 |
| scimark_lu                 | 113 ms                                                       | 110 ms: 1.03x faster                                                  |
| genshi_text                | 21.5 ms                                                      | 21.0 ms: 1.03x faster                                                 |
| logging_format             | 6.84 us                                                      | 6.67 us: 1.03x faster                                                 |
| json_loads                 | 27.0 us                                                      | 26.3 us: 1.03x faster                                                 |
| docutils                   | 2.62 sec                                                     | 2.55 sec: 1.03x faster                                                |
| float                      | 77.5 ms                                                      | 75.7 ms: 1.02x faster                                                 |
| fannkuch                   | 370 ms                                                       | 362 ms: 1.02x faster                                                  |
| sympy_sum                  | 156 ms                                                       | 152 ms: 1.02x faster                                                  |
| 2to3                       | 260 ms                                                       | 255 ms: 1.02x faster                                                  |
| hexiom                     | 5.99 ms                                                      | 5.90 ms: 1.02x faster                                                 |
| sqlglot_optimize           | 52.7 ms                                                      | 52.0 ms: 1.02x faster                                                 |
| sympy_str                  | 275 ms                                                       | 271 ms: 1.01x faster                                                  |
| json                       | 4.93 ms                                                      | 4.88 ms: 1.01x faster                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 67.3 ms: 1.01x faster                                                 |
| sympy_integrate            | 19.8 ms                                                      | 19.8 ms: 1.00x faster                                                 |
| unpickle_pure_python       | 210 us                                                       | 209 us: 1.00x faster                                                  |
| pidigits                   | 217 ms                                                       | 217 ms: 1.00x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.14 ms: 1.00x slower                                                 |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.00x slower                                                  |
| chaos                      | 57.3 ms                                                      | 57.6 ms: 1.01x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 7.50 ms: 1.01x slower                                                 |
| typing_runtime_protocols   | 155 us                                                       | 157 us: 1.02x slower                                                  |
| raytrace                   | 253 ms                                                       | 258 ms: 1.02x slower                                                  |
| django_template            | 34.1 ms                                                      | 35.2 ms: 1.03x slower                                                 |
| comprehensions             | 16.5 us                                                      | 17.0 us: 1.03x slower                                                 |
| regex_v8                   | 22.7 ms                                                      | 23.5 ms: 1.03x slower                                                 |
| mako                       | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 306 us: 1.04x slower                                                  |
| logging_silent             | 103 ns                                                       | 107 ns: 1.04x slower                                                  |
| nbody                      | 85.1 ms                                                      | 89.6 ms: 1.05x slower                                                 |
| mdp                        | 2.36 sec                                                     | 2.50 sec: 1.06x slower                                                |
| json_dumps                 | 10.5 ms                                                      | 11.3 ms: 1.07x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.03 ms: 1.12x slower                                                 |
| python_startup             | 11.0 ms                                                      | 14.7 ms: 1.34x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.84 ms: 1.38x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.41 ms: 1.40x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 89.0 ms: 8.09x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.02x faster                                                          |

Benchmark hidden because not significant (8): pycparser, genshi_xml, dulwich_log, sqlite_synth, sqlglot_transpile, nqueens, sympy_expand, sqlglot_parse
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241220-3.14.0a3+-d6d4c73/bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.048x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.10x