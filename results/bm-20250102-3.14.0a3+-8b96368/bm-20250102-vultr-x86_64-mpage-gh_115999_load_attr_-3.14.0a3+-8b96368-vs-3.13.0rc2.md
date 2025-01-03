# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: 8b96368
- commit date: 2025-01-02
- overall geometric mean: 1.060x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 254 ms: 1.02x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.55 sec: 1.03x faster                                                |
| Geometric mean | (ref)                                                        | 1.02x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 604 ms: 1.51x faster                                                  |
| async_tree_io              | 876 ms                                                       | 608 ms: 1.44x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 321 ms: 1.43x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 295 ms: 1.40x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 483 ms: 1.38x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 464 ms: 1.37x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 248 ms: 1.35x faster                                                  |
| async_tree_none            | 354 ms                                                       | 267 ms: 1.32x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 21.0 ms: 1.12x faster                                                 |
| async_generators           | 377 ms                                                       | 352 ms: 1.07x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.01x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.30x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 184 ms: 1.18x faster                                                  |
| float          | 77.5 ms                                                      | 72.4 ms: 1.07x faster                                                 |
| nbody          | 85.1 ms                                                      | 91.4 ms: 1.07x slower                                                 |
| Geometric mean | (ref)                                                        | 1.05x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.74 ms: 1.13x faster                                                 |
| regex_dna      | 180 ms                                                       | 169 ms: 1.06x faster                                                  |
| regex_compile  | 132 ms                                                       | 128 ms: 1.04x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 23.9 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                        | 1.04x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.07x faster                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 90.6 ms: 1.05x faster                                                 |
| json_loads           | 27.0 us                                                      | 26.0 us: 1.04x faster                                                 |
| tomli_loads          | 2.01 sec                                                     | 1.93 sec: 1.04x faster                                                |
| xml_etree_process    | 59.3 ms                                                      | 57.6 ms: 1.03x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 83.2 ms: 1.03x faster                                                 |
| unpickle_pure_python | 210 us                                                       | 209 us: 1.00x faster                                                  |
| pickle_pure_python   | 294 us                                                       | 310 us: 1.05x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 11.2 ms: 1.07x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.48 ms: 1.01x slower                                                 |
| python_startup         | 11.0 ms                                                      | 14.7 ms: 1.34x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.16x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.0 ms: 1.03x faster                                                 |
| genshi_xml      | 48.8 ms                                                      | 48.0 ms: 1.01x faster                                                 |
| django_template | 34.1 ms                                                      | 34.6 ms: 1.01x slower                                                 |
| mako            | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.00x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 604 ms: 1.51x faster                                                  |
| async_tree_io              | 876 ms                                                       | 608 ms: 1.44x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 321 ms: 1.43x faster                                                  |
| deepcopy                   | 355 us                                                       | 250 us: 1.42x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 295 ms: 1.40x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 483 ms: 1.38x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 464 ms: 1.37x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 248 ms: 1.35x faster                                                  |
| async_tree_none            | 354 ms                                                       | 267 ms: 1.32x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 29.8 us: 1.31x faster                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 2.56 us: 1.21x faster                                                 |
| go                         | 141 ms                                                       | 118 ms: 1.19x faster                                                  |
| scimark_sor                | 134 ms                                                       | 114 ms: 1.18x faster                                                  |
| pidigits                   | 217 ms                                                       | 184 ms: 1.18x faster                                                  |
| spectral_norm              | 111 ms                                                       | 96.0 ms: 1.16x faster                                                 |
| pylint                     | 317 ms                                                       | 279 ms: 1.14x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.74 ms: 1.13x faster                                                 |
| coroutines                 | 23.6 ms                                                      | 21.0 ms: 1.12x faster                                                 |
| scimark_fft                | 349 ms                                                       | 315 ms: 1.11x faster                                                  |
| pyflate                    | 449 ms                                                       | 414 ms: 1.08x faster                                                  |
| thrift                     | 778 us                                                       | 723 us: 1.08x faster                                                  |
| telco                      | 7.82 ms                                                      | 7.30 ms: 1.07x faster                                                 |
| richards                   | 45.2 ms                                                      | 42.2 ms: 1.07x faster                                                 |
| async_generators           | 377 ms                                                       | 352 ms: 1.07x faster                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.40 ms: 1.07x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 689 ms: 1.07x faster                                                  |
| float                      | 77.5 ms                                                      | 72.4 ms: 1.07x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.07x faster                                                  |
| regex_dna                  | 180 ms                                                       | 169 ms: 1.06x faster                                                  |
| richards_super             | 51.6 ms                                                      | 48.6 ms: 1.06x faster                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.41 sec: 1.06x faster                                                |
| pathlib                    | 19.2 ms                                                      | 18.1 ms: 1.06x faster                                                 |
| coverage                   | 83.0 ms                                                      | 78.6 ms: 1.06x faster                                                 |
| generators                 | 28.8 ms                                                      | 27.4 ms: 1.05x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.6 ms: 1.05x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.26 sec: 1.04x faster                                                |
| json                       | 4.93 ms                                                      | 4.73 ms: 1.04x faster                                                 |
| json_loads                 | 27.0 us                                                      | 26.0 us: 1.04x faster                                                 |
| tomli_loads                | 2.01 sec                                                     | 1.93 sec: 1.04x faster                                                |
| regex_compile              | 132 ms                                                       | 128 ms: 1.04x faster                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 63.0 ms: 1.04x faster                                                 |
| sqlglot_normalize          | 106 ms                                                       | 102 ms: 1.03x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 57.6 ms: 1.03x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 83.2 ms: 1.03x faster                                                 |
| docutils                   | 2.62 sec                                                     | 2.55 sec: 1.03x faster                                                |
| hexiom                     | 5.99 ms                                                      | 5.84 ms: 1.03x faster                                                 |
| genshi_text                | 21.5 ms                                                      | 21.0 ms: 1.03x faster                                                 |
| logging_simple             | 6.16 us                                                      | 6.02 us: 1.02x faster                                                 |
| 2to3                       | 260 ms                                                       | 254 ms: 1.02x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.72 us: 1.02x faster                                                 |
| sqlglot_optimize           | 52.7 ms                                                      | 51.9 ms: 1.02x faster                                                 |
| meteor_contest             | 102 ms                                                       | 100.0 ms: 1.02x faster                                                |
| sqlglot_transpile          | 1.56 ms                                                      | 1.54 ms: 1.02x faster                                                 |
| genshi_xml                 | 48.8 ms                                                      | 48.0 ms: 1.01x faster                                                 |
| sqlglot_parse              | 1.25 ms                                                      | 1.23 ms: 1.01x faster                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 66.9 ms: 1.01x faster                                                 |
| mdp                        | 2.36 sec                                                     | 2.32 sec: 1.01x faster                                                |
| sympy_sum                  | 156 ms                                                       | 154 ms: 1.01x faster                                                  |
| pycparser                  | 1.12 sec                                                     | 1.11 sec: 1.01x faster                                                |
| nqueens                    | 78.6 ms                                                      | 77.8 ms: 1.01x faster                                                 |
| fannkuch                   | 370 ms                                                       | 366 ms: 1.01x faster                                                  |
| sympy_str                  | 275 ms                                                       | 272 ms: 1.01x faster                                                  |
| unpickle_pure_python       | 210 us                                                       | 209 us: 1.00x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 112 ms: 1.00x faster                                                  |
| sympy_integrate            | 19.8 ms                                                      | 19.8 ms: 1.00x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.01x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.14 ms: 1.01x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 7.48 ms: 1.01x slower                                                 |
| django_template            | 34.1 ms                                                      | 34.6 ms: 1.01x slower                                                 |
| chaos                      | 57.3 ms                                                      | 58.1 ms: 1.01x slower                                                 |
| raytrace                   | 253 ms                                                       | 258 ms: 1.02x slower                                                  |
| comprehensions             | 16.5 us                                                      | 17.0 us: 1.03x slower                                                 |
| mako                       | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                 |
| regex_v8                   | 22.7 ms                                                      | 23.9 ms: 1.05x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 310 us: 1.05x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 11.2 ms: 1.07x slower                                                 |
| nbody                      | 85.1 ms                                                      | 91.4 ms: 1.07x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.04 ms: 1.13x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.19 ms: 1.33x slower                                                 |
| python_startup             | 11.0 ms                                                      | 14.7 ms: 1.34x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.83 ms: 1.37x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 89.0 ms: 8.09x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.03x faster                                                          |

Benchmark hidden because not significant (5): logging_silent, sqlite_synth, dulwich_log, typing_runtime_protocols, sympy_expand
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250102-3.14.0a3+-8b96368/bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.060x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.10x