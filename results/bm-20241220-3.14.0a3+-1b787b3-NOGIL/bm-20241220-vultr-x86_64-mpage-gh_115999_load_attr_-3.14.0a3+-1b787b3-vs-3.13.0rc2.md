# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: 1b787b3
- commit date: 2024-12-20
- overall geometric mean: 1.115x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-1b787b3 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 322 ms: 1.24x slower                                                  |
| docutils       | 2.62 sec                                                     | 2.85 sec: 1.09x slower                                                |
| html5lib       | 67.0 ms                                                      | 73.7 ms: 1.10x slower                                                 |
| Geometric mean | (ref)                                                        | 1.14x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-1b787b3 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 591 ms: 1.55x faster                                                  |
| async_tree_io              | 876 ms                                                       | 606 ms: 1.45x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 239 ms: 1.41x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 311 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 483 ms: 1.32x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 349 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 520 ms: 1.28x faster                                                  |
| async_tree_none            | 354 ms                                                       | 284 ms: 1.25x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 24.4 ms: 1.04x slower                                                 |
| async_generators           | 377 ms                                                       | 414 ms: 1.10x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.24x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-1b787b3 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 184 ms: 1.18x faster                                                  |
| float          | 77.5 ms                                                      | 81.3 ms: 1.05x slower                                                 |
| nbody          | 85.1 ms                                                      | 130 ms: 1.53x slower                                                  |
| Geometric mean | (ref)                                                        | 1.11x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-1b787b3 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.68 ms: 1.15x faster                                                 |
| regex_dna      | 180 ms                                                       | 172 ms: 1.05x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 23.5 ms: 1.03x slower                                                 |
| regex_compile  | 132 ms                                                       | 150 ms: 1.14x slower                                                  |
| Geometric mean | (ref)                                                        | 1.01x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-1b787b3 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 88.3 ms: 1.08x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.05x faster                                                  |
| json_loads           | 27.0 us                                                      | 28.1 us: 1.04x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 96.0 ms: 1.12x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 68.2 ms: 1.15x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 254 us: 1.21x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 13.1 ms: 1.24x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 370 us: 1.26x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.52 sec: 1.26x slower                                                |
| Geometric mean       | (ref)                                                        | 1.12x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-1b787b3 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.2 ms: 1.37x slower                                                 |
| python_startup         | 11.0 ms                                                      | 17.1 ms: 1.55x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.46x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-1b787b3 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 60.0 ms: 1.23x slower                                                 |
| django_template | 34.1 ms                                                      | 42.4 ms: 1.24x slower                                                 |
| genshi_text     | 21.5 ms                                                      | 28.3 ms: 1.31x slower                                                 |
| mako            | 11.3 ms                                                      | 15.6 ms: 1.38x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.29x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-1b787b3 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 591 ms: 1.55x faster                                                  |
| async_tree_io              | 876 ms                                                       | 606 ms: 1.45x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 239 ms: 1.41x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 311 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 483 ms: 1.32x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 349 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 520 ms: 1.28x faster                                                  |
| async_tree_none            | 354 ms                                                       | 284 ms: 1.25x faster                                                  |
| pidigits                   | 217 ms                                                       | 184 ms: 1.18x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.68 ms: 1.15x faster                                                 |
| deepcopy                   | 355 us                                                       | 311 us: 1.14x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 88.3 ms: 1.08x faster                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.07 us: 1.07x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.05x faster                                                  |
| regex_dna                  | 180 ms                                                       | 172 ms: 1.05x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 18.8 ms: 1.02x faster                                                 |
| deepcopy_memo              | 39.1 us                                                      | 38.4 us: 1.02x faster                                                 |
| spectral_norm              | 111 ms                                                       | 113 ms: 1.01x slower                                                  |
| go                         | 141 ms                                                       | 143 ms: 1.02x slower                                                  |
| regex_v8                   | 22.7 ms                                                      | 23.5 ms: 1.03x slower                                                 |
| coroutines                 | 23.6 ms                                                      | 24.4 ms: 1.04x slower                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 3.23 us: 1.04x slower                                                 |
| json_loads                 | 27.0 us                                                      | 28.1 us: 1.04x slower                                                 |
| float                      | 77.5 ms                                                      | 81.3 ms: 1.05x slower                                                 |
| generators                 | 28.8 ms                                                      | 30.5 ms: 1.06x slower                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.76 sec: 1.07x slower                                                |
| pylint                     | 317 ms                                                       | 344 ms: 1.09x slower                                                  |
| telco                      | 7.82 ms                                                      | 8.50 ms: 1.09x slower                                                 |
| docutils                   | 2.62 sec                                                     | 2.85 sec: 1.09x slower                                                |
| pycparser                  | 1.12 sec                                                     | 1.22 sec: 1.09x slower                                                |
| scimark_fft                | 349 ms                                                       | 383 ms: 1.10x slower                                                  |
| async_generators           | 377 ms                                                       | 414 ms: 1.10x slower                                                  |
| logging_silent             | 103 ns                                                       | 113 ns: 1.10x slower                                                  |
| dulwich_log                | 74.8 ms                                                      | 82.3 ms: 1.10x slower                                                 |
| html5lib                   | 67.0 ms                                                      | 73.7 ms: 1.10x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 3.49 ms: 1.11x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 96.0 ms: 1.12x slower                                                 |
| regex_compile              | 132 ms                                                       | 150 ms: 1.14x slower                                                  |
| sqlglot_normalize          | 106 ms                                                       | 121 ms: 1.14x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 68.2 ms: 1.15x slower                                                 |
| pyflate                    | 449 ms                                                       | 516 ms: 1.15x slower                                                  |
| pprint_safe_repr           | 738 ms                                                       | 850 ms: 1.15x slower                                                  |
| sqlglot_optimize           | 52.7 ms                                                      | 60.9 ms: 1.16x slower                                                 |
| thrift                     | 778 us                                                       | 905 us: 1.16x slower                                                  |
| logging_simple             | 6.16 us                                                      | 7.21 us: 1.17x slower                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.75 sec: 1.17x slower                                                |
| mdp                        | 2.36 sec                                                     | 2.78 sec: 1.18x slower                                                |
| scimark_sor                | 134 ms                                                       | 161 ms: 1.20x slower                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.67 ms: 1.20x slower                                                 |
| coverage                   | 83.0 ms                                                      | 100.0 ms: 1.20x slower                                                |
| logging_format             | 6.84 us                                                      | 8.27 us: 1.21x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 254 us: 1.21x slower                                                  |
| richards                   | 45.2 ms                                                      | 54.8 ms: 1.21x slower                                                 |
| genshi_xml                 | 48.8 ms                                                      | 60.0 ms: 1.23x slower                                                 |
| richards_super             | 51.6 ms                                                      | 63.8 ms: 1.24x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 97.1 ms: 1.24x slower                                                 |
| sqlglot_transpile          | 1.56 ms                                                      | 1.93 ms: 1.24x slower                                                 |
| chaos                      | 57.3 ms                                                      | 71.0 ms: 1.24x slower                                                 |
| 2to3                       | 260 ms                                                       | 322 ms: 1.24x slower                                                  |
| django_template            | 34.1 ms                                                      | 42.4 ms: 1.24x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 13.1 ms: 1.24x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 370 us: 1.26x slower                                                  |
| tomli_loads                | 2.01 sec                                                     | 2.52 sec: 1.26x slower                                                |
| scimark_lu                 | 113 ms                                                       | 142 ms: 1.26x slower                                                  |
| raytrace                   | 253 ms                                                       | 322 ms: 1.27x slower                                                  |
| meteor_contest             | 102 ms                                                       | 130 ms: 1.28x slower                                                  |
| hexiom                     | 5.99 ms                                                      | 7.66 ms: 1.28x slower                                                 |
| typing_runtime_protocols   | 155 us                                                       | 199 us: 1.28x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 1.60 ms: 1.28x slower                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 87.5 ms: 1.29x slower                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 84.6 ms: 1.29x slower                                                 |
| comprehensions             | 16.5 us                                                      | 21.4 us: 1.30x slower                                                 |
| genshi_text                | 21.5 ms                                                      | 28.3 ms: 1.31x slower                                                 |
| fannkuch                   | 370 ms                                                       | 489 ms: 1.32x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.82 ms: 1.36x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 10.2 ms: 1.37x slower                                                 |
| mako                       | 11.3 ms                                                      | 15.6 ms: 1.38x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 28.7 ms: 1.45x slower                                                 |
| nbody                      | 85.1 ms                                                      | 130 ms: 1.53x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 4.82 ms: 1.54x slower                                                 |
| python_startup             | 11.0 ms                                                      | 17.1 ms: 1.55x slower                                                 |
| sympy_str                  | 275 ms                                                       | 458 ms: 1.67x slower                                                  |
| sympy_expand               | 457 ms                                                       | 926 ms: 2.03x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 341 ms: 2.19x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 3.33 ms: 3.62x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 105 ms: 9.59x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.17x slower                                                          |

Benchmark hidden because not significant (2): asyncio_websockets, json
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241220-3.14.0a3+-1b787b3-NOGIL/bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-1b787b3.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.115x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.33x