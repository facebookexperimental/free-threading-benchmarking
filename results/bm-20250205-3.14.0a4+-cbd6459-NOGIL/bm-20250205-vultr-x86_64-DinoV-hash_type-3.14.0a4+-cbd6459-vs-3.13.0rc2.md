# Results vs. 3.13.0rc2

- fork: DinoV
- ref: hash_type
- machine: linux-x86_64
- commit hash: cbd6459
- commit date: 2025-02-05
- overall geometric mean: 1.080x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 303 ms: 1.17x slower                                       |
| docutils       | 2.62 sec                                                     | 2.85 sec: 1.09x slower                                     |
| html5lib       | 67.0 ms                                                      | 70.2 ms: 1.05x slower                                      |
| Geometric mean | (ref)                                                        | 1.10x slower                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 575 ms: 1.59x faster                                       |
| async_tree_io              | 876 ms                                                       | 604 ms: 1.45x faster                                       |
| async_tree_none_tg         | 336 ms                                                       | 250 ms: 1.35x faster                                       |
| async_tree_memoization     | 461 ms                                                       | 352 ms: 1.31x faster                                       |
| async_tree_memoization_tg  | 414 ms                                                       | 319 ms: 1.30x faster                                       |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 504 ms: 1.26x faster                                       |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 537 ms: 1.24x faster                                       |
| async_tree_none            | 354 ms                                                       | 286 ms: 1.24x faster                                       |
| async_generators           | 377 ms                                                       | 375 ms: 1.01x faster                                       |
| coroutines                 | 23.6 ms                                                      | 23.9 ms: 1.02x slower                                      |
| Geometric mean             | (ref)                                                        | 1.24x faster                                               |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 193 ms: 1.12x faster                                       |
| float          | 77.5 ms                                                      | 76.6 ms: 1.01x faster                                      |
| nbody          | 85.1 ms                                                      | 135 ms: 1.59x slower                                       |
| Geometric mean | (ref)                                                        | 1.12x slower                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.87 ms: 1.07x faster                                      |
| regex_dna      | 180 ms                                                       | 183 ms: 1.02x slower                                       |
| regex_v8       | 22.7 ms                                                      | 23.7 ms: 1.05x slower                                      |
| regex_compile  | 132 ms                                                       | 149 ms: 1.13x slower                                       |
| Geometric mean | (ref)                                                        | 1.03x slower                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 87.1 ms: 1.09x faster                                      |
| xml_etree_parse      | 136 ms                                                       | 127 ms: 1.07x faster                                       |
| xml_etree_generate   | 85.4 ms                                                      | 95.7 ms: 1.12x slower                                      |
| xml_etree_process    | 59.3 ms                                                      | 68.4 ms: 1.15x slower                                      |
| json_loads           | 27.0 us                                                      | 31.2 us: 1.16x slower                                      |
| tomli_loads          | 2.01 sec                                                     | 2.32 sec: 1.16x slower                                     |
| unpickle_pure_python | 210 us                                                       | 250 us: 1.19x slower                                       |
| json_dumps           | 10.5 ms                                                      | 12.8 ms: 1.22x slower                                      |
| pickle_pure_python   | 294 us                                                       | 368 us: 1.25x slower                                       |
| Geometric mean       | (ref)                                                        | 1.12x slower                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.63 ms: 1.30x slower                                      |
| python_startup         | 11.0 ms                                                      | 15.3 ms: 1.40x slower                                      |
| Geometric mean         | (ref)                                                        | 1.35x slower                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 60.2 ms: 1.24x slower                                      |
| django_template | 34.1 ms                                                      | 42.7 ms: 1.25x slower                                      |
| genshi_text     | 21.5 ms                                                      | 28.1 ms: 1.30x slower                                      |
| mako            | 11.3 ms                                                      | 15.8 ms: 1.40x slower                                      |
| Geometric mean  | (ref)                                                        | 1.29x slower                                               |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| gc_traversal               | 3.14 ms                                                      | 1.76 ms: 1.79x faster                                      |
| async_tree_io_tg           | 913 ms                                                       | 575 ms: 1.59x faster                                       |
| async_tree_io              | 876 ms                                                       | 604 ms: 1.45x faster                                       |
| async_tree_none_tg         | 336 ms                                                       | 250 ms: 1.35x faster                                       |
| async_tree_memoization     | 461 ms                                                       | 352 ms: 1.31x faster                                       |
| async_tree_memoization_tg  | 414 ms                                                       | 319 ms: 1.30x faster                                       |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 504 ms: 1.26x faster                                       |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 537 ms: 1.24x faster                                       |
| async_tree_none            | 354 ms                                                       | 286 ms: 1.24x faster                                       |
| deepcopy                   | 355 us                                                       | 311 us: 1.14x faster                                       |
| pidigits                   | 217 ms                                                       | 193 ms: 1.12x faster                                       |
| xml_etree_iterparse        | 94.9 ms                                                      | 87.1 ms: 1.09x faster                                      |
| sqlite_synth               | 2.21 us                                                      | 2.03 us: 1.09x faster                                      |
| regex_effbot               | 3.08 ms                                                      | 2.87 ms: 1.07x faster                                      |
| xml_etree_parse            | 136 ms                                                       | 127 ms: 1.07x faster                                       |
| pathlib                    | 19.2 ms                                                      | 18.6 ms: 1.03x faster                                      |
| deepcopy_memo              | 39.1 us                                                      | 38.3 us: 1.02x faster                                      |
| spectral_norm              | 111 ms                                                       | 109 ms: 1.02x faster                                       |
| scimark_sor                | 134 ms                                                       | 132 ms: 1.02x faster                                       |
| float                      | 77.5 ms                                                      | 76.6 ms: 1.01x faster                                      |
| go                         | 141 ms                                                       | 139 ms: 1.01x faster                                       |
| async_generators           | 377 ms                                                       | 375 ms: 1.01x faster                                       |
| coroutines                 | 23.6 ms                                                      | 23.9 ms: 1.02x slower                                      |
| regex_dna                  | 180 ms                                                       | 183 ms: 1.02x slower                                       |
| deepcopy_reduce            | 3.11 us                                                      | 3.19 us: 1.03x slower                                      |
| create_gc_cycles           | 1.34 ms                                                      | 1.39 ms: 1.04x slower                                      |
| bpe_tokeniser              | 4.45 sec                                                     | 4.62 sec: 1.04x slower                                     |
| regex_v8                   | 22.7 ms                                                      | 23.7 ms: 1.05x slower                                      |
| html5lib                   | 67.0 ms                                                      | 70.2 ms: 1.05x slower                                      |
| pycparser                  | 1.12 sec                                                     | 1.19 sec: 1.07x slower                                     |
| docutils                   | 2.62 sec                                                     | 2.85 sec: 1.09x slower                                     |
| dulwich_log                | 74.8 ms                                                      | 81.7 ms: 1.09x slower                                      |
| scimark_fft                | 349 ms                                                       | 383 ms: 1.10x slower                                       |
| json                       | 4.93 ms                                                      | 5.40 ms: 1.10x slower                                      |
| logging_silent             | 103 ns                                                       | 113 ns: 1.10x slower                                       |
| telco                      | 7.82 ms                                                      | 8.66 ms: 1.11x slower                                      |
| pprint_safe_repr           | 738 ms                                                       | 822 ms: 1.11x slower                                       |
| xml_etree_generate         | 85.4 ms                                                      | 95.7 ms: 1.12x slower                                      |
| mdp                        | 2.36 sec                                                     | 2.64 sec: 1.12x slower                                     |
| regex_compile              | 132 ms                                                       | 149 ms: 1.13x slower                                       |
| pprint_pformat             | 1.50 sec                                                     | 1.69 sec: 1.13x slower                                     |
| pyflate                    | 449 ms                                                       | 511 ms: 1.14x slower                                       |
| xml_etree_process          | 59.3 ms                                                      | 68.4 ms: 1.15x slower                                      |
| json_loads                 | 27.0 us                                                      | 31.2 us: 1.16x slower                                      |
| tomli_loads                | 2.01 sec                                                     | 2.32 sec: 1.16x slower                                     |
| sqlglot_normalize          | 106 ms                                                       | 123 ms: 1.17x slower                                       |
| 2to3                       | 260 ms                                                       | 303 ms: 1.17x slower                                       |
| generators                 | 28.8 ms                                                      | 33.6 ms: 1.17x slower                                      |
| thrift                     | 778 us                                                       | 908 us: 1.17x slower                                       |
| sqlglot_optimize           | 52.7 ms                                                      | 61.9 ms: 1.17x slower                                      |
| coverage                   | 83.0 ms                                                      | 97.5 ms: 1.17x slower                                      |
| logging_simple             | 6.16 us                                                      | 7.24 us: 1.18x slower                                      |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.60 ms: 1.19x slower                                      |
| unpickle_pure_python       | 210 us                                                       | 250 us: 1.19x slower                                       |
| logging_format             | 6.84 us                                                      | 8.17 us: 1.19x slower                                      |
| sympy_sum                  | 156 ms                                                       | 186 ms: 1.20x slower                                       |
| scimark_lu                 | 113 ms                                                       | 135 ms: 1.20x slower                                       |
| sympy_expand               | 457 ms                                                       | 551 ms: 1.21x slower                                       |
| comprehensions             | 16.5 us                                                      | 19.9 us: 1.21x slower                                      |
| json_dumps                 | 10.5 ms                                                      | 12.8 ms: 1.22x slower                                      |
| sympy_str                  | 275 ms                                                       | 334 ms: 1.22x slower                                       |
| nqueens                    | 78.6 ms                                                      | 96.0 ms: 1.22x slower                                      |
| chaos                      | 57.3 ms                                                      | 70.2 ms: 1.22x slower                                      |
| sympy_integrate            | 19.8 ms                                                      | 24.3 ms: 1.22x slower                                      |
| sqlglot_transpile          | 1.56 ms                                                      | 1.92 ms: 1.23x slower                                      |
| hexiom                     | 5.99 ms                                                      | 7.39 ms: 1.23x slower                                      |
| genshi_xml                 | 48.8 ms                                                      | 60.2 ms: 1.24x slower                                      |
| richards                   | 45.2 ms                                                      | 56.5 ms: 1.25x slower                                      |
| pickle_pure_python         | 294 us                                                       | 368 us: 1.25x slower                                       |
| django_template            | 34.1 ms                                                      | 42.7 ms: 1.25x slower                                      |
| richards_super             | 51.6 ms                                                      | 65.0 ms: 1.26x slower                                      |
| scimark_monte_carlo        | 65.4 ms                                                      | 82.6 ms: 1.26x slower                                      |
| meteor_contest             | 102 ms                                                       | 129 ms: 1.27x slower                                       |
| sqlglot_parse              | 1.25 ms                                                      | 1.58 ms: 1.27x slower                                      |
| typing_runtime_protocols   | 155 us                                                       | 200 us: 1.29x slower                                       |
| crypto_pyaes               | 67.9 ms                                                      | 88.1 ms: 1.30x slower                                      |
| raytrace                   | 253 ms                                                       | 329 ms: 1.30x slower                                       |
| genshi_text                | 21.5 ms                                                      | 28.1 ms: 1.30x slower                                      |
| python_startup_no_site     | 7.39 ms                                                      | 9.63 ms: 1.30x slower                                      |
| fannkuch                   | 370 ms                                                       | 486 ms: 1.31x slower                                       |
| mako                       | 11.3 ms                                                      | 15.8 ms: 1.40x slower                                      |
| python_startup             | 11.0 ms                                                      | 15.3 ms: 1.40x slower                                      |
| deltablue                  | 3.12 ms                                                      | 4.75 ms: 1.52x slower                                      |
| nbody                      | 85.1 ms                                                      | 135 ms: 1.59x slower                                       |
| bench_thread_pool          | 919 us                                                       | 3.31 ms: 3.60x slower                                      |
| bench_mp_pool              | 11.0 ms                                                      | 94.6 ms: 8.60x slower                                      |
| Geometric mean             | (ref)                                                        | 1.13x slower                                               |

Benchmark hidden because not significant (2): asyncio_websockets, pylint
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250205-3.14.0a4+-cbd6459-NOGIL/bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.080x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.34x