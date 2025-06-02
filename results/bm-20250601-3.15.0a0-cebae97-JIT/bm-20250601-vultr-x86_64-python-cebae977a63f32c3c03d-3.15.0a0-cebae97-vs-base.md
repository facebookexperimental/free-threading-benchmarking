# Results vs. base

- fork: python
- ref: cebae977a63f32c3c03d
- machine: linux-x86_64
- commit hash: cebae97
- commit date: 2025-06-01
- overall geometric mean: 1.394x faster
- HPT reliability: 99.64%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250601-3.15.0a0-cebae97/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json | results/bm-20250601-3.15.0a0-cebae97-JIT/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| docutils       | 2.56 sec                                                                                                        | 2.58 sec: 1.01x slower                                                                                              |
| html5lib       | 61.7 ms                                                                                                         | 62.2 ms: 1.01x slower                                                                                               |
| Geometric mean | (ref)                                                                                                           | 1.00x slower                                                                                                        |

Benchmark hidden because not significant (2): 2to3, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250601-3.15.0a0-cebae97/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json | results/bm-20250601-3.15.0a0-cebae97-JIT/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| coroutines                 | 23.9 ms                                                                                                         | 23.2 ms: 1.03x faster                                                                                               |
| asyncio_tcp                | 515 ms                                                                                                          | 502 ms: 1.03x faster                                                                                                |
| async_tree_memoization     | 316 ms                                                                                                          | 309 ms: 1.02x faster                                                                                                |
| async_tree_cpu_io_mixed    | 518 ms                                                                                                          | 508 ms: 1.02x faster                                                                                                |
| async_tree_cpu_io_mixed_tg | 507 ms                                                                                                          | 501 ms: 1.01x faster                                                                                                |
| asyncio_tcp_ssl            | 1.54 sec                                                                                                        | 1.52 sec: 1.01x faster                                                                                              |
| asyncio_websockets         | 519 ms                                                                                                          | 517 ms: 1.00x faster                                                                                                |
| async_tree_io              | 603 ms                                                                                                          | 613 ms: 1.02x slower                                                                                                |
| async_generators           | 342 ms                                                                                                          | 352 ms: 1.03x slower                                                                                                |
| Geometric mean             | (ref)                                                                                                           | 1.01x faster                                                                                                        |

