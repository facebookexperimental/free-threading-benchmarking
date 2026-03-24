# Results vs. 3.13.0rc2

- fork: python
- ref: bcff99cb3f3b887a08c4
- machine: linux-x86_64
- commit hash: bcff99c
- commit date: 2026-03-23
- overall geometric mean: 1.031x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 252 ms: 1.03x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.46 sec: 1.06x faster                                                 |
| html5lib       | 67.0 ms                                                      | 60.0 ms: 1.12x faster                                                  |
| Geometric mean | (ref)                                                        | 1.07x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 571 ms: 1.60x faster                                                   |
| async_tree_io              | 876 ms                                                       | 591 ms: 1.48x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 315 ms: 1.46x faster                                                   |
| async_tree_none            | 354 ms                                                       | 250 ms: 1.41x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 246 ms: 1.37x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 307 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 510 ms: 1.31x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 522 ms: 1.22x faster                                                   |
| async_generators           | 377 ms                                                       | 344 ms: 1.10x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 23.5 ms: 1.00x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.28x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 69.8 ms: 1.11x faster                                                  |
| pidigits       | 217 ms                                                       | 204 ms: 1.06x faster                                                   |
| nbody          | 85.1 ms                                                      | 94.9 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                        | 1.02x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.68 ms: 1.15x faster                                                  |
| regex_dna      | 180 ms                                                       | 165 ms: 1.09x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 21.1 ms: 1.08x faster                                                  |
| regex_compile  | 132 ms                                                       | 125 ms: 1.06x faster                                                   |
| Geometric mean | (ref)                                                        | 1.09x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 85.2 ms: 1.11x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 1.84 sec: 1.09x faster                                                 |
| json_dumps           | 10.5 ms                                                      | 10.1 ms: 1.04x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 132 ms: 1.04x faster                                                   |
| unpickle_pure_python | 210 us                                                       | 215 us: 1.02x slower                                                   |
| json_loads           | 27.0 us                                                      | 27.8 us: 1.03x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 308 us: 1.05x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.02x faster                                                           |

