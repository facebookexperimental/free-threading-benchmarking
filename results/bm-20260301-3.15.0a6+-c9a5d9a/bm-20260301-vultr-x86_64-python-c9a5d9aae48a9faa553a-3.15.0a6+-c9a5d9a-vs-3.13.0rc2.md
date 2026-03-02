# Results vs. 3.13.0rc2

- fork: python
- ref: c9a5d9aae48a9faa553a
- machine: linux-x86_64
- commit hash: c9a5d9a
- commit date: 2026-03-01
- overall geometric mean: 1.036x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 251 ms: 1.03x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.59 sec: 1.01x faster                                                 |
| html5lib       | 67.0 ms                                                      | 59.5 ms: 1.13x faster                                                  |
| Geometric mean | (ref)                                                        | 1.06x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 570 ms: 1.60x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 307 ms: 1.50x faster                                                   |
| async_tree_io              | 876 ms                                                       | 583 ms: 1.50x faster                                                   |
| async_tree_none            | 354 ms                                                       | 245 ms: 1.44x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 241 ms: 1.39x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 308 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 499 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 505 ms: 1.26x faster                                                   |
| async_generators           | 377 ms                                                       | 337 ms: 1.12x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                   |
| coroutines                 | 23.6 ms                                                      | 24.7 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.29x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 70.8 ms: 1.09x faster                                                  |
| pidigits       | 217 ms                                                       | 201 ms: 1.08x faster                                                   |
| nbody          | 85.1 ms                                                      | 90.6 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.77 ms: 1.11x faster                                                  |
| regex_compile  | 132 ms                                                       | 124 ms: 1.07x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 21.7 ms: 1.05x faster                                                  |
| regex_dna      | 180 ms                                                       | 174 ms: 1.04x faster                                                   |
| Geometric mean | (ref)                                                        | 1.07x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 85.0 ms: 1.12x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 1.84 sec: 1.09x faster                                                 |
| json_dumps           | 10.5 ms                                                      | 9.87 ms: 1.07x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 132 ms: 1.03x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 83.8 ms: 1.02x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 58.8 ms: 1.01x faster                                                  |
| unpickle_pure_python | 210 us                                                       | 208 us: 1.01x faster                                                   |
| json_loads           | 27.0 us                                                      | 28.0 us: 1.04x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 308 us: 1.04x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.41 ms: 1.00x slower                                                  |
| python_startup         | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.07x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.1 ms: 1.02x faster                                                  |
| genshi_xml      | 48.8 ms                                                      | 49.1 ms: 1.01x slower                                                  |
| mako            | 11.3 ms                                                      | 11.9 ms: 1.05x slower                                                  |
| django_template | 34.1 ms                                                      | 35.8 ms: 1.05x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.15 sec: 2.05x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 570 ms: 1.60x faster                                                   |
| deepcopy                   | 355 us                                                       | 233 us: 1.52x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 307 ms: 1.50x faster                                                   |
| async_tree_io              | 876 ms                                                       | 583 ms: 1.50x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 26.5 us: 1.48x faster                                                  |
| async_tree_none            | 354 ms                                                       | 245 ms: 1.44x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 241 ms: 1.39x faster                                                   |
| go                         | 141 ms                                                       | 104 ms: 1.35x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 308 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 499 ms: 1.33x faster                                                   |
| scimark_sor                | 134 ms                                                       | 106 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 505 ms: 1.26x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.54 us: 1.23x faster                                                  |
| spectral_norm              | 111 ms                                                       | 93.2 ms: 1.19x faster                                                  |
| scimark_fft                | 349 ms                                                       | 307 ms: 1.14x faster                                                   |
| html5lib                   | 67.0 ms                                                      | 59.5 ms: 1.13x faster                                                  |
| async_generators           | 377 ms                                                       | 337 ms: 1.12x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 85.0 ms: 1.12x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.77 ms: 1.11x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 67.3 ms: 1.11x faster                                                  |
| pylint                     | 317 ms                                                       | 286 ms: 1.11x faster                                                   |
| pyflate                    | 449 ms                                                       | 405 ms: 1.11x faster                                                   |
| pathlib                    | 19.2 ms                                                      | 17.5 ms: 1.10x faster                                                  |
| float                      | 77.5 ms                                                      | 70.8 ms: 1.09x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.84 sec: 1.09x faster                                                 |
| pidigits                   | 217 ms                                                       | 201 ms: 1.08x faster                                                   |
| richards_super             | 51.6 ms                                                      | 48.1 ms: 1.07x faster                                                  |
| richards                   | 45.2 ms                                                      | 42.2 ms: 1.07x faster                                                  |
| regex_compile              | 132 ms                                                       | 124 ms: 1.07x faster                                                   |
| json_dumps                 | 10.5 ms                                                      | 9.87 ms: 1.07x faster                                                  |
| chaos                      | 57.3 ms                                                      | 53.8 ms: 1.06x faster                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.44 ms: 1.06x faster                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 62.0 ms: 1.05x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.22 sec: 1.05x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.71 ms: 1.05x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 21.7 ms: 1.05x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 108 ms: 1.05x faster                                                   |
| regex_dna                  | 180 ms                                                       | 174 ms: 1.04x faster                                                   |
| 2to3                       | 260 ms                                                       | 251 ms: 1.03x faster                                                   |
| sympy_integrate            | 19.8 ms                                                      | 19.2 ms: 1.03x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 132 ms: 1.03x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.46 sec: 1.02x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 721 ms: 1.02x faster                                                   |
| logging_simple             | 6.16 us                                                      | 6.04 us: 1.02x faster                                                  |
| comprehensions             | 16.5 us                                                      | 16.1 us: 1.02x faster                                                  |
| genshi_text                | 21.5 ms                                                      | 21.1 ms: 1.02x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 83.8 ms: 1.02x faster                                                  |
| coverage                   | 83.0 ms                                                      | 81.8 ms: 1.01x faster                                                  |
| pycparser                  | 1.12 sec                                                     | 1.10 sec: 1.01x faster                                                 |
| docutils                   | 2.62 sec                                                     | 2.59 sec: 1.01x faster                                                 |
| xml_etree_process          | 59.3 ms                                                      | 58.8 ms: 1.01x faster                                                  |
| generators                 | 28.8 ms                                                      | 28.6 ms: 1.01x faster                                                  |
| unpickle_pure_python       | 210 us                                                       | 208 us: 1.01x faster                                                   |
| logging_silent             | 103 ns                                                       | 102 ns: 1.01x faster                                                   |
| meteor_contest             | 102 ms                                                       | 101 ms: 1.01x faster                                                   |
| raytrace                   | 253 ms                                                       | 252 ms: 1.00x faster                                                   |
| python_startup_no_site     | 7.39 ms                                                      | 7.41 ms: 1.00x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 156 ms: 1.01x slower                                                   |
| genshi_xml                 | 48.8 ms                                                      | 49.1 ms: 1.01x slower                                                  |
| nqueens                    | 78.6 ms                                                      | 79.5 ms: 1.01x slower                                                  |
| sympy_str                  | 275 ms                                                       | 278 ms: 1.01x slower                                                   |
| sqlite_synth               | 2.21 us                                                      | 2.25 us: 1.02x slower                                                  |
| json                       | 4.93 ms                                                      | 5.04 ms: 1.02x slower                                                  |
| thrift                     | 778 us                                                       | 800 us: 1.03x slower                                                   |
| typing_runtime_protocols   | 155 us                                                       | 160 us: 1.04x slower                                                   |
| json_loads                 | 27.0 us                                                      | 28.0 us: 1.04x slower                                                  |
| sympy_expand               | 457 ms                                                       | 477 ms: 1.04x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 308 us: 1.04x slower                                                   |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                   |
| coroutines                 | 23.6 ms                                                      | 24.7 ms: 1.05x slower                                                  |
| mako                       | 11.3 ms                                                      | 11.9 ms: 1.05x slower                                                  |
| fannkuch                   | 370 ms                                                       | 388 ms: 1.05x slower                                                   |
| django_template            | 34.1 ms                                                      | 35.8 ms: 1.05x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.29 ms: 1.05x slower                                                  |
| nbody                      | 85.1 ms                                                      | 90.6 ms: 1.06x slower                                                  |
| python_startup             | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.86 ms: 1.39x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.31 ms: 1.42x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.65 ms: 1.48x slower                                                  |
| telco                      | 7.82 ms                                                      | 157 ms: 20.00x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 291 ms: 26.43x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (2): crypto_pyaes, logging_format
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260301-3.15.0a6+-c9a5d9a/bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.036x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.16x