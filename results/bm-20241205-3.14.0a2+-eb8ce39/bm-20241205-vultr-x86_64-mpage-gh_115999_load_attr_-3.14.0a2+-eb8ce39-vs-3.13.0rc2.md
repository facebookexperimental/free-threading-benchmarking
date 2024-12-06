# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: eb8ce39
- commit date: 2024-12-05
- overall geometric mean: 1.027x faster
- HPT reliability: 93.24%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 258 ms: 1.01x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.57 sec: 1.02x faster                                                |
| Geometric mean | (ref)                                                        | 1.01x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 629 ms: 1.45x faster                                                  |
| async_tree_io              | 876 ms                                                       | 629 ms: 1.39x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 340 ms: 1.36x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 313 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 505 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 487 ms: 1.31x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 262 ms: 1.28x faster                                                  |
| async_tree_none            | 354 ms                                                       | 276 ms: 1.28x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 22.5 ms: 1.05x faster                                                 |
| async_generators           | 377 ms                                                       | 364 ms: 1.04x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.00x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.25x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 185 ms: 1.17x faster                                                  |
| nbody          | 85.1 ms                                                      | 94.7 ms: 1.11x slower                                                 |
| Geometric mean | (ref)                                                        | 1.02x faster                                                          |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.77 ms: 1.11x faster                                                 |
| regex_dna      | 180 ms                                                       | 175 ms: 1.03x faster                                                  |
| regex_compile  | 132 ms                                                       | 130 ms: 1.02x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 24.8 ms: 1.09x slower                                                 |
| Geometric mean | (ref)                                                        | 1.02x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_loads           | 27.0 us                                                      | 24.8 us: 1.09x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.05x faster                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 91.7 ms: 1.04x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 86.0 ms: 1.01x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 213 us: 1.02x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.12 sec: 1.05x slower                                                |
| pickle_pure_python   | 294 us                                                       | 314 us: 1.07x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 11.3 ms: 1.08x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.00x slower                                                          |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.46 ms: 1.01x slower                                                 |
| python_startup         | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.16x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 22.0 ms: 1.02x slower                                                 |
| mako            | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                 |
| genshi_xml      | 48.8 ms                                                      | 50.8 ms: 1.04x slower                                                 |
| django_template | 34.1 ms                                                      | 35.9 ms: 1.05x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.04x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 629 ms: 1.45x faster                                                  |
| async_tree_io              | 876 ms                                                       | 629 ms: 1.39x faster                                                  |
| deepcopy                   | 355 us                                                       | 261 us: 1.36x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 340 ms: 1.36x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 313 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 505 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 487 ms: 1.31x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 30.3 us: 1.29x faster                                                 |
| async_tree_none_tg         | 336 ms                                                       | 262 ms: 1.28x faster                                                  |
| async_tree_none            | 354 ms                                                       | 276 ms: 1.28x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.61 us: 1.19x faster                                                 |
| go                         | 141 ms                                                       | 119 ms: 1.18x faster                                                  |
| pidigits                   | 217 ms                                                       | 185 ms: 1.17x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.77 ms: 1.11x faster                                                 |
| pylint                     | 317 ms                                                       | 285 ms: 1.11x faster                                                  |
| json_loads                 | 27.0 us                                                      | 24.8 us: 1.09x faster                                                 |
| json                       | 4.93 ms                                                      | 4.55 ms: 1.08x faster                                                 |
| telco                      | 7.82 ms                                                      | 7.41 ms: 1.06x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.05x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 22.5 ms: 1.05x faster                                                 |
| coverage                   | 83.0 ms                                                      | 79.3 ms: 1.05x faster                                                 |
| pathlib                    | 19.2 ms                                                      | 18.4 ms: 1.04x faster                                                 |
| async_generators           | 377 ms                                                       | 364 ms: 1.04x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 91.7 ms: 1.04x faster                                                 |
| thrift                     | 778 us                                                       | 755 us: 1.03x faster                                                  |
| regex_dna                  | 180 ms                                                       | 175 ms: 1.03x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.32 sec: 1.03x faster                                                |
| pprint_safe_repr           | 738 ms                                                       | 719 ms: 1.03x faster                                                  |
| hexiom                     | 5.99 ms                                                      | 5.87 ms: 1.02x faster                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.47 sec: 1.02x faster                                                |
| docutils                   | 2.62 sec                                                     | 2.57 sec: 1.02x faster                                                |
| meteor_contest             | 102 ms                                                       | 99.8 ms: 1.02x faster                                                 |
| spectral_norm              | 111 ms                                                       | 109 ms: 1.02x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 111 ms: 1.02x faster                                                  |
| regex_compile              | 132 ms                                                       | 130 ms: 1.02x faster                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.66 ms: 1.01x faster                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 67.3 ms: 1.01x faster                                                 |
| scimark_fft                | 349 ms                                                       | 346 ms: 1.01x faster                                                  |
| scimark_sor                | 134 ms                                                       | 133 ms: 1.01x faster                                                  |
| 2to3                       | 260 ms                                                       | 258 ms: 1.01x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.00x slower                                                  |
| richards_super             | 51.6 ms                                                      | 51.9 ms: 1.01x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 86.0 ms: 1.01x slower                                                 |
| logging_simple             | 6.16 us                                                      | 6.22 us: 1.01x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 7.46 ms: 1.01x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 79.4 ms: 1.01x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 20.0 ms: 1.01x slower                                                 |
| fannkuch                   | 370 ms                                                       | 374 ms: 1.01x slower                                                  |
| logging_format             | 6.84 us                                                      | 6.92 us: 1.01x slower                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.24 us: 1.01x slower                                                 |
| richards                   | 45.2 ms                                                      | 45.8 ms: 1.01x slower                                                 |
| dulwich_log                | 74.8 ms                                                      | 75.9 ms: 1.01x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 213 us: 1.02x slower                                                  |
| sympy_expand               | 457 ms                                                       | 466 ms: 1.02x slower                                                  |
| sqlglot_optimize           | 52.7 ms                                                      | 53.7 ms: 1.02x slower                                                 |
| sqlglot_normalize          | 106 ms                                                       | 108 ms: 1.02x slower                                                  |
| genshi_text                | 21.5 ms                                                      | 22.0 ms: 1.02x slower                                                 |
| chaos                      | 57.3 ms                                                      | 58.6 ms: 1.02x slower                                                 |
| pycparser                  | 1.12 sec                                                     | 1.14 sec: 1.02x slower                                                |
| logging_silent             | 103 ns                                                       | 105 ns: 1.03x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 159 us: 1.03x slower                                                  |
| mako                       | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.23 ms: 1.03x slower                                                 |
| sqlglot_transpile          | 1.56 ms                                                      | 1.61 ms: 1.03x slower                                                 |
| sqlglot_parse              | 1.25 ms                                                      | 1.30 ms: 1.04x slower                                                 |
| genshi_xml                 | 48.8 ms                                                      | 50.8 ms: 1.04x slower                                                 |
| raytrace                   | 253 ms                                                       | 265 ms: 1.05x slower                                                  |
| django_template            | 34.1 ms                                                      | 35.9 ms: 1.05x slower                                                 |
| comprehensions             | 16.5 us                                                      | 17.3 us: 1.05x slower                                                 |
| tomli_loads                | 2.01 sec                                                     | 2.12 sec: 1.05x slower                                                |
| pickle_pure_python         | 294 us                                                       | 314 us: 1.07x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 11.3 ms: 1.08x slower                                                 |
| regex_v8                   | 22.7 ms                                                      | 24.8 ms: 1.09x slower                                                 |
| nbody                      | 85.1 ms                                                      | 94.7 ms: 1.11x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.03 ms: 1.12x slower                                                 |
| python_startup             | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.85 ms: 1.38x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.61 ms: 1.47x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 88.9 ms: 8.09x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.00x faster                                                          |

Benchmark hidden because not significant (8): scimark_monte_carlo, sympy_sum, pyflate, xml_etree_process, mdp, generators, float, sympy_str
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241205-3.14.0a2+-eb8ce39/bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.027x faster

# HPT report

- Reliability score: 93.24% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.09x