Benchmark hidden because not significant (4): async_tree_none, async_tree_memoization_tg, async_tree_io_tg, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250601-3.15.0a0-cebae97/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json | results/bm-20250601-3.15.0a0-cebae97-JIT/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| float          | 72.4 ms                                                                                                         | 65.0 ms: 1.11x faster                                                                                               |
| nbody          | 88.3 ms                                                                                                         | 82.6 ms: 1.07x faster                                                                                               |
| pidigits       | 199 ms                                                                                                          | 194 ms: 1.03x faster                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.07x faster                                                                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250601-3.15.0a0-cebae97/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json | results/bm-20250601-3.15.0a0-cebae97-JIT/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| regex_effbot   | 2.55 ms                                                                                                         | 2.52 ms: 1.01x faster                                                                                               |
| regex_dna      | 166 ms                                                                                                          | 168 ms: 1.01x slower                                                                                                |
| regex_v8       | 21.0 ms                                                                                                         | 21.3 ms: 1.01x slower                                                                                               |
| Geometric mean | (ref)                                                                                                           | 1.00x slower                                                                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250601-3.15.0a0-cebae97/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json | results/bm-20250601-3.15.0a0-cebae97-JIT/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| xml_etree_process    | 58.7 ms                                                                                                         | 53.4 ms: 1.10x faster                                                                                               |
| unpickle_pure_python | 209 us                                                                                                          | 191 us: 1.10x faster                                                                                                |
| tomli_loads          | 1.95 sec                                                                                                        | 1.78 sec: 1.09x faster                                                                                              |
| xml_etree_generate   | 83.6 ms                                                                                                         | 77.9 ms: 1.07x faster                                                                                               |
| json_loads           | 29.2 us                                                                                                         | 28.0 us: 1.04x faster                                                                                               |
| xml_etree_iterparse  | 96.4 ms                                                                                                         | 92.3 ms: 1.04x faster                                                                                               |
| unpickle_list        | 5.03 us                                                                                                         | 4.87 us: 1.03x faster                                                                                               |
| xml_etree_parse      | 134 ms                                                                                                          | 131 ms: 1.03x faster                                                                                                |
| unpickle             | 14.2 us                                                                                                         | 13.9 us: 1.02x faster                                                                                               |
| pickle               | 12.5 us                                                                                                         | 12.5 us: 1.00x faster                                                                                               |
| pickle_pure_python   | 308 us                                                                                                          | 310 us: 1.01x slower                                                                                                |
| json_dumps           | 10.7 ms                                                                                                         | 10.9 ms: 1.02x slower                                                                                               |
| pickle_list          | 4.93 us                                                                                                         | 5.09 us: 1.03x slower                                                                                               |
| pickle_dict          | 31.5 us                                                                                                         | 32.8 us: 1.04x slower                                                                                               |
| Geometric mean       | (ref)                                                                                                           | 1.03x faster                                                                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250601-3.15.0a0-cebae97/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json | results/bm-20250601-3.15.0a0-cebae97-JIT/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| python_startup_no_site | 7.54 ms                                                                                                         | 7.31 ms: 1.03x faster                                                                                               |
| python_startup         | 12.8 ms                                                                                                         | 12.5 ms: 1.03x faster                                                                                               |
| Geometric mean         | (ref)                                                                                                           | 1.03x faster                                                                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250601-3.15.0a0-cebae97/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json | results/bm-20250601-3.15.0a0-cebae97-JIT/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| mako            | 11.9 ms                                                                                                         | 11.1 ms: 1.08x faster                                                                                               |
| genshi_text     | 20.8 ms                                                                                                         | 20.5 ms: 1.01x faster                                                                                               |
| django_template | 34.6 ms                                                                                                         | 34.9 ms: 1.01x slower                                                                                               |
| genshi_xml      | 48.0 ms                                                                                                         | 48.7 ms: 1.01x slower                                                                                               |
| Geometric mean  | (ref)                                                                                                           | 1.02x faster                                                                                                        |

All benchmarks:
===============

