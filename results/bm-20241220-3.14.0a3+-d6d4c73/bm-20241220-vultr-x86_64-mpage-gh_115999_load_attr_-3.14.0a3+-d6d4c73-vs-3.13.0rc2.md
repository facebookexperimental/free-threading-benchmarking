# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: d6d4c73
- commit date: 2024-12-20
- overall geometric mean: 1.058x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 254 ms: 1.02x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.54 sec: 1.03x faster                                                |
| Geometric mean | (ref)                                                        | 1.03x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 602 ms: 1.52x faster                                                  |
| async_tree_io              | 876 ms                                                       | 616 ms: 1.42x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 328 ms: 1.41x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 302 ms: 1.37x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 491 ms: 1.36x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 475 ms: 1.34x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 252 ms: 1.34x faster                                                  |
| async_tree_none            | 354 ms                                                       | 272 ms: 1.30x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 21.7 ms: 1.09x faster                                                 |
| async_generators           | 377 ms                                                       | 355 ms: 1.06x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.00x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.28x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 185 ms: 1.17x faster                                                  |
| float          | 77.5 ms                                                      | 74.2 ms: 1.04x faster                                                 |
| nbody          | 85.1 ms                                                      | 89.9 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                        | 1.05x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.72 ms: 1.13x faster                                                 |
| regex_dna      | 180 ms                                                       | 166 ms: 1.09x faster                                                  |
| regex_compile  | 132 ms                                                       | 127 ms: 1.04x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 23.2 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                        | 1.06x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 127 ms: 1.07x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 1.89 sec: 1.06x faster                                                |
| xml_etree_iterparse  | 94.9 ms                                                      | 90.3 ms: 1.05x faster                                                 |
| json_loads           | 27.0 us                                                      | 25.9 us: 1.04x faster                                                 |
| xml_etree_process    | 59.3 ms                                                      | 57.7 ms: 1.03x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 83.2 ms: 1.03x faster                                                 |
| unpickle_pure_python | 210 us                                                       | 210 us: 1.00x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 308 us: 1.05x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 11.3 ms: 1.07x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.02x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.44 ms: 1.01x slower                                                 |
| python_startup         | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.16x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.1 ms: 1.02x faster                                                 |
| django_template | 34.1 ms                                                      | 34.7 ms: 1.02x slower                                                 |
| mako            | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.00x slower                                                          |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 602 ms: 1.52x faster                                                  |
| async_tree_io              | 876 ms                                                       | 616 ms: 1.42x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 328 ms: 1.41x faster                                                  |
| deepcopy                   | 355 us                                                       | 255 us: 1.40x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 302 ms: 1.37x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 491 ms: 1.36x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 475 ms: 1.34x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 252 ms: 1.34x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 29.8 us: 1.31x faster                                                 |
| async_tree_none            | 354 ms                                                       | 272 ms: 1.30x faster                                                  |
| go                         | 141 ms                                                       | 114 ms: 1.24x faster                                                  |
| scimark_sor                | 134 ms                                                       | 113 ms: 1.19x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.64 us: 1.18x faster                                                 |
| spectral_norm              | 111 ms                                                       | 94.5 ms: 1.18x faster                                                 |
| pidigits                   | 217 ms                                                       | 185 ms: 1.17x faster                                                  |
| pylint                     | 317 ms                                                       | 279 ms: 1.14x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.72 ms: 1.13x faster                                                 |
| scimark_fft                | 349 ms                                                       | 309 ms: 1.13x faster                                                  |
| telco                      | 7.82 ms                                                      | 7.12 ms: 1.10x faster                                                 |
| coroutines                 | 23.6 ms                                                      | 21.7 ms: 1.09x faster                                                 |
| regex_dna                  | 180 ms                                                       | 166 ms: 1.09x faster                                                  |
| pyflate                    | 449 ms                                                       | 415 ms: 1.08x faster                                                  |
| generators                 | 28.8 ms                                                      | 26.9 ms: 1.07x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 127 ms: 1.07x faster                                                  |
| richards_super             | 51.6 ms                                                      | 48.3 ms: 1.07x faster                                                 |
| richards                   | 45.2 ms                                                      | 42.4 ms: 1.07x faster                                                 |
| async_generators           | 377 ms                                                       | 355 ms: 1.06x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.89 sec: 1.06x faster                                                |
| pathlib                    | 19.2 ms                                                      | 18.1 ms: 1.06x faster                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.45 ms: 1.06x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.22 sec: 1.05x faster                                                |
| thrift                     | 778 us                                                       | 739 us: 1.05x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.3 ms: 1.05x faster                                                 |
| coverage                   | 83.0 ms                                                      | 79.3 ms: 1.05x faster                                                 |
| regex_compile              | 132 ms                                                       | 127 ms: 1.04x faster                                                  |
| float                      | 77.5 ms                                                      | 74.2 ms: 1.04x faster                                                 |
| json_loads                 | 27.0 us                                                      | 25.9 us: 1.04x faster                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 62.8 ms: 1.04x faster                                                 |
| json                       | 4.93 ms                                                      | 4.74 ms: 1.04x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 710 ms: 1.04x faster                                                  |
| hexiom                     | 5.99 ms                                                      | 5.77 ms: 1.04x faster                                                 |
| meteor_contest             | 102 ms                                                       | 98.7 ms: 1.03x faster                                                 |
| sqlglot_normalize          | 106 ms                                                       | 103 ms: 1.03x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.54 sec: 1.03x faster                                                |
| pprint_pformat             | 1.50 sec                                                     | 1.46 sec: 1.03x faster                                                |
| xml_etree_process          | 59.3 ms                                                      | 57.7 ms: 1.03x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 83.2 ms: 1.03x faster                                                 |
| 2to3                       | 260 ms                                                       | 254 ms: 1.02x faster                                                  |
| genshi_text                | 21.5 ms                                                      | 21.1 ms: 1.02x faster                                                 |
| logging_simple             | 6.16 us                                                      | 6.03 us: 1.02x faster                                                 |
| fannkuch                   | 370 ms                                                       | 362 ms: 1.02x faster                                                  |
| sympy_sum                  | 156 ms                                                       | 153 ms: 1.02x faster                                                  |
| sqlglot_optimize           | 52.7 ms                                                      | 51.8 ms: 1.02x faster                                                 |
| logging_format             | 6.84 us                                                      | 6.74 us: 1.01x faster                                                 |
| sympy_expand               | 457 ms                                                       | 451 ms: 1.01x faster                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 67.0 ms: 1.01x faster                                                 |
| deltablue                  | 3.12 ms                                                      | 3.09 ms: 1.01x faster                                                 |
| nqueens                    | 78.6 ms                                                      | 77.7 ms: 1.01x faster                                                 |
| sympy_str                  | 275 ms                                                       | 272 ms: 1.01x faster                                                  |
| logging_silent             | 103 ns                                                       | 102 ns: 1.01x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 112 ms: 1.00x faster                                                  |
| pycparser                  | 1.12 sec                                                     | 1.11 sec: 1.00x faster                                                |
| unpickle_pure_python       | 210 us                                                       | 210 us: 1.00x slower                                                  |
| dulwich_log                | 74.8 ms                                                      | 75.1 ms: 1.00x slower                                                 |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.00x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 1.25 ms: 1.00x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 7.44 ms: 1.01x slower                                                 |
| chaos                      | 57.3 ms                                                      | 58.1 ms: 1.01x slower                                                 |
| django_template            | 34.1 ms                                                      | 34.7 ms: 1.02x slower                                                 |
| typing_runtime_protocols   | 155 us                                                       | 158 us: 1.02x slower                                                  |
| regex_v8                   | 22.7 ms                                                      | 23.2 ms: 1.02x slower                                                 |
| mako                       | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                 |
| comprehensions             | 16.5 us                                                      | 16.9 us: 1.03x slower                                                 |
| raytrace                   | 253 ms                                                       | 260 ms: 1.03x slower                                                  |
| mdp                        | 2.36 sec                                                     | 2.45 sec: 1.04x slower                                                |
| pickle_pure_python         | 294 us                                                       | 308 us: 1.05x slower                                                  |
| nbody                      | 85.1 ms                                                      | 89.9 ms: 1.06x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 11.3 ms: 1.07x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.03 ms: 1.12x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.17 ms: 1.33x slower                                                 |
| python_startup             | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.82 ms: 1.36x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 88.6 ms: 8.06x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.03x faster                                                          |

Benchmark hidden because not significant (4): genshi_xml, sympy_integrate, sqlite_synth, sqlglot_transpile
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241220-3.14.0a3+-d6d4c73/bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.058x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.10x