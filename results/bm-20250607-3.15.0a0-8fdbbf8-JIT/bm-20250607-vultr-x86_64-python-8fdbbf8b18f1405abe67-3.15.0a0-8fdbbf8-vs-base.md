# Results vs. base

- fork: python
- ref: 8fdbbf8b18f1405abe67
- machine: linux-x86_64
- commit hash: 8fdbbf8
- commit date: 2025-06-07
- overall geometric mean: 1.012x faster
- HPT reliability: 65.41%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250607-3.15.0a0-8fdbbf8/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json | results/bm-20250607-3.15.0a0-8fdbbf8-JIT/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 250 ms                                                                                                          | 255 ms: 1.02x slower                                                                                                |
| docutils       | 2.54 sec                                                                                                        | 2.58 sec: 1.01x slower                                                                                              |
| Geometric mean | (ref)                                                                                                           | 1.01x slower                                                                                                        |

Benchmark hidden because not significant (2): html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250607-3.15.0a0-8fdbbf8/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json | results/bm-20250607-3.15.0a0-8fdbbf8-JIT/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 521 ms                                                                                                          | 502 ms: 1.04x faster                                                                                                |
| async_tree_cpu_io_mixed_tg | 514 ms                                                                                                          | 506 ms: 1.02x faster                                                                                                |
| coroutines                 | 23.1 ms                                                                                                         | 23.0 ms: 1.00x faster                                                                                               |
| async_tree_none_tg         | 251 ms                                                                                                          | 254 ms: 1.01x slower                                                                                                |
| async_tree_memoization     | 307 ms                                                                                                          | 311 ms: 1.01x slower                                                                                                |
| async_tree_memoization_tg  | 306 ms                                                                                                          | 312 ms: 1.02x slower                                                                                                |
| async_generators           | 340 ms                                                                                                          | 349 ms: 1.03x slower                                                                                                |
| async_tree_io              | 593 ms                                                                                                          | 614 ms: 1.04x slower                                                                                                |
| Geometric mean             | (ref)                                                                                                           | 1.00x slower                                                                                                        |

Benchmark hidden because not significant (5): async_tree_none, asyncio_tcp_ssl, asyncio_websockets, asyncio_tcp, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250607-3.15.0a0-8fdbbf8/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json | results/bm-20250607-3.15.0a0-8fdbbf8-JIT/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| float          | 71.8 ms                                                                                                         | 64.2 ms: 1.12x faster                                                                                               |
| nbody          | 87.5 ms                                                                                                         | 85.1 ms: 1.03x faster                                                                                               |
| pidigits       | 197 ms                                                                                                          | 208 ms: 1.05x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.03x faster                                                                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250607-3.15.0a0-8fdbbf8/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json | results/bm-20250607-3.15.0a0-8fdbbf8-JIT/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| regex_effbot   | 2.88 ms                                                                                                         | 2.60 ms: 1.11x faster                                                                                               |
| regex_v8       | 23.0 ms                                                                                                         | 21.5 ms: 1.07x faster                                                                                               |
| regex_dna      | 176 ms                                                                                                          | 168 ms: 1.04x faster                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.06x faster                                                                                                        |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250607-3.15.0a0-8fdbbf8/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json | results/bm-20250607-3.15.0a0-8fdbbf8-JIT/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| unpickle_pure_python | 208 us                                                                                                          | 191 us: 1.09x faster                                                                                                |
| pickle_dict          | 32.4 us                                                                                                         | 29.9 us: 1.08x faster                                                                                               |
| tomli_loads          | 1.95 sec                                                                                                        | 1.81 sec: 1.08x faster                                                                                              |
| xml_etree_process    | 58.5 ms                                                                                                         | 54.5 ms: 1.07x faster                                                                                               |
| xml_etree_generate   | 83.3 ms                                                                                                         | 78.4 ms: 1.06x faster                                                                                               |
| unpickle_list        | 5.00 us                                                                                                         | 4.76 us: 1.05x faster                                                                                               |
| pickle_list          | 5.14 us                                                                                                         | 4.91 us: 1.05x faster                                                                                               |
| json_loads           | 29.1 us                                                                                                         | 28.1 us: 1.03x faster                                                                                               |
| pickle               | 12.2 us                                                                                                         | 12.0 us: 1.01x faster                                                                                               |
| json_dumps           | 10.9 ms                                                                                                         | 10.8 ms: 1.01x faster                                                                                               |
| xml_etree_parse      | 133 ms                                                                                                          | 132 ms: 1.01x faster                                                                                                |
| unpickle             | 13.8 us                                                                                                         | 14.0 us: 1.01x slower                                                                                               |
| Geometric mean       | (ref)                                                                                                           | 1.04x faster                                                                                                        |