| Benchmark                  | results/bm-20250601-3.15.0a0-cebae97/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json | results/bm-20250601-3.15.0a0-cebae97-JIT/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| pprint_pformat             | 1.58 sec                                                                                                        | 1.38 us: 1145445.72x faster                                                                                         |
| pprint_safe_repr           | 773 ms                                                                                                          | 797 ns: 970326.94x faster                                                                                           |
| richards                   | 40.9 ms                                                                                                         | 32.2 ms: 1.27x faster                                                                                               |
| richards_super             | 46.5 ms                                                                                                         | 36.7 ms: 1.27x faster                                                                                               |
| scimark_fft                | 339 ms                                                                                                          | 289 ms: 1.17x faster                                                                                                |
| spectral_norm              | 102 ms                                                                                                          | 89.6 ms: 1.14x faster                                                                                               |
| deltablue                  | 3.31 ms                                                                                                         | 2.91 ms: 1.14x faster                                                                                               |
| float                      | 72.4 ms                                                                                                         | 65.0 ms: 1.11x faster                                                                                               |
| xml_etree_process          | 58.7 ms                                                                                                         | 53.4 ms: 1.10x faster                                                                                               |
| generators                 | 30.1 ms                                                                                                         | 27.4 ms: 1.10x faster                                                                                               |
| unpickle_pure_python       | 209 us                                                                                                          | 191 us: 1.10x faster                                                                                                |
| scimark_sparse_mat_mult    | 4.80 ms                                                                                                         | 4.40 ms: 1.09x faster                                                                                               |
| tomli_loads                | 1.95 sec                                                                                                        | 1.78 sec: 1.09x faster                                                                                              |
| mako                       | 11.9 ms                                                                                                         | 11.1 ms: 1.08x faster                                                                                               |
| xml_etree_generate         | 83.6 ms                                                                                                         | 77.9 ms: 1.07x faster                                                                                               |
| nbody                      | 88.3 ms                                                                                                         | 82.6 ms: 1.07x faster                                                                                               |
| create_gc_cycles           | 2.03 ms                                                                                                         | 1.90 ms: 1.07x faster                                                                                               |
| k_core                     | 2.14 sec                                                                                                        | 2.02 sec: 1.06x faster                                                                                              |
| shortest_path              | 456 ms                                                                                                          | 433 ms: 1.05x faster                                                                                                |
| connected_components       | 411 ms                                                                                                          | 390 ms: 1.05x faster                                                                                                |
| pyflate                    | 413 ms                                                                                                          | 393 ms: 1.05x faster                                                                                                |
| bpe_tokeniser              | 4.19 sec                                                                                                        | 4.00 sec: 1.05x faster                                                                                              |
| json_loads                 | 29.2 us                                                                                                         | 28.0 us: 1.04x faster                                                                                               |
| xml_etree_iterparse        | 96.4 ms                                                                                                         | 92.3 ms: 1.04x faster                                                                                               |
| json                       | 5.22 ms                                                                                                         | 5.05 ms: 1.03x faster                                                                                               |
| unpickle_list              | 5.03 us                                                                                                         | 4.87 us: 1.03x faster                                                                                               |
| coroutines                 | 23.9 ms                                                                                                         | 23.2 ms: 1.03x faster                                                                                               |
| sqlite_synth               | 2.23 us                                                                                                         | 2.17 us: 1.03x faster                                                                                               |
| python_startup_no_site     | 7.54 ms                                                                                                         | 7.31 ms: 1.03x faster                                                                                               |
| mdp                        | 1.20 sec                                                                                                        | 1.17 sec: 1.03x faster                                                                                              |
| bench_mp_pool              | 101 ms                                                                                                          | 98.3 ms: 1.03x faster                                                                                               |
| python_startup             | 12.8 ms                                                                                                         | 12.5 ms: 1.03x faster                                                                                               |
| pidigits                   | 199 ms                                                                                                          | 194 ms: 1.03x faster                                                                                                |
| telco                      | 7.31 ms                                                                                                         | 7.13 ms: 1.03x faster                                                                                               |
| xml_etree_parse            | 134 ms                                                                                                          | 131 ms: 1.03x faster                                                                                                |
| asyncio_tcp                | 515 ms                                                                                                          | 502 ms: 1.03x faster                                                                                                |
| unpickle                   | 14.2 us                                                                                                         | 13.9 us: 1.02x faster                                                                                               |
| async_tree_memoization     | 316 ms                                                                                                          | 309 ms: 1.02x faster                                                                                                |
| async_tree_cpu_io_mixed    | 518 ms                                                                                                          | 508 ms: 1.02x faster                                                                                                |
| fannkuch                   | 375 ms                                                                                                          | 370 ms: 1.01x faster                                                                                                |
| scimark_monte_carlo        | 61.4 ms                                                                                                         | 60.5 ms: 1.01x faster                                                                                               |
| deepcopy                   | 253 us                                                                                                          | 249 us: 1.01x faster                                                                                                |
| genshi_text                | 20.8 ms                                                                                                         | 20.5 ms: 1.01x faster                                                                                               |
| regex_effbot               | 2.55 ms                                                                                                         | 2.52 ms: 1.01x faster                                                                                               |
| async_tree_cpu_io_mixed_tg | 507 ms                                                                                                          | 501 ms: 1.01x faster                                                                                                |
| asyncio_tcp_ssl            | 1.54 sec                                                                                                        | 1.52 sec: 1.01x faster                                                                                              |
| coverage                   | 82.7 ms                                                                                                         | 81.9 ms: 1.01x faster                                                                                               |
| deepcopy_reduce            | 2.69 us                                                                                                         | 2.66 us: 1.01x faster                                                                                               |
| scimark_lu                 | 110 ms                                                                                                          | 110 ms: 1.01x faster                                                                                                |
| logging_silent             | 469 ns                                                                                                          | 465 ns: 1.01x faster                                                                                                |
| pickle                     | 12.5 us                                                                                                         | 12.5 us: 1.00x faster                                                                                               |
| asyncio_websockets         | 519 ms                                                                                                          | 517 ms: 1.00x faster                                                                                                |
| sqlglot_v2_normalize       | 98.5 ms                                                                                                         | 99.0 ms: 1.00x slower                                                                                               |
| pickle_pure_python         | 308 us                                                                                                          | 310 us: 1.01x slower                                                                                                |
| raytrace                   | 253 ms                                                                                                          | 254 ms: 1.01x slower                                                                                                |
| deepcopy_memo              | 28.9 us                                                                                                         | 29.1 us: 1.01x slower                                                                                               |
| docutils                   | 2.56 sec                                                                                                        | 2.58 sec: 1.01x slower                                                                                              |
| sqlglot_v2_optimize        | 49.7 ms                                                                                                         | 50.0 ms: 1.01x slower                                                                                               |
| django_template            | 34.6 ms                                                                                                         | 34.9 ms: 1.01x slower                                                                                               |
| sympy_str                  | 268 ms                                                                                                          | 271 ms: 1.01x slower                                                                                                |
| html5lib                   | 61.7 ms                                                                                                         | 62.2 ms: 1.01x slower                                                                                               |
| sympy_integrate            | 18.9 ms                                                                                                         | 19.1 ms: 1.01x slower                                                                                               |
| logging_simple             | 6.62 us                                                                                                         | 6.69 us: 1.01x slower                                                                                               |
| pycparser                  | 1.13 sec                                                                                                        | 1.14 sec: 1.01x slower                                                                                              |
| regex_dna                  | 166 ms                                                                                                          | 168 ms: 1.01x slower                                                                                                |
| regex_v8                   | 21.0 ms                                                                                                         | 21.3 ms: 1.01x slower                                                                                               |
| genshi_xml                 | 48.0 ms                                                                                                         | 48.7 ms: 1.01x slower                                                                                               |
| async_tree_io              | 603 ms                                                                                                          | 613 ms: 1.02x slower                                                                                                |
| dulwich_log                | 66.5 ms                                                                                                         | 67.7 ms: 1.02x slower                                                                                               |
| sqlglot_v2_parse           | 1.22 ms                                                                                                         | 1.24 ms: 1.02x slower                                                                                               |
| json_dumps                 | 10.7 ms                                                                                                         | 10.9 ms: 1.02x slower                                                                                               |
| many_optionals             | 1.05 ms                                                                                                         | 1.07 ms: 1.02x slower                                                                                               |
| crypto_pyaes               | 68.2 ms                                                                                                         | 69.8 ms: 1.02x slower                                                                                               |
| sqlglot_v2_transpile       | 1.51 ms                                                                                                         | 1.55 ms: 1.03x slower                                                                                               |
| async_generators           | 342 ms                                                                                                          | 352 ms: 1.03x slower                                                                                                |
| sympy_expand               | 450 ms                                                                                                          | 464 ms: 1.03x slower                                                                                                |
| nqueens                    | 75.9 ms                                                                                                         | 78.3 ms: 1.03x slower                                                                                               |
| pickle_list                | 4.93 us                                                                                                         | 5.09 us: 1.03x slower                                                                                               |
| pickle_dict                | 31.5 us                                                                                                         | 32.8 us: 1.04x slower                                                                                               |
| comprehensions             | 15.7 us                                                                                                         | 16.7 us: 1.07x slower                                                                                               |
| hexiom                     | 5.63 ms                                                                                                         | 6.26 ms: 1.11x slower                                                                                               |
| go                         | 105 ms                                                                                                          | 120 ms: 1.14x slower                                                                                                |
| unpack_sequence            | 41.3 ns                                                                                                         | 61.7 ns: 1.50x slower                                                                                               |
| Geometric mean             | (ref)                                                                                                           | 1.34x faster                                                                                                        |

Benchmark hidden because not significant (18): async_tree_none, pylint, sphinx, subparsers, async_tree_memoization_tg, async_tree_io_tg, gc_traversal, sympy_sum, pathlib, meteor_contest, chaos, thrift, bench_thread_pool, typing_runtime_protocols, async_tree_none_tg, scimark_sor, 2to3, logging_format
Ignored benchmarks (1) of results/bm-20250601-3.15.0a0-cebae97/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json: regex_compile

- Geometric mean (including insignificant results): 1.394x faster

# HPT report

- Reliability score: 99.64% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x