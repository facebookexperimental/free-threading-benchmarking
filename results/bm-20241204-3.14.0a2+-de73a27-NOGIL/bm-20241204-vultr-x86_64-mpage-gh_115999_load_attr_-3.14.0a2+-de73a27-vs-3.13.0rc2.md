# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: de73a27
- commit date: 2024-12-04
- overall geometric mean: 1.248x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.18x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 365 ms: 1.41x slower                                                  |
| docutils       | 2.62 sec                                                     | 3.07 sec: 1.17x slower                                                |
| html5lib       | 67.0 ms                                                      | 99.2 ms: 1.48x slower                                                 |
| Geometric mean | (ref)                                                        | 1.35x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 798 ms: 1.14x faster                                                  |
| async_tree_io              | 876 ms                                                       | 818 ms: 1.07x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 626 ms: 1.06x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 602 ms: 1.06x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 348 ms: 1.03x slower                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 437 ms: 1.06x slower                                                  |
| async_tree_none            | 354 ms                                                       | 379 ms: 1.07x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 25.8 ms: 1.10x slower                                                 |
| async_generators           | 377 ms                                                       | 454 ms: 1.20x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.01x slower                                                          |

Benchmark hidden because not significant (2): async_tree_memoization, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 183 ms: 1.18x faster                                                  |
| nbody          | 85.1 ms                                                      | 134 ms: 1.58x slower                                                  |
| float          | 77.5 ms                                                      | 142 ms: 1.83x slower                                                  |
| Geometric mean | (ref)                                                        | 1.35x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.94 ms: 1.05x faster                                                 |
| regex_dna      | 180 ms                                                       | 188 ms: 1.04x slower                                                  |
| regex_v8       | 22.7 ms                                                      | 24.7 ms: 1.09x slower                                                 |
| regex_compile  | 132 ms                                                       | 181 ms: 1.37x slower                                                  |
| Geometric mean | (ref)                                                        | 1.10x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 92.0 ms: 1.03x faster                                                 |
| json_loads           | 27.0 us                                                      | 28.4 us: 1.05x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 98.2 ms: 1.15x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 78.6 ms: 1.32x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 14.1 ms: 1.34x slower                                                 |
| tomli_loads          | 2.01 sec                                                     | 2.68 sec: 1.34x slower                                                |
| unpickle_pure_python | 210 us                                                       | 338 us: 1.61x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 513 us: 1.74x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.25x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                 |
| python_startup         | 11.0 ms                                                      | 17.2 ms: 1.57x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.47x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 63.0 ms: 1.29x slower                                                 |
| genshi_text     | 21.5 ms                                                      | 30.4 ms: 1.41x slower                                                 |
| django_template | 34.1 ms                                                      | 50.6 ms: 1.48x slower                                                 |
| mako            | 11.3 ms                                                      | 17.1 ms: 1.51x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.42x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits                   | 217 ms                                                       | 183 ms: 1.18x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 798 ms: 1.14x faster                                                  |
| deepcopy                   | 355 us                                                       | 323 us: 1.10x faster                                                  |
| async_tree_io              | 876 ms                                                       | 818 ms: 1.07x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 626 ms: 1.06x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 602 ms: 1.06x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.94 ms: 1.05x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 92.0 ms: 1.03x faster                                                 |
| deepcopy_memo              | 39.1 us                                                      | 40.0 us: 1.02x slower                                                 |
| json                       | 4.93 ms                                                      | 5.07 ms: 1.03x slower                                                 |
| async_tree_none_tg         | 336 ms                                                       | 348 ms: 1.03x slower                                                  |
| regex_dna                  | 180 ms                                                       | 188 ms: 1.04x slower                                                  |
| pathlib                    | 19.2 ms                                                      | 20.1 ms: 1.05x slower                                                 |
| json_loads                 | 27.0 us                                                      | 28.4 us: 1.05x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 3.31 ms: 1.05x slower                                                 |
| async_tree_memoization_tg  | 414 ms                                                       | 437 ms: 1.06x slower                                                  |
| async_tree_none            | 354 ms                                                       | 379 ms: 1.07x slower                                                  |
| regex_v8                   | 22.7 ms                                                      | 24.7 ms: 1.09x slower                                                 |
| coroutines                 | 23.6 ms                                                      | 25.8 ms: 1.10x slower                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 3.41 us: 1.10x slower                                                 |
| spectral_norm              | 111 ms                                                       | 122 ms: 1.10x slower                                                  |
| telco                      | 7.82 ms                                                      | 8.68 ms: 1.11x slower                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.99 sec: 1.12x slower                                                |
| scimark_fft                | 349 ms                                                       | 394 ms: 1.13x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 98.2 ms: 1.15x slower                                                 |
| pylint                     | 317 ms                                                       | 372 ms: 1.17x slower                                                  |
| docutils                   | 2.62 sec                                                     | 3.07 sec: 1.17x slower                                                |
| mdp                        | 2.36 sec                                                     | 2.79 sec: 1.19x slower                                                |
| async_generators           | 377 ms                                                       | 454 ms: 1.20x slower                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.69 ms: 1.21x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 98.1 ms: 1.25x slower                                                 |
| coverage                   | 83.0 ms                                                      | 104 ms: 1.26x slower                                                  |
| dulwich_log                | 74.8 ms                                                      | 95.0 ms: 1.27x slower                                                 |
| sqlglot_optimize           | 52.7 ms                                                      | 67.3 ms: 1.28x slower                                                 |
| sqlglot_normalize          | 106 ms                                                       | 136 ms: 1.29x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 63.0 ms: 1.29x slower                                                 |
| meteor_contest             | 102 ms                                                       | 134 ms: 1.32x slower                                                  |
| pprint_safe_repr           | 738 ms                                                       | 973 ms: 1.32x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 89.7 ms: 1.32x slower                                                 |
| xml_etree_process          | 59.3 ms                                                      | 78.6 ms: 1.32x slower                                                 |
| typing_runtime_protocols   | 155 us                                                       | 206 us: 1.33x slower                                                  |
| fannkuch                   | 370 ms                                                       | 492 ms: 1.33x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 14.1 ms: 1.34x slower                                                 |
| tomli_loads                | 2.01 sec                                                     | 2.68 sec: 1.34x slower                                                |
| pprint_pformat             | 1.50 sec                                                     | 2.02 sec: 1.35x slower                                                |
| pycparser                  | 1.12 sec                                                     | 1.52 sec: 1.36x slower                                                |
| create_gc_cycles           | 1.34 ms                                                      | 1.83 ms: 1.37x slower                                                 |
| regex_compile              | 132 ms                                                       | 181 ms: 1.37x slower                                                  |
| generators                 | 28.8 ms                                                      | 39.6 ms: 1.38x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                 |
| 2to3                       | 260 ms                                                       | 365 ms: 1.41x slower                                                  |
| genshi_text                | 21.5 ms                                                      | 30.4 ms: 1.41x slower                                                 |
| thrift                     | 778 us                                                       | 1.12 ms: 1.44x slower                                                 |
| html5lib                   | 67.0 ms                                                      | 99.2 ms: 1.48x slower                                                 |
| django_template            | 34.1 ms                                                      | 50.6 ms: 1.48x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 29.6 ms: 1.49x slower                                                 |
| mako                       | 11.3 ms                                                      | 17.1 ms: 1.51x slower                                                 |
| python_startup             | 11.0 ms                                                      | 17.2 ms: 1.57x slower                                                 |
| pyflate                    | 449 ms                                                       | 703 ms: 1.57x slower                                                  |
| nbody                      | 85.1 ms                                                      | 134 ms: 1.58x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 338 us: 1.61x slower                                                  |
| logging_format             | 6.84 us                                                      | 11.1 us: 1.62x slower                                                 |
| scimark_lu                 | 113 ms                                                       | 184 ms: 1.63x slower                                                  |
| logging_simple             | 6.16 us                                                      | 10.1 us: 1.64x slower                                                 |
| hexiom                     | 5.99 ms                                                      | 10.0 ms: 1.67x slower                                                 |
| comprehensions             | 16.5 us                                                      | 28.1 us: 1.71x slower                                                 |
| richards_super             | 51.6 ms                                                      | 89.5 ms: 1.73x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 513 us: 1.74x slower                                                  |
| sympy_str                  | 275 ms                                                       | 479 ms: 1.74x slower                                                  |
| richards                   | 45.2 ms                                                      | 79.4 ms: 1.76x slower                                                 |
| scimark_sor                | 134 ms                                                       | 237 ms: 1.76x slower                                                  |
| chaos                      | 57.3 ms                                                      | 104 ms: 1.82x slower                                                  |
| float                      | 77.5 ms                                                      | 142 ms: 1.83x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 121 ms: 1.85x slower                                                  |
| logging_silent             | 103 ns                                                       | 190 ns: 1.85x slower                                                  |
| sqlglot_transpile          | 1.56 ms                                                      | 3.02 ms: 1.93x slower                                                 |
| go                         | 141 ms                                                       | 275 ms: 1.95x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 2.62 ms: 2.10x slower                                                 |
| sympy_expand               | 457 ms                                                       | 961 ms: 2.10x slower                                                  |
| raytrace                   | 253 ms                                                       | 559 ms: 2.21x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 349 ms: 2.25x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 8.34 ms: 2.67x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 3.33 ms: 3.62x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 108 ms: 9.83x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.38x slower                                                          |

Benchmark hidden because not significant (3): async_tree_memoization, asyncio_websockets, sqlite_synth
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241204-3.14.0a2+-de73a27-NOGIL/bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.248x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.24x
- 95% likely to have a slowdown of 1.21x
- 99% likely to have a slowdown of 1.18x

# Memory
- memory change: 1.32x