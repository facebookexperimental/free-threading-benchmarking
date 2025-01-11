# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: 7ab3ec6
- commit date: 2025-01-10
- overall geometric mean: 1.062x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 253 ms: 1.03x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.55 sec: 1.03x faster                                                |
| Geometric mean | (ref)                                                        | 1.03x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 598 ms: 1.53x faster                                                  |
| async_tree_io              | 876 ms                                                       | 601 ms: 1.46x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 320 ms: 1.44x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 297 ms: 1.40x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 486 ms: 1.37x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 469 ms: 1.36x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 250 ms: 1.35x faster                                                  |
| async_tree_none            | 354 ms                                                       | 266 ms: 1.33x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 21.1 ms: 1.12x faster                                                 |
| async_generators           | 377 ms                                                       | 357 ms: 1.06x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 522 ms: 1.00x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.30x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 184 ms: 1.18x faster                                                  |
| float          | 77.5 ms                                                      | 71.7 ms: 1.08x faster                                                 |
| nbody          | 85.1 ms                                                      | 88.2 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                        | 1.07x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.79 ms: 1.10x faster                                                 |
| regex_compile  | 132 ms                                                       | 125 ms: 1.05x faster                                                  |
| regex_dna      | 180 ms                                                       | 179 ms: 1.01x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 24.3 ms: 1.07x slower                                                 |
| Geometric mean | (ref)                                                        | 1.02x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 127 ms: 1.07x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 1.89 sec: 1.06x faster                                                |
| json_loads           | 27.0 us                                                      | 25.6 us: 1.06x faster                                                 |
| xml_etree_iterparse  | 94.9 ms                                                      | 90.3 ms: 1.05x faster                                                 |
| xml_etree_process    | 59.3 ms                                                      | 57.5 ms: 1.03x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 83.1 ms: 1.03x faster                                                 |
| unpickle_pure_python | 210 us                                                       | 211 us: 1.01x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 305 us: 1.04x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 11.4 ms: 1.08x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.02x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.48 ms: 1.01x slower                                                 |
| python_startup         | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.16x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.1 ms: 1.02x faster                                                 |
| genshi_xml      | 48.8 ms                                                      | 48.3 ms: 1.01x faster                                                 |
| django_template | 34.1 ms                                                      | 34.8 ms: 1.02x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.00x faster                                                          |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 598 ms: 1.53x faster                                                  |
| async_tree_io              | 876 ms                                                       | 601 ms: 1.46x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 320 ms: 1.44x faster                                                  |
| deepcopy                   | 355 us                                                       | 251 us: 1.41x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 297 ms: 1.40x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 486 ms: 1.37x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 469 ms: 1.36x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 250 ms: 1.35x faster                                                  |
| async_tree_none            | 354 ms                                                       | 266 ms: 1.33x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 29.4 us: 1.33x faster                                                 |
| go                         | 141 ms                                                       | 115 ms: 1.22x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.55 us: 1.22x faster                                                 |
| pidigits                   | 217 ms                                                       | 184 ms: 1.18x faster                                                  |
| scimark_sor                | 134 ms                                                       | 115 ms: 1.17x faster                                                  |
| pylint                     | 317 ms                                                       | 279 ms: 1.14x faster                                                  |
| scimark_fft                | 349 ms                                                       | 313 ms: 1.12x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 21.1 ms: 1.12x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.79 ms: 1.10x faster                                                 |
| spectral_norm              | 111 ms                                                       | 101 ms: 1.10x faster                                                  |
| float                      | 77.5 ms                                                      | 71.7 ms: 1.08x faster                                                 |
| richards_super             | 51.6 ms                                                      | 47.8 ms: 1.08x faster                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.37 ms: 1.08x faster                                                 |
| richards                   | 45.2 ms                                                      | 42.0 ms: 1.08x faster                                                 |
| pyflate                    | 449 ms                                                       | 417 ms: 1.08x faster                                                  |
| telco                      | 7.82 ms                                                      | 7.29 ms: 1.07x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 127 ms: 1.07x faster                                                  |
| generators                 | 28.8 ms                                                      | 26.9 ms: 1.07x faster                                                 |
| pathlib                    | 19.2 ms                                                      | 18.0 ms: 1.07x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 691 ms: 1.07x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.89 sec: 1.06x faster                                                |
| pprint_pformat             | 1.50 sec                                                     | 1.41 sec: 1.06x faster                                                |
| thrift                     | 778 us                                                       | 735 us: 1.06x faster                                                  |
| async_generators           | 377 ms                                                       | 357 ms: 1.06x faster                                                  |
| json_loads                 | 27.0 us                                                      | 25.6 us: 1.06x faster                                                 |
| regex_compile              | 132 ms                                                       | 125 ms: 1.05x faster                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 62.1 ms: 1.05x faster                                                 |
| json                       | 4.93 ms                                                      | 4.68 ms: 1.05x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.3 ms: 1.05x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.24 sec: 1.05x faster                                                |
| coverage                   | 83.0 ms                                                      | 79.4 ms: 1.05x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.76 ms: 1.04x faster                                                 |
| logging_simple             | 6.16 us                                                      | 5.95 us: 1.04x faster                                                 |
| xml_etree_process          | 59.3 ms                                                      | 57.5 ms: 1.03x faster                                                 |
| meteor_contest             | 102 ms                                                       | 98.6 ms: 1.03x faster                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 65.9 ms: 1.03x faster                                                 |
| docutils                   | 2.62 sec                                                     | 2.55 sec: 1.03x faster                                                |
| xml_etree_generate         | 85.4 ms                                                      | 83.1 ms: 1.03x faster                                                 |
| 2to3                       | 260 ms                                                       | 253 ms: 1.03x faster                                                  |
| sqlglot_normalize          | 106 ms                                                       | 103 ms: 1.02x faster                                                  |
| sympy_sum                  | 156 ms                                                       | 152 ms: 1.02x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 110 ms: 1.02x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.16 us: 1.02x faster                                                 |
| genshi_text                | 21.5 ms                                                      | 21.1 ms: 1.02x faster                                                 |
| mdp                        | 2.36 sec                                                     | 2.31 sec: 1.02x faster                                                |
| nqueens                    | 78.6 ms                                                      | 77.6 ms: 1.01x faster                                                 |
| sqlglot_optimize           | 52.7 ms                                                      | 52.1 ms: 1.01x faster                                                 |
| sympy_str                  | 275 ms                                                       | 271 ms: 1.01x faster                                                  |
| pycparser                  | 1.12 sec                                                     | 1.11 sec: 1.01x faster                                                |
| logging_format             | 6.84 us                                                      | 6.77 us: 1.01x faster                                                 |
| sqlglot_transpile          | 1.56 ms                                                      | 1.55 ms: 1.01x faster                                                 |
| genshi_xml                 | 48.8 ms                                                      | 48.3 ms: 1.01x faster                                                 |
| sympy_expand               | 457 ms                                                       | 453 ms: 1.01x faster                                                  |
| regex_dna                  | 180 ms                                                       | 179 ms: 1.01x faster                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 1.24 ms: 1.01x faster                                                 |
| deltablue                  | 3.12 ms                                                      | 3.11 ms: 1.01x faster                                                 |
| dulwich_log                | 74.8 ms                                                      | 74.4 ms: 1.01x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 522 ms: 1.00x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 211 us: 1.01x slower                                                  |
| raytrace                   | 253 ms                                                       | 255 ms: 1.01x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.48 ms: 1.01x slower                                                 |
| django_template            | 34.1 ms                                                      | 34.8 ms: 1.02x slower                                                 |
| fannkuch                   | 370 ms                                                       | 377 ms: 1.02x slower                                                  |
| comprehensions             | 16.5 us                                                      | 16.8 us: 1.02x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 305 us: 1.04x slower                                                  |
| nbody                      | 85.1 ms                                                      | 88.2 ms: 1.04x slower                                                 |
| regex_v8                   | 22.7 ms                                                      | 24.3 ms: 1.07x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 11.4 ms: 1.08x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.03 ms: 1.12x slower                                                 |
| python_startup             | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.20 ms: 1.34x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.84 ms: 1.37x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 88.8 ms: 8.07x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.03x faster                                                          |

Benchmark hidden because not significant (5): typing_runtime_protocols, sympy_integrate, mako, logging_silent, chaos
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250110-3.14.0a3+-7ab3ec6/bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.062x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.10x