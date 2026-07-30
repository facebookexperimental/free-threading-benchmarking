# Results vs. 3.13.0rc2

- fork: python
- ref: 8b048eb35eb7f83dbff8
- machine: linux-x86_64
- commit hash: 8b048eb
- commit date: 2026-07-28
- overall geometric mean: 1.069x slower
- HPT reliability: 97.85%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 298 ms: 1.15x slower                                                  |
| docutils       | 2.62 sec                                                     | 2.91 sec: 1.11x slower                                                |
| Geometric mean | (ref)                                                        | 1.08x slower                                                          |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 686 ms: 1.33x faster                                                  |
| async_tree_io              | 876 ms                                                       | 703 ms: 1.25x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 580 ms: 1.10x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 608 ms: 1.10x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 423 ms: 1.09x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 391 ms: 1.06x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 322 ms: 1.04x faster                                                  |
| async_tree_none            | 354 ms                                                       | 344 ms: 1.03x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 513 ms: 1.02x faster                                                  |
| async_generators           | 377 ms                                                       | 381 ms: 1.01x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 24.5 ms: 1.04x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.08x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 180 ms: 1.20x faster                                                  |
| float          | 77.5 ms                                                      | 83.1 ms: 1.07x slower                                                 |
| nbody          | 85.1 ms                                                      | 120 ms: 1.42x slower                                                  |
| Geometric mean | (ref)                                                        | 1.08x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 22.7 ms                                                      | 20.6 ms: 1.10x faster                                                 |
| regex_effbot   | 3.08 ms                                                      | 3.05 ms: 1.01x faster                                                 |
| regex_dna      | 180 ms                                                       | 183 ms: 1.02x slower                                                  |
| regex_compile  | 132 ms                                                       | 169 ms: 1.28x slower                                                  |
| Geometric mean | (ref)                                                        | 1.04x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.97 sec: 1.02x faster                                                |
| xml_etree_iterparse  | 94.9 ms                                                      | 95.4 ms: 1.01x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 10.6 ms: 1.01x slower                                                 |
| xml_etree_parse      | 136 ms                                                       | 140 ms: 1.03x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 238 us: 1.13x slower                                                  |
| json_loads           | 27.0 us                                                      | 30.6 us: 1.13x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 336 us: 1.14x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 102 ms: 1.20x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 75.7 ms: 1.28x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.10x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.22 ms: 1.25x slower                                                 |
| python_startup         | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.33x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 41.2 ms: 1.21x slower                                                 |
| mako            | 11.3 ms                                                      | 15.9 ms: 1.40x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.30x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 130 ms: 2.44x faster                                                  |
| mdp                        | 2.36 sec                                                     | 1.30 sec: 1.81x faster                                                |
| gc_traversal               | 3.14 ms                                                      | 1.78 ms: 1.77x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 686 ms: 1.33x faster                                                  |
| deepcopy                   | 355 us                                                       | 275 us: 1.29x faster                                                  |
| async_tree_io              | 876 ms                                                       | 703 ms: 1.25x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 31.5 us: 1.24x faster                                                 |
| pidigits                   | 217 ms                                                       | 180 ms: 1.20x faster                                                  |
| go                         | 141 ms                                                       | 119 ms: 1.18x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 1.95 us: 1.13x faster                                                 |
| regex_v8                   | 22.7 ms                                                      | 20.6 ms: 1.10x faster                                                 |
| scimark_sor                | 134 ms                                                       | 122 ms: 1.10x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 580 ms: 1.10x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 608 ms: 1.10x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 423 ms: 1.09x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 17.8 ms: 1.08x faster                                                 |
| dulwich_log                | 74.8 ms                                                      | 69.8 ms: 1.07x faster                                                 |
| typing_runtime_protocols   | 155 us                                                       | 145 us: 1.07x faster                                                  |
| spectral_norm              | 111 ms                                                       | 105 ms: 1.06x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 391 ms: 1.06x faster                                                  |
| scimark_fft                | 349 ms                                                       | 335 ms: 1.04x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 322 ms: 1.04x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.99 us: 1.04x faster                                                 |
| async_tree_none            | 354 ms                                                       | 344 ms: 1.03x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.37 sec: 1.02x faster                                                |
| tomli_loads                | 2.01 sec                                                     | 1.97 sec: 1.02x faster                                                |
| asyncio_websockets         | 520 ms                                                       | 513 ms: 1.02x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 3.05 ms: 1.01x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 95.4 ms: 1.01x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 10.6 ms: 1.01x slower                                                 |
| async_generators           | 377 ms                                                       | 381 ms: 1.01x slower                                                  |
| regex_dna                  | 180 ms                                                       | 183 ms: 1.02x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.37 ms: 1.03x slower                                                 |
| xml_etree_parse            | 136 ms                                                       | 140 ms: 1.03x slower                                                  |
| logging_silent             | 103 ns                                                       | 106 ns: 1.04x slower                                                  |
| pyflate                    | 449 ms                                                       | 466 ms: 1.04x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 24.5 ms: 1.04x slower                                                 |
| pycparser                  | 1.12 sec                                                     | 1.17 sec: 1.05x slower                                                |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.97 ms: 1.05x slower                                                 |
| chaos                      | 57.3 ms                                                      | 60.6 ms: 1.06x slower                                                 |
| float                      | 77.5 ms                                                      | 83.1 ms: 1.07x slower                                                 |
| hexiom                     | 5.99 ms                                                      | 6.48 ms: 1.08x slower                                                 |
| json                       | 4.93 ms                                                      | 5.36 ms: 1.09x slower                                                 |
| comprehensions             | 16.5 us                                                      | 18.1 us: 1.10x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 21.8 ms: 1.10x slower                                                 |
| docutils                   | 2.62 sec                                                     | 2.91 sec: 1.11x slower                                                |
| pprint_safe_repr           | 738 ms                                                       | 822 ms: 1.12x slower                                                  |
| nqueens                    | 78.6 ms                                                      | 87.9 ms: 1.12x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 238 us: 1.13x slower                                                  |
| json_loads                 | 27.0 us                                                      | 30.6 us: 1.13x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 336 us: 1.14x slower                                                  |
| logging_simple             | 6.16 us                                                      | 7.04 us: 1.14x slower                                                 |
| 2to3                       | 260 ms                                                       | 298 ms: 1.15x slower                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.72 sec: 1.15x slower                                                |
| raytrace                   | 253 ms                                                       | 290 ms: 1.15x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 130 ms: 1.15x slower                                                  |
| richards_super             | 51.6 ms                                                      | 59.7 ms: 1.16x slower                                                 |
| richards                   | 45.2 ms                                                      | 52.3 ms: 1.16x slower                                                 |
| sympy_sum                  | 156 ms                                                       | 181 ms: 1.16x slower                                                  |
| sympy_str                  | 275 ms                                                       | 320 ms: 1.17x slower                                                  |
| generators                 | 28.8 ms                                                      | 33.8 ms: 1.17x slower                                                 |
| sympy_expand               | 457 ms                                                       | 537 ms: 1.17x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.68 ms: 1.18x slower                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 77.5 ms: 1.19x slower                                                 |
| thrift                     | 778 us                                                       | 925 us: 1.19x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 102 ms: 1.20x slower                                                  |
| logging_format             | 6.84 us                                                      | 8.20 us: 1.20x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 13.3 ms: 1.21x slower                                                 |
| django_template            | 34.1 ms                                                      | 41.2 ms: 1.21x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 9.22 ms: 1.25x slower                                                 |
| fannkuch                   | 370 ms                                                       | 467 ms: 1.26x slower                                                  |
| meteor_contest             | 102 ms                                                       | 129 ms: 1.27x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 75.7 ms: 1.28x slower                                                 |
| regex_compile              | 132 ms                                                       | 169 ms: 1.28x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 87.7 ms: 1.29x slower                                                 |
| coverage                   | 83.0 ms                                                      | 116 ms: 1.40x slower                                                  |
| mako                       | 11.3 ms                                                      | 15.9 ms: 1.40x slower                                                 |
| nbody                      | 85.1 ms                                                      | 120 ms: 1.42x slower                                                  |
| python_startup             | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.49 ms: 1.62x slower                                                 |
| telco                      | 7.82 ms                                                      | 175 ms: 22.40x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.08x slower                                                          |

Benchmark hidden because not significant (1): html5lib
Ignored benchmarks (20) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260728-3.16.0a0-8b048eb-NOGIL/bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.069x slower

# HPT report

- Reliability score: 97.85% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.36x