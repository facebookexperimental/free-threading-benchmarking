# Results vs. 3.13.0rc2

- fork: corona10
- ref: gh_115999_BINARY_SUB
- machine: linux-x86_64
- commit hash: 47b80b4
- commit date: 2024-12-19
- overall geometric mean: 1.024x faster
- HPT reliability: 93.59%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 258 ms: 1.01x faster                                                     |
| docutils       | 2.62 sec                                                     | 2.57 sec: 1.02x faster                                                   |
| Geometric mean | (ref)                                                        | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 626 ms: 1.46x faster                                                     |
| async_tree_io              | 876 ms                                                       | 612 ms: 1.43x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 342 ms: 1.35x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 507 ms: 1.31x faster                                                     |
| async_tree_none            | 354 ms                                                       | 276 ms: 1.28x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 502 ms: 1.27x faster                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 336 ms: 1.23x faster                                                     |
| async_tree_none_tg         | 336 ms                                                       | 275 ms: 1.22x faster                                                     |
| async_generators           | 377 ms                                                       | 360 ms: 1.05x faster                                                     |
| coroutines                 | 23.6 ms                                                      | 22.5 ms: 1.05x faster                                                    |
| asyncio_websockets         | 520 ms                                                       | 524 ms: 1.01x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.23x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 186 ms: 1.17x faster                                                     |
| float          | 77.5 ms                                                      | 79.3 ms: 1.02x slower                                                    |
| nbody          | 85.1 ms                                                      | 94.7 ms: 1.11x slower                                                    |
| Geometric mean | (ref)                                                        | 1.01x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.72 ms: 1.13x faster                                                    |
| regex_dna      | 180 ms                                                       | 176 ms: 1.02x faster                                                     |
| regex_compile  | 132 ms                                                       | 130 ms: 1.02x faster                                                     |
| regex_v8       | 22.7 ms                                                      | 24.8 ms: 1.09x slower                                                    |
| Geometric mean | (ref)                                                        | 1.02x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 127 ms: 1.07x faster                                                     |
| json_loads           | 27.0 us                                                      | 25.9 us: 1.04x faster                                                    |
| xml_etree_iterparse  | 94.9 ms                                                      | 91.0 ms: 1.04x faster                                                    |
| xml_etree_generate   | 85.4 ms                                                      | 84.8 ms: 1.01x faster                                                    |
| xml_etree_process    | 59.3 ms                                                      | 59.0 ms: 1.01x faster                                                    |
| unpickle_pure_python | 210 us                                                       | 219 us: 1.04x slower                                                     |
| tomli_loads          | 2.01 sec                                                     | 2.12 sec: 1.06x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 316 us: 1.07x slower                                                     |
| json_dumps           | 10.5 ms                                                      | 11.5 ms: 1.09x slower                                                    |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.49 ms: 1.01x slower                                                    |
| python_startup         | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                    |
| Geometric mean         | (ref)                                                        | 1.16x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 22.2 ms: 1.03x slower                                                    |
| django_template | 34.1 ms                                                      | 35.4 ms: 1.04x slower                                                    |
| genshi_xml      | 48.8 ms                                                      | 50.7 ms: 1.04x slower                                                    |
| mako            | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                    |
| Geometric mean  | (ref)                                                        | 1.04x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 626 ms: 1.46x faster                                                     |
| async_tree_io              | 876 ms                                                       | 612 ms: 1.43x faster                                                     |
| deepcopy                   | 355 us                                                       | 263 us: 1.35x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 342 ms: 1.35x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 507 ms: 1.31x faster                                                     |
| deepcopy_memo              | 39.1 us                                                      | 30.2 us: 1.29x faster                                                    |
| async_tree_none            | 354 ms                                                       | 276 ms: 1.28x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 502 ms: 1.27x faster                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 336 ms: 1.23x faster                                                     |
| async_tree_none_tg         | 336 ms                                                       | 275 ms: 1.22x faster                                                     |
| pidigits                   | 217 ms                                                       | 186 ms: 1.17x faster                                                     |
| deepcopy_reduce            | 3.11 us                                                      | 2.68 us: 1.16x faster                                                    |
| go                         | 141 ms                                                       | 121 ms: 1.16x faster                                                     |
| regex_effbot               | 3.08 ms                                                      | 2.72 ms: 1.13x faster                                                    |
| pylint                     | 317 ms                                                       | 280 ms: 1.13x faster                                                     |
| telco                      | 7.82 ms                                                      | 7.30 ms: 1.07x faster                                                    |
| xml_etree_parse            | 136 ms                                                       | 127 ms: 1.07x faster                                                     |
| json                       | 4.93 ms                                                      | 4.67 ms: 1.06x faster                                                    |
| pathlib                    | 19.2 ms                                                      | 18.2 ms: 1.05x faster                                                    |
| async_generators           | 377 ms                                                       | 360 ms: 1.05x faster                                                     |
| thrift                     | 778 us                                                       | 744 us: 1.05x faster                                                     |
| coroutines                 | 23.6 ms                                                      | 22.5 ms: 1.05x faster                                                    |
| json_loads                 | 27.0 us                                                      | 25.9 us: 1.04x faster                                                    |
| xml_etree_iterparse        | 94.9 ms                                                      | 91.0 ms: 1.04x faster                                                    |
| coverage                   | 83.0 ms                                                      | 80.5 ms: 1.03x faster                                                    |
| pprint_safe_repr           | 738 ms                                                       | 720 ms: 1.02x faster                                                     |
| bpe_tokeniser              | 4.45 sec                                                     | 4.34 sec: 1.02x faster                                                   |
| regex_dna                  | 180 ms                                                       | 176 ms: 1.02x faster                                                     |
| meteor_contest             | 102 ms                                                       | 99.3 ms: 1.02x faster                                                    |
| regex_compile              | 132 ms                                                       | 130 ms: 1.02x faster                                                     |
| scimark_lu                 | 113 ms                                                       | 110 ms: 1.02x faster                                                     |
| scimark_fft                | 349 ms                                                       | 343 ms: 1.02x faster                                                     |
| docutils                   | 2.62 sec                                                     | 2.57 sec: 1.02x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.47 sec: 1.02x faster                                                   |
| sympy_sum                  | 156 ms                                                       | 153 ms: 1.01x faster                                                     |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.67 ms: 1.01x faster                                                    |
| crypto_pyaes               | 67.9 ms                                                      | 67.4 ms: 1.01x faster                                                    |
| xml_etree_generate         | 85.4 ms                                                      | 84.8 ms: 1.01x faster                                                    |
| 2to3                       | 260 ms                                                       | 258 ms: 1.01x faster                                                     |
| xml_etree_process          | 59.3 ms                                                      | 59.0 ms: 1.01x faster                                                    |
| hexiom                     | 5.99 ms                                                      | 5.98 ms: 1.00x faster                                                    |
| sympy_integrate            | 19.8 ms                                                      | 19.9 ms: 1.00x slower                                                    |
| asyncio_websockets         | 520 ms                                                       | 524 ms: 1.01x slower                                                     |
| nqueens                    | 78.6 ms                                                      | 79.2 ms: 1.01x slower                                                    |
| spectral_norm              | 111 ms                                                       | 112 ms: 1.01x slower                                                     |
| pyflate                    | 449 ms                                                       | 453 ms: 1.01x slower                                                     |
| sqlite_synth               | 2.21 us                                                      | 2.23 us: 1.01x slower                                                    |
| python_startup_no_site     | 7.39 ms                                                      | 7.49 ms: 1.01x slower                                                    |
| sympy_expand               | 457 ms                                                       | 464 ms: 1.02x slower                                                     |
| dulwich_log                | 74.8 ms                                                      | 76.0 ms: 1.02x slower                                                    |
| sqlglot_normalize          | 106 ms                                                       | 108 ms: 1.02x slower                                                     |
| sqlglot_optimize           | 52.7 ms                                                      | 53.8 ms: 1.02x slower                                                    |
| float                      | 77.5 ms                                                      | 79.3 ms: 1.02x slower                                                    |
| richards_super             | 51.6 ms                                                      | 52.9 ms: 1.02x slower                                                    |
| logging_simple             | 6.16 us                                                      | 6.32 us: 1.03x slower                                                    |
| logging_format             | 6.84 us                                                      | 7.03 us: 1.03x slower                                                    |
| richards                   | 45.2 ms                                                      | 46.5 ms: 1.03x slower                                                    |
| sqlglot_transpile          | 1.56 ms                                                      | 1.60 ms: 1.03x slower                                                    |
| genshi_text                | 21.5 ms                                                      | 22.2 ms: 1.03x slower                                                    |
| typing_runtime_protocols   | 155 us                                                       | 159 us: 1.03x slower                                                     |
| deltablue                  | 3.12 ms                                                      | 3.23 ms: 1.03x slower                                                    |
| django_template            | 34.1 ms                                                      | 35.4 ms: 1.04x slower                                                    |
| sqlglot_parse              | 1.25 ms                                                      | 1.30 ms: 1.04x slower                                                    |
| genshi_xml                 | 48.8 ms                                                      | 50.7 ms: 1.04x slower                                                    |
| mako                       | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                    |
| chaos                      | 57.3 ms                                                      | 59.7 ms: 1.04x slower                                                    |
| unpickle_pure_python       | 210 us                                                       | 219 us: 1.04x slower                                                     |
| logging_silent             | 103 ns                                                       | 107 ns: 1.05x slower                                                     |
| fannkuch                   | 370 ms                                                       | 388 ms: 1.05x slower                                                     |
| raytrace                   | 253 ms                                                       | 266 ms: 1.05x slower                                                     |
| tomli_loads                | 2.01 sec                                                     | 2.12 sec: 1.06x slower                                                   |
| comprehensions             | 16.5 us                                                      | 17.5 us: 1.07x slower                                                    |
| pickle_pure_python         | 294 us                                                       | 316 us: 1.07x slower                                                     |
| mdp                        | 2.36 sec                                                     | 2.53 sec: 1.07x slower                                                   |
| regex_v8                   | 22.7 ms                                                      | 24.8 ms: 1.09x slower                                                    |
| json_dumps                 | 10.5 ms                                                      | 11.5 ms: 1.09x slower                                                    |
| nbody                      | 85.1 ms                                                      | 94.7 ms: 1.11x slower                                                    |
| bench_thread_pool          | 919 us                                                       | 1.03 ms: 1.12x slower                                                    |
| create_gc_cycles           | 1.34 ms                                                      | 1.70 ms: 1.27x slower                                                    |
| python_startup             | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                    |
| gc_traversal               | 3.14 ms                                                      | 4.65 ms: 1.48x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                      | 85.7 ms: 7.79x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.00x slower                                                             |

Benchmark hidden because not significant (5): scimark_sor, pycparser, scimark_monte_carlo, sympy_str, generators
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241219-3.14.0a2+-47b80b4/bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.024x faster

# HPT report

- Reliability score: 93.59% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x