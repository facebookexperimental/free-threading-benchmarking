# Results vs. base

- fork: python
- ref: bc26f95e8ff60ccca981
- machine: linux-x86_64
- commit hash: bc26f95
- commit date: 2025-03-22
- overall geometric mean: 1.023x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-JIT/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 257 ms                                                                                                            | 260 ms: 1.01x slower                                                                                                  |
| docutils       | 2.60 sec                                                                                                          | 2.64 sec: 1.02x slower                                                                                                |
| Geometric mean | (ref)                                                                                                             | 1.01x slower                                                                                                          |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-JIT/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 524 ms                                                                                                            | 485 ms: 1.08x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 535 ms                                                                                                            | 500 ms: 1.07x faster                                                                                                  |
| coroutines                 | 23.6 ms                                                                                                           | 22.7 ms: 1.04x faster                                                                                                 |
| async_tree_memoization     | 321 ms                                                                                                            | 312 ms: 1.03x faster                                                                                                  |
| async_tree_none_tg         | 261 ms                                                                                                            | 253 ms: 1.03x faster                                                                                                  |
| async_tree_memoization_tg  | 311 ms                                                                                                            | 303 ms: 1.03x faster                                                                                                  |
| async_tree_io              | 632 ms                                                                                                            | 616 ms: 1.03x faster                                                                                                  |
| async_tree_none            | 279 ms                                                                                                            | 272 ms: 1.02x faster                                                                                                  |
| async_tree_io_tg           | 641 ms                                                                                                            | 630 ms: 1.02x faster                                                                                                  |
| async_generators           | 337 ms                                                                                                            | 354 ms: 1.05x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                             | 1.02x faster                                                                                                          |

Benchmark hidden because not significant (3): asyncio_websockets, asyncio_tcp_ssl, asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-JIT/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| nbody          | 98.6 ms                                                                                                           | 82.7 ms: 1.19x faster                                                                                                 |
| pidigits       | 210 ms                                                                                                            | 192 ms: 1.10x faster                                                                                                  |
| float          | 72.2 ms                                                                                                           | 66.3 ms: 1.09x faster                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.12x faster                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-JIT/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_effbot   | 2.82 ms                                                                                                           | 2.72 ms: 1.04x faster                                                                                                 |
| regex_dna      | 181 ms                                                                                                            | 175 ms: 1.04x faster                                                                                                  |
| regex_v8       | 22.3 ms                                                                                                           | 21.7 ms: 1.03x faster                                                                                                 |
| regex_compile  | 128 ms                                                                                                            | 127 ms: 1.01x faster                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.03x faster                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-JIT/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_process    | 60.3 ms                                                                                                           | 55.8 ms: 1.08x faster                                                                                                 |
| unpickle_pure_python | 221 us                                                                                                            | 205 us: 1.08x faster                                                                                                  |
| tomli_loads          | 1.98 sec                                                                                                          | 1.84 sec: 1.07x faster                                                                                                |
| xml_etree_generate   | 85.2 ms                                                                                                           | 79.8 ms: 1.07x faster                                                                                                 |
| pickle_pure_python   | 322 us                                                                                                            | 312 us: 1.03x faster                                                                                                  |
| xml_etree_iterparse  | 92.9 ms                                                                                                           | 91.1 ms: 1.02x faster                                                                                                 |
| pickle               | 12.3 us                                                                                                           | 12.1 us: 1.02x faster                                                                                                 |
| xml_etree_parse      | 131 ms                                                                                                            | 130 ms: 1.01x faster                                                                                                  |
| unpickle_list        | 4.82 us                                                                                                           | 4.79 us: 1.01x faster                                                                                                 |
| json_dumps           | 11.3 ms                                                                                                           | 11.4 ms: 1.01x slower                                                                                                 |
| pickle_dict          | 30.3 us                                                                                                           | 30.8 us: 1.02x slower                                                                                                 |
| pickle_list          | 4.92 us                                                                                                           | 5.00 us: 1.02x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                             | 1.02x faster                                                                                                          |

