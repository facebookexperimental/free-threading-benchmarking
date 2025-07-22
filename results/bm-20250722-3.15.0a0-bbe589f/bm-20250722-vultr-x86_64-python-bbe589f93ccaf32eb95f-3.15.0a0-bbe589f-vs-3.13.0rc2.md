# Results vs. 3.13.0rc2

- fork: python
- ref: bbe589f93ccaf32eb95f
- machine: linux-x86_64
- commit hash: bbe589f
- commit date: 2025-07-22
- overall geometric mean: 1.037x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 249 ms: 1.04x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.56 sec: 1.02x faster                                                |
| html5lib       | 67.0 ms                                                      | 61.2 ms: 1.09x faster                                                 |
| Geometric mean | (ref)                                                        | 1.05x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 585 ms: 1.50x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 612 ms: 1.49x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 312 ms: 1.48x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 491 ms: 1.36x faster                                                  |
| async_tree_none            | 354 ms                                                       | 264 ms: 1.34x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 313 ms: 1.32x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 258 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 491 ms: 1.30x faster                                                  |
| async_generators           | 377 ms                                                       | 338 ms: 1.12x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                  |
| Geometric mean             | (ref)                                                        | 1.28x faster                                                          |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 71.8 ms: 1.08x faster                                                 |
| pidigits       | 217 ms                                                       | 217 ms: 1.00x slower                                                  |
| nbody          | 85.1 ms                                                      | 89.3 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                        | 1.01x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.60 ms: 1.18x faster                                                 |
| regex_dna      | 180 ms                                                       | 164 ms: 1.10x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 20.8 ms: 1.09x faster                                                 |
| regex_compile  | 132 ms                                                       | 124 ms: 1.07x faster                                                  |
| Geometric mean | (ref)                                                        | 1.11x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.93 sec: 1.04x faster                                                |
| xml_etree_process    | 59.3 ms                                                      | 57.4 ms: 1.03x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 83.0 ms: 1.03x faster                                                 |
| xml_etree_iterparse  | 94.9 ms                                                      | 92.6 ms: 1.03x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 133 ms: 1.02x faster                                                  |
| unpickle_pure_python | 210 us                                                       | 207 us: 1.01x faster                                                  |
| json_dumps           | 10.5 ms                                                      | 10.7 ms: 1.02x slower                                                 |
| json_loads           | 27.0 us                                                      | 27.9 us: 1.03x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 306 us: 1.04x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.24 ms: 1.02x faster                                                 |
| python_startup         | 11.0 ms                                                      | 12.5 ms: 1.13x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.05x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 20.8 ms: 1.04x faster                                                 |
| genshi_xml      | 48.8 ms                                                      | 47.9 ms: 1.02x faster                                                 |
| mako            | 11.3 ms                                                      | 11.6 ms: 1.02x slower                                                 |
| django_template | 34.1 ms                                                      | 35.0 ms: 1.02x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.00x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.14 sec: 2.07x faster                                                |
| async_tree_io              | 876 ms                                                       | 585 ms: 1.50x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 612 ms: 1.49x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 312 ms: 1.48x faster                                                  |
| deepcopy                   | 355 us                                                       | 250 us: 1.42x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 28.3 us: 1.38x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 491 ms: 1.36x faster                                                  |
| go                         | 141 ms                                                       | 104 ms: 1.35x faster                                                  |
| async_tree_none            | 354 ms                                                       | 264 ms: 1.34x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 313 ms: 1.32x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 258 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 491 ms: 1.30x faster                                                  |
| scimark_sor                | 134 ms                                                       | 107 ms: 1.25x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.60 ms: 1.18x faster                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 2.64 us: 1.18x faster                                                 |
| spectral_norm              | 111 ms                                                       | 96.6 ms: 1.15x faster                                                 |
| pylint                     | 317 ms                                                       | 281 ms: 1.13x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 66.3 ms: 1.13x faster                                                 |
| pyflate                    | 449 ms                                                       | 398 ms: 1.13x faster                                                  |
| async_generators           | 377 ms                                                       | 338 ms: 1.12x faster                                                  |
| richards                   | 45.2 ms                                                      | 41.0 ms: 1.10x faster                                                 |
| regex_dna                  | 180 ms                                                       | 164 ms: 1.10x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 61.2 ms: 1.09x faster                                                 |
| richards_super             | 51.6 ms                                                      | 47.2 ms: 1.09x faster                                                 |
| regex_v8                   | 22.7 ms                                                      | 20.8 ms: 1.09x faster                                                 |
| float                      | 77.5 ms                                                      | 71.8 ms: 1.08x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 686 ms: 1.08x faster                                                  |
| scimark_fft                | 349 ms                                                       | 326 ms: 1.07x faster                                                  |
| regex_compile              | 132 ms                                                       | 124 ms: 1.07x faster                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 61.1 ms: 1.07x faster                                                 |
| comprehensions             | 16.5 us                                                      | 15.4 us: 1.07x faster                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.40 sec: 1.07x faster                                                |
| logging_silent             | 103 ns                                                       | 96.2 ns: 1.07x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.19 sec: 1.06x faster                                                |
| hexiom                     | 5.99 ms                                                      | 5.66 ms: 1.06x faster                                                 |
| logging_simple             | 6.16 us                                                      | 5.84 us: 1.05x faster                                                 |
| sympy_integrate            | 19.8 ms                                                      | 18.9 ms: 1.05x faster                                                 |
| thrift                     | 778 us                                                       | 747 us: 1.04x faster                                                  |
| 2to3                       | 260 ms                                                       | 249 ms: 1.04x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.93 sec: 1.04x faster                                                |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.53 ms: 1.04x faster                                                 |
| logging_format             | 6.84 us                                                      | 6.60 us: 1.04x faster                                                 |
| genshi_text                | 21.5 ms                                                      | 20.8 ms: 1.04x faster                                                 |
| xml_etree_process          | 59.3 ms                                                      | 57.4 ms: 1.03x faster                                                 |
| scimark_lu                 | 113 ms                                                       | 109 ms: 1.03x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 83.0 ms: 1.03x faster                                                 |
| nqueens                    | 78.6 ms                                                      | 76.5 ms: 1.03x faster                                                 |
| chaos                      | 57.3 ms                                                      | 55.8 ms: 1.03x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 92.6 ms: 1.03x faster                                                 |
| generators                 | 28.8 ms                                                      | 28.1 ms: 1.02x faster                                                 |
| meteor_contest             | 102 ms                                                       | 99.1 ms: 1.02x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 133 ms: 1.02x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.56 sec: 1.02x faster                                                |
| pycparser                  | 1.12 sec                                                     | 1.09 sec: 1.02x faster                                                |
| python_startup_no_site     | 7.39 ms                                                      | 7.24 ms: 1.02x faster                                                 |
| sympy_str                  | 275 ms                                                       | 269 ms: 1.02x faster                                                  |
| coverage                   | 83.0 ms                                                      | 81.5 ms: 1.02x faster                                                 |
| genshi_xml                 | 48.8 ms                                                      | 47.9 ms: 1.02x faster                                                 |
| deltablue                  | 3.12 ms                                                      | 3.07 ms: 1.02x faster                                                 |
| raytrace                   | 253 ms                                                       | 249 ms: 1.02x faster                                                  |
| unpickle_pure_python       | 210 us                                                       | 207 us: 1.01x faster                                                  |
| sympy_sum                  | 156 ms                                                       | 154 ms: 1.01x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                  |
| pidigits                   | 217 ms                                                       | 217 ms: 1.00x slower                                                  |
| pathlib                    | 19.2 ms                                                      | 19.3 ms: 1.01x slower                                                 |
| sympy_expand               | 457 ms                                                       | 464 ms: 1.01x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 10.7 ms: 1.02x slower                                                 |
| mako                       | 11.3 ms                                                      | 11.6 ms: 1.02x slower                                                 |
| django_template            | 34.1 ms                                                      | 35.0 ms: 1.02x slower                                                 |
| fannkuch                   | 370 ms                                                       | 379 ms: 1.03x slower                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.27 us: 1.03x slower                                                 |
| json_loads                 | 27.0 us                                                      | 27.9 us: 1.03x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 306 us: 1.04x slower                                                  |
| json                       | 4.93 ms                                                      | 5.14 ms: 1.04x slower                                                 |
| nbody                      | 85.1 ms                                                      | 89.3 ms: 1.05x slower                                                 |
| python_startup             | 11.0 ms                                                      | 12.5 ms: 1.13x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.05 ms: 1.14x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.93 ms: 1.45x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.78 ms: 1.52x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 102 ms: 9.32x slower                                                  |
| telco                      | 7.82 ms                                                      | 157 ms: 20.10x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.01x faster                                                          |

Benchmark hidden because not significant (3): typing_runtime_protocols, coroutines, crypto_pyaes
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250722-3.15.0a0-bbe589f/bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.037x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.15x