Benchmark hidden because not significant (2): xml_etree_iterparse, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark      | results/bm-20250607-3.15.0a0-8fdbbf8/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json | results/bm-20250607-3.15.0a0-8fdbbf8-JIT/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| python_startup | 12.6 ms                                                                                                         | 12.6 ms: 1.00x faster                                                                                               |
| Geometric mean | (ref)                                                                                                           | 1.00x faster                                                                                                        |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250607-3.15.0a0-8fdbbf8/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json | results/bm-20250607-3.15.0a0-8fdbbf8-JIT/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| mako            | 11.8 ms                                                                                                         | 11.1 ms: 1.06x faster                                                                                               |
| genshi_text     | 20.5 ms                                                                                                         | 20.4 ms: 1.01x faster                                                                                               |
| django_template | 34.8 ms                                                                                                         | 34.5 ms: 1.01x faster                                                                                               |
| Geometric mean  | (ref)                                                                                                           | 1.02x faster                                                                                                        |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | results/bm-20250607-3.15.0a0-8fdbbf8/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json | results/bm-20250607-3.15.0a0-8fdbbf8-JIT/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| richards                   | 41.1 ms                                                                                                         | 31.8 ms: 1.29x faster                                                                                               |
| richards_super             | 46.3 ms                                                                                                         | 36.4 ms: 1.27x faster                                                                                               |
| scimark_fft                | 340 ms                                                                                                          | 292 ms: 1.16x faster                                                                                                |
| deltablue                  | 3.23 ms                                                                                                         | 2.87 ms: 1.12x faster                                                                                               |
| float                      | 71.8 ms                                                                                                         | 64.2 ms: 1.12x faster                                                                                               |
| regex_effbot               | 2.88 ms                                                                                                         | 2.60 ms: 1.11x faster                                                                                               |
| spectral_norm              | 101 ms                                                                                                          | 92.1 ms: 1.10x faster                                                                                               |
| unpickle_pure_python       | 208 us                                                                                                          | 191 us: 1.09x faster                                                                                                |
| pickle_dict                | 32.4 us                                                                                                         | 29.9 us: 1.08x faster                                                                                               |
| tomli_loads                | 1.95 sec                                                                                                        | 1.81 sec: 1.08x faster                                                                                              |
| scimark_sparse_mat_mult    | 4.83 ms                                                                                                         | 4.48 ms: 1.08x faster                                                                                               |
| regex_v8                   | 23.0 ms                                                                                                         | 21.5 ms: 1.07x faster                                                                                               |
| xml_etree_process          | 58.5 ms                                                                                                         | 54.5 ms: 1.07x faster                                                                                               |
| mako                       | 11.8 ms                                                                                                         | 11.1 ms: 1.06x faster                                                                                               |
| xml_etree_generate         | 83.3 ms                                                                                                         | 78.4 ms: 1.06x faster                                                                                               |
| unpickle_list              | 5.00 us                                                                                                         | 4.76 us: 1.05x faster                                                                                               |
| pickle_list                | 5.14 us                                                                                                         | 4.91 us: 1.05x faster                                                                                               |
| regex_dna                  | 176 ms                                                                                                          | 168 ms: 1.04x faster                                                                                                |
| telco                      | 7.24 ms                                                                                                         | 6.98 ms: 1.04x faster                                                                                               |
| async_tree_cpu_io_mixed    | 521 ms                                                                                                          | 502 ms: 1.04x faster                                                                                                |
| json_loads                 | 29.1 us                                                                                                         | 28.1 us: 1.03x faster                                                                                               |
| bpe_tokeniser              | 4.16 sec                                                                                                        | 4.03 sec: 1.03x faster                                                                                              |
| scimark_sor                | 111 ms                                                                                                          | 108 ms: 1.03x faster                                                                                                |
| scimark_monte_carlo        | 62.0 ms                                                                                                         | 60.1 ms: 1.03x faster                                                                                               |
| json                       | 5.26 ms                                                                                                         | 5.11 ms: 1.03x faster                                                                                               |
| fannkuch                   | 378 ms                                                                                                          | 367 ms: 1.03x faster                                                                                                |
| nbody                      | 87.5 ms                                                                                                         | 85.1 ms: 1.03x faster                                                                                               |
| pyflate                    | 406 ms                                                                                                          | 395 ms: 1.03x faster                                                                                                |
| logging_simple             | 6.53 us                                                                                                         | 6.42 us: 1.02x faster                                                                                               |
| sqlite_synth               | 2.25 us                                                                                                         | 2.21 us: 1.02x faster                                                                                               |
| connected_components       | 400 ms                                                                                                          | 394 ms: 1.02x faster                                                                                                |
| async_tree_cpu_io_mixed_tg | 514 ms                                                                                                          | 506 ms: 1.02x faster                                                                                                |
| coverage                   | 82.8 ms                                                                                                         | 81.6 ms: 1.01x faster                                                                                               |
| deepcopy_reduce            | 2.67 us                                                                                                         | 2.64 us: 1.01x faster                                                                                               |
| pickle                     | 12.2 us                                                                                                         | 12.0 us: 1.01x faster                                                                                               |
| logging_format             | 7.32 us                                                                                                         | 7.23 us: 1.01x faster                                                                                               |
| chaos                      | 57.0 ms                                                                                                         | 56.4 ms: 1.01x faster                                                                                               |
| scimark_lu                 | 110 ms                                                                                                          | 109 ms: 1.01x faster                                                                                                |
| genshi_text                | 20.5 ms                                                                                                         | 20.4 ms: 1.01x faster                                                                                               |
| json_dumps                 | 10.9 ms                                                                                                         | 10.8 ms: 1.01x faster                                                                                               |
| xml_etree_parse            | 133 ms                                                                                                          | 132 ms: 1.01x faster                                                                                                |
| django_template            | 34.8 ms                                                                                                         | 34.5 ms: 1.01x faster                                                                                               |
| subparsers                 | 25.2 ms                                                                                                         | 25.0 ms: 1.01x faster                                                                                               |
| logging_silent             | 470 ns                                                                                                          | 468 ns: 1.01x faster                                                                                                |
| raytrace                   | 253 ms                                                                                                          | 251 ms: 1.00x faster                                                                                                |
| coroutines                 | 23.1 ms                                                                                                         | 23.0 ms: 1.00x faster                                                                                               |
| python_startup             | 12.6 ms                                                                                                         | 12.6 ms: 1.00x faster                                                                                               |
| mdp                        | 1.15 sec                                                                                                        | 1.16 sec: 1.00x slower                                                                                              |
| async_tree_none_tg         | 251 ms                                                                                                          | 254 ms: 1.01x slower                                                                                                |
| sqlglot_v2_optimize        | 49.7 ms                                                                                                         | 50.3 ms: 1.01x slower                                                                                               |
| sqlglot_v2_normalize       | 98.5 ms                                                                                                         | 99.6 ms: 1.01x slower                                                                                               |
| async_tree_memoization     | 307 ms                                                                                                          | 311 ms: 1.01x slower                                                                                                |
| unpickle                   | 13.8 us                                                                                                         | 14.0 us: 1.01x slower                                                                                               |
| docutils                   | 2.54 sec                                                                                                        | 2.58 sec: 1.01x slower                                                                                              |
| create_gc_cycles           | 1.89 ms                                                                                                         | 1.92 ms: 1.01x slower                                                                                               |
| 2to3                       | 250 ms                                                                                                          | 255 ms: 1.02x slower                                                                                                |
| sympy_integrate            | 18.8 ms                                                                                                         | 19.1 ms: 1.02x slower                                                                                               |
| crypto_pyaes               | 67.3 ms                                                                                                         | 68.6 ms: 1.02x slower                                                                                               |
| dulwich_log                | 66.4 ms                                                                                                         | 67.7 ms: 1.02x slower                                                                                               |
| meteor_contest             | 98.7 ms                                                                                                         | 101 ms: 1.02x slower                                                                                                |
| async_tree_memoization_tg  | 306 ms                                                                                                          | 312 ms: 1.02x slower                                                                                                |
| generators                 | 27.7 ms                                                                                                         | 28.3 ms: 1.02x slower                                                                                               |
| many_optionals             | 1.04 ms                                                                                                         | 1.06 ms: 1.02x slower                                                                                               |
| sympy_str                  | 267 ms                                                                                                          | 274 ms: 1.02x slower                                                                                                |
| nqueens                    | 75.8 ms                                                                                                         | 77.7 ms: 1.02x slower                                                                                               |
| sqlglot_v2_transpile       | 1.49 ms                                                                                                         | 1.53 ms: 1.03x slower                                                                                               |
| async_generators           | 340 ms                                                                                                          | 349 ms: 1.03x slower                                                                                                |
| typing_runtime_protocols   | 153 us                                                                                                          | 158 us: 1.03x slower                                                                                                |
| async_tree_io              | 593 ms                                                                                                          | 614 ms: 1.04x slower                                                                                                |
| sqlglot_v2_parse           | 1.20 ms                                                                                                         | 1.24 ms: 1.04x slower                                                                                               |
| sympy_expand               | 450 ms                                                                                                          | 469 ms: 1.04x slower                                                                                                |
| pidigits                   | 197 ms                                                                                                          | 208 ms: 1.05x slower                                                                                                |
| gc_traversal               | 4.26 ms                                                                                                         | 4.50 ms: 1.06x slower                                                                                               |
| comprehensions             | 15.7 us                                                                                                         | 16.7 us: 1.06x slower                                                                                               |
| hexiom                     | 5.46 ms                                                                                                         | 6.07 ms: 1.11x slower                                                                                               |
| go                         | 105 ms                                                                                                          | 118 ms: 1.12x slower                                                                                                |
| pprint_safe_repr           | 763 ms                                                                                                          | 853 ms: 1.12x slower                                                                                                |
| pprint_pformat             | 1.57 sec                                                                                                        | 1.76 sec: 1.12x slower                                                                                              |
| unpack_sequence            | 41.8 ns                                                                                                         | 60.6 ns: 1.45x slower                                                                                               |
| Geometric mean             | (ref)                                                                                                           | 1.01x faster                                                                                                        |

Benchmark hidden because not significant (23): bench_mp_pool, genshi_xml, regex_compile, async_tree_none, deepcopy_memo, k_core, shortest_path, pathlib, python_startup_no_site, asyncio_tcp_ssl, asyncio_websockets, bench_thread_pool, asyncio_tcp, xml_etree_iterparse, pycparser, sympy_sum, deepcopy, html5lib, pickle_pure_python, sphinx, thrift, async_tree_io_tg, pylint

- Geometric mean (including insignificant results): 1.012x faster

# HPT report

- Reliability score: 65.41% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x