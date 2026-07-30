# Results vs. 3.13.0rc2

- fork: python
- ref: 8b048eb35eb7f83dbff8
- machine: linux-x86_64
- commit hash: 8b048eb
- commit date: 2026-07-28
- overall geometric mean: 1.028x faster
- HPT reliability: 99.38%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 262 ms: 1.01x slower                                                  |
| docutils       | 2.62 sec                                                     | 2.39 sec: 1.10x faster                                                |
| html5lib       | 67.0 ms                                                      | 60.5 ms: 1.11x faster                                                 |
| Geometric mean | (ref)                                                        | 1.06x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 666 ms                                                       | 538 ms: 1.24x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 377 ms: 1.22x faster                                                  |
| async_tree_io              | 876 ms                                                       | 721 ms: 1.22x faster                                                  |
| async_tree_none            | 354 ms                                                       | 291 ms: 1.21x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 763 ms: 1.20x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 553 ms: 1.15x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 365 ms: 1.13x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 297 ms: 1.13x faster                                                  |
| async_generators           | 377 ms                                                       | 349 ms: 1.08x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.4 ms: 1.01x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.14x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 187 ms: 1.16x faster                                                  |
| float          | 77.5 ms                                                      | 73.8 ms: 1.05x faster                                                 |
| nbody          | 85.1 ms                                                      | 92.3 ms: 1.09x slower                                                 |
| Geometric mean | (ref)                                                        | 1.04x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.83 ms: 1.09x faster                                                 |
| regex_v8       | 22.7 ms                                                      | 22.0 ms: 1.03x faster                                                 |
| regex_dna      | 180 ms                                                       | 192 ms: 1.07x slower                                                  |
| regex_compile  | 132 ms                                                       | 149 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                        | 1.02x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.80 sec: 1.11x faster                                                |
| json_dumps           | 10.5 ms                                                      | 9.87 ms: 1.07x faster                                                 |
| xml_etree_iterparse  | 94.9 ms                                                      | 91.7 ms: 1.04x faster                                                 |
| unpickle_pure_python | 210 us                                                       | 214 us: 1.02x slower                                                  |
| json_loads           | 27.0 us                                                      | 27.5 us: 1.02x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 88.1 ms: 1.03x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 304 us: 1.03x slower                                                  |
| xml_etree_parse      | 136 ms                                                       | 143 ms: 1.05x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 62.5 ms: 1.05x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.00x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.07 ms: 1.05x faster                                                 |
| python_startup         | 11.0 ms                                                      | 12.6 ms: 1.14x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.05x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 12.0 ms: 1.05x slower                                                 |
| django_template | 34.1 ms                                                      | 36.2 ms: 1.06x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.06x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 114 ms: 2.79x faster                                                  |
| mdp                        | 2.36 sec                                                     | 1.14 sec: 2.07x faster                                                |
| deepcopy                   | 355 us                                                       | 233 us: 1.53x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 26.7 us: 1.46x faster                                                 |
| go                         | 141 ms                                                       | 106 ms: 1.33x faster                                                  |
| typing_runtime_protocols   | 155 us                                                       | 119 us: 1.30x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 538 ms: 1.24x faster                                                  |
| scimark_sor                | 134 ms                                                       | 109 ms: 1.23x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 377 ms: 1.22x faster                                                  |
| async_tree_io              | 876 ms                                                       | 721 ms: 1.22x faster                                                  |
| async_tree_none            | 354 ms                                                       | 291 ms: 1.21x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.58 us: 1.21x faster                                                 |
| spectral_norm              | 111 ms                                                       | 92.3 ms: 1.20x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 763 ms: 1.20x faster                                                  |
| pidigits                   | 217 ms                                                       | 187 ms: 1.16x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 553 ms: 1.15x faster                                                  |
| scimark_fft                | 349 ms                                                       | 307 ms: 1.14x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 365 ms: 1.13x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 297 ms: 1.13x faster                                                  |
| pyflate                    | 449 ms                                                       | 400 ms: 1.12x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.80 sec: 1.11x faster                                                |
| html5lib                   | 67.0 ms                                                      | 60.5 ms: 1.11x faster                                                 |
| dulwich_log                | 74.8 ms                                                      | 67.9 ms: 1.10x faster                                                 |
| docutils                   | 2.62 sec                                                     | 2.39 sec: 1.10x faster                                                |
| regex_effbot               | 3.08 ms                                                      | 2.83 ms: 1.09x faster                                                 |
| async_generators           | 377 ms                                                       | 349 ms: 1.08x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 17.9 ms: 1.07x faster                                                 |
| json_dumps                 | 10.5 ms                                                      | 9.87 ms: 1.07x faster                                                 |
| nqueens                    | 78.6 ms                                                      | 74.3 ms: 1.06x faster                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.46 ms: 1.06x faster                                                 |
| chaos                      | 57.3 ms                                                      | 54.3 ms: 1.06x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.21 sec: 1.06x faster                                                |
| hexiom                     | 5.99 ms                                                      | 5.68 ms: 1.06x faster                                                 |
| float                      | 77.5 ms                                                      | 73.8 ms: 1.05x faster                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 62.5 ms: 1.05x faster                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 7.07 ms: 1.05x faster                                                 |
| logging_silent             | 103 ns                                                       | 98.7 ns: 1.04x faster                                                 |
| sympy_integrate            | 19.8 ms                                                      | 19.1 ms: 1.04x faster                                                 |
| comprehensions             | 16.5 us                                                      | 15.9 us: 1.04x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 91.7 ms: 1.04x faster                                                 |
| regex_v8                   | 22.7 ms                                                      | 22.0 ms: 1.03x faster                                                 |
| logging_simple             | 6.16 us                                                      | 5.99 us: 1.03x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 721 ms: 1.02x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.47 sec: 1.02x faster                                                |
| logging_format             | 6.84 us                                                      | 6.75 us: 1.01x faster                                                 |
| json                       | 4.93 ms                                                      | 4.87 ms: 1.01x faster                                                 |
| richards_super             | 51.6 ms                                                      | 51.2 ms: 1.01x faster                                                 |
| coroutines                 | 23.6 ms                                                      | 23.4 ms: 1.01x faster                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 68.2 ms: 1.00x slower                                                 |
| raytrace                   | 253 ms                                                       | 254 ms: 1.00x slower                                                  |
| meteor_contest             | 102 ms                                                       | 102 ms: 1.01x slower                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.23 us: 1.01x slower                                                 |
| 2to3                       | 260 ms                                                       | 262 ms: 1.01x slower                                                  |
| coverage                   | 83.0 ms                                                      | 83.8 ms: 1.01x slower                                                 |
| pycparser                  | 1.12 sec                                                     | 1.13 sec: 1.01x slower                                                |
| sympy_str                  | 275 ms                                                       | 278 ms: 1.01x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 158 ms: 1.01x slower                                                  |
| fannkuch                   | 370 ms                                                       | 376 ms: 1.02x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 214 us: 1.02x slower                                                  |
| json_loads                 | 27.0 us                                                      | 27.5 us: 1.02x slower                                                 |
| generators                 | 28.8 ms                                                      | 29.3 ms: 1.02x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 88.1 ms: 1.03x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 304 us: 1.03x slower                                                  |
| sympy_expand               | 457 ms                                                       | 472 ms: 1.03x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                  |
| xml_etree_parse            | 136 ms                                                       | 143 ms: 1.05x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 118 ms: 1.05x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 62.5 ms: 1.05x slower                                                 |
| mako                       | 11.3 ms                                                      | 12.0 ms: 1.05x slower                                                 |
| django_template            | 34.1 ms                                                      | 36.2 ms: 1.06x slower                                                 |
| regex_dna                  | 180 ms                                                       | 192 ms: 1.07x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.37 ms: 1.08x slower                                                 |
| nbody                      | 85.1 ms                                                      | 92.3 ms: 1.09x slower                                                 |
| regex_compile              | 132 ms                                                       | 149 ms: 1.12x slower                                                  |
| python_startup             | 11.0 ms                                                      | 12.6 ms: 1.14x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.69 ms: 1.26x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.03 ms: 1.28x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.34 ms: 1.46x slower                                                 |
| telco                      | 7.82 ms                                                      | 159 ms: 20.26x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 262 ms: 23.80x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.01x slower                                                          |

Benchmark hidden because not significant (2): richards, thrift
Ignored benchmarks (20) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260728-3.16.0a0-8b048eb/bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.028x faster

# HPT report

- Reliability score: 99.38% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.14x