Benchmark hidden because not significant (2): unpickle, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-JIT/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 14.9 ms                                                                                                           | 15.0 ms: 1.00x slower                                                                                                 |
| python_startup_no_site | 8.61 ms                                                                                                           | 8.65 ms: 1.00x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                             | 1.00x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-JIT/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| genshi_text     | 21.9 ms                                                                                                           | 20.7 ms: 1.06x faster                                                                                                 |
| mako            | 12.1 ms                                                                                                           | 11.5 ms: 1.06x faster                                                                                                 |
| django_template | 36.1 ms                                                                                                           | 35.0 ms: 1.03x faster                                                                                                 |
| genshi_xml      | 50.5 ms                                                                                                           | 49.3 ms: 1.02x faster                                                                                                 |
| Geometric mean  | (ref)                                                                                                             | 1.04x faster                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-JIT/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| richards                   | 43.6 ms                                                                                                           | 34.9 ms: 1.25x faster                                                                                                 |
| richards_super             | 50.0 ms                                                                                                           | 40.7 ms: 1.23x faster                                                                                                 |
| nbody                      | 98.6 ms                                                                                                           | 82.7 ms: 1.19x faster                                                                                                 |
| scimark_fft                | 332 ms                                                                                                            | 285 ms: 1.17x faster                                                                                                  |
| pidigits                   | 210 ms                                                                                                            | 192 ms: 1.10x faster                                                                                                  |
| generators                 | 29.7 ms                                                                                                           | 27.3 ms: 1.09x faster                                                                                                 |
| float                      | 72.2 ms                                                                                                           | 66.3 ms: 1.09x faster                                                                                                 |
| async_tree_cpu_io_mixed_tg | 524 ms                                                                                                            | 485 ms: 1.08x faster                                                                                                  |
| xml_etree_process          | 60.3 ms                                                                                                           | 55.8 ms: 1.08x faster                                                                                                 |
| deltablue                  | 3.15 ms                                                                                                           | 2.92 ms: 1.08x faster                                                                                                 |
| unpickle_pure_python       | 221 us                                                                                                            | 205 us: 1.08x faster                                                                                                  |
| tomli_loads                | 1.98 sec                                                                                                          | 1.84 sec: 1.07x faster                                                                                                |
| async_tree_cpu_io_mixed    | 535 ms                                                                                                            | 500 ms: 1.07x faster                                                                                                  |
| xml_etree_generate         | 85.2 ms                                                                                                           | 79.8 ms: 1.07x faster                                                                                                 |
| deepcopy_reduce            | 2.74 us                                                                                                           | 2.59 us: 1.06x faster                                                                                                 |
| genshi_text                | 21.9 ms                                                                                                           | 20.7 ms: 1.06x faster                                                                                                 |
| mako                       | 12.1 ms                                                                                                           | 11.5 ms: 1.06x faster                                                                                                 |
| fannkuch                   | 401 ms                                                                                                            | 380 ms: 1.06x faster                                                                                                  |
| spectral_norm              | 92.8 ms                                                                                                           | 88.0 ms: 1.05x faster                                                                                                 |
| telco                      | 7.50 ms                                                                                                           | 7.12 ms: 1.05x faster                                                                                                 |
| deepcopy                   | 264 us                                                                                                            | 252 us: 1.05x faster                                                                                                  |
| coroutines                 | 23.6 ms                                                                                                           | 22.7 ms: 1.04x faster                                                                                                 |
| logging_simple             | 6.12 us                                                                                                           | 5.88 us: 1.04x faster                                                                                                 |
| scimark_monte_carlo        | 66.4 ms                                                                                                           | 64.0 ms: 1.04x faster                                                                                                 |
| regex_effbot               | 2.82 ms                                                                                                           | 2.72 ms: 1.04x faster                                                                                                 |
| regex_dna                  | 181 ms                                                                                                            | 175 ms: 1.04x faster                                                                                                  |
| sqlite_synth               | 2.20 us                                                                                                           | 2.13 us: 1.03x faster                                                                                                 |
| pickle_pure_python         | 322 us                                                                                                            | 312 us: 1.03x faster                                                                                                  |
| django_template            | 36.1 ms                                                                                                           | 35.0 ms: 1.03x faster                                                                                                 |
| bpe_tokeniser              | 4.35 sec                                                                                                          | 4.23 sec: 1.03x faster                                                                                                |
| logging_format             | 6.77 us                                                                                                           | 6.57 us: 1.03x faster                                                                                                 |
| scimark_sor                | 115 ms                                                                                                            | 112 ms: 1.03x faster                                                                                                  |
| async_tree_memoization     | 321 ms                                                                                                            | 312 ms: 1.03x faster                                                                                                  |
| async_tree_none_tg         | 261 ms                                                                                                            | 253 ms: 1.03x faster                                                                                                  |
| regex_v8                   | 22.3 ms                                                                                                           | 21.7 ms: 1.03x faster                                                                                                 |
| async_tree_memoization_tg  | 311 ms                                                                                                            | 303 ms: 1.03x faster                                                                                                  |
| scimark_sparse_mat_mult    | 4.53 ms                                                                                                           | 4.42 ms: 1.03x faster                                                                                                 |
| async_tree_io              | 632 ms                                                                                                            | 616 ms: 1.03x faster                                                                                                  |
| genshi_xml                 | 50.5 ms                                                                                                           | 49.3 ms: 1.02x faster                                                                                                 |
| async_tree_none            | 279 ms                                                                                                            | 272 ms: 1.02x faster                                                                                                  |
| pyflate                    | 418 ms                                                                                                            | 408 ms: 1.02x faster                                                                                                  |
| typing_runtime_protocols   | 159 us                                                                                                            | 156 us: 1.02x faster                                                                                                  |
| thrift                     | 786 us                                                                                                            | 771 us: 1.02x faster                                                                                                  |
| xml_etree_iterparse        | 92.9 ms                                                                                                           | 91.1 ms: 1.02x faster                                                                                                 |
| pickle                     | 12.3 us                                                                                                           | 12.1 us: 1.02x faster                                                                                                 |
| nqueens                    | 81.8 ms                                                                                                           | 80.4 ms: 1.02x faster                                                                                                 |
| sqlglot_v2_transpile       | 1.61 ms                                                                                                           | 1.58 ms: 1.02x faster                                                                                                 |
| async_tree_io_tg           | 641 ms                                                                                                            | 630 ms: 1.02x faster                                                                                                  |
| sqlglot_v2_parse           | 1.30 ms                                                                                                           | 1.28 ms: 1.02x faster                                                                                                 |
| raytrace                   | 267 ms                                                                                                            | 263 ms: 1.02x faster                                                                                                  |
| create_gc_cycles           | 1.87 ms                                                                                                           | 1.84 ms: 1.01x faster                                                                                                 |
| deepcopy_memo              | 30.3 us                                                                                                           | 30.0 us: 1.01x faster                                                                                                 |
| chaos                      | 57.8 ms                                                                                                           | 57.1 ms: 1.01x faster                                                                                                 |
| shortest_path              | 445 ms                                                                                                            | 440 ms: 1.01x faster                                                                                                  |
| sqlglot_v2_normalize       | 104 ms                                                                                                            | 102 ms: 1.01x faster                                                                                                  |
| xml_etree_parse            | 131 ms                                                                                                            | 130 ms: 1.01x faster                                                                                                  |
| regex_compile              | 128 ms                                                                                                            | 127 ms: 1.01x faster                                                                                                  |
| unpickle_list              | 4.82 us                                                                                                           | 4.79 us: 1.01x faster                                                                                                 |
| meteor_contest             | 103 ms                                                                                                            | 102 ms: 1.01x faster                                                                                                  |
| coverage                   | 79.5 ms                                                                                                           | 79.1 ms: 1.01x faster                                                                                                 |
| python_startup             | 14.9 ms                                                                                                           | 15.0 ms: 1.00x slower                                                                                                 |
| python_startup_no_site     | 8.61 ms                                                                                                           | 8.65 ms: 1.00x slower                                                                                                 |
| crypto_pyaes               | 70.9 ms                                                                                                           | 71.4 ms: 1.01x slower                                                                                                 |
| sympy_str                  | 276 ms                                                                                                            | 278 ms: 1.01x slower                                                                                                  |
| many_optionals             | 1.04 ms                                                                                                           | 1.06 ms: 1.01x slower                                                                                                 |
| 2to3                       | 257 ms                                                                                                            | 260 ms: 1.01x slower                                                                                                  |
| json_dumps                 | 11.3 ms                                                                                                           | 11.4 ms: 1.01x slower                                                                                                 |
| docutils                   | 2.60 sec                                                                                                          | 2.64 sec: 1.02x slower                                                                                                |
| pickle_dict                | 30.3 us                                                                                                           | 30.8 us: 1.02x slower                                                                                                 |
| pickle_list                | 4.92 us                                                                                                           | 5.00 us: 1.02x slower                                                                                                 |
| pycparser                  | 1.13 sec                                                                                                          | 1.15 sec: 1.02x slower                                                                                                |
| sympy_expand               | 466 ms                                                                                                            | 478 ms: 1.03x slower                                                                                                  |
| async_generators           | 337 ms                                                                                                            | 354 ms: 1.05x slower                                                                                                  |
| hexiom                     | 6.09 ms                                                                                                           | 6.61 ms: 1.08x slower                                                                                                 |
| pprint_safe_repr           | 733 ms                                                                                                            | 795 ms: 1.09x slower                                                                                                  |
| pprint_pformat             | 1.49 sec                                                                                                          | 1.62 sec: 1.09x slower                                                                                                |
| comprehensions             | 16.8 us                                                                                                           | 18.4 us: 1.09x slower                                                                                                 |
| go                         | 113 ms                                                                                                            | 128 ms: 1.13x slower                                                                                                  |
| unpack_sequence            | 52.7 ns                                                                                                           | 66.0 ns: 1.25x slower                                                                                                 |
| Geometric mean             | (ref)                                                                                                             | 1.02x faster                                                                                                          |

Benchmark hidden because not significant (24): pylint, k_core, connected_components, subparsers, pathlib, sympy_sum, gc_traversal, asyncio_websockets, sqlglot_v2_optimize, sqlalchemy_declarative, sphinx, scimark_lu, mdp, asyncio_tcp_ssl, asyncio_tcp, bench_thread_pool, logging_silent, sympy_integrate, json, unpickle, json_loads, dulwich_log, bench_mp_pool, sqlalchemy_imperative

- Geometric mean (including insignificant results): 1.023x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x