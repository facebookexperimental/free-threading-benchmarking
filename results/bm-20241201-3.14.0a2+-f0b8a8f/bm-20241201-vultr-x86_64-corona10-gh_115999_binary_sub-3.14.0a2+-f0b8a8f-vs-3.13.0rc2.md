# Results vs. 3.13.0rc2

- fork: corona10
- ref: gh_115999_binary_sub
- machine: linux-x86_64
- commit hash: f0b8a8f
- commit date: 2024-12-01
- overall geometric mean: 1.002x slower
- HPT reliability: 82.98%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241201-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-f0b8a8f |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 258 ms: 1.01x faster                                                     |
| docutils       | 2.62 sec                                                     | 2.63 sec: 1.00x slower                                                   |
| Geometric mean | (ref)                                                        | 1.00x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241201-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-f0b8a8f |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 666 ms                                                       | 569 ms: 1.17x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 406 ms: 1.14x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 567 ms: 1.12x faster                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 387 ms: 1.07x faster                                                     |
| async_tree_none            | 354 ms                                                       | 331 ms: 1.07x faster                                                     |
| async_tree_io              | 876 ms                                                       | 839 ms: 1.04x faster                                                     |
| async_tree_io_tg           | 913 ms                                                       | 877 ms: 1.04x faster                                                     |
| coroutines                 | 23.6 ms                                                      | 23.2 ms: 1.01x faster                                                    |
| async_generators           | 377 ms                                                       | 373 ms: 1.01x faster                                                     |
| asyncio_websockets         | 520 ms                                                       | 522 ms: 1.00x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.06x faster                                                             |

