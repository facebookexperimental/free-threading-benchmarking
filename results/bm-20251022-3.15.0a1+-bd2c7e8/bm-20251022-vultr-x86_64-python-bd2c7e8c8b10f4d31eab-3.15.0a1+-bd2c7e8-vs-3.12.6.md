# Results vs. 3.12.6

- fork: python
- ref: bd2c7e8c8b10f4d31eab
- machine: linux-x86_64
- commit hash: bd2c7e8
- commit date: 2025-10-22
- overall geometric mean: 1.071x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 248 ms: 1.06x faster                                                   |
| docutils       | 2.64 sec                                               | 2.58 sec: 1.02x faster                                                 |
| html5lib       | 63.6 ms                                                | 61.5 ms: 1.03x faster                                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 555 ms: 1.95x faster                                                   |
| async_tree_none            | 464 ms                                                 | 246 ms: 1.89x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 592 ms: 1.88x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 311 ms: 1.80x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 308 ms: 1.80x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 248 ms: 1.80x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 494 ms: 1.46x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 494 ms: 1.45x faster                                                   |
| async_generators           | 384 ms                                                 | 352 ms: 1.09x faster                                                   |
| coroutines                 | 23.9 ms                                                | 24.1 ms: 1.01x slower                                                  |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.50x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.7 ms: 1.14x faster                                                  |
| pidigits       | 184 ms                                                 | 193 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.69 ms: 1.18x faster                                                  |
| regex_compile  | 142 ms                                                 | 125 ms: 1.14x faster                                                   |
| regex_dna      | 168 ms                                                 | 177 ms: 1.05x slower                                                   |
| regex_v8       | 20.6 ms                                                | 22.7 ms: 1.10x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 84.6 ms: 1.14x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 1.92 sec: 1.10x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                   |
| json_dumps           | 10.4 ms                                                | 9.74 ms: 1.06x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 209 us: 1.05x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 82.8 ms: 1.03x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 58.5 ms: 1.01x faster                                                  |
| pickle_pure_python   | 308 us                                                 | 310 us: 1.01x slower                                                   |
| json_loads           | 26.5 us                                                | 28.1 us: 1.06x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.24 ms: 1.01x slower                                                  |
| python_startup         | 9.93 ms                                                | 12.4 ms: 1.25x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.12x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text    | 22.8 ms                                                | 20.9 ms: 1.09x faster                                                  |
| genshi_xml     | 50.2 ms                                                | 48.6 ms: 1.03x faster                                                  |
| mako           | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.15 sec: 2.10x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 555 ms: 1.95x faster                                                   |
| async_tree_none            | 464 ms                                                 | 246 ms: 1.89x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 592 ms: 1.88x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 311 ms: 1.80x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 308 ms: 1.80x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 248 ms: 1.80x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 26.3 us: 1.53x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 494 ms: 1.46x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 494 ms: 1.45x faster                                                   |
| deepcopy                   | 352 us                                                 | 246 us: 1.43x faster                                                   |
| go                         | 139 ms                                                 | 104 ms: 1.34x faster                                                   |
| comprehensions             | 19.8 us                                                | 15.4 us: 1.29x faster                                                  |
| pathlib                    | 21.5 ms                                                | 17.7 ms: 1.22x faster                                                  |
| scimark_sor                | 130 ms                                                 | 108 ms: 1.21x faster                                                   |
| raytrace                   | 299 ms                                                 | 253 ms: 1.18x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.69 ms: 1.18x faster                                                  |
| generators                 | 32.2 ms                                                | 27.7 ms: 1.16x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.65 us: 1.16x faster                                                  |
| spectral_norm              | 110 ms                                                 | 95.8 ms: 1.15x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 68.8 ms: 1.15x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 84.6 ms: 1.14x faster                                                  |
| float                      | 80.8 ms                                                | 70.7 ms: 1.14x faster                                                  |
| regex_compile              | 142 ms                                                 | 125 ms: 1.14x faster                                                   |
| richards                   | 45.9 ms                                                | 40.9 ms: 1.12x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.23 sec: 1.12x faster                                                 |
| logging_silent             | 109 ns                                                 | 97.6 ns: 1.12x faster                                                  |
| logging_simple             | 6.63 us                                                | 5.97 us: 1.11x faster                                                  |
| chaos                      | 62.8 ms                                                | 56.6 ms: 1.11x faster                                                  |
| richards_super             | 51.9 ms                                                | 46.9 ms: 1.11x faster                                                  |
| pylint                     | 319 ms                                                 | 288 ms: 1.10x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 69.4 ms: 1.10x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 62.1 ms: 1.10x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.92 sec: 1.10x faster                                                 |
| logging_format             | 7.35 us                                                | 6.71 us: 1.09x faster                                                  |
| async_generators           | 384 ms                                                 | 352 ms: 1.09x faster                                                   |
| genshi_text                | 22.8 ms                                                | 20.9 ms: 1.09x faster                                                  |
| scimark_fft                | 342 ms                                                 | 316 ms: 1.08x faster                                                   |
| hexiom                     | 6.17 ms                                                | 5.71 ms: 1.08x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.09 sec: 1.08x faster                                                 |
| pyflate                    | 448 ms                                                 | 417 ms: 1.08x faster                                                   |
| sympy_integrate            | 20.5 ms                                                | 19.1 ms: 1.07x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.42 sec: 1.07x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                   |
| json_dumps                 | 10.4 ms                                                | 9.74 ms: 1.06x faster                                                  |
| 2to3                       | 264 ms                                                 | 248 ms: 1.06x faster                                                   |
| pprint_safe_repr           | 743 ms                                                 | 700 ms: 1.06x faster                                                   |
| sympy_sum                  | 166 ms                                                 | 157 ms: 1.06x faster                                                   |
| unpickle_pure_python       | 221 us                                                 | 209 us: 1.05x faster                                                   |
| sympy_str                  | 292 ms                                                 | 278 ms: 1.05x faster                                                   |
| typing_runtime_protocols   | 163 us                                                 | 156 us: 1.05x faster                                                   |
| deltablue                  | 3.45 ms                                                | 3.31 ms: 1.04x faster                                                  |
| meteor_contest             | 104 ms                                                 | 99.7 ms: 1.04x faster                                                  |
| scimark_lu                 | 114 ms                                                 | 110 ms: 1.04x faster                                                   |
| html5lib                   | 63.6 ms                                                | 61.5 ms: 1.03x faster                                                  |
| genshi_xml                 | 50.2 ms                                                | 48.6 ms: 1.03x faster                                                  |
| xml_etree_generate         | 85.2 ms                                                | 82.8 ms: 1.03x faster                                                  |
| thrift                     | 791 us                                                 | 770 us: 1.03x faster                                                   |
| docutils                   | 2.64 sec                                               | 2.58 sec: 1.02x faster                                                 |
| nqueens                    | 80.1 ms                                                | 79.0 ms: 1.01x faster                                                  |
| xml_etree_process          | 59.0 ms                                                | 58.5 ms: 1.01x faster                                                  |
| coroutines                 | 23.9 ms                                                | 24.1 ms: 1.01x slower                                                  |
| json                       | 5.02 ms                                                | 5.06 ms: 1.01x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 310 us: 1.01x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 7.24 ms: 1.01x slower                                                  |
| sympy_expand               | 468 ms                                                 | 479 ms: 1.02x slower                                                   |
| sqlite_synth               | 2.20 us                                                | 2.28 us: 1.04x slower                                                  |
| pidigits                   | 184 ms                                                 | 193 ms: 1.05x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.63 ms: 1.05x slower                                                  |
| regex_dna                  | 168 ms                                                 | 177 ms: 1.05x slower                                                   |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                   |
| fannkuch                   | 372 ms                                                 | 393 ms: 1.06x slower                                                   |
| json_loads                 | 26.5 us                                                | 28.1 us: 1.06x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 998 us: 1.06x slower                                                   |
| mako                       | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 22.7 ms: 1.10x slower                                                  |
| coverage                   | 71.4 ms                                                | 81.6 ms: 1.14x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 12.4 ms: 1.15x slower                                                  |
| python_startup             | 9.93 ms                                                | 12.4 ms: 1.25x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.68 ms: 1.35x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.93 ms: 1.77x slower                                                  |
| telco                      | 6.53 ms                                                | 159 ms: 24.37x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                           |

Benchmark hidden because not significant (2): django_template, nbody
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251022-3.15.0a1+-bd2c7e8/bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.071x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.16x