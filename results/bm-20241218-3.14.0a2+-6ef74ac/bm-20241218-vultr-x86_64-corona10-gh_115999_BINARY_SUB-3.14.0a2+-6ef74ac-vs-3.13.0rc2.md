# Results vs. 3.13.0rc2

- fork: corona10
- ref: gh_115999_BINARY_SUB
- machine: linux-x86_64
- commit hash: 6ef74ac
- commit date: 2024-12-18
- overall geometric mean: 1.022x faster
- HPT reliability: 97.86%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 258 ms: 1.01x faster                                                     |
| docutils       | 2.62 sec                                                     | 2.57 sec: 1.02x faster                                                   |
| Geometric mean | (ref)                                                        | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 623 ms: 1.47x faster                                                     |
| async_tree_io              | 876 ms                                                       | 607 ms: 1.44x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 341 ms: 1.35x faster                                                     |
| async_tree_none            | 354 ms                                                       | 276 ms: 1.28x faster                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 332 ms: 1.25x faster                                                     |
| async_tree_none_tg         | 336 ms                                                       | 273 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 603 ms: 1.10x faster                                                     |
| coroutines                 | 23.6 ms                                                      | 21.9 ms: 1.07x faster                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 597 ms: 1.07x faster                                                     |
| async_generators           | 377 ms                                                       | 363 ms: 1.04x faster                                                     |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.00x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.20x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 78.6 ms: 1.01x slower                                                    |
| pidigits       | 217 ms                                                       | 221 ms: 1.02x slower                                                     |
| nbody          | 85.1 ms                                                      | 95.5 ms: 1.12x slower                                                    |
| Geometric mean | (ref)                                                        | 1.05x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.70 ms: 1.14x faster                                                    |
| regex_dna      | 180 ms                                                       | 175 ms: 1.03x faster                                                     |
| regex_compile  | 132 ms                                                       | 129 ms: 1.03x faster                                                     |
| regex_v8       | 22.7 ms                                                      | 24.7 ms: 1.09x slower                                                    |
| Geometric mean | (ref)                                                        | 1.03x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_loads           | 27.0 us                                                      | 25.0 us: 1.08x faster                                                    |
| xml_etree_parse      | 136 ms                                                       | 127 ms: 1.07x faster                                                     |
| xml_etree_iterparse  | 94.9 ms                                                      | 91.3 ms: 1.04x faster                                                    |
| unpickle_pure_python | 210 us                                                       | 214 us: 1.02x slower                                                     |
| tomli_loads          | 2.01 sec                                                     | 2.10 sec: 1.05x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 319 us: 1.08x slower                                                     |
| json_dumps           | 10.5 ms                                                      | 11.6 ms: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                             |

