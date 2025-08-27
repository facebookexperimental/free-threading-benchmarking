# Results vs. 3.13.0rc2

- fork: python
- ref: ffaec6e2a11fb7b41fac
- machine: linux-x86_64
- commit hash: ffaec6e
- commit date: 2025-08-27
- overall geometric mean: 1.037x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 250 ms: 1.04x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.56 sec: 1.02x faster                                                |
| html5lib       | 67.0 ms                                                      | 61.5 ms: 1.09x faster                                                 |
| Geometric mean | (ref)                                                        | 1.05x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 594 ms: 1.48x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 619 ms: 1.47x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 314 ms: 1.47x faster                                                  |
| async_tree_none            | 354 ms                                                       | 256 ms: 1.38x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 498 ms: 1.34x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 311 ms: 1.33x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 254 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 505 ms: 1.26x faster                                                  |
| async_generators           | 377 ms                                                       | 340 ms: 1.11x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.7 ms: 1.00x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.28x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 72.1 ms: 1.07x faster                                                 |
| pidigits       | 217 ms                                                       | 218 ms: 1.01x slower                                                  |
| nbody          | 85.1 ms                                                      | 91.3 ms: 1.07x slower                                                 |
| Geometric mean | (ref)                                                        | 1.00x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.60 ms: 1.19x faster                                                 |
| regex_dna      | 180 ms                                                       | 167 ms: 1.08x faster                                                  |
| regex_compile  | 132 ms                                                       | 123 ms: 1.08x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 21.6 ms: 1.05x faster                                                 |
| Geometric mean | (ref)                                                        | 1.10x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e |
|---------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps          | 10.5 ms                                                      | 9.69 ms: 1.09x faster                                                 |
| tomli_loads         | 2.01 sec                                                     | 1.89 sec: 1.06x faster                                                |
| xml_etree_parse     | 136 ms                                                       | 131 ms: 1.04x faster                                                  |
| xml_etree_generate  | 85.4 ms                                                      | 82.4 ms: 1.04x faster                                                 |
| xml_etree_process   | 59.3 ms                                                      | 57.8 ms: 1.03x faster                                                 |
| xml_etree_iterparse | 94.9 ms                                                      | 92.6 ms: 1.03x faster                                                 |
| pickle_pure_python  | 294 us                                                       | 304 us: 1.03x slower                                                  |
| json_loads          | 27.0 us                                                      | 28.3 us: 1.05x slower                                                 |
| Geometric mean      | (ref)                                                        | 1.02x faster                                                          |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.21 ms: 1.03x faster                                                 |
| python_startup         | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.05x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 20.7 ms: 1.04x faster                                                 |
| django_template | 34.1 ms                                                      | 34.7 ms: 1.02x slower                                                 |
| mako            | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.00x slower                                                          |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.15 sec: 2.04x faster                                                |
| async_tree_io              | 876 ms                                                       | 594 ms: 1.48x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 619 ms: 1.47x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 314 ms: 1.47x faster                                                  |
| deepcopy                   | 355 us                                                       | 252 us: 1.41x faster                                                  |
| async_tree_none            | 354 ms                                                       | 256 ms: 1.38x faster                                                  |
| go                         | 141 ms                                                       | 104 ms: 1.36x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 28.8 us: 1.36x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 498 ms: 1.34x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 311 ms: 1.33x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 254 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 505 ms: 1.26x faster                                                  |
| scimark_sor                | 134 ms                                                       | 108 ms: 1.24x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.61 us: 1.19x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.60 ms: 1.19x faster                                                 |
| spectral_norm              | 111 ms                                                       | 94.4 ms: 1.18x faster                                                 |
| pylint                     | 317 ms                                                       | 279 ms: 1.14x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 66.1 ms: 1.13x faster                                                 |
| pyflate                    | 449 ms                                                       | 399 ms: 1.12x faster                                                  |
| async_generators           | 377 ms                                                       | 340 ms: 1.11x faster                                                  |
| richards_super             | 51.6 ms                                                      | 47.0 ms: 1.10x faster                                                 |
| richards                   | 45.2 ms                                                      | 41.3 ms: 1.09x faster                                                 |
| html5lib                   | 67.0 ms                                                      | 61.5 ms: 1.09x faster                                                 |
| json_dumps                 | 10.5 ms                                                      | 9.69 ms: 1.09x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 680 ms: 1.08x faster                                                  |
| regex_dna                  | 180 ms                                                       | 167 ms: 1.08x faster                                                  |
| regex_compile              | 132 ms                                                       | 123 ms: 1.08x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.39 sec: 1.08x faster                                                |
| float                      | 77.5 ms                                                      | 72.1 ms: 1.07x faster                                                 |
| logging_simple             | 6.16 us                                                      | 5.74 us: 1.07x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.63 ms: 1.06x faster                                                 |
| tomli_loads                | 2.01 sec                                                     | 1.89 sec: 1.06x faster                                                |
| logging_format             | 6.84 us                                                      | 6.44 us: 1.06x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.20 sec: 1.06x faster                                                |
| sympy_integrate            | 19.8 ms                                                      | 18.8 ms: 1.06x faster                                                 |
| scimark_fft                | 349 ms                                                       | 331 ms: 1.06x faster                                                  |
| thrift                     | 778 us                                                       | 738 us: 1.05x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 21.6 ms: 1.05x faster                                                 |
| comprehensions             | 16.5 us                                                      | 15.6 us: 1.05x faster                                                 |
| generators                 | 28.8 ms                                                      | 27.6 ms: 1.04x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                  |
| logging_silent             | 103 ns                                                       | 98.5 ns: 1.04x faster                                                 |
| 2to3                       | 260 ms                                                       | 250 ms: 1.04x faster                                                  |
| genshi_text                | 21.5 ms                                                      | 20.7 ms: 1.04x faster                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 63.0 ms: 1.04x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 82.4 ms: 1.04x faster                                                 |
| pycparser                  | 1.12 sec                                                     | 1.08 sec: 1.03x faster                                                |
| nqueens                    | 78.6 ms                                                      | 76.4 ms: 1.03x faster                                                 |
| chaos                      | 57.3 ms                                                      | 55.8 ms: 1.03x faster                                                 |
| xml_etree_process          | 59.3 ms                                                      | 57.8 ms: 1.03x faster                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 7.21 ms: 1.03x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 92.6 ms: 1.03x faster                                                 |
| sympy_str                  | 275 ms                                                       | 269 ms: 1.02x faster                                                  |
| sympy_sum                  | 156 ms                                                       | 152 ms: 1.02x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.56 sec: 1.02x faster                                                |
| meteor_contest             | 102 ms                                                       | 99.9 ms: 1.02x faster                                                 |
| coverage                   | 83.0 ms                                                      | 81.9 ms: 1.01x faster                                                 |
| deltablue                  | 3.12 ms                                                      | 3.08 ms: 1.01x faster                                                 |
| scimark_lu                 | 113 ms                                                       | 112 ms: 1.01x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 19.1 ms: 1.01x faster                                                 |
| raytrace                   | 253 ms                                                       | 251 ms: 1.01x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.7 ms: 1.00x slower                                                 |
| pidigits                   | 217 ms                                                       | 218 ms: 1.01x slower                                                  |
| django_template            | 34.1 ms                                                      | 34.7 ms: 1.02x slower                                                 |
| sympy_expand               | 457 ms                                                       | 465 ms: 1.02x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 69.3 ms: 1.02x slower                                                 |
| fannkuch                   | 370 ms                                                       | 380 ms: 1.03x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 304 us: 1.03x slower                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.29 us: 1.04x slower                                                 |
| mako                       | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                 |
| json_loads                 | 27.0 us                                                      | 28.3 us: 1.05x slower                                                 |
| json                       | 4.93 ms                                                      | 5.21 ms: 1.06x slower                                                 |
| nbody                      | 85.1 ms                                                      | 91.3 ms: 1.07x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.01 ms: 1.10x slower                                                 |
| python_startup             | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.37 ms: 1.39x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.93 ms: 1.44x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 103 ms: 9.39x slower                                                  |
| telco                      | 7.82 ms                                                      | 158 ms: 20.14x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.01x faster                                                          |

Benchmark hidden because not significant (4): typing_runtime_protocols, scimark_sparse_mat_mult, unpickle_pure_python, genshi_xml
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250827-3.15.0a0-ffaec6e/bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.037x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.15x