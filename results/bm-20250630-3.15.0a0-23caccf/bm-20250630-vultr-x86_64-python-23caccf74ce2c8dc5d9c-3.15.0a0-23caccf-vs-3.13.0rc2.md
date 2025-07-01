# Results vs. 3.13.0rc2

- fork: python
- ref: 23caccf74ce2c8dc5d9c
- machine: linux-x86_64
- commit hash: 23caccf
- commit date: 2025-06-30
- overall geometric mean: 1.072x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 250 ms: 1.04x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.53 sec: 1.04x faster                                                |
| html5lib       | 67.0 ms                                                      | 61.5 ms: 1.09x faster                                                 |
| Geometric mean | (ref)                                                        | 1.05x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 461 ms                                                       | 307 ms: 1.50x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 627 ms: 1.46x faster                                                  |
| async_tree_io              | 876 ms                                                       | 609 ms: 1.44x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 497 ms: 1.34x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 310 ms: 1.34x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 254 ms: 1.33x faster                                                  |
| async_tree_none            | 354 ms                                                       | 268 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 498 ms: 1.28x faster                                                  |
| async_generators           | 377 ms                                                       | 340 ms: 1.11x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.2 ms: 1.01x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                  |
| Geometric mean             | (ref)                                                        | 1.27x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 203 ms: 1.07x faster                                                  |
| float          | 77.5 ms                                                      | 72.7 ms: 1.06x faster                                                 |
| nbody          | 85.1 ms                                                      | 88.3 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                        | 1.03x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.60 ms: 1.19x faster                                                 |
| regex_v8       | 22.7 ms                                                      | 21.1 ms: 1.07x faster                                                 |
| regex_compile  | 132 ms                                                       | 124 ms: 1.06x faster                                                  |
| regex_dna      | 180 ms                                                       | 173 ms: 1.04x faster                                                  |
| Geometric mean | (ref)                                                        | 1.09x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.92 sec: 1.04x faster                                                |
| xml_etree_generate   | 85.4 ms                                                      | 83.6 ms: 1.02x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 134 ms: 1.02x faster                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 93.3 ms: 1.02x faster                                                 |
| xml_etree_process    | 59.3 ms                                                      | 58.4 ms: 1.02x faster                                                 |
| unpickle_pure_python | 210 us                                                       | 207 us: 1.01x faster                                                  |
| json_dumps           | 10.5 ms                                                      | 10.7 ms: 1.02x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 306 us: 1.04x slower                                                  |
| json_loads           | 27.0 us                                                      | 28.9 us: 1.07x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.00x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.32 ms: 1.01x faster                                                 |
| python_startup         | 11.0 ms                                                      | 12.6 ms: 1.14x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.06x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 20.8 ms: 1.04x faster                                                 |
| genshi_xml      | 48.8 ms                                                      | 48.2 ms: 1.01x faster                                                 |
| django_template | 34.1 ms                                                      | 34.5 ms: 1.01x slower                                                 |
| mako            | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.00x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.14 sec: 2.06x faster                                                |
| async_tree_memoization     | 461 ms                                                       | 307 ms: 1.50x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 627 ms: 1.46x faster                                                  |
| async_tree_io              | 876 ms                                                       | 609 ms: 1.44x faster                                                  |
| deepcopy                   | 355 us                                                       | 253 us: 1.41x faster                                                  |
| go                         | 141 ms                                                       | 104 ms: 1.36x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 29.1 us: 1.34x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 497 ms: 1.34x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 310 ms: 1.34x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 254 ms: 1.33x faster                                                  |
| async_tree_none            | 354 ms                                                       | 268 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 498 ms: 1.28x faster                                                  |
| scimark_sor                | 134 ms                                                       | 110 ms: 1.22x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.60 ms: 1.19x faster                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 2.65 us: 1.17x faster                                                 |
| spectral_norm              | 111 ms                                                       | 97.1 ms: 1.14x faster                                                 |
| pylint                     | 317 ms                                                       | 279 ms: 1.13x faster                                                  |
| pyflate                    | 449 ms                                                       | 399 ms: 1.12x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 67.0 ms: 1.12x faster                                                 |
| async_generators           | 377 ms                                                       | 340 ms: 1.11x faster                                                  |
| richards_super             | 51.6 ms                                                      | 46.7 ms: 1.11x faster                                                 |
| richards                   | 45.2 ms                                                      | 41.2 ms: 1.10x faster                                                 |
| html5lib                   | 67.0 ms                                                      | 61.5 ms: 1.09x faster                                                 |
| regex_v8                   | 22.7 ms                                                      | 21.1 ms: 1.07x faster                                                 |
| pidigits                   | 217 ms                                                       | 203 ms: 1.07x faster                                                  |
| pprint_safe_repr           | 738 ms                                                       | 691 ms: 1.07x faster                                                  |
| float                      | 77.5 ms                                                      | 72.7 ms: 1.06x faster                                                 |
| regex_compile              | 132 ms                                                       | 124 ms: 1.06x faster                                                  |
| hexiom                     | 5.99 ms                                                      | 5.64 ms: 1.06x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.19 sec: 1.06x faster                                                |
| pprint_pformat             | 1.50 sec                                                     | 1.41 sec: 1.06x faster                                                |
| scimark_monte_carlo        | 65.4 ms                                                      | 61.6 ms: 1.06x faster                                                 |
| sympy_integrate            | 19.8 ms                                                      | 18.7 ms: 1.06x faster                                                 |
| telco                      | 7.82 ms                                                      | 7.39 ms: 1.06x faster                                                 |
| comprehensions             | 16.5 us                                                      | 15.6 us: 1.06x faster                                                 |
| thrift                     | 778 us                                                       | 740 us: 1.05x faster                                                  |
| logging_silent             | 103 ns                                                       | 97.7 ns: 1.05x faster                                                 |
| tomli_loads                | 2.01 sec                                                     | 1.92 sec: 1.04x faster                                                |
| regex_dna                  | 180 ms                                                       | 173 ms: 1.04x faster                                                  |
| 2to3                       | 260 ms                                                       | 250 ms: 1.04x faster                                                  |
| genshi_text                | 21.5 ms                                                      | 20.8 ms: 1.04x faster                                                 |
| scimark_fft                | 349 ms                                                       | 337 ms: 1.04x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.53 sec: 1.04x faster                                                |
| generators                 | 28.8 ms                                                      | 27.8 ms: 1.03x faster                                                 |
| logging_simple             | 6.16 us                                                      | 5.97 us: 1.03x faster                                                 |
| chaos                      | 57.3 ms                                                      | 56.0 ms: 1.02x faster                                                 |
| logging_format             | 6.84 us                                                      | 6.69 us: 1.02x faster                                                 |
| meteor_contest             | 102 ms                                                       | 99.5 ms: 1.02x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 83.6 ms: 1.02x faster                                                 |
| sympy_str                  | 275 ms                                                       | 269 ms: 1.02x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 134 ms: 1.02x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 93.3 ms: 1.02x faster                                                 |
| coverage                   | 83.0 ms                                                      | 81.6 ms: 1.02x faster                                                 |
| xml_etree_process          | 59.3 ms                                                      | 58.4 ms: 1.02x faster                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 66.8 ms: 1.02x faster                                                 |
| pycparser                  | 1.12 sec                                                     | 1.10 sec: 1.02x faster                                                |
| coroutines                 | 23.6 ms                                                      | 23.2 ms: 1.01x faster                                                 |
| unpickle_pure_python       | 210 us                                                       | 207 us: 1.01x faster                                                  |
| nqueens                    | 78.6 ms                                                      | 77.6 ms: 1.01x faster                                                 |
| genshi_xml                 | 48.8 ms                                                      | 48.2 ms: 1.01x faster                                                 |
| sympy_sum                  | 156 ms                                                       | 154 ms: 1.01x faster                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.32 ms: 1.01x faster                                                 |
| scimark_lu                 | 113 ms                                                       | 112 ms: 1.01x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                  |
| raytrace                   | 253 ms                                                       | 252 ms: 1.00x faster                                                  |
| sympy_expand               | 457 ms                                                       | 460 ms: 1.01x slower                                                  |
| django_template            | 34.1 ms                                                      | 34.5 ms: 1.01x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 10.7 ms: 1.02x slower                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.25 us: 1.02x slower                                                 |
| pathlib                    | 19.2 ms                                                      | 19.8 ms: 1.03x slower                                                 |
| mako                       | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                 |
| nbody                      | 85.1 ms                                                      | 88.3 ms: 1.04x slower                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.89 ms: 1.04x slower                                                 |
| json                       | 4.93 ms                                                      | 5.12 ms: 1.04x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 306 us: 1.04x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.26 ms: 1.04x slower                                                 |
| fannkuch                   | 370 ms                                                       | 389 ms: 1.05x slower                                                  |
| json_loads                 | 27.0 us                                                      | 28.9 us: 1.07x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.05 ms: 1.14x slower                                                 |
| python_startup             | 11.0 ms                                                      | 12.6 ms: 1.14x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.33 ms: 1.38x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.89 ms: 1.42x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 99.0 ms: 9.01x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                          |

Benchmark hidden because not significant (1): typing_runtime_protocols
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250630-3.15.0a0-23caccf/bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.072x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.14x