Benchmark hidden because not significant (2): xml_etree_generate, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.53 ms: 1.02x slower                                                    |
| python_startup         | 11.0 ms                                                      | 14.7 ms: 1.33x slower                                                    |
| Geometric mean         | (ref)                                                        | 1.17x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.9 ms: 1.02x slower                                                    |
| django_template | 34.1 ms                                                      | 35.2 ms: 1.03x slower                                                    |
| genshi_xml      | 48.8 ms                                                      | 50.9 ms: 1.04x slower                                                    |
| mako            | 11.3 ms                                                      | 11.9 ms: 1.05x slower                                                    |
| Geometric mean  | (ref)                                                        | 1.04x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 623 ms: 1.47x faster                                                     |
| async_tree_io              | 876 ms                                                       | 607 ms: 1.44x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 341 ms: 1.35x faster                                                     |
| deepcopy                   | 355 us                                                       | 264 us: 1.35x faster                                                     |
| async_tree_none            | 354 ms                                                       | 276 ms: 1.28x faster                                                     |
| deepcopy_memo              | 39.1 us                                                      | 30.6 us: 1.28x faster                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 332 ms: 1.25x faster                                                     |
| async_tree_none_tg         | 336 ms                                                       | 273 ms: 1.23x faster                                                     |
| go                         | 141 ms                                                       | 119 ms: 1.18x faster                                                     |
| deepcopy_reduce            | 3.11 us                                                      | 2.64 us: 1.18x faster                                                    |
| regex_effbot               | 3.08 ms                                                      | 2.70 ms: 1.14x faster                                                    |
| pylint                     | 317 ms                                                       | 280 ms: 1.13x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 603 ms: 1.10x faster                                                     |
| json                       | 4.93 ms                                                      | 4.54 ms: 1.09x faster                                                    |
| telco                      | 7.82 ms                                                      | 7.22 ms: 1.08x faster                                                    |
| json_loads                 | 27.0 us                                                      | 25.0 us: 1.08x faster                                                    |
| coroutines                 | 23.6 ms                                                      | 21.9 ms: 1.07x faster                                                    |
| xml_etree_parse            | 136 ms                                                       | 127 ms: 1.07x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 597 ms: 1.07x faster                                                     |
| pathlib                    | 19.2 ms                                                      | 18.2 ms: 1.05x faster                                                    |
| thrift                     | 778 us                                                       | 742 us: 1.05x faster                                                     |
| coverage                   | 83.0 ms                                                      | 79.7 ms: 1.04x faster                                                    |
| xml_etree_iterparse        | 94.9 ms                                                      | 91.3 ms: 1.04x faster                                                    |
| async_generators           | 377 ms                                                       | 363 ms: 1.04x faster                                                     |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.54 ms: 1.04x faster                                                    |
| scimark_fft                | 349 ms                                                       | 338 ms: 1.03x faster                                                     |
| regex_dna                  | 180 ms                                                       | 175 ms: 1.03x faster                                                     |
| regex_compile              | 132 ms                                                       | 129 ms: 1.03x faster                                                     |
| scimark_lu                 | 113 ms                                                       | 110 ms: 1.02x faster                                                     |
| bpe_tokeniser              | 4.45 sec                                                     | 4.35 sec: 1.02x faster                                                   |
| crypto_pyaes               | 67.9 ms                                                      | 66.5 ms: 1.02x faster                                                    |
| spectral_norm              | 111 ms                                                       | 109 ms: 1.02x faster                                                     |
| docutils                   | 2.62 sec                                                     | 2.57 sec: 1.02x faster                                                   |
| scimark_sor                | 134 ms                                                       | 132 ms: 1.01x faster                                                     |
| pprint_safe_repr           | 738 ms                                                       | 727 ms: 1.01x faster                                                     |
| hexiom                     | 5.99 ms                                                      | 5.91 ms: 1.01x faster                                                    |
| scimark_monte_carlo        | 65.4 ms                                                      | 64.5 ms: 1.01x faster                                                    |
| pprint_pformat             | 1.50 sec                                                     | 1.48 sec: 1.01x faster                                                   |
| meteor_contest             | 102 ms                                                       | 101 ms: 1.01x faster                                                     |
| sympy_sum                  | 156 ms                                                       | 154 ms: 1.01x faster                                                     |
| 2to3                       | 260 ms                                                       | 258 ms: 1.01x faster                                                     |
| generators                 | 28.8 ms                                                      | 28.6 ms: 1.01x faster                                                    |
| pyflate                    | 449 ms                                                       | 446 ms: 1.01x faster                                                     |
| logging_simple             | 6.16 us                                                      | 6.12 us: 1.01x faster                                                    |
| logging_silent             | 103 ns                                                       | 102 ns: 1.00x faster                                                     |
| richards                   | 45.2 ms                                                      | 45.0 ms: 1.00x faster                                                    |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.00x slower                                                     |
| nqueens                    | 78.6 ms                                                      | 79.0 ms: 1.01x slower                                                    |
| logging_format             | 6.84 us                                                      | 6.88 us: 1.01x slower                                                    |
| sympy_integrate            | 19.8 ms                                                      | 20.0 ms: 1.01x slower                                                    |
| fannkuch                   | 370 ms                                                       | 373 ms: 1.01x slower                                                     |
| sympy_expand               | 457 ms                                                       | 463 ms: 1.01x slower                                                     |
| float                      | 77.5 ms                                                      | 78.6 ms: 1.01x slower                                                    |
| dulwich_log                | 74.8 ms                                                      | 76.1 ms: 1.02x slower                                                    |
| python_startup_no_site     | 7.39 ms                                                      | 7.53 ms: 1.02x slower                                                    |
| genshi_text                | 21.5 ms                                                      | 21.9 ms: 1.02x slower                                                    |
| unpickle_pure_python       | 210 us                                                       | 214 us: 1.02x slower                                                     |
| pidigits                   | 217 ms                                                       | 221 ms: 1.02x slower                                                     |
| sqlglot_optimize           | 52.7 ms                                                      | 53.9 ms: 1.02x slower                                                    |
| deltablue                  | 3.12 ms                                                      | 3.19 ms: 1.02x slower                                                    |
| typing_runtime_protocols   | 155 us                                                       | 158 us: 1.02x slower                                                     |
| sqlglot_transpile          | 1.56 ms                                                      | 1.60 ms: 1.03x slower                                                    |
| chaos                      | 57.3 ms                                                      | 58.9 ms: 1.03x slower                                                    |
| sqlglot_normalize          | 106 ms                                                       | 109 ms: 1.03x slower                                                     |
| django_template            | 34.1 ms                                                      | 35.2 ms: 1.03x slower                                                    |
| sqlglot_parse              | 1.25 ms                                                      | 1.29 ms: 1.03x slower                                                    |
| raytrace                   | 253 ms                                                       | 263 ms: 1.04x slower                                                     |
| genshi_xml                 | 48.8 ms                                                      | 50.9 ms: 1.04x slower                                                    |
| tomli_loads                | 2.01 sec                                                     | 2.10 sec: 1.05x slower                                                   |
| mako                       | 11.3 ms                                                      | 11.9 ms: 1.05x slower                                                    |
| mdp                        | 2.36 sec                                                     | 2.50 sec: 1.06x slower                                                   |
| comprehensions             | 16.5 us                                                      | 17.6 us: 1.07x slower                                                    |
| pickle_pure_python         | 294 us                                                       | 319 us: 1.08x slower                                                     |
| regex_v8                   | 22.7 ms                                                      | 24.7 ms: 1.09x slower                                                    |
| json_dumps                 | 10.5 ms                                                      | 11.6 ms: 1.10x slower                                                    |
| nbody                      | 85.1 ms                                                      | 95.5 ms: 1.12x slower                                                    |
| bench_thread_pool          | 919 us                                                       | 1.03 ms: 1.12x slower                                                    |
| create_gc_cycles           | 1.34 ms                                                      | 1.73 ms: 1.30x slower                                                    |
| python_startup             | 11.0 ms                                                      | 14.7 ms: 1.33x slower                                                    |
| gc_traversal               | 3.14 ms                                                      | 4.77 ms: 1.52x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                      | 86.2 ms: 7.84x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.00x slower                                                             |

Benchmark hidden because not significant (6): xml_etree_generate, sympy_str, richards_super, xml_etree_process, sqlite_synth, pycparser
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241218-3.14.0a2+-6ef74ac/bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.022x faster

# HPT report

- Reliability score: 97.86% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x