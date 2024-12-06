# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: de73a27
- commit date: 2024-12-04
- overall geometric mean: 1.244x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.18x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 363 ms: 1.40x slower                                                  |
| docutils       | 2.62 sec                                                     | 3.08 sec: 1.18x slower                                                |
| html5lib       | 67.0 ms                                                      | 97.9 ms: 1.46x slower                                                 |
| Geometric mean | (ref)                                                        | 1.34x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 804 ms: 1.14x faster                                                  |
| async_tree_io              | 876 ms                                                       | 821 ms: 1.07x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 626 ms: 1.06x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 606 ms: 1.05x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 350 ms: 1.04x slower                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 439 ms: 1.06x slower                                                  |
| async_tree_none            | 354 ms                                                       | 379 ms: 1.07x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 25.5 ms: 1.08x slower                                                 |
| async_generators           | 377 ms                                                       | 459 ms: 1.22x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.01x slower                                                          |

Benchmark hidden because not significant (2): async_tree_memoization, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 181 ms: 1.19x faster                                                  |
| nbody          | 85.1 ms                                                      | 126 ms: 1.48x slower                                                  |
| float          | 77.5 ms                                                      | 139 ms: 1.79x slower                                                  |
| Geometric mean | (ref)                                                        | 1.30x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.89 ms: 1.07x faster                                                 |
| regex_dna      | 180 ms                                                       | 185 ms: 1.03x slower                                                  |
| regex_v8       | 22.7 ms                                                      | 24.7 ms: 1.09x slower                                                 |
| regex_compile  | 132 ms                                                       | 178 ms: 1.35x slower                                                  |
| Geometric mean | (ref)                                                        | 1.09x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 91.2 ms: 1.04x faster                                                 |
| json_loads           | 27.0 us                                                      | 28.3 us: 1.05x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 97.6 ms: 1.14x slower                                                 |
| tomli_loads          | 2.01 sec                                                     | 2.64 sec: 1.32x slower                                                |
| xml_etree_process    | 59.3 ms                                                      | 78.2 ms: 1.32x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 13.9 ms: 1.32x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 332 us: 1.58x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 512 us: 1.74x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.24x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                 |
| python_startup         | 11.0 ms                                                      | 17.2 ms: 1.57x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.48x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 62.7 ms: 1.29x slower                                                 |
| genshi_text     | 21.5 ms                                                      | 30.3 ms: 1.41x slower                                                 |
| django_template | 34.1 ms                                                      | 50.5 ms: 1.48x slower                                                 |
| mako            | 11.3 ms                                                      | 16.9 ms: 1.49x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.41x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits                   | 217 ms                                                       | 181 ms: 1.19x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 804 ms: 1.14x faster                                                  |
| deepcopy                   | 355 us                                                       | 325 us: 1.09x faster                                                  |
| async_tree_io              | 876 ms                                                       | 821 ms: 1.07x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.89 ms: 1.07x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 626 ms: 1.06x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 606 ms: 1.05x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 91.2 ms: 1.04x faster                                                 |
| json                       | 4.93 ms                                                      | 5.01 ms: 1.02x slower                                                 |
| deepcopy_memo              | 39.1 us                                                      | 40.1 us: 1.03x slower                                                 |
| regex_dna                  | 180 ms                                                       | 185 ms: 1.03x slower                                                  |
| async_tree_none_tg         | 336 ms                                                       | 350 ms: 1.04x slower                                                  |
| json_loads                 | 27.0 us                                                      | 28.3 us: 1.05x slower                                                 |
| pathlib                    | 19.2 ms                                                      | 20.1 ms: 1.05x slower                                                 |
| async_tree_memoization_tg  | 414 ms                                                       | 439 ms: 1.06x slower                                                  |
| async_tree_none            | 354 ms                                                       | 379 ms: 1.07x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 25.5 ms: 1.08x slower                                                 |
| spectral_norm              | 111 ms                                                       | 121 ms: 1.09x slower                                                  |
| regex_v8                   | 22.7 ms                                                      | 24.7 ms: 1.09x slower                                                 |
| scimark_fft                | 349 ms                                                       | 388 ms: 1.11x slower                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 3.46 us: 1.11x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 3.53 ms: 1.12x slower                                                 |
| telco                      | 7.82 ms                                                      | 8.84 ms: 1.13x slower                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 5.04 sec: 1.13x slower                                                |
| xml_etree_generate         | 85.4 ms                                                      | 97.6 ms: 1.14x slower                                                 |
| pylint                     | 317 ms                                                       | 371 ms: 1.17x slower                                                  |
| docutils                   | 2.62 sec                                                     | 3.08 sec: 1.18x slower                                                |
| mdp                        | 2.36 sec                                                     | 2.79 sec: 1.19x slower                                                |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.62 ms: 1.19x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 95.6 ms: 1.22x slower                                                 |
| async_generators           | 377 ms                                                       | 459 ms: 1.22x slower                                                  |
| coverage                   | 83.0 ms                                                      | 101 ms: 1.22x slower                                                  |
| dulwich_log                | 74.8 ms                                                      | 94.9 ms: 1.27x slower                                                 |
| sqlglot_optimize           | 52.7 ms                                                      | 67.0 ms: 1.27x slower                                                 |
| genshi_xml                 | 48.8 ms                                                      | 62.7 ms: 1.29x slower                                                 |
| sqlglot_normalize          | 106 ms                                                       | 136 ms: 1.29x slower                                                  |
| pprint_safe_repr           | 738 ms                                                       | 954 ms: 1.29x slower                                                  |
| meteor_contest             | 102 ms                                                       | 132 ms: 1.30x slower                                                  |
| tomli_loads                | 2.01 sec                                                     | 2.64 sec: 1.32x slower                                                |
| xml_etree_process          | 59.3 ms                                                      | 78.2 ms: 1.32x slower                                                 |
| typing_runtime_protocols   | 155 us                                                       | 205 us: 1.32x slower                                                  |
| fannkuch                   | 370 ms                                                       | 489 ms: 1.32x slower                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.98 sec: 1.32x slower                                                |
| json_dumps                 | 10.5 ms                                                      | 13.9 ms: 1.32x slower                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 90.5 ms: 1.33x slower                                                 |
| generators                 | 28.8 ms                                                      | 38.6 ms: 1.34x slower                                                 |
| regex_compile              | 132 ms                                                       | 178 ms: 1.35x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.52 sec: 1.36x slower                                                |
| python_startup_no_site     | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                 |
| 2to3                       | 260 ms                                                       | 363 ms: 1.40x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.87 ms: 1.40x slower                                                 |
| genshi_text                | 21.5 ms                                                      | 30.3 ms: 1.41x slower                                                 |
| html5lib                   | 67.0 ms                                                      | 97.9 ms: 1.46x slower                                                 |
| thrift                     | 778 us                                                       | 1.15 ms: 1.47x slower                                                 |
| nbody                      | 85.1 ms                                                      | 126 ms: 1.48x slower                                                  |
| django_template            | 34.1 ms                                                      | 50.5 ms: 1.48x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 29.5 ms: 1.49x slower                                                 |
| mako                       | 11.3 ms                                                      | 16.9 ms: 1.49x slower                                                 |
| pyflate                    | 449 ms                                                       | 703 ms: 1.57x slower                                                  |
| python_startup             | 11.0 ms                                                      | 17.2 ms: 1.57x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 332 us: 1.58x slower                                                  |
| logging_format             | 6.84 us                                                      | 11.0 us: 1.61x slower                                                 |
| hexiom                     | 5.99 ms                                                      | 9.82 ms: 1.64x slower                                                 |
| logging_simple             | 6.16 us                                                      | 10.2 us: 1.65x slower                                                 |
| scimark_lu                 | 113 ms                                                       | 187 ms: 1.66x slower                                                  |
| comprehensions             | 16.5 us                                                      | 27.8 us: 1.69x slower                                                 |
| richards_super             | 51.6 ms                                                      | 88.0 ms: 1.70x slower                                                 |
| sympy_str                  | 275 ms                                                       | 476 ms: 1.73x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 512 us: 1.74x slower                                                  |
| richards                   | 45.2 ms                                                      | 78.8 ms: 1.74x slower                                                 |
| scimark_sor                | 134 ms                                                       | 237 ms: 1.76x slower                                                  |
| float                      | 77.5 ms                                                      | 139 ms: 1.79x slower                                                  |
| chaos                      | 57.3 ms                                                      | 103 ms: 1.79x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 118 ms: 1.81x slower                                                  |
| logging_silent             | 103 ns                                                       | 186 ns: 1.81x slower                                                  |
| sqlglot_transpile          | 1.56 ms                                                      | 2.96 ms: 1.90x slower                                                 |
| go                         | 141 ms                                                       | 270 ms: 1.92x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 2.57 ms: 2.06x slower                                                 |
| sympy_expand               | 457 ms                                                       | 955 ms: 2.09x slower                                                  |
| raytrace                   | 253 ms                                                       | 559 ms: 2.21x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 349 ms: 2.24x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 8.20 ms: 2.63x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 3.34 ms: 3.64x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 108 ms: 9.84x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.37x slower                                                          |

Benchmark hidden because not significant (3): async_tree_memoization, asyncio_websockets, sqlite_synth
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241204-3.14.0a2+-de73a27-NOGIL/bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.244x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.22x
- 95% likely to have a slowdown of 1.21x
- 99% likely to have a slowdown of 1.18x

# Memory
- memory change: 1.32x