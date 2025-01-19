# Results vs. 3.13.0rc2

- fork: mpage
- ref: aa_test_3
- machine: linux-x86_64
- commit hash: 278858b
- commit date: 2025-01-18
- overall geometric mean: 1.044x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250118-vultr-x86_64-mpage-aa_test_3-3.14.0a4+-278858b |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 255 ms: 1.02x faster                                       |
| docutils       | 2.62 sec                                                     | 2.57 sec: 1.02x faster                                     |
| Geometric mean | (ref)                                                        | 1.02x faster                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250118-vultr-x86_64-mpage-aa_test_3-3.14.0a4+-278858b |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 623 ms: 1.47x faster                                       |
| async_tree_io              | 876 ms                                                       | 615 ms: 1.42x faster                                       |
| async_tree_memoization     | 461 ms                                                       | 330 ms: 1.40x faster                                       |
| async_tree_memoization_tg  | 414 ms                                                       | 307 ms: 1.35x faster                                       |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 495 ms: 1.34x faster                                       |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 475 ms: 1.34x faster                                       |
| async_tree_none_tg         | 336 ms                                                       | 258 ms: 1.30x faster                                       |
| async_tree_none            | 354 ms                                                       | 273 ms: 1.29x faster                                       |
| async_generators           | 377 ms                                                       | 329 ms: 1.15x faster                                       |
| coroutines                 | 23.6 ms                                                      | 21.7 ms: 1.09x faster                                      |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.00x slower                                       |
| Geometric mean             | (ref)                                                        | 1.28x faster                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250118-vultr-x86_64-mpage-aa_test_3-3.14.0a4+-278858b |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| float          | 77.5 ms                                                      | 73.2 ms: 1.06x faster                                      |
| pidigits       | 217 ms                                                       | 214 ms: 1.01x faster                                       |
| nbody          | 85.1 ms                                                      | 87.8 ms: 1.03x slower                                      |
| Geometric mean | (ref)                                                        | 1.01x faster                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250118-vultr-x86_64-mpage-aa_test_3-3.14.0a4+-278858b |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.76 ms: 1.12x faster                                      |
| regex_dna      | 180 ms                                                       | 168 ms: 1.07x faster                                       |
| regex_compile  | 132 ms                                                       | 127 ms: 1.04x faster                                       |
| regex_v8       | 22.7 ms                                                      | 23.5 ms: 1.04x slower                                      |
| Geometric mean | (ref)                                                        | 1.05x faster                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250118-vultr-x86_64-mpage-aa_test_3-3.14.0a4+-278858b |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.07x faster                                       |
| xml_etree_iterparse  | 94.9 ms                                                      | 91.4 ms: 1.04x faster                                      |
| tomli_loads          | 2.01 sec                                                     | 1.93 sec: 1.04x faster                                     |
| xml_etree_generate   | 85.4 ms                                                      | 84.6 ms: 1.01x faster                                      |
| xml_etree_process    | 59.3 ms                                                      | 59.7 ms: 1.01x slower                                      |
| json_loads           | 27.0 us                                                      | 27.7 us: 1.02x slower                                      |
| unpickle_pure_python | 210 us                                                       | 215 us: 1.03x slower                                       |
| pickle_pure_python   | 294 us                                                       | 316 us: 1.07x slower                                       |
| json_dumps           | 10.5 ms                                                      | 11.6 ms: 1.10x slower                                      |
| Geometric mean       | (ref)                                                        | 1.01x slower                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250118-vultr-x86_64-mpage-aa_test_3-3.14.0a4+-278858b |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.47 ms: 1.01x slower                                      |
| python_startup         | 11.0 ms                                                      | 14.7 ms: 1.34x slower                                      |
| Geometric mean         | (ref)                                                        | 1.16x slower                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250118-vultr-x86_64-mpage-aa_test_3-3.14.0a4+-278858b |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 49.0 ms: 1.00x slower                                      |
| mako            | 11.3 ms                                                      | 11.7 ms: 1.04x slower                                      |
| django_template | 34.1 ms                                                      | 35.4 ms: 1.04x slower                                      |
| Geometric mean  | (ref)                                                        | 1.02x slower                                               |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250118-vultr-x86_64-mpage-aa_test_3-3.14.0a4+-278858b |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 623 ms: 1.47x faster                                       |
| async_tree_io              | 876 ms                                                       | 615 ms: 1.42x faster                                       |
| async_tree_memoization     | 461 ms                                                       | 330 ms: 1.40x faster                                       |
| deepcopy                   | 355 us                                                       | 259 us: 1.37x faster                                       |
| async_tree_memoization_tg  | 414 ms                                                       | 307 ms: 1.35x faster                                       |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 495 ms: 1.34x faster                                       |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 475 ms: 1.34x faster                                       |
| async_tree_none_tg         | 336 ms                                                       | 258 ms: 1.30x faster                                       |
| async_tree_none            | 354 ms                                                       | 273 ms: 1.29x faster                                       |
| deepcopy_memo              | 39.1 us                                                      | 30.7 us: 1.27x faster                                      |
| go                         | 141 ms                                                       | 115 ms: 1.22x faster                                       |
| deepcopy_reduce            | 3.11 us                                                      | 2.62 us: 1.19x faster                                      |
| spectral_norm              | 111 ms                                                       | 95.1 ms: 1.17x faster                                      |
| scimark_sor                | 134 ms                                                       | 116 ms: 1.16x faster                                       |
| async_generators           | 377 ms                                                       | 329 ms: 1.15x faster                                       |
| pylint                     | 317 ms                                                       | 282 ms: 1.12x faster                                       |
| regex_effbot               | 3.08 ms                                                      | 2.76 ms: 1.12x faster                                      |
| scimark_fft                | 349 ms                                                       | 320 ms: 1.09x faster                                       |
| telco                      | 7.82 ms                                                      | 7.19 ms: 1.09x faster                                      |
| coroutines                 | 23.6 ms                                                      | 21.7 ms: 1.09x faster                                      |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.38 ms: 1.08x faster                                      |
| regex_dna                  | 180 ms                                                       | 168 ms: 1.07x faster                                       |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.07x faster                                       |
| richards                   | 45.2 ms                                                      | 42.5 ms: 1.06x faster                                      |
| pyflate                    | 449 ms                                                       | 422 ms: 1.06x faster                                       |
| float                      | 77.5 ms                                                      | 73.2 ms: 1.06x faster                                      |
| richards_super             | 51.6 ms                                                      | 48.8 ms: 1.06x faster                                      |
| pathlib                    | 19.2 ms                                                      | 18.3 ms: 1.05x faster                                      |
| thrift                     | 778 us                                                       | 745 us: 1.04x faster                                       |
| bpe_tokeniser              | 4.45 sec                                                     | 4.26 sec: 1.04x faster                                     |
| xml_etree_iterparse        | 94.9 ms                                                      | 91.4 ms: 1.04x faster                                      |
| regex_compile              | 132 ms                                                       | 127 ms: 1.04x faster                                       |
| tomli_loads                | 2.01 sec                                                     | 1.93 sec: 1.04x faster                                     |
| hexiom                     | 5.99 ms                                                      | 5.79 ms: 1.03x faster                                      |
| pprint_safe_repr           | 738 ms                                                       | 715 ms: 1.03x faster                                       |
| coverage                   | 83.0 ms                                                      | 80.4 ms: 1.03x faster                                      |
| pprint_pformat             | 1.50 sec                                                     | 1.45 sec: 1.03x faster                                     |
| 2to3                       | 260 ms                                                       | 255 ms: 1.02x faster                                       |
| sqlite_synth               | 2.21 us                                                      | 2.17 us: 1.02x faster                                      |
| docutils                   | 2.62 sec                                                     | 2.57 sec: 1.02x faster                                     |
| meteor_contest             | 102 ms                                                       | 100 ms: 1.01x faster                                       |
| crypto_pyaes               | 67.9 ms                                                      | 67.0 ms: 1.01x faster                                      |
| sympy_sum                  | 156 ms                                                       | 154 ms: 1.01x faster                                       |
| pidigits                   | 217 ms                                                       | 214 ms: 1.01x faster                                       |
| logging_silent             | 103 ns                                                       | 102 ns: 1.01x faster                                       |
| xml_etree_generate         | 85.4 ms                                                      | 84.6 ms: 1.01x faster                                      |
| chaos                      | 57.3 ms                                                      | 56.8 ms: 1.01x faster                                      |
| scimark_monte_carlo        | 65.4 ms                                                      | 65.1 ms: 1.00x faster                                      |
| nqueens                    | 78.6 ms                                                      | 78.8 ms: 1.00x slower                                      |
| sqlglot_optimize           | 52.7 ms                                                      | 52.9 ms: 1.00x slower                                      |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.00x slower                                       |
| scimark_lu                 | 113 ms                                                       | 113 ms: 1.00x slower                                       |
| genshi_xml                 | 48.8 ms                                                      | 49.0 ms: 1.00x slower                                      |
| sympy_integrate            | 19.8 ms                                                      | 19.9 ms: 1.01x slower                                      |
| xml_etree_process          | 59.3 ms                                                      | 59.7 ms: 1.01x slower                                      |
| fannkuch                   | 370 ms                                                       | 372 ms: 1.01x slower                                       |
| python_startup_no_site     | 7.39 ms                                                      | 7.47 ms: 1.01x slower                                      |
| deltablue                  | 3.12 ms                                                      | 3.16 ms: 1.01x slower                                      |
| dulwich_log                | 74.8 ms                                                      | 75.6 ms: 1.01x slower                                      |
| sympy_expand               | 457 ms                                                       | 462 ms: 1.01x slower                                       |
| sqlglot_transpile          | 1.56 ms                                                      | 1.58 ms: 1.02x slower                                      |
| json                       | 4.93 ms                                                      | 5.02 ms: 1.02x slower                                      |
| sqlglot_parse              | 1.25 ms                                                      | 1.27 ms: 1.02x slower                                      |
| comprehensions             | 16.5 us                                                      | 16.9 us: 1.02x slower                                      |
| json_loads                 | 27.0 us                                                      | 27.7 us: 1.02x slower                                      |
| unpickle_pure_python       | 210 us                                                       | 215 us: 1.03x slower                                       |
| nbody                      | 85.1 ms                                                      | 87.8 ms: 1.03x slower                                      |
| regex_v8                   | 22.7 ms                                                      | 23.5 ms: 1.04x slower                                      |
| mako                       | 11.3 ms                                                      | 11.7 ms: 1.04x slower                                      |
| django_template            | 34.1 ms                                                      | 35.4 ms: 1.04x slower                                      |
| typing_runtime_protocols   | 155 us                                                       | 160 us: 1.04x slower                                       |
| raytrace                   | 253 ms                                                       | 268 ms: 1.06x slower                                       |
| pickle_pure_python         | 294 us                                                       | 316 us: 1.07x slower                                       |
| json_dumps                 | 10.5 ms                                                      | 11.6 ms: 1.10x slower                                      |
| bench_thread_pool          | 919 us                                                       | 1.04 ms: 1.14x slower                                      |
| python_startup             | 11.0 ms                                                      | 14.7 ms: 1.34x slower                                      |
| gc_traversal               | 3.14 ms                                                      | 4.28 ms: 1.36x slower                                      |
| create_gc_cycles           | 1.34 ms                                                      | 1.82 ms: 1.36x slower                                      |
| bench_mp_pool              | 11.0 ms                                                      | 88.7 ms: 8.07x slower                                      |
| Geometric mean             | (ref)                                                        | 1.02x faster                                               |

Benchmark hidden because not significant (8): logging_format, genshi_text, pycparser, mdp, sympy_str, sqlglot_normalize, generators, logging_simple
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250118-3.14.0a4+-278858b/bm-20250118-vultr-x86_64-mpage-aa_test_3-3.14.0a4+-278858b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.044x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x