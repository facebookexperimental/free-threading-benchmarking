# Results vs. 3.13.0rc2

- fork: corona10
- ref: gh_115999_BINARY_SUB
- machine: linux-x86_64
- commit hash: 7b72e7b
- commit date: 2024-12-17
- overall geometric mean: 1.027x faster
- HPT reliability: 98.73%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 257 ms: 1.01x faster                                                     |
| docutils       | 2.62 sec                                                     | 2.56 sec: 1.02x faster                                                   |
| Geometric mean | (ref)                                                        | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 617 ms: 1.48x faster                                                     |
| async_tree_io              | 876 ms                                                       | 601 ms: 1.46x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 338 ms: 1.37x faster                                                     |
| async_tree_none            | 354 ms                                                       | 275 ms: 1.29x faster                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 330 ms: 1.26x faster                                                     |
| async_tree_none_tg         | 336 ms                                                       | 274 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 601 ms: 1.11x faster                                                     |
| coroutines                 | 23.6 ms                                                      | 21.8 ms: 1.08x faster                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 598 ms: 1.07x faster                                                     |
| async_generators           | 377 ms                                                       | 359 ms: 1.05x faster                                                     |
| asyncio_websockets         | 520 ms                                                       | 522 ms: 1.00x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.21x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 219 ms: 1.01x slower                                                     |
| float          | 77.5 ms                                                      | 79.5 ms: 1.03x slower                                                    |
| nbody          | 85.1 ms                                                      | 93.9 ms: 1.10x slower                                                    |
| Geometric mean | (ref)                                                        | 1.05x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.78 ms: 1.11x faster                                                    |
| regex_dna      | 180 ms                                                       | 172 ms: 1.05x faster                                                     |
| regex_compile  | 132 ms                                                       | 128 ms: 1.03x faster                                                     |
| regex_v8       | 22.7 ms                                                      | 24.0 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                        | 1.03x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_loads           | 27.0 us                                                      | 24.9 us: 1.08x faster                                                    |
| xml_etree_parse      | 136 ms                                                       | 126 ms: 1.08x faster                                                     |
| xml_etree_iterparse  | 94.9 ms                                                      | 90.2 ms: 1.05x faster                                                    |
| xml_etree_generate   | 85.4 ms                                                      | 85.8 ms: 1.00x slower                                                    |
| xml_etree_process    | 59.3 ms                                                      | 59.7 ms: 1.01x slower                                                    |
| unpickle_pure_python | 210 us                                                       | 214 us: 1.02x slower                                                     |
| tomli_loads          | 2.01 sec                                                     | 2.10 sec: 1.05x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 316 us: 1.07x slower                                                     |
| json_dumps           | 10.5 ms                                                      | 11.3 ms: 1.08x slower                                                    |
| Geometric mean       | (ref)                                                        | 1.00x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.46 ms: 1.01x slower                                                    |
| python_startup         | 11.0 ms                                                      | 14.5 ms: 1.32x slower                                                    |
| Geometric mean         | (ref)                                                        | 1.16x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 22.0 ms: 1.02x slower                                                    |
| genshi_xml      | 48.8 ms                                                      | 50.0 ms: 1.03x slower                                                    |
| django_template | 34.1 ms                                                      | 35.3 ms: 1.04x slower                                                    |
| mako            | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                    |
| Geometric mean  | (ref)                                                        | 1.03x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 617 ms: 1.48x faster                                                     |
| async_tree_io              | 876 ms                                                       | 601 ms: 1.46x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 338 ms: 1.37x faster                                                     |
| deepcopy                   | 355 us                                                       | 261 us: 1.36x faster                                                     |
| deepcopy_memo              | 39.1 us                                                      | 30.2 us: 1.29x faster                                                    |
| async_tree_none            | 354 ms                                                       | 275 ms: 1.29x faster                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 330 ms: 1.26x faster                                                     |
| async_tree_none_tg         | 336 ms                                                       | 274 ms: 1.23x faster                                                     |
| deepcopy_reduce            | 3.11 us                                                      | 2.63 us: 1.18x faster                                                    |
| go                         | 141 ms                                                       | 122 ms: 1.16x faster                                                     |
| pylint                     | 317 ms                                                       | 280 ms: 1.13x faster                                                     |
| regex_effbot               | 3.08 ms                                                      | 2.78 ms: 1.11x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 601 ms: 1.11x faster                                                     |
| json                       | 4.93 ms                                                      | 4.49 ms: 1.10x faster                                                    |
| json_loads                 | 27.0 us                                                      | 24.9 us: 1.08x faster                                                    |
| coroutines                 | 23.6 ms                                                      | 21.8 ms: 1.08x faster                                                    |
| xml_etree_parse            | 136 ms                                                       | 126 ms: 1.08x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 598 ms: 1.07x faster                                                     |
| telco                      | 7.82 ms                                                      | 7.34 ms: 1.07x faster                                                    |
| pathlib                    | 19.2 ms                                                      | 18.2 ms: 1.05x faster                                                    |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.47 ms: 1.05x faster                                                    |
| thrift                     | 778 us                                                       | 740 us: 1.05x faster                                                     |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.2 ms: 1.05x faster                                                    |
| regex_dna                  | 180 ms                                                       | 172 ms: 1.05x faster                                                     |
| async_generators           | 377 ms                                                       | 359 ms: 1.05x faster                                                     |
| coverage                   | 83.0 ms                                                      | 80.0 ms: 1.04x faster                                                    |
| scimark_fft                | 349 ms                                                       | 337 ms: 1.04x faster                                                     |
| regex_compile              | 132 ms                                                       | 128 ms: 1.03x faster                                                     |
| pprint_safe_repr           | 738 ms                                                       | 718 ms: 1.03x faster                                                     |
| meteor_contest             | 102 ms                                                       | 99.2 ms: 1.02x faster                                                    |
| scimark_lu                 | 113 ms                                                       | 110 ms: 1.02x faster                                                     |
| bpe_tokeniser              | 4.45 sec                                                     | 4.34 sec: 1.02x faster                                                   |
| spectral_norm              | 111 ms                                                       | 109 ms: 1.02x faster                                                     |
| docutils                   | 2.62 sec                                                     | 2.56 sec: 1.02x faster                                                   |
| logging_simple             | 6.16 us                                                      | 6.04 us: 1.02x faster                                                    |
| logging_format             | 6.84 us                                                      | 6.73 us: 1.02x faster                                                    |
| sympy_sum                  | 156 ms                                                       | 153 ms: 1.02x faster                                                     |
| hexiom                     | 5.99 ms                                                      | 5.91 ms: 1.01x faster                                                    |
| pprint_pformat             | 1.50 sec                                                     | 1.48 sec: 1.01x faster                                                   |
| pycparser                  | 1.12 sec                                                     | 1.10 sec: 1.01x faster                                                   |
| nqueens                    | 78.6 ms                                                      | 77.8 ms: 1.01x faster                                                    |
| 2to3                       | 260 ms                                                       | 257 ms: 1.01x faster                                                     |
| asyncio_websockets         | 520 ms                                                       | 522 ms: 1.00x slower                                                     |
| xml_etree_generate         | 85.4 ms                                                      | 85.8 ms: 1.00x slower                                                    |
| xml_etree_process          | 59.3 ms                                                      | 59.7 ms: 1.01x slower                                                    |
| richards_super             | 51.6 ms                                                      | 52.0 ms: 1.01x slower                                                    |
| dulwich_log                | 74.8 ms                                                      | 75.3 ms: 1.01x slower                                                    |
| python_startup_no_site     | 7.39 ms                                                      | 7.46 ms: 1.01x slower                                                    |
| richards                   | 45.2 ms                                                      | 45.6 ms: 1.01x slower                                                    |
| sqlite_synth               | 2.21 us                                                      | 2.23 us: 1.01x slower                                                    |
| sympy_expand               | 457 ms                                                       | 462 ms: 1.01x slower                                                     |
| sqlglot_optimize           | 52.7 ms                                                      | 53.3 ms: 1.01x slower                                                    |
| sqlglot_normalize          | 106 ms                                                       | 107 ms: 1.01x slower                                                     |
| pidigits                   | 217 ms                                                       | 219 ms: 1.01x slower                                                     |
| crypto_pyaes               | 67.9 ms                                                      | 68.7 ms: 1.01x slower                                                    |
| typing_runtime_protocols   | 155 us                                                       | 157 us: 1.02x slower                                                     |
| unpickle_pure_python       | 210 us                                                       | 214 us: 1.02x slower                                                     |
| fannkuch                   | 370 ms                                                       | 377 ms: 1.02x slower                                                     |
| genshi_text                | 21.5 ms                                                      | 22.0 ms: 1.02x slower                                                    |
| sqlglot_transpile          | 1.56 ms                                                      | 1.60 ms: 1.02x slower                                                    |
| genshi_xml                 | 48.8 ms                                                      | 50.0 ms: 1.03x slower                                                    |
| float                      | 77.5 ms                                                      | 79.5 ms: 1.03x slower                                                    |
| deltablue                  | 3.12 ms                                                      | 3.22 ms: 1.03x slower                                                    |
| chaos                      | 57.3 ms                                                      | 59.1 ms: 1.03x slower                                                    |
| sqlglot_parse              | 1.25 ms                                                      | 1.29 ms: 1.03x slower                                                    |
| django_template            | 34.1 ms                                                      | 35.3 ms: 1.04x slower                                                    |
| mako                       | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                    |
| logging_silent             | 103 ns                                                       | 107 ns: 1.04x slower                                                     |
| comprehensions             | 16.5 us                                                      | 17.2 us: 1.05x slower                                                    |
| tomli_loads                | 2.01 sec                                                     | 2.10 sec: 1.05x slower                                                   |
| raytrace                   | 253 ms                                                       | 267 ms: 1.06x slower                                                     |
| regex_v8                   | 22.7 ms                                                      | 24.0 ms: 1.06x slower                                                    |
| pickle_pure_python         | 294 us                                                       | 316 us: 1.07x slower                                                     |
| json_dumps                 | 10.5 ms                                                      | 11.3 ms: 1.08x slower                                                    |
| nbody                      | 85.1 ms                                                      | 93.9 ms: 1.10x slower                                                    |
| bench_thread_pool          | 919 us                                                       | 1.03 ms: 1.12x slower                                                    |
| create_gc_cycles           | 1.34 ms                                                      | 1.71 ms: 1.28x slower                                                    |
| python_startup             | 11.0 ms                                                      | 14.5 ms: 1.32x slower                                                    |
| gc_traversal               | 3.14 ms                                                      | 4.41 ms: 1.40x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                      | 85.5 ms: 7.77x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.00x faster                                                             |

Benchmark hidden because not significant (7): sympy_str, scimark_monte_carlo, generators, sympy_integrate, mdp, scimark_sor, pyflate
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241217-3.14.0a2+-7b72e7b/bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.027x faster

# HPT report

- Reliability score: 98.73% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x