Benchmark hidden because not significant (2): xml_etree_generate, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.42 ms: 1.00x slower                                                  |
| python_startup         | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.07x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.4 ms: 1.01x faster                                                  |
| django_template | 34.1 ms                                                      | 35.5 ms: 1.04x slower                                                  |
| genshi_xml      | 48.8 ms                                                      | 51.2 ms: 1.05x slower                                                  |
| mako            | 11.3 ms                                                      | 12.0 ms: 1.06x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.04x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.15 sec: 2.04x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 571 ms: 1.60x faster                                                   |
| deepcopy                   | 355 us                                                       | 234 us: 1.52x faster                                                   |
| async_tree_io              | 876 ms                                                       | 591 ms: 1.48x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 26.5 us: 1.48x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 315 ms: 1.46x faster                                                   |
| async_tree_none            | 354 ms                                                       | 250 ms: 1.41x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 246 ms: 1.37x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 307 ms: 1.35x faster                                                   |
| go                         | 141 ms                                                       | 104 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 510 ms: 1.31x faster                                                   |
| scimark_sor                | 134 ms                                                       | 110 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 522 ms: 1.22x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.57 us: 1.21x faster                                                  |
| spectral_norm              | 111 ms                                                       | 93.1 ms: 1.19x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.68 ms: 1.15x faster                                                  |
| pylint                     | 317 ms                                                       | 283 ms: 1.12x faster                                                   |
| html5lib                   | 67.0 ms                                                      | 60.0 ms: 1.12x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 85.2 ms: 1.11x faster                                                  |
| float                      | 77.5 ms                                                      | 69.8 ms: 1.11x faster                                                  |
| scimark_fft                | 349 ms                                                       | 316 ms: 1.11x faster                                                   |
| pyflate                    | 449 ms                                                       | 407 ms: 1.10x faster                                                   |
| async_generators           | 377 ms                                                       | 344 ms: 1.10x faster                                                   |
| regex_dna                  | 180 ms                                                       | 165 ms: 1.09x faster                                                   |
| dulwich_log                | 74.8 ms                                                      | 68.5 ms: 1.09x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.84 sec: 1.09x faster                                                 |
| pathlib                    | 19.2 ms                                                      | 17.8 ms: 1.08x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 21.1 ms: 1.08x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.16 sec: 1.07x faster                                                 |
| richards                   | 45.2 ms                                                      | 42.3 ms: 1.07x faster                                                  |
| logging_simple             | 6.16 us                                                      | 5.78 us: 1.06x faster                                                  |
| richards_super             | 51.6 ms                                                      | 48.5 ms: 1.06x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.46 sec: 1.06x faster                                                 |
| pidigits                   | 217 ms                                                       | 204 ms: 1.06x faster                                                   |
| regex_compile              | 132 ms                                                       | 125 ms: 1.06x faster                                                   |
| logging_silent             | 103 ns                                                       | 97.1 ns: 1.06x faster                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 62.2 ms: 1.05x faster                                                  |
| chaos                      | 57.3 ms                                                      | 54.9 ms: 1.04x faster                                                  |
| hexiom                     | 5.99 ms                                                      | 5.75 ms: 1.04x faster                                                  |
| json_dumps                 | 10.5 ms                                                      | 10.1 ms: 1.04x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 109 ms: 1.04x faster                                                   |
| xml_etree_parse            | 136 ms                                                       | 132 ms: 1.04x faster                                                   |
| 2to3                       | 260 ms                                                       | 252 ms: 1.03x faster                                                   |
| nqueens                    | 78.6 ms                                                      | 76.3 ms: 1.03x faster                                                  |
| pycparser                  | 1.12 sec                                                     | 1.09 sec: 1.03x faster                                                 |
| sympy_integrate            | 19.8 ms                                                      | 19.3 ms: 1.02x faster                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.60 ms: 1.02x faster                                                  |
| pprint_safe_repr           | 738 ms                                                       | 723 ms: 1.02x faster                                                   |
| logging_format             | 6.84 us                                                      | 6.71 us: 1.02x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.48 sec: 1.01x faster                                                 |
| meteor_contest             | 102 ms                                                       | 101 ms: 1.01x faster                                                   |
| genshi_text                | 21.5 ms                                                      | 21.4 ms: 1.01x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.5 ms: 1.00x faster                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.42 ms: 1.00x slower                                                  |
| coverage                   | 83.0 ms                                                      | 83.3 ms: 1.00x slower                                                  |
| raytrace                   | 253 ms                                                       | 254 ms: 1.01x slower                                                   |
| sympy_sum                  | 156 ms                                                       | 159 ms: 1.02x slower                                                   |
| unpickle_pure_python       | 210 us                                                       | 215 us: 1.02x slower                                                   |
| generators                 | 28.8 ms                                                      | 29.5 ms: 1.02x slower                                                  |
| sympy_str                  | 275 ms                                                       | 282 ms: 1.03x slower                                                   |
| json_loads                 | 27.0 us                                                      | 27.8 us: 1.03x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 70.0 ms: 1.03x slower                                                  |
| fannkuch                   | 370 ms                                                       | 382 ms: 1.03x slower                                                   |
| typing_runtime_protocols   | 155 us                                                       | 160 us: 1.03x slower                                                   |
| json                       | 4.93 ms                                                      | 5.11 ms: 1.04x slower                                                  |
| django_template            | 34.1 ms                                                      | 35.5 ms: 1.04x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 308 us: 1.05x slower                                                   |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                   |
| genshi_xml                 | 48.8 ms                                                      | 51.2 ms: 1.05x slower                                                  |
| mako                       | 11.3 ms                                                      | 12.0 ms: 1.06x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.31 ms: 1.06x slower                                                  |
| sympy_expand               | 457 ms                                                       | 495 ms: 1.08x slower                                                   |
| nbody                      | 85.1 ms                                                      | 94.9 ms: 1.12x slower                                                  |
| python_startup             | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.83 ms: 1.37x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.46 ms: 1.42x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.33 ms: 1.45x slower                                                  |
| telco                      | 7.82 ms                                                      | 161 ms: 20.61x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 298 ms: 27.14x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (5): xml_etree_generate, comprehensions, thrift, xml_etree_process, sqlite_synth
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260323-3.15.0a7+-bcff99c/bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.031x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.16x