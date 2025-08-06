# Results vs. 3.13.0rc2

- fork: python
- ref: c2428ca9ea0c4eac9c7f
- machine: linux-x86_64
- commit hash: c2428ca
- commit date: 2025-08-05
- overall geometric mean: 1.029x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 250 ms: 1.04x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.56 sec: 1.02x faster                                                |
| html5lib       | 67.0 ms                                                      | 61.1 ms: 1.10x faster                                                 |
| Geometric mean | (ref)                                                        | 1.05x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 461 ms                                                       | 307 ms: 1.50x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 610 ms: 1.50x faster                                                  |
| async_tree_io              | 876 ms                                                       | 601 ms: 1.46x faster                                                  |
| async_tree_none            | 354 ms                                                       | 266 ms: 1.33x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 313 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 508 ms: 1.31x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 257 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 505 ms: 1.26x faster                                                  |
| async_generators           | 377 ms                                                       | 335 ms: 1.13x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.0 ms: 1.02x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                  |
| Geometric mean             | (ref)                                                        | 1.28x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 71.1 ms: 1.09x faster                                                 |
| pidigits       | 217 ms                                                       | 202 ms: 1.07x faster                                                  |
| nbody          | 85.1 ms                                                      | 88.8 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                        | 1.04x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.70 ms: 1.14x faster                                                 |
| regex_compile  | 132 ms                                                       | 124 ms: 1.06x faster                                                  |
| regex_dna      | 180 ms                                                       | 174 ms: 1.03x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 22.0 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                        | 1.07x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.92 sec: 1.05x faster                                                |
| xml_etree_iterparse  | 94.9 ms                                                      | 93.0 ms: 1.02x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 83.7 ms: 1.02x faster                                                 |
| xml_etree_process    | 59.3 ms                                                      | 58.3 ms: 1.02x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 134 ms: 1.02x faster                                                  |
| unpickle_pure_python | 210 us                                                       | 209 us: 1.01x faster                                                  |
| json_dumps           | 10.5 ms                                                      | 10.8 ms: 1.02x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 313 us: 1.06x slower                                                  |
| json_loads           | 27.0 us                                                      | 28.8 us: 1.06x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.00x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.25 ms: 1.02x faster                                                 |
| python_startup         | 11.0 ms                                                      | 12.6 ms: 1.14x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.06x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 20.4 ms: 1.06x faster                                                 |
| django_template | 34.1 ms                                                      | 34.7 ms: 1.02x slower                                                 |
| mako            | 11.3 ms                                                      | 11.6 ms: 1.02x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.01x faster                                                          |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.16 sec: 2.04x faster                                                |
| async_tree_memoization     | 461 ms                                                       | 307 ms: 1.50x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 610 ms: 1.50x faster                                                  |
| async_tree_io              | 876 ms                                                       | 601 ms: 1.46x faster                                                  |
| deepcopy                   | 355 us                                                       | 257 us: 1.38x faster                                                  |
| go                         | 141 ms                                                       | 105 ms: 1.34x faster                                                  |
| async_tree_none            | 354 ms                                                       | 266 ms: 1.33x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 313 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 508 ms: 1.31x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 257 ms: 1.31x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 30.8 us: 1.27x faster                                                 |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 505 ms: 1.26x faster                                                  |
| scimark_sor                | 134 ms                                                       | 108 ms: 1.24x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.68 us: 1.16x faster                                                 |
| spectral_norm              | 111 ms                                                       | 97.2 ms: 1.14x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.70 ms: 1.14x faster                                                 |
| dulwich_log                | 74.8 ms                                                      | 66.4 ms: 1.13x faster                                                 |
| pylint                     | 317 ms                                                       | 282 ms: 1.13x faster                                                  |
| async_generators           | 377 ms                                                       | 335 ms: 1.13x faster                                                  |
| pyflate                    | 449 ms                                                       | 402 ms: 1.12x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 61.1 ms: 1.10x faster                                                 |
| richards_super             | 51.6 ms                                                      | 47.2 ms: 1.09x faster                                                 |
| richards                   | 45.2 ms                                                      | 41.4 ms: 1.09x faster                                                 |
| float                      | 77.5 ms                                                      | 71.1 ms: 1.09x faster                                                 |
| pidigits                   | 217 ms                                                       | 202 ms: 1.07x faster                                                  |
| logging_silent             | 103 ns                                                       | 95.9 ns: 1.07x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.18 sec: 1.06x faster                                                |
| regex_compile              | 132 ms                                                       | 124 ms: 1.06x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.46 us: 1.06x faster                                                 |
| logging_simple             | 6.16 us                                                      | 5.83 us: 1.06x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.67 ms: 1.06x faster                                                 |
| genshi_text                | 21.5 ms                                                      | 20.4 ms: 1.06x faster                                                 |
| comprehensions             | 16.5 us                                                      | 15.7 us: 1.05x faster                                                 |
| scimark_fft                | 349 ms                                                       | 333 ms: 1.05x faster                                                  |
| pprint_safe_repr           | 738 ms                                                       | 704 ms: 1.05x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.92 sec: 1.05x faster                                                |
| sympy_integrate            | 19.8 ms                                                      | 19.0 ms: 1.04x faster                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.43 sec: 1.04x faster                                                |
| 2to3                       | 260 ms                                                       | 250 ms: 1.04x faster                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 62.9 ms: 1.04x faster                                                 |
| regex_dna                  | 180 ms                                                       | 174 ms: 1.03x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 22.0 ms: 1.03x faster                                                 |
| chaos                      | 57.3 ms                                                      | 55.7 ms: 1.03x faster                                                 |
| thrift                     | 778 us                                                       | 759 us: 1.03x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.56 sec: 1.02x faster                                                |
| coroutines                 | 23.6 ms                                                      | 23.0 ms: 1.02x faster                                                 |
| pycparser                  | 1.12 sec                                                     | 1.09 sec: 1.02x faster                                                |
| xml_etree_iterparse        | 94.9 ms                                                      | 93.0 ms: 1.02x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 83.7 ms: 1.02x faster                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 7.25 ms: 1.02x faster                                                 |
| generators                 | 28.8 ms                                                      | 28.3 ms: 1.02x faster                                                 |
| xml_etree_process          | 59.3 ms                                                      | 58.3 ms: 1.02x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 134 ms: 1.02x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 18.9 ms: 1.02x faster                                                 |
| meteor_contest             | 102 ms                                                       | 99.9 ms: 1.02x faster                                                 |
| raytrace                   | 253 ms                                                       | 249 ms: 1.01x faster                                                  |
| sympy_str                  | 275 ms                                                       | 271 ms: 1.01x faster                                                  |
| coverage                   | 83.0 ms                                                      | 82.0 ms: 1.01x faster                                                 |
| typing_runtime_protocols   | 155 us                                                       | 153 us: 1.01x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 111 ms: 1.01x faster                                                  |
| unpickle_pure_python       | 210 us                                                       | 209 us: 1.01x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                  |
| nqueens                    | 78.6 ms                                                      | 78.2 ms: 1.00x faster                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 68.7 ms: 1.01x slower                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.79 ms: 1.02x slower                                                 |
| django_template            | 34.1 ms                                                      | 34.7 ms: 1.02x slower                                                 |
| mako                       | 11.3 ms                                                      | 11.6 ms: 1.02x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 10.8 ms: 1.02x slower                                                 |
| fannkuch                   | 370 ms                                                       | 380 ms: 1.03x slower                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.27 us: 1.03x slower                                                 |
| nbody                      | 85.1 ms                                                      | 88.8 ms: 1.04x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.30 ms: 1.06x slower                                                 |
| json                       | 4.93 ms                                                      | 5.24 ms: 1.06x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 313 us: 1.06x slower                                                  |
| json_loads                 | 27.0 us                                                      | 28.8 us: 1.06x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.05 ms: 1.14x slower                                                 |
| python_startup             | 11.0 ms                                                      | 12.6 ms: 1.14x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.35 ms: 1.38x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.94 ms: 1.45x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 103 ms: 9.37x slower                                                  |
| telco                      | 7.82 ms                                                      | 160 ms: 20.40x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.00x faster                                                          |

Benchmark hidden because not significant (3): genshi_xml, sympy_sum, sympy_expand
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250805-3.15.0a0-c2428ca/bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.029x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.15x