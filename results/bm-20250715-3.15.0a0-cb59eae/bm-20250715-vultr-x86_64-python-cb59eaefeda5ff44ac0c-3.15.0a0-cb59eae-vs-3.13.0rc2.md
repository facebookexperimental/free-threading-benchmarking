# Results vs. 3.13.0rc2

- fork: python
- ref: cb59eaefeda5ff44ac0c
- machine: linux-x86_64
- commit hash: cb59eae
- commit date: 2025-07-15
- overall geometric mean: 1.034x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 251 ms: 1.04x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.57 sec: 1.02x faster                                                |
| html5lib       | 67.0 ms                                                      | 61.2 ms: 1.10x faster                                                 |
| Geometric mean | (ref)                                                        | 1.05x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 615 ms: 1.48x faster                                                  |
| async_tree_io              | 876 ms                                                       | 594 ms: 1.47x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 315 ms: 1.47x faster                                                  |
| async_tree_none            | 354 ms                                                       | 255 ms: 1.39x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 500 ms: 1.33x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 313 ms: 1.33x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 255 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 505 ms: 1.26x faster                                                  |
| async_generators           | 377 ms                                                       | 342 ms: 1.10x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.2 ms: 1.01x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                  |
| Geometric mean             | (ref)                                                        | 1.28x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 203 ms: 1.07x faster                                                  |
| float          | 77.5 ms                                                      | 72.6 ms: 1.07x faster                                                 |
| nbody          | 85.1 ms                                                      | 87.8 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                        | 1.03x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.62 ms: 1.18x faster                                                 |
| regex_compile  | 132 ms                                                       | 124 ms: 1.06x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 21.5 ms: 1.05x faster                                                 |
| regex_dna      | 180 ms                                                       | 174 ms: 1.04x faster                                                  |
| Geometric mean | (ref)                                                        | 1.08x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|---------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads         | 2.01 sec                                                     | 1.92 sec: 1.04x faster                                                |
| xml_etree_parse     | 136 ms                                                       | 131 ms: 1.04x faster                                                  |
| xml_etree_iterparse | 94.9 ms                                                      | 92.5 ms: 1.03x faster                                                 |
| xml_etree_process   | 59.3 ms                                                      | 58.0 ms: 1.02x faster                                                 |
| xml_etree_generate  | 85.4 ms                                                      | 83.6 ms: 1.02x faster                                                 |
| json_dumps          | 10.5 ms                                                      | 10.8 ms: 1.03x slower                                                 |
| pickle_pure_python  | 294 us                                                       | 304 us: 1.03x slower                                                  |
| json_loads          | 27.0 us                                                      | 27.9 us: 1.03x slower                                                 |
| Geometric mean      | (ref)                                                        | 1.01x faster                                                          |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.15 ms: 1.03x faster                                                 |
| python_startup         | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.05x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 20.6 ms: 1.05x faster                                                 |
| django_template | 34.1 ms                                                      | 34.5 ms: 1.01x slower                                                 |
| mako            | 11.3 ms                                                      | 11.5 ms: 1.01x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.01x faster                                                          |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.15 sec: 2.05x faster                                                |
| async_tree_io_tg           | 913 ms                                                       | 615 ms: 1.48x faster                                                  |
| async_tree_io              | 876 ms                                                       | 594 ms: 1.47x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 315 ms: 1.47x faster                                                  |
| deepcopy                   | 355 us                                                       | 252 us: 1.41x faster                                                  |
| async_tree_none            | 354 ms                                                       | 255 ms: 1.39x faster                                                  |
| go                         | 141 ms                                                       | 103 ms: 1.37x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 29.3 us: 1.33x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 500 ms: 1.33x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 313 ms: 1.33x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 255 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 505 ms: 1.26x faster                                                  |
| scimark_sor                | 134 ms                                                       | 109 ms: 1.23x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.62 ms: 1.18x faster                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 2.68 us: 1.16x faster                                                 |
| spectral_norm              | 111 ms                                                       | 96.4 ms: 1.15x faster                                                 |
| pylint                     | 317 ms                                                       | 279 ms: 1.13x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 66.5 ms: 1.13x faster                                                 |
| richards_super             | 51.6 ms                                                      | 46.6 ms: 1.11x faster                                                 |
| richards                   | 45.2 ms                                                      | 40.9 ms: 1.11x faster                                                 |
| async_generators           | 377 ms                                                       | 342 ms: 1.10x faster                                                  |
| pyflate                    | 449 ms                                                       | 407 ms: 1.10x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 61.2 ms: 1.10x faster                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 61.0 ms: 1.07x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.60 ms: 1.07x faster                                                 |
| pidigits                   | 217 ms                                                       | 203 ms: 1.07x faster                                                  |
| float                      | 77.5 ms                                                      | 72.6 ms: 1.07x faster                                                 |
| comprehensions             | 16.5 us                                                      | 15.4 us: 1.07x faster                                                 |
| regex_compile              | 132 ms                                                       | 124 ms: 1.06x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 21.5 ms: 1.05x faster                                                 |
| sympy_integrate            | 19.8 ms                                                      | 18.8 ms: 1.05x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.22 sec: 1.05x faster                                                |
| thrift                     | 778 us                                                       | 740 us: 1.05x faster                                                  |
| logging_simple             | 6.16 us                                                      | 5.87 us: 1.05x faster                                                 |
| genshi_text                | 21.5 ms                                                      | 20.6 ms: 1.05x faster                                                 |
| tomli_loads                | 2.01 sec                                                     | 1.92 sec: 1.04x faster                                                |
| pprint_safe_repr           | 738 ms                                                       | 707 ms: 1.04x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.44 sec: 1.04x faster                                                |
| logging_silent             | 103 ns                                                       | 99.0 ns: 1.04x faster                                                 |
| 2to3                       | 260 ms                                                       | 251 ms: 1.04x faster                                                  |
| regex_dna                  | 180 ms                                                       | 174 ms: 1.04x faster                                                  |
| scimark_fft                | 349 ms                                                       | 338 ms: 1.03x faster                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.15 ms: 1.03x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 92.5 ms: 1.03x faster                                                 |
| sympy_str                  | 275 ms                                                       | 268 ms: 1.02x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 58.0 ms: 1.02x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 83.6 ms: 1.02x faster                                                 |
| meteor_contest             | 102 ms                                                       | 99.6 ms: 1.02x faster                                                 |
| deltablue                  | 3.12 ms                                                      | 3.06 ms: 1.02x faster                                                 |
| pycparser                  | 1.12 sec                                                     | 1.10 sec: 1.02x faster                                                |
| chaos                      | 57.3 ms                                                      | 56.3 ms: 1.02x faster                                                 |
| typing_runtime_protocols   | 155 us                                                       | 152 us: 1.02x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.57 sec: 1.02x faster                                                |
| coverage                   | 83.0 ms                                                      | 81.6 ms: 1.02x faster                                                 |
| scimark_lu                 | 113 ms                                                       | 111 ms: 1.01x faster                                                  |
| generators                 | 28.8 ms                                                      | 28.4 ms: 1.01x faster                                                 |
| coroutines                 | 23.6 ms                                                      | 23.2 ms: 1.01x faster                                                 |
| sympy_sum                  | 156 ms                                                       | 154 ms: 1.01x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.77 us: 1.01x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                  |
| nqueens                    | 78.6 ms                                                      | 78.2 ms: 1.00x faster                                                 |
| raytrace                   | 253 ms                                                       | 252 ms: 1.00x faster                                                  |
| sympy_expand               | 457 ms                                                       | 460 ms: 1.01x slower                                                  |
| django_template            | 34.1 ms                                                      | 34.5 ms: 1.01x slower                                                 |
| mako                       | 11.3 ms                                                      | 11.5 ms: 1.01x slower                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 69.1 ms: 1.02x slower                                                 |
| pathlib                    | 19.2 ms                                                      | 19.6 ms: 1.02x slower                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.82 ms: 1.02x slower                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.27 us: 1.03x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 10.8 ms: 1.03x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 304 us: 1.03x slower                                                  |
| nbody                      | 85.1 ms                                                      | 87.8 ms: 1.03x slower                                                 |
| json_loads                 | 27.0 us                                                      | 27.9 us: 1.03x slower                                                 |
| fannkuch                   | 370 ms                                                       | 385 ms: 1.04x slower                                                  |
| json                       | 4.93 ms                                                      | 5.13 ms: 1.04x slower                                                 |
| python_startup             | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.05 ms: 1.14x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.30 ms: 1.37x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.93 ms: 1.44x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 103 ms: 9.37x slower                                                  |
| telco                      | 7.82 ms                                                      | 159 ms: 20.36x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.01x faster                                                          |

Benchmark hidden because not significant (2): unpickle_pure_python, genshi_xml
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250715-3.15.0a0-cb59eae/bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.034x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.15x