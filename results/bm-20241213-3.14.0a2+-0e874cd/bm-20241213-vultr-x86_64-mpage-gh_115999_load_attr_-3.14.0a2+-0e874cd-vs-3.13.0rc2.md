# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: 0e874cd
- commit date: 2024-12-13
- overall geometric mean: 1.048x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 255 ms: 1.02x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.55 sec: 1.03x faster                                                |
| Geometric mean | (ref)                                                        | 1.02x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 619 ms: 1.47x faster                                                  |
| async_tree_io              | 876 ms                                                       | 629 ms: 1.39x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 338 ms: 1.36x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 308 ms: 1.34x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 505 ms: 1.32x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 257 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 488 ms: 1.31x faster                                                  |
| async_tree_none            | 354 ms                                                       | 281 ms: 1.26x faster                                                  |
| async_generators           | 377 ms                                                       | 352 ms: 1.07x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 22.2 ms: 1.06x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.00x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.25x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 185 ms: 1.17x faster                                                  |
| float          | 77.5 ms                                                      | 76.5 ms: 1.01x faster                                                 |
| nbody          | 85.1 ms                                                      | 89.6 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                        | 1.04x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.73 ms: 1.13x faster                                                 |
| regex_compile  | 132 ms                                                       | 127 ms: 1.04x faster                                                  |
| regex_dna      | 180 ms                                                       | 176 ms: 1.02x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 24.7 ms: 1.09x slower                                                 |
| Geometric mean | (ref)                                                        | 1.03x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.07x faster                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 90.2 ms: 1.05x faster                                                 |
| json_loads           | 27.0 us                                                      | 26.1 us: 1.04x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 83.1 ms: 1.03x faster                                                 |
| xml_etree_process    | 59.3 ms                                                      | 58.0 ms: 1.02x faster                                                 |
| tomli_loads          | 2.01 sec                                                     | 1.98 sec: 1.02x faster                                                |
| unpickle_pure_python | 210 us                                                       | 211 us: 1.00x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 315 us: 1.07x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 11.4 ms: 1.09x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.53 ms: 1.02x slower                                                 |
| python_startup         | 11.0 ms                                                      | 14.7 ms: 1.34x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.17x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 11.6 ms: 1.02x slower                                                 |
| genshi_text     | 21.5 ms                                                      | 22.1 ms: 1.02x slower                                                 |
| django_template | 34.1 ms                                                      | 35.0 ms: 1.03x slower                                                 |
| genshi_xml      | 48.8 ms                                                      | 50.0 ms: 1.03x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 619 ms: 1.47x faster                                                  |
| deepcopy                   | 355 us                                                       | 251 us: 1.42x faster                                                  |
| async_tree_io              | 876 ms                                                       | 629 ms: 1.39x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 338 ms: 1.36x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 28.9 us: 1.35x faster                                                 |
| async_tree_memoization_tg  | 414 ms                                                       | 308 ms: 1.34x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 505 ms: 1.32x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 257 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 488 ms: 1.31x faster                                                  |
| async_tree_none            | 354 ms                                                       | 281 ms: 1.26x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.55 us: 1.22x faster                                                 |
| go                         | 141 ms                                                       | 116 ms: 1.21x faster                                                  |
| pidigits                   | 217 ms                                                       | 185 ms: 1.17x faster                                                  |
| scimark_fft                | 349 ms                                                       | 308 ms: 1.13x faster                                                  |
| pylint                     | 317 ms                                                       | 280 ms: 1.13x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.73 ms: 1.13x faster                                                 |
| spectral_norm              | 111 ms                                                       | 99.1 ms: 1.12x faster                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.23 ms: 1.11x faster                                                 |
| scimark_sor                | 134 ms                                                       | 124 ms: 1.09x faster                                                  |
| async_generators           | 377 ms                                                       | 352 ms: 1.07x faster                                                  |
| telco                      | 7.82 ms                                                      | 7.30 ms: 1.07x faster                                                 |
| generators                 | 28.8 ms                                                      | 27.0 ms: 1.07x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.07x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 22.2 ms: 1.06x faster                                                 |
| thrift                     | 778 us                                                       | 734 us: 1.06x faster                                                  |
| pyflate                    | 449 ms                                                       | 424 ms: 1.06x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 18.2 ms: 1.05x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.2 ms: 1.05x faster                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 62.3 ms: 1.05x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 704 ms: 1.05x faster                                                  |
| coverage                   | 83.0 ms                                                      | 79.4 ms: 1.05x faster                                                 |
| richards_super             | 51.6 ms                                                      | 49.5 ms: 1.04x faster                                                 |
| regex_compile              | 132 ms                                                       | 127 ms: 1.04x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.27 sec: 1.04x faster                                                |
| richards                   | 45.2 ms                                                      | 43.6 ms: 1.04x faster                                                 |
| json_loads                 | 27.0 us                                                      | 26.1 us: 1.04x faster                                                 |
| sqlglot_normalize          | 106 ms                                                       | 102 ms: 1.03x faster                                                  |
| json                       | 4.93 ms                                                      | 4.76 ms: 1.03x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.80 ms: 1.03x faster                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.45 sec: 1.03x faster                                                |
| xml_etree_generate         | 85.4 ms                                                      | 83.1 ms: 1.03x faster                                                 |
| meteor_contest             | 102 ms                                                       | 99.0 ms: 1.03x faster                                                 |
| docutils                   | 2.62 sec                                                     | 2.55 sec: 1.03x faster                                                |
| xml_etree_process          | 59.3 ms                                                      | 58.0 ms: 1.02x faster                                                 |
| sympy_sum                  | 156 ms                                                       | 152 ms: 1.02x faster                                                  |
| regex_dna                  | 180 ms                                                       | 176 ms: 1.02x faster                                                  |
| sqlglot_optimize           | 52.7 ms                                                      | 51.7 ms: 1.02x faster                                                 |
| 2to3                       | 260 ms                                                       | 255 ms: 1.02x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.98 sec: 1.02x faster                                                |
| nqueens                    | 78.6 ms                                                      | 77.4 ms: 1.01x faster                                                 |
| float                      | 77.5 ms                                                      | 76.5 ms: 1.01x faster                                                 |
| sympy_str                  | 275 ms                                                       | 271 ms: 1.01x faster                                                  |
| typing_runtime_protocols   | 155 us                                                       | 153 us: 1.01x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 112 ms: 1.01x faster                                                  |
| fannkuch                   | 370 ms                                                       | 367 ms: 1.01x faster                                                  |
| sympy_integrate            | 19.8 ms                                                      | 19.7 ms: 1.00x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.00x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 211 us: 1.00x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.12 sec: 1.01x slower                                                |
| dulwich_log                | 74.8 ms                                                      | 75.5 ms: 1.01x slower                                                 |
| sqlglot_transpile          | 1.56 ms                                                      | 1.57 ms: 1.01x slower                                                 |
| raytrace                   | 253 ms                                                       | 256 ms: 1.01x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 1.27 ms: 1.01x slower                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 68.9 ms: 1.02x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 7.53 ms: 1.02x slower                                                 |
| mako                       | 11.3 ms                                                      | 11.6 ms: 1.02x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.18 ms: 1.02x slower                                                 |
| genshi_text                | 21.5 ms                                                      | 22.1 ms: 1.02x slower                                                 |
| django_template            | 34.1 ms                                                      | 35.0 ms: 1.03x slower                                                 |
| genshi_xml                 | 48.8 ms                                                      | 50.0 ms: 1.03x slower                                                 |
| logging_silent             | 103 ns                                                       | 106 ns: 1.03x slower                                                  |
| comprehensions             | 16.5 us                                                      | 17.1 us: 1.04x slower                                                 |
| nbody                      | 85.1 ms                                                      | 89.6 ms: 1.05x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 315 us: 1.07x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 11.4 ms: 1.09x slower                                                 |
| regex_v8                   | 22.7 ms                                                      | 24.7 ms: 1.09x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.03 ms: 1.12x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.19 ms: 1.33x slower                                                 |
| python_startup             | 11.0 ms                                                      | 14.7 ms: 1.34x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.84 ms: 1.37x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 89.2 ms: 8.11x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.02x faster                                                          |

Benchmark hidden because not significant (6): logging_simple, logging_format, sqlite_synth, mdp, sympy_expand, chaos
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241213-3.14.0a2+-0e874cd/bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.048x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.10x