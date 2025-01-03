# Results vs. 3.13.0rc2

- fork: python
- ref: 8eebe4e6d02bb4ad3f1c
- machine: linux-x86_64
- commit hash: 8eebe4e
- commit date: 2025-01-02
- overall geometric mean: 1.056x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 254 ms: 1.02x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.55 sec: 1.03x faster                                                 |
| Geometric mean | (ref)                                                        | 1.02x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 603 ms: 1.51x faster                                                   |
| async_tree_io              | 876 ms                                                       | 609 ms: 1.44x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 327 ms: 1.41x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 298 ms: 1.39x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 250 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 499 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 479 ms: 1.33x faster                                                   |
| async_tree_none            | 354 ms                                                       | 272 ms: 1.30x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 20.8 ms: 1.13x faster                                                  |
| async_generators           | 377 ms                                                       | 355 ms: 1.06x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.01x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.29x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 192 ms: 1.13x faster                                                   |
| float          | 77.5 ms                                                      | 72.2 ms: 1.07x faster                                                  |
| nbody          | 85.1 ms                                                      | 92.1 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.83 ms: 1.09x faster                                                  |
| regex_compile  | 132 ms                                                       | 127 ms: 1.04x faster                                                   |
| regex_dna      | 180 ms                                                       | 182 ms: 1.01x slower                                                   |
| regex_v8       | 22.7 ms                                                      | 25.0 ms: 1.10x slower                                                  |
| Geometric mean | (ref)                                                        | 1.00x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 127 ms: 1.07x faster                                                   |
| tomli_loads          | 2.01 sec                                                     | 1.88 sec: 1.06x faster                                                 |
| xml_etree_iterparse  | 94.9 ms                                                      | 90.4 ms: 1.05x faster                                                  |
| json_loads           | 27.0 us                                                      | 25.9 us: 1.04x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 82.7 ms: 1.03x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 58.0 ms: 1.02x faster                                                  |
| unpickle_pure_python | 210 us                                                       | 211 us: 1.01x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 312 us: 1.06x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 11.2 ms: 1.06x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.02x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.51 ms: 1.02x slower                                                  |
| python_startup         | 11.0 ms                                                      | 14.7 ms: 1.34x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.17x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.1 ms: 1.02x faster                                                  |
| genshi_xml      | 48.8 ms                                                      | 48.3 ms: 1.01x faster                                                  |
| django_template | 34.1 ms                                                      | 34.8 ms: 1.02x slower                                                  |
| mako            | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.00x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 603 ms: 1.51x faster                                                   |
| async_tree_io              | 876 ms                                                       | 609 ms: 1.44x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 327 ms: 1.41x faster                                                   |
| deepcopy                   | 355 us                                                       | 255 us: 1.39x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 298 ms: 1.39x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 250 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 499 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 479 ms: 1.33x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 29.4 us: 1.33x faster                                                  |
| async_tree_none            | 354 ms                                                       | 272 ms: 1.30x faster                                                   |
| go                         | 141 ms                                                       | 115 ms: 1.22x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.56 us: 1.21x faster                                                  |
| scimark_sor                | 134 ms                                                       | 113 ms: 1.18x faster                                                   |
| spectral_norm              | 111 ms                                                       | 93.8 ms: 1.18x faster                                                  |
| pylint                     | 317 ms                                                       | 278 ms: 1.14x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 20.8 ms: 1.13x faster                                                  |
| pidigits                   | 217 ms                                                       | 192 ms: 1.13x faster                                                   |
| scimark_fft                | 349 ms                                                       | 313 ms: 1.11x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.83 ms: 1.09x faster                                                  |
| pyflate                    | 449 ms                                                       | 413 ms: 1.09x faster                                                   |
| richards                   | 45.2 ms                                                      | 41.9 ms: 1.08x faster                                                  |
| pprint_safe_repr           | 738 ms                                                       | 685 ms: 1.08x faster                                                   |
| richards_super             | 51.6 ms                                                      | 48.0 ms: 1.08x faster                                                  |
| telco                      | 7.82 ms                                                      | 7.27 ms: 1.08x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 127 ms: 1.07x faster                                                   |
| float                      | 77.5 ms                                                      | 72.2 ms: 1.07x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.40 sec: 1.07x faster                                                 |
| pathlib                    | 19.2 ms                                                      | 18.0 ms: 1.07x faster                                                  |
| thrift                     | 778 us                                                       | 729 us: 1.07x faster                                                   |
| tomli_loads                | 2.01 sec                                                     | 1.88 sec: 1.06x faster                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.43 ms: 1.06x faster                                                  |
| async_generators           | 377 ms                                                       | 355 ms: 1.06x faster                                                   |
| generators                 | 28.8 ms                                                      | 27.3 ms: 1.06x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.23 sec: 1.05x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.4 ms: 1.05x faster                                                  |
| json                       | 4.93 ms                                                      | 4.72 ms: 1.04x faster                                                  |
| json_loads                 | 27.0 us                                                      | 25.9 us: 1.04x faster                                                  |
| coverage                   | 83.0 ms                                                      | 79.8 ms: 1.04x faster                                                  |
| regex_compile              | 132 ms                                                       | 127 ms: 1.04x faster                                                   |
| logging_simple             | 6.16 us                                                      | 5.94 us: 1.04x faster                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 63.0 ms: 1.04x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 82.7 ms: 1.03x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.55 sec: 1.03x faster                                                 |
| sqlglot_normalize          | 106 ms                                                       | 103 ms: 1.02x faster                                                   |
| meteor_contest             | 102 ms                                                       | 99.3 ms: 1.02x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 58.0 ms: 1.02x faster                                                  |
| genshi_text                | 21.5 ms                                                      | 21.1 ms: 1.02x faster                                                  |
| 2to3                       | 260 ms                                                       | 254 ms: 1.02x faster                                                   |
| crypto_pyaes               | 67.9 ms                                                      | 66.5 ms: 1.02x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.72 us: 1.02x faster                                                  |
| sympy_str                  | 275 ms                                                       | 270 ms: 1.02x faster                                                   |
| fannkuch                   | 370 ms                                                       | 364 ms: 1.02x faster                                                   |
| sympy_sum                  | 156 ms                                                       | 153 ms: 1.01x faster                                                   |
| sqlglot_optimize           | 52.7 ms                                                      | 52.1 ms: 1.01x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 111 ms: 1.01x faster                                                   |
| hexiom                     | 5.99 ms                                                      | 5.93 ms: 1.01x faster                                                  |
| genshi_xml                 | 48.8 ms                                                      | 48.3 ms: 1.01x faster                                                  |
| sympy_integrate            | 19.8 ms                                                      | 19.6 ms: 1.01x faster                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 1.24 ms: 1.01x faster                                                  |
| sqlglot_transpile          | 1.56 ms                                                      | 1.55 ms: 1.01x faster                                                  |
| nqueens                    | 78.6 ms                                                      | 78.1 ms: 1.01x faster                                                  |
| deltablue                  | 3.12 ms                                                      | 3.11 ms: 1.00x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.01x slower                                                   |
| chaos                      | 57.3 ms                                                      | 57.7 ms: 1.01x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 211 us: 1.01x slower                                                   |
| logging_silent             | 103 ns                                                       | 103 ns: 1.01x slower                                                   |
| regex_dna                  | 180 ms                                                       | 182 ms: 1.01x slower                                                   |
| python_startup_no_site     | 7.39 ms                                                      | 7.51 ms: 1.02x slower                                                  |
| django_template            | 34.1 ms                                                      | 34.8 ms: 1.02x slower                                                  |
| raytrace                   | 253 ms                                                       | 259 ms: 1.02x slower                                                   |
| mako                       | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                  |
| comprehensions             | 16.5 us                                                      | 17.0 us: 1.03x slower                                                  |
| mdp                        | 2.36 sec                                                     | 2.44 sec: 1.04x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 312 us: 1.06x slower                                                   |
| json_dumps                 | 10.5 ms                                                      | 11.2 ms: 1.06x slower                                                  |
| nbody                      | 85.1 ms                                                      | 92.1 ms: 1.08x slower                                                  |
| regex_v8                   | 22.7 ms                                                      | 25.0 ms: 1.10x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.03 ms: 1.12x slower                                                  |
| python_startup             | 11.0 ms                                                      | 14.7 ms: 1.34x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.29 ms: 1.37x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.84 ms: 1.38x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 89.5 ms: 8.14x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.03x faster                                                           |

Benchmark hidden because not significant (5): typing_runtime_protocols, dulwich_log, pycparser, sympy_expand, sqlite_synth
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250102-3.14.0a3+-8eebe4e/bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.056x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.09x