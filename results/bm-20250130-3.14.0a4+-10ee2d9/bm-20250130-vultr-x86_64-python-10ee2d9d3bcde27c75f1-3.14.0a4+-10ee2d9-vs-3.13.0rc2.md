# Results vs. 3.13.0rc2

- fork: python
- ref: 10ee2d9d3bcde27c75f1
- machine: linux-x86_64
- commit hash: 10ee2d9
- commit date: 2025-01-30
- overall geometric mean: 1.058x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 253 ms: 1.03x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.54 sec: 1.03x faster                                                 |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 623 ms: 1.47x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 323 ms: 1.43x faster                                                   |
| async_tree_io              | 876 ms                                                       | 622 ms: 1.41x faster                                                   |
| async_tree_none            | 354 ms                                                       | 268 ms: 1.32x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 318 ms: 1.30x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 264 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 552 ms: 1.21x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 538 ms: 1.18x faster                                                   |
| async_generators           | 377 ms                                                       | 321 ms: 1.17x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 21.9 ms: 1.08x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.25x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 70.8 ms: 1.09x faster                                                  |
| pidigits       | 217 ms                                                       | 210 ms: 1.03x faster                                                   |
| nbody          | 85.1 ms                                                      | 88.7 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.84 ms: 1.09x faster                                                  |
| regex_compile  | 132 ms                                                       | 125 ms: 1.06x faster                                                   |
| regex_dna      | 180 ms                                                       | 171 ms: 1.05x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 22.8 ms: 1.00x slower                                                  |
| Geometric mean | (ref)                                                        | 1.05x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.85 sec: 1.08x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.06x faster                                                   |
| xml_etree_iterparse  | 94.9 ms                                                      | 91.4 ms: 1.04x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 58.0 ms: 1.02x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 83.5 ms: 1.02x faster                                                  |
| unpickle_pure_python | 210 us                                                       | 209 us: 1.01x faster                                                   |
| pickle_pure_python   | 294 us                                                       | 309 us: 1.05x slower                                                   |
| json_loads           | 27.0 us                                                      | 28.5 us: 1.05x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 11.2 ms: 1.06x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.47 ms: 1.01x slower                                                  |
| python_startup         | 11.0 ms                                                      | 14.7 ms: 1.34x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.16x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text    | 21.5 ms                                                      | 20.7 ms: 1.04x faster                                                  |
| genshi_xml     | 48.8 ms                                                      | 48.1 ms: 1.01x faster                                                  |
| mako           | 11.3 ms                                                      | 11.6 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                        | 1.01x faster                                                           |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 623 ms: 1.47x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 323 ms: 1.43x faster                                                   |
| async_tree_io              | 876 ms                                                       | 622 ms: 1.41x faster                                                   |
| deepcopy                   | 355 us                                                       | 252 us: 1.41x faster                                                   |
| async_tree_none            | 354 ms                                                       | 268 ms: 1.32x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 29.6 us: 1.32x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 318 ms: 1.30x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 264 ms: 1.28x faster                                                   |
| go                         | 141 ms                                                       | 112 ms: 1.26x faster                                                   |
| spectral_norm              | 111 ms                                                       | 89.3 ms: 1.24x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 552 ms: 1.21x faster                                                   |
| scimark_sor                | 134 ms                                                       | 112 ms: 1.20x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.61 us: 1.19x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 538 ms: 1.18x faster                                                   |
| async_generators           | 377 ms                                                       | 321 ms: 1.17x faster                                                   |
| pylint                     | 317 ms                                                       | 277 ms: 1.14x faster                                                   |
| scimark_fft                | 349 ms                                                       | 311 ms: 1.12x faster                                                   |
| pyflate                    | 449 ms                                                       | 407 ms: 1.10x faster                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.29 ms: 1.10x faster                                                  |
| float                      | 77.5 ms                                                      | 70.8 ms: 1.09x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.84 ms: 1.09x faster                                                  |
| richards                   | 45.2 ms                                                      | 41.7 ms: 1.08x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.85 sec: 1.08x faster                                                 |
| coroutines                 | 23.6 ms                                                      | 21.9 ms: 1.08x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.14 sec: 1.07x faster                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 60.9 ms: 1.07x faster                                                  |
| richards_super             | 51.6 ms                                                      | 48.2 ms: 1.07x faster                                                  |
| telco                      | 7.82 ms                                                      | 7.31 ms: 1.07x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 18.0 ms: 1.07x faster                                                  |
| thrift                     | 778 us                                                       | 731 us: 1.06x faster                                                   |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.06x faster                                                   |
| regex_compile              | 132 ms                                                       | 125 ms: 1.06x faster                                                   |
| pprint_safe_repr           | 738 ms                                                       | 698 ms: 1.06x faster                                                   |
| regex_dna                  | 180 ms                                                       | 171 ms: 1.05x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.43 sec: 1.05x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.73 ms: 1.05x faster                                                  |
| logging_simple             | 6.16 us                                                      | 5.89 us: 1.05x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.55 us: 1.04x faster                                                  |
| genshi_text                | 21.5 ms                                                      | 20.7 ms: 1.04x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 91.4 ms: 1.04x faster                                                  |
| coverage                   | 83.0 ms                                                      | 80.0 ms: 1.04x faster                                                  |
| chaos                      | 57.3 ms                                                      | 55.4 ms: 1.03x faster                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 65.7 ms: 1.03x faster                                                  |
| pidigits                   | 217 ms                                                       | 210 ms: 1.03x faster                                                   |
| meteor_contest             | 102 ms                                                       | 98.6 ms: 1.03x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.54 sec: 1.03x faster                                                 |
| sympy_sum                  | 156 ms                                                       | 151 ms: 1.03x faster                                                   |
| 2to3                       | 260 ms                                                       | 253 ms: 1.03x faster                                                   |
| sqlglot_optimize           | 52.7 ms                                                      | 51.4 ms: 1.03x faster                                                  |
| sqlglot_normalize          | 106 ms                                                       | 103 ms: 1.03x faster                                                   |
| xml_etree_process          | 59.3 ms                                                      | 58.0 ms: 1.02x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 83.5 ms: 1.02x faster                                                  |
| sympy_str                  | 275 ms                                                       | 269 ms: 1.02x faster                                                   |
| nqueens                    | 78.6 ms                                                      | 76.9 ms: 1.02x faster                                                  |
| deltablue                  | 3.12 ms                                                      | 3.06 ms: 1.02x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.17 us: 1.02x faster                                                  |
| sympy_expand               | 457 ms                                                       | 450 ms: 1.02x faster                                                   |
| fannkuch                   | 370 ms                                                       | 364 ms: 1.01x faster                                                   |
| genshi_xml                 | 48.8 ms                                                      | 48.1 ms: 1.01x faster                                                  |
| sympy_integrate            | 19.8 ms                                                      | 19.6 ms: 1.01x faster                                                  |
| sqlglot_transpile          | 1.56 ms                                                      | 1.54 ms: 1.01x faster                                                  |
| typing_runtime_protocols   | 155 us                                                       | 153 us: 1.01x faster                                                   |
| pycparser                  | 1.12 sec                                                     | 1.11 sec: 1.01x faster                                                 |
| sqlglot_parse              | 1.25 ms                                                      | 1.24 ms: 1.01x faster                                                  |
| comprehensions             | 16.5 us                                                      | 16.4 us: 1.01x faster                                                  |
| unpickle_pure_python       | 210 us                                                       | 209 us: 1.01x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                   |
| regex_v8                   | 22.7 ms                                                      | 22.8 ms: 1.00x slower                                                  |
| generators                 | 28.8 ms                                                      | 29.0 ms: 1.01x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.47 ms: 1.01x slower                                                  |
| logging_silent             | 103 ns                                                       | 105 ns: 1.02x slower                                                   |
| json                       | 4.93 ms                                                      | 5.03 ms: 1.02x slower                                                  |
| mako                       | 11.3 ms                                                      | 11.6 ms: 1.02x slower                                                  |
| raytrace                   | 253 ms                                                       | 261 ms: 1.03x slower                                                   |
| mdp                        | 2.36 sec                                                     | 2.45 sec: 1.04x slower                                                 |
| nbody                      | 85.1 ms                                                      | 88.7 ms: 1.04x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 309 us: 1.05x slower                                                   |
| json_loads                 | 27.0 us                                                      | 28.5 us: 1.05x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 11.2 ms: 1.06x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.03 ms: 1.12x slower                                                  |
| python_startup             | 11.0 ms                                                      | 14.7 ms: 1.34x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.27 ms: 1.36x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.84 ms: 1.37x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 88.0 ms: 8.01x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.03x faster                                                           |

Benchmark hidden because not significant (3): dulwich_log, django_template, scimark_lu
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250130-3.14.0a4+-10ee2d9/bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.058x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.10x