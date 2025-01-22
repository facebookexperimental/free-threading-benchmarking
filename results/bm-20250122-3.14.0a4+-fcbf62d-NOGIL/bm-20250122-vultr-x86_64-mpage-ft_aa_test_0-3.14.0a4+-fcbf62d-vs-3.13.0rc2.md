# Results vs. 3.13.0rc2

- fork: mpage
- ref: ft_aa_test_0
- machine: linux-x86_64
- commit hash: fcbf62d
- commit date: 2025-01-22
- overall geometric mean: 1.111x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4+-fcbf62d |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 314 ms: 1.21x slower                                          |
| docutils       | 2.62 sec                                                     | 2.86 sec: 1.09x slower                                        |
| html5lib       | 67.0 ms                                                      | 74.9 ms: 1.12x slower                                         |
| Geometric mean | (ref)                                                        | 1.14x slower                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4+-fcbf62d |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 582 ms: 1.57x faster                                          |
| async_tree_io              | 876 ms                                                       | 619 ms: 1.42x faster                                          |
| async_tree_none_tg         | 336 ms                                                       | 246 ms: 1.37x faster                                          |
| async_tree_memoization_tg  | 414 ms                                                       | 318 ms: 1.30x faster                                          |
| async_tree_memoization     | 461 ms                                                       | 357 ms: 1.29x faster                                          |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 502 ms: 1.27x faster                                          |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 537 ms: 1.24x faster                                          |
| async_tree_none            | 354 ms                                                       | 289 ms: 1.22x faster                                          |
| asyncio_websockets         | 520 ms                                                       | 513 ms: 1.01x faster                                          |
| async_generators           | 377 ms                                                       | 376 ms: 1.00x faster                                          |
| coroutines                 | 23.6 ms                                                      | 25.4 ms: 1.08x slower                                         |
| Geometric mean             | (ref)                                                        | 1.22x faster                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4+-fcbf62d |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 196 ms: 1.11x faster                                          |
| float          | 77.5 ms                                                      | 78.0 ms: 1.01x slower                                         |
| nbody          | 85.1 ms                                                      | 141 ms: 1.66x slower                                          |
| Geometric mean | (ref)                                                        | 1.15x slower                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4+-fcbf62d |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.88 ms: 1.07x faster                                         |
| regex_dna      | 180 ms                                                       | 183 ms: 1.01x slower                                          |
| regex_v8       | 22.7 ms                                                      | 23.8 ms: 1.05x slower                                         |
| regex_compile  | 132 ms                                                       | 160 ms: 1.21x slower                                          |
| Geometric mean | (ref)                                                        | 1.05x slower                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4+-fcbf62d |
|----------------------|:------------------------------------------------------------:|:-------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 87.9 ms: 1.08x faster                                         |
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.07x faster                                          |
| json_loads           | 27.0 us                                                      | 30.6 us: 1.13x slower                                         |
| xml_etree_generate   | 85.4 ms                                                      | 99.0 ms: 1.16x slower                                         |
| json_dumps           | 10.5 ms                                                      | 13.0 ms: 1.23x slower                                         |
| tomli_loads          | 2.01 sec                                                     | 2.49 sec: 1.24x slower                                        |
| xml_etree_process    | 59.3 ms                                                      | 75.6 ms: 1.27x slower                                         |
| unpickle_pure_python | 210 us                                                       | 275 us: 1.31x slower                                          |
| pickle_pure_python   | 294 us                                                       | 399 us: 1.36x slower                                          |
| Geometric mean       | (ref)                                                        | 1.16x slower                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4+-fcbf62d |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.53 ms: 1.29x slower                                         |
| python_startup         | 11.0 ms                                                      | 15.3 ms: 1.39x slower                                         |
| Geometric mean         | (ref)                                                        | 1.34x slower                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4+-fcbf62d |
|-----------------|:------------------------------------------------------------:|:-------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 64.0 ms: 1.31x slower                                         |
| django_template | 34.1 ms                                                      | 45.0 ms: 1.32x slower                                         |
| genshi_text     | 21.5 ms                                                      | 29.9 ms: 1.39x slower                                         |
| mako            | 11.3 ms                                                      | 16.3 ms: 1.44x slower                                         |
| Geometric mean  | (ref)                                                        | 1.36x slower                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4+-fcbf62d |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 582 ms: 1.57x faster                                          |
| async_tree_io              | 876 ms                                                       | 619 ms: 1.42x faster                                          |
| async_tree_none_tg         | 336 ms                                                       | 246 ms: 1.37x faster                                          |
| async_tree_memoization_tg  | 414 ms                                                       | 318 ms: 1.30x faster                                          |
| async_tree_memoization     | 461 ms                                                       | 357 ms: 1.29x faster                                          |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 502 ms: 1.27x faster                                          |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 537 ms: 1.24x faster                                          |
| async_tree_none            | 354 ms                                                       | 289 ms: 1.22x faster                                          |
| pidigits                   | 217 ms                                                       | 196 ms: 1.11x faster                                          |
| deepcopy                   | 355 us                                                       | 328 us: 1.08x faster                                          |
| xml_etree_iterparse        | 94.9 ms                                                      | 87.9 ms: 1.08x faster                                         |
| sqlite_synth               | 2.21 us                                                      | 2.05 us: 1.08x faster                                         |
| regex_effbot               | 3.08 ms                                                      | 2.88 ms: 1.07x faster                                         |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.07x faster                                          |
| create_gc_cycles           | 1.34 ms                                                      | 1.32 ms: 1.02x faster                                         |
| asyncio_websockets         | 520 ms                                                       | 513 ms: 1.01x faster                                          |
| pathlib                    | 19.2 ms                                                      | 18.9 ms: 1.01x faster                                         |
| async_generators           | 377 ms                                                       | 376 ms: 1.00x faster                                          |
| float                      | 77.5 ms                                                      | 78.0 ms: 1.01x slower                                         |
| regex_dna                  | 180 ms                                                       | 183 ms: 1.01x slower                                          |
| spectral_norm              | 111 ms                                                       | 113 ms: 1.02x slower                                          |
| go                         | 141 ms                                                       | 145 ms: 1.03x slower                                          |
| gc_traversal               | 3.14 ms                                                      | 3.25 ms: 1.03x slower                                         |
| deepcopy_memo              | 39.1 us                                                      | 40.8 us: 1.04x slower                                         |
| scimark_sor                | 134 ms                                                       | 141 ms: 1.05x slower                                          |
| regex_v8                   | 22.7 ms                                                      | 23.8 ms: 1.05x slower                                         |
| coroutines                 | 23.6 ms                                                      | 25.4 ms: 1.08x slower                                         |
| json                       | 4.93 ms                                                      | 5.34 ms: 1.08x slower                                         |
| bpe_tokeniser              | 4.45 sec                                                     | 4.82 sec: 1.09x slower                                        |
| docutils                   | 2.62 sec                                                     | 2.86 sec: 1.09x slower                                        |
| deepcopy_reduce            | 3.11 us                                                      | 3.44 us: 1.10x slower                                         |
| telco                      | 7.82 ms                                                      | 8.66 ms: 1.11x slower                                         |
| pycparser                  | 1.12 sec                                                     | 1.24 sec: 1.11x slower                                        |
| html5lib                   | 67.0 ms                                                      | 74.9 ms: 1.12x slower                                         |
| dulwich_log                | 74.8 ms                                                      | 83.8 ms: 1.12x slower                                         |
| json_loads                 | 27.0 us                                                      | 30.6 us: 1.13x slower                                         |
| scimark_fft                | 349 ms                                                       | 398 ms: 1.14x slower                                          |
| generators                 | 28.8 ms                                                      | 33.3 ms: 1.16x slower                                         |
| xml_etree_generate         | 85.4 ms                                                      | 99.0 ms: 1.16x slower                                         |
| mdp                        | 2.36 sec                                                     | 2.74 sec: 1.16x slower                                        |
| pprint_safe_repr           | 738 ms                                                       | 859 ms: 1.16x slower                                          |
| pyflate                    | 449 ms                                                       | 525 ms: 1.17x slower                                          |
| sqlglot_normalize          | 106 ms                                                       | 124 ms: 1.17x slower                                          |
| logging_silent             | 103 ns                                                       | 121 ns: 1.18x slower                                          |
| sqlglot_optimize           | 52.7 ms                                                      | 62.5 ms: 1.19x slower                                         |
| pprint_pformat             | 1.50 sec                                                     | 1.78 sec: 1.19x slower                                        |
| thrift                     | 778 us                                                       | 925 us: 1.19x slower                                          |
| coverage                   | 83.0 ms                                                      | 98.8 ms: 1.19x slower                                         |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.67 ms: 1.20x slower                                         |
| 2to3                       | 260 ms                                                       | 314 ms: 1.21x slower                                          |
| regex_compile              | 132 ms                                                       | 160 ms: 1.21x slower                                          |
| sympy_expand               | 457 ms                                                       | 561 ms: 1.23x slower                                          |
| sympy_sum                  | 156 ms                                                       | 191 ms: 1.23x slower                                          |
| json_dumps                 | 10.5 ms                                                      | 13.0 ms: 1.23x slower                                         |
| tomli_loads                | 2.01 sec                                                     | 2.49 sec: 1.24x slower                                        |
| richards                   | 45.2 ms                                                      | 56.6 ms: 1.25x slower                                         |
| sympy_integrate            | 19.8 ms                                                      | 24.9 ms: 1.26x slower                                         |
| chaos                      | 57.3 ms                                                      | 72.1 ms: 1.26x slower                                         |
| sympy_str                  | 275 ms                                                       | 346 ms: 1.26x slower                                          |
| scimark_lu                 | 113 ms                                                       | 142 ms: 1.26x slower                                          |
| logging_simple             | 6.16 us                                                      | 7.80 us: 1.27x slower                                         |
| xml_etree_process          | 59.3 ms                                                      | 75.6 ms: 1.27x slower                                         |
| richards_super             | 51.6 ms                                                      | 66.0 ms: 1.28x slower                                         |
| sqlglot_transpile          | 1.56 ms                                                      | 2.00 ms: 1.28x slower                                         |
| nqueens                    | 78.6 ms                                                      | 101 ms: 1.28x slower                                          |
| sqlglot_parse              | 1.25 ms                                                      | 1.61 ms: 1.29x slower                                         |
| logging_format             | 6.84 us                                                      | 8.81 us: 1.29x slower                                         |
| python_startup_no_site     | 7.39 ms                                                      | 9.53 ms: 1.29x slower                                         |
| scimark_monte_carlo        | 65.4 ms                                                      | 84.3 ms: 1.29x slower                                         |
| comprehensions             | 16.5 us                                                      | 21.3 us: 1.30x slower                                         |
| hexiom                     | 5.99 ms                                                      | 7.77 ms: 1.30x slower                                         |
| meteor_contest             | 102 ms                                                       | 133 ms: 1.31x slower                                          |
| crypto_pyaes               | 67.9 ms                                                      | 88.9 ms: 1.31x slower                                         |
| unpickle_pure_python       | 210 us                                                       | 275 us: 1.31x slower                                          |
| genshi_xml                 | 48.8 ms                                                      | 64.0 ms: 1.31x slower                                         |
| django_template            | 34.1 ms                                                      | 45.0 ms: 1.32x slower                                         |
| raytrace                   | 253 ms                                                       | 340 ms: 1.35x slower                                          |
| pickle_pure_python         | 294 us                                                       | 399 us: 1.36x slower                                          |
| fannkuch                   | 370 ms                                                       | 502 ms: 1.36x slower                                          |
| typing_runtime_protocols   | 155 us                                                       | 211 us: 1.36x slower                                          |
| genshi_text                | 21.5 ms                                                      | 29.9 ms: 1.39x slower                                         |
| python_startup             | 11.0 ms                                                      | 15.3 ms: 1.39x slower                                         |
| mako                       | 11.3 ms                                                      | 16.3 ms: 1.44x slower                                         |
| deltablue                  | 3.12 ms                                                      | 4.77 ms: 1.53x slower                                         |
| nbody                      | 85.1 ms                                                      | 141 ms: 1.66x slower                                          |
| bench_thread_pool          | 919 us                                                       | 3.32 ms: 3.62x slower                                         |
| bench_mp_pool              | 11.0 ms                                                      | 95.4 ms: 8.68x slower                                         |
| Geometric mean             | (ref)                                                        | 1.17x slower                                                  |

Benchmark hidden because not significant (1): pylint
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250122-3.14.0a4+-fcbf62d-NOGIL/bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4+-fcbf62d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.111x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.33x