Benchmark hidden because not significant (1): async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241201-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-f0b8a8f |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 187 ms: 1.16x faster                                                     |
| float          | 77.5 ms                                                      | 80.9 ms: 1.04x slower                                                    |
| nbody          | 85.1 ms                                                      | 96.1 ms: 1.13x slower                                                    |
| Geometric mean | (ref)                                                        | 1.01x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241201-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-f0b8a8f |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.69 ms: 1.15x faster                                                    |
| regex_dna      | 180 ms                                                       | 174 ms: 1.04x faster                                                     |
| regex_v8       | 22.7 ms                                                      | 23.0 ms: 1.01x slower                                                    |
| regex_compile  | 132 ms                                                       | 137 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                        | 1.03x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241201-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-f0b8a8f |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_loads           | 27.0 us                                                      | 25.3 us: 1.07x faster                                                    |
| xml_etree_parse      | 136 ms                                                       | 138 ms: 1.01x slower                                                     |
| xml_etree_generate   | 85.4 ms                                                      | 86.9 ms: 1.02x slower                                                    |
| xml_etree_process    | 59.3 ms                                                      | 61.0 ms: 1.03x slower                                                    |
| xml_etree_iterparse  | 94.9 ms                                                      | 98.6 ms: 1.04x slower                                                    |
| unpickle_pure_python | 210 us                                                       | 221 us: 1.05x slower                                                     |
| tomli_loads          | 2.01 sec                                                     | 2.12 sec: 1.06x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 320 us: 1.09x slower                                                     |
| json_dumps           | 10.5 ms                                                      | 11.5 ms: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                        | 1.03x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241201-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-f0b8a8f |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.40 ms: 1.00x slower                                                    |
| python_startup         | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                    |
| Geometric mean         | (ref)                                                        | 1.15x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241201-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-f0b8a8f |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 50.1 ms: 1.03x slower                                                    |
| genshi_text     | 21.5 ms                                                      | 22.3 ms: 1.04x slower                                                    |
| django_template | 34.1 ms                                                      | 35.6 ms: 1.04x slower                                                    |
| mako            | 11.3 ms                                                      | 12.0 ms: 1.06x slower                                                    |
| Geometric mean  | (ref)                                                        | 1.04x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241201-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-f0b8a8f |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| deepcopy                   | 355 us                                                       | 260 us: 1.37x faster                                                     |
| deepcopy_memo              | 39.1 us                                                      | 30.6 us: 1.28x faster                                                    |
| deepcopy_reduce            | 3.11 us                                                      | 2.61 us: 1.19x faster                                                    |
| pylint                     | 317 ms                                                       | 270 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 569 ms: 1.17x faster                                                     |
| pidigits                   | 217 ms                                                       | 187 ms: 1.16x faster                                                     |
| regex_effbot               | 3.08 ms                                                      | 2.69 ms: 1.15x faster                                                    |
| async_tree_memoization     | 461 ms                                                       | 406 ms: 1.14x faster                                                     |
| go                         | 141 ms                                                       | 124 ms: 1.13x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 567 ms: 1.12x faster                                                     |
| json                       | 4.93 ms                                                      | 4.56 ms: 1.08x faster                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 387 ms: 1.07x faster                                                     |
| async_tree_none            | 354 ms                                                       | 331 ms: 1.07x faster                                                     |
| json_loads                 | 27.0 us                                                      | 25.3 us: 1.07x faster                                                    |
| telco                      | 7.82 ms                                                      | 7.33 ms: 1.07x faster                                                    |
| thrift                     | 778 us                                                       | 743 us: 1.05x faster                                                     |
| async_tree_io              | 876 ms                                                       | 839 ms: 1.04x faster                                                     |
| async_tree_io_tg           | 913 ms                                                       | 877 ms: 1.04x faster                                                     |
| regex_dna                  | 180 ms                                                       | 174 ms: 1.04x faster                                                     |
| pathlib                    | 19.2 ms                                                      | 18.6 ms: 1.03x faster                                                    |
| scimark_fft                | 349 ms                                                       | 338 ms: 1.03x faster                                                     |
| coverage                   | 83.0 ms                                                      | 80.5 ms: 1.03x faster                                                    |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.61 ms: 1.02x faster                                                    |
| pprint_safe_repr           | 738 ms                                                       | 724 ms: 1.02x faster                                                     |
| sympy_sum                  | 156 ms                                                       | 153 ms: 1.02x faster                                                     |
| coroutines                 | 23.6 ms                                                      | 23.2 ms: 1.01x faster                                                    |
| async_generators           | 377 ms                                                       | 373 ms: 1.01x faster                                                     |
| pprint_pformat             | 1.50 sec                                                     | 1.48 sec: 1.01x faster                                                   |
| meteor_contest             | 102 ms                                                       | 101 ms: 1.01x faster                                                     |
| 2to3                       | 260 ms                                                       | 258 ms: 1.01x faster                                                     |
| sympy_str                  | 275 ms                                                       | 273 ms: 1.01x faster                                                     |
| bpe_tokeniser              | 4.45 sec                                                     | 4.43 sec: 1.00x faster                                                   |
| python_startup_no_site     | 7.39 ms                                                      | 7.40 ms: 1.00x slower                                                    |
| crypto_pyaes               | 67.9 ms                                                      | 68.2 ms: 1.00x slower                                                    |
| asyncio_websockets         | 520 ms                                                       | 522 ms: 1.00x slower                                                     |
| docutils                   | 2.62 sec                                                     | 2.63 sec: 1.00x slower                                                   |
| scimark_sor                | 134 ms                                                       | 135 ms: 1.01x slower                                                     |
| sympy_integrate            | 19.8 ms                                                      | 20.0 ms: 1.01x slower                                                    |
| pycparser                  | 1.12 sec                                                     | 1.13 sec: 1.01x slower                                                   |
| fannkuch                   | 370 ms                                                       | 373 ms: 1.01x slower                                                     |
| xml_etree_parse            | 136 ms                                                       | 138 ms: 1.01x slower                                                     |
| sympy_expand               | 457 ms                                                       | 462 ms: 1.01x slower                                                     |
| regex_v8                   | 22.7 ms                                                      | 23.0 ms: 1.01x slower                                                    |
| nqueens                    | 78.6 ms                                                      | 79.6 ms: 1.01x slower                                                    |
| sqlglot_normalize          | 106 ms                                                       | 108 ms: 1.02x slower                                                     |
| xml_etree_generate         | 85.4 ms                                                      | 86.9 ms: 1.02x slower                                                    |
| sqlite_synth               | 2.21 us                                                      | 2.25 us: 1.02x slower                                                    |
| dulwich_log                | 74.8 ms                                                      | 76.2 ms: 1.02x slower                                                    |
| scimark_monte_carlo        | 65.4 ms                                                      | 66.6 ms: 1.02x slower                                                    |
| logging_simple             | 6.16 us                                                      | 6.29 us: 1.02x slower                                                    |
| spectral_norm              | 111 ms                                                       | 113 ms: 1.02x slower                                                     |
| hexiom                     | 5.99 ms                                                      | 6.14 ms: 1.02x slower                                                    |
| sqlglot_optimize           | 52.7 ms                                                      | 54.0 ms: 1.02x slower                                                    |
| genshi_xml                 | 48.8 ms                                                      | 50.1 ms: 1.03x slower                                                    |
| scimark_lu                 | 113 ms                                                       | 116 ms: 1.03x slower                                                     |
| xml_etree_process          | 59.3 ms                                                      | 61.0 ms: 1.03x slower                                                    |
| typing_runtime_protocols   | 155 us                                                       | 159 us: 1.03x slower                                                     |
| logging_format             | 6.84 us                                                      | 7.07 us: 1.03x slower                                                    |
| regex_compile              | 132 ms                                                       | 137 ms: 1.03x slower                                                     |
| sqlglot_transpile          | 1.56 ms                                                      | 1.61 ms: 1.03x slower                                                    |
| genshi_text                | 21.5 ms                                                      | 22.3 ms: 1.04x slower                                                    |
| xml_etree_iterparse        | 94.9 ms                                                      | 98.6 ms: 1.04x slower                                                    |
| chaos                      | 57.3 ms                                                      | 59.8 ms: 1.04x slower                                                    |
| django_template            | 34.1 ms                                                      | 35.6 ms: 1.04x slower                                                    |
| float                      | 77.5 ms                                                      | 80.9 ms: 1.04x slower                                                    |
| unpickle_pure_python       | 210 us                                                       | 221 us: 1.05x slower                                                     |
| sqlglot_parse              | 1.25 ms                                                      | 1.32 ms: 1.05x slower                                                    |
| richards_super             | 51.6 ms                                                      | 54.5 ms: 1.05x slower                                                    |
| tomli_loads                | 2.01 sec                                                     | 2.12 sec: 1.06x slower                                                   |
| richards                   | 45.2 ms                                                      | 47.8 ms: 1.06x slower                                                    |
| mako                       | 11.3 ms                                                      | 12.0 ms: 1.06x slower                                                    |
| comprehensions             | 16.5 us                                                      | 17.5 us: 1.06x slower                                                    |
| raytrace                   | 253 ms                                                       | 271 ms: 1.07x slower                                                     |
| generators                 | 28.8 ms                                                      | 31.0 ms: 1.07x slower                                                    |
| logging_silent             | 103 ns                                                       | 111 ns: 1.08x slower                                                     |
| pickle_pure_python         | 294 us                                                       | 320 us: 1.09x slower                                                     |
| deltablue                  | 3.12 ms                                                      | 3.42 ms: 1.09x slower                                                    |
| json_dumps                 | 10.5 ms                                                      | 11.5 ms: 1.10x slower                                                    |
| bench_thread_pool          | 919 us                                                       | 1.02 ms: 1.11x slower                                                    |
| nbody                      | 85.1 ms                                                      | 96.1 ms: 1.13x slower                                                    |
| gc_traversal               | 3.14 ms                                                      | 4.01 ms: 1.28x slower                                                    |
| python_startup             | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                    |
| create_gc_cycles           | 1.34 ms                                                      | 1.94 ms: 1.45x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                      | 86.3 ms: 7.85x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.03x slower                                                             |

Benchmark hidden because not significant (3): pyflate, mdp, async_tree_none_tg
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241201-3.14.0a2+-f0b8a8f/bm-20241201-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-f0b8a8f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.002x slower

# HPT report

- Reliability score: 82.98% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.09x