# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: eb8ce39
- commit date: 2024-12-05
- overall geometric mean: 1.238x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 361 ms: 1.39x slower                                                  |
| docutils       | 2.62 sec                                                     | 3.07 sec: 1.17x slower                                                |
| html5lib       | 67.0 ms                                                      | 98.7 ms: 1.47x slower                                                 |
| Geometric mean | (ref)                                                        | 1.34x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 786 ms: 1.16x faster                                                  |
| async_tree_io              | 876 ms                                                       | 811 ms: 1.08x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 626 ms: 1.06x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 610 ms: 1.05x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 518 ms: 1.00x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 345 ms: 1.03x slower                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 432 ms: 1.04x slower                                                  |
| async_tree_none            | 354 ms                                                       | 374 ms: 1.06x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 25.1 ms: 1.07x slower                                                 |
| async_generators           | 377 ms                                                       | 453 ms: 1.20x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.00x slower                                                          |

Benchmark hidden because not significant (1): async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 184 ms: 1.18x faster                                                  |
| nbody          | 85.1 ms                                                      | 125 ms: 1.46x slower                                                  |
| float          | 77.5 ms                                                      | 137 ms: 1.77x slower                                                  |
| Geometric mean | (ref)                                                        | 1.30x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.81 ms: 1.10x faster                                                 |
| regex_dna      | 180 ms                                                       | 184 ms: 1.02x slower                                                  |
| regex_v8       | 22.7 ms                                                      | 24.2 ms: 1.07x slower                                                 |
| regex_compile  | 132 ms                                                       | 179 ms: 1.36x slower                                                  |
| Geometric mean | (ref)                                                        | 1.08x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 91.5 ms: 1.04x faster                                                 |
| json_loads           | 27.0 us                                                      | 28.8 us: 1.07x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 97.4 ms: 1.14x slower                                                 |
| tomli_loads          | 2.01 sec                                                     | 2.64 sec: 1.32x slower                                                |
| xml_etree_process    | 59.3 ms                                                      | 78.5 ms: 1.32x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 14.3 ms: 1.36x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 331 us: 1.58x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 518 us: 1.76x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.25x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                 |
| python_startup         | 11.0 ms                                                      | 17.1 ms: 1.56x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.47x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 62.7 ms: 1.29x slower                                                 |
| genshi_text     | 21.5 ms                                                      | 30.4 ms: 1.41x slower                                                 |
| django_template | 34.1 ms                                                      | 50.2 ms: 1.47x slower                                                 |
| mako            | 11.3 ms                                                      | 16.8 ms: 1.48x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.41x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits                   | 217 ms                                                       | 184 ms: 1.18x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 786 ms: 1.16x faster                                                  |
| deepcopy                   | 355 us                                                       | 320 us: 1.11x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.81 ms: 1.10x faster                                                 |
| async_tree_io              | 876 ms                                                       | 811 ms: 1.08x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 626 ms: 1.06x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 610 ms: 1.05x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 91.5 ms: 1.04x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 518 ms: 1.00x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 39.5 us: 1.01x slower                                                 |
| regex_dna                  | 180 ms                                                       | 184 ms: 1.02x slower                                                  |
| async_tree_none_tg         | 336 ms                                                       | 345 ms: 1.03x slower                                                  |
| json                       | 4.93 ms                                                      | 5.06 ms: 1.03x slower                                                 |
| async_tree_memoization_tg  | 414 ms                                                       | 432 ms: 1.04x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 3.29 ms: 1.05x slower                                                 |
| pathlib                    | 19.2 ms                                                      | 20.1 ms: 1.05x slower                                                 |
| async_tree_none            | 354 ms                                                       | 374 ms: 1.06x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 25.1 ms: 1.07x slower                                                 |
| regex_v8                   | 22.7 ms                                                      | 24.2 ms: 1.07x slower                                                 |
| json_loads                 | 27.0 us                                                      | 28.8 us: 1.07x slower                                                 |
| spectral_norm              | 111 ms                                                       | 119 ms: 1.07x slower                                                  |
| telco                      | 7.82 ms                                                      | 8.59 ms: 1.10x slower                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 3.44 us: 1.11x slower                                                 |
| scimark_fft                | 349 ms                                                       | 391 ms: 1.12x slower                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 5.00 sec: 1.12x slower                                                |
| xml_etree_generate         | 85.4 ms                                                      | 97.4 ms: 1.14x slower                                                 |
| mdp                        | 2.36 sec                                                     | 2.74 sec: 1.16x slower                                                |
| pylint                     | 317 ms                                                       | 370 ms: 1.17x slower                                                  |
| docutils                   | 2.62 sec                                                     | 3.07 sec: 1.17x slower                                                |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.57 ms: 1.18x slower                                                 |
| async_generators           | 377 ms                                                       | 453 ms: 1.20x slower                                                  |
| coverage                   | 83.0 ms                                                      | 101 ms: 1.22x slower                                                  |
| nqueens                    | 78.6 ms                                                      | 96.5 ms: 1.23x slower                                                 |
| sqlglot_optimize           | 52.7 ms                                                      | 66.8 ms: 1.27x slower                                                 |
| meteor_contest             | 102 ms                                                       | 129 ms: 1.27x slower                                                  |
| dulwich_log                | 74.8 ms                                                      | 95.0 ms: 1.27x slower                                                 |
| sqlglot_normalize          | 106 ms                                                       | 136 ms: 1.28x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 62.7 ms: 1.29x slower                                                 |
| pprint_safe_repr           | 738 ms                                                       | 959 ms: 1.30x slower                                                  |
| tomli_loads                | 2.01 sec                                                     | 2.64 sec: 1.32x slower                                                |
| generators                 | 28.8 ms                                                      | 38.1 ms: 1.32x slower                                                 |
| typing_runtime_protocols   | 155 us                                                       | 204 us: 1.32x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 78.5 ms: 1.32x slower                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.99 sec: 1.33x slower                                                |
| fannkuch                   | 370 ms                                                       | 491 ms: 1.33x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 91.6 ms: 1.35x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.81 ms: 1.35x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 14.3 ms: 1.36x slower                                                 |
| regex_compile              | 132 ms                                                       | 179 ms: 1.36x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.53 sec: 1.37x slower                                                |
| python_startup_no_site     | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                 |
| 2to3                       | 260 ms                                                       | 361 ms: 1.39x slower                                                  |
| genshi_text                | 21.5 ms                                                      | 30.4 ms: 1.41x slower                                                 |
| thrift                     | 778 us                                                       | 1.11 ms: 1.43x slower                                                 |
| nbody                      | 85.1 ms                                                      | 125 ms: 1.46x slower                                                  |
| django_template            | 34.1 ms                                                      | 50.2 ms: 1.47x slower                                                 |
| html5lib                   | 67.0 ms                                                      | 98.7 ms: 1.47x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 29.3 ms: 1.48x slower                                                 |
| mako                       | 11.3 ms                                                      | 16.8 ms: 1.48x slower                                                 |
| pyflate                    | 449 ms                                                       | 690 ms: 1.54x slower                                                  |
| python_startup             | 11.0 ms                                                      | 17.1 ms: 1.56x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 331 us: 1.58x slower                                                  |
| logging_simple             | 6.16 us                                                      | 9.82 us: 1.59x slower                                                 |
| logging_format             | 6.84 us                                                      | 10.9 us: 1.60x slower                                                 |
| scimark_lu                 | 113 ms                                                       | 182 ms: 1.62x slower                                                  |
| hexiom                     | 5.99 ms                                                      | 9.78 ms: 1.63x slower                                                 |
| richards_super             | 51.6 ms                                                      | 85.5 ms: 1.66x slower                                                 |
| comprehensions             | 16.5 us                                                      | 27.5 us: 1.67x slower                                                 |
| richards                   | 45.2 ms                                                      | 76.1 ms: 1.68x slower                                                 |
| sympy_str                  | 275 ms                                                       | 474 ms: 1.72x slower                                                  |
| scimark_sor                | 134 ms                                                       | 233 ms: 1.73x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 518 us: 1.76x slower                                                  |
| float                      | 77.5 ms                                                      | 137 ms: 1.77x slower                                                  |
| chaos                      | 57.3 ms                                                      | 103 ms: 1.79x slower                                                  |
| logging_silent             | 103 ns                                                       | 184 ns: 1.79x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 119 ms: 1.82x slower                                                  |
| sqlglot_transpile          | 1.56 ms                                                      | 2.93 ms: 1.88x slower                                                 |
| go                         | 141 ms                                                       | 266 ms: 1.89x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 2.54 ms: 2.04x slower                                                 |
| sympy_expand               | 457 ms                                                       | 952 ms: 2.08x slower                                                  |
| raytrace                   | 253 ms                                                       | 551 ms: 2.18x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 348 ms: 2.24x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 8.08 ms: 2.59x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 3.32 ms: 3.61x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 108 ms: 9.82x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.36x slower                                                          |

Benchmark hidden because not significant (2): async_tree_memoization, sqlite_synth
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241205-3.14.0a2+-eb8ce39-NOGIL/bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.238x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.22x
- 95% likely to have a slowdown of 1.20x
- 99% likely to have a slowdown of 1.17x

# Memory
- memory change: 1.32x