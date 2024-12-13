# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: 39cab3f
- commit date: 2024-12-12
- overall geometric mean: 1.041x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 253 ms: 1.03x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.53 sec: 1.03x faster                                                |
| Geometric mean | (ref)                                                        | 1.03x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 606 ms: 1.51x faster                                                  |
| async_tree_io              | 876 ms                                                       | 619 ms: 1.41x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 332 ms: 1.39x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 305 ms: 1.36x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 256 ms: 1.32x faster                                                  |
| async_tree_none            | 354 ms                                                       | 276 ms: 1.28x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 599 ms: 1.11x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 21.4 ms: 1.10x faster                                                 |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 580 ms: 1.10x faster                                                  |
| async_generators           | 377 ms                                                       | 362 ms: 1.04x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.01x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.23x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 76.3 ms: 1.02x faster                                                 |
| pidigits       | 217 ms                                                       | 225 ms: 1.04x slower                                                  |
| nbody          | 85.1 ms                                                      | 89.8 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                        | 1.03x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.73 ms: 1.13x faster                                                 |
| regex_dna      | 180 ms                                                       | 168 ms: 1.07x faster                                                  |
| regex_compile  | 132 ms                                                       | 128 ms: 1.04x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 23.0 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                        | 1.06x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|---------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse     | 136 ms                                                       | 129 ms: 1.06x faster                                                  |
| xml_etree_iterparse | 94.9 ms                                                      | 90.2 ms: 1.05x faster                                                 |
| json_loads          | 27.0 us                                                      | 25.9 us: 1.04x faster                                                 |
| xml_etree_generate  | 85.4 ms                                                      | 83.5 ms: 1.02x faster                                                 |
| xml_etree_process   | 59.3 ms                                                      | 58.8 ms: 1.01x faster                                                 |
| tomli_loads         | 2.01 sec                                                     | 2.08 sec: 1.04x slower                                                |
| json_dumps          | 10.5 ms                                                      | 11.2 ms: 1.07x slower                                                 |
| pickle_pure_python  | 294 us                                                       | 315 us: 1.07x slower                                                  |
| Geometric mean      | (ref)                                                        | 1.00x faster                                                          |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.47 ms: 1.01x slower                                                 |
| python_startup         | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.16x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.3 ms: 1.01x faster                                                 |
| genshi_xml      | 48.8 ms                                                      | 49.5 ms: 1.01x slower                                                 |
| django_template | 34.1 ms                                                      | 35.3 ms: 1.03x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.01x slower                                                          |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 606 ms: 1.51x faster                                                  |
| deepcopy                   | 355 us                                                       | 251 us: 1.42x faster                                                  |
| async_tree_io              | 876 ms                                                       | 619 ms: 1.41x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 332 ms: 1.39x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 305 ms: 1.36x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 29.2 us: 1.34x faster                                                 |
| async_tree_none_tg         | 336 ms                                                       | 256 ms: 1.32x faster                                                  |
| async_tree_none            | 354 ms                                                       | 276 ms: 1.28x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.54 us: 1.22x faster                                                 |
| go                         | 141 ms                                                       | 118 ms: 1.19x faster                                                  |
| pylint                     | 317 ms                                                       | 278 ms: 1.14x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.73 ms: 1.13x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 599 ms: 1.11x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 21.4 ms: 1.10x faster                                                 |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 580 ms: 1.10x faster                                                  |
| telco                      | 7.82 ms                                                      | 7.17 ms: 1.09x faster                                                 |
| generators                 | 28.8 ms                                                      | 26.7 ms: 1.08x faster                                                 |
| regex_dna                  | 180 ms                                                       | 168 ms: 1.07x faster                                                  |
| thrift                     | 778 us                                                       | 733 us: 1.06x faster                                                  |
| scimark_fft                | 349 ms                                                       | 330 ms: 1.06x faster                                                  |
| coverage                   | 83.0 ms                                                      | 78.5 ms: 1.06x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.06x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.21 sec: 1.06x faster                                                |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.2 ms: 1.05x faster                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.48 ms: 1.05x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 703 ms: 1.05x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 18.3 ms: 1.05x faster                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.43 sec: 1.05x faster                                                |
| json_loads                 | 27.0 us                                                      | 25.9 us: 1.04x faster                                                 |
| spectral_norm              | 111 ms                                                       | 106 ms: 1.04x faster                                                  |
| async_generators           | 377 ms                                                       | 362 ms: 1.04x faster                                                  |
| json                       | 4.93 ms                                                      | 4.73 ms: 1.04x faster                                                 |
| logging_simple             | 6.16 us                                                      | 5.93 us: 1.04x faster                                                 |
| regex_compile              | 132 ms                                                       | 128 ms: 1.04x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.53 sec: 1.03x faster                                                |
| scimark_monte_carlo        | 65.4 ms                                                      | 63.4 ms: 1.03x faster                                                 |
| sympy_sum                  | 156 ms                                                       | 151 ms: 1.03x faster                                                  |
| scimark_sor                | 134 ms                                                       | 131 ms: 1.03x faster                                                  |
| 2to3                       | 260 ms                                                       | 253 ms: 1.03x faster                                                  |
| sympy_str                  | 275 ms                                                       | 268 ms: 1.02x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.68 us: 1.02x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 83.5 ms: 1.02x faster                                                 |
| sqlglot_normalize          | 106 ms                                                       | 103 ms: 1.02x faster                                                  |
| hexiom                     | 5.99 ms                                                      | 5.87 ms: 1.02x faster                                                 |
| meteor_contest             | 102 ms                                                       | 99.5 ms: 1.02x faster                                                 |
| richards_super             | 51.6 ms                                                      | 50.8 ms: 1.02x faster                                                 |
| pyflate                    | 449 ms                                                       | 442 ms: 1.02x faster                                                  |
| float                      | 77.5 ms                                                      | 76.3 ms: 1.02x faster                                                 |
| scimark_lu                 | 113 ms                                                       | 111 ms: 1.01x faster                                                  |
| genshi_text                | 21.5 ms                                                      | 21.3 ms: 1.01x faster                                                 |
| mdp                        | 2.36 sec                                                     | 2.33 sec: 1.01x faster                                                |
| richards                   | 45.2 ms                                                      | 44.7 ms: 1.01x faster                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 67.1 ms: 1.01x faster                                                 |
| sqlglot_optimize           | 52.7 ms                                                      | 52.2 ms: 1.01x faster                                                 |
| sympy_expand               | 457 ms                                                       | 453 ms: 1.01x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 58.8 ms: 1.01x faster                                                 |
| sympy_integrate            | 19.8 ms                                                      | 19.7 ms: 1.01x faster                                                 |
| pycparser                  | 1.12 sec                                                     | 1.11 sec: 1.01x faster                                                |
| sqlglot_transpile          | 1.56 ms                                                      | 1.57 ms: 1.00x slower                                                 |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.01x slower                                                  |
| chaos                      | 57.3 ms                                                      | 57.7 ms: 1.01x slower                                                 |
| fannkuch                   | 370 ms                                                       | 372 ms: 1.01x slower                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.23 us: 1.01x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 7.47 ms: 1.01x slower                                                 |
| sqlglot_parse              | 1.25 ms                                                      | 1.26 ms: 1.01x slower                                                 |
| regex_v8                   | 22.7 ms                                                      | 23.0 ms: 1.01x slower                                                 |
| genshi_xml                 | 48.8 ms                                                      | 49.5 ms: 1.01x slower                                                 |
| logging_silent             | 103 ns                                                       | 105 ns: 1.02x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.22 ms: 1.03x slower                                                 |
| comprehensions             | 16.5 us                                                      | 17.0 us: 1.03x slower                                                 |
| django_template            | 34.1 ms                                                      | 35.3 ms: 1.03x slower                                                 |
| raytrace                   | 253 ms                                                       | 261 ms: 1.03x slower                                                  |
| tomli_loads                | 2.01 sec                                                     | 2.08 sec: 1.04x slower                                                |
| pidigits                   | 217 ms                                                       | 225 ms: 1.04x slower                                                  |
| nbody                      | 85.1 ms                                                      | 89.8 ms: 1.06x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 11.2 ms: 1.07x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 315 us: 1.07x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.03 ms: 1.12x slower                                                 |
| python_startup             | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.21 ms: 1.34x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.84 ms: 1.38x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 88.7 ms: 8.06x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.02x faster                                                          |

Benchmark hidden because not significant (5): dulwich_log, nqueens, mako, unpickle_pure_python, typing_runtime_protocols
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241212-3.14.0a2+-39cab3f/bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.041x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.09x