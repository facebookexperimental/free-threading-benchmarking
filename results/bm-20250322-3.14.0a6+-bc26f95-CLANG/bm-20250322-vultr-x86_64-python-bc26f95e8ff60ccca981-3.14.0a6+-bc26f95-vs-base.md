# Results vs. base

- fork: python
- ref: bc26f95e8ff60ccca981
- machine: linux-x86_64
- commit hash: bc26f95
- commit date: 2025-03-22
- overall geometric mean: 1.069x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-CLANG/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 257 ms                                                                                                            | 244 ms: 1.05x faster                                                                                                    |
| docutils       | 2.60 sec                                                                                                          | 2.51 sec: 1.04x faster                                                                                                  |
| sphinx         | 1.01 sec                                                                                                          | 957 ms: 1.05x faster                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.05x faster                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-CLANG/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 524 ms                                                                                                            | 449 ms: 1.17x faster                                                                                                    |
| coroutines                 | 23.6 ms                                                                                                           | 20.6 ms: 1.15x faster                                                                                                   |
| async_tree_cpu_io_mixed    | 535 ms                                                                                                            | 468 ms: 1.14x faster                                                                                                    |
| async_tree_none            | 279 ms                                                                                                            | 256 ms: 1.09x faster                                                                                                    |
| async_tree_memoization_tg  | 311 ms                                                                                                            | 285 ms: 1.09x faster                                                                                                    |
| async_tree_none_tg         | 261 ms                                                                                                            | 239 ms: 1.09x faster                                                                                                    |
| async_tree_memoization     | 321 ms                                                                                                            | 295 ms: 1.09x faster                                                                                                    |
| async_tree_io              | 632 ms                                                                                                            | 583 ms: 1.08x faster                                                                                                    |
| async_generators           | 337 ms                                                                                                            | 315 ms: 1.07x faster                                                                                                    |
| async_tree_io_tg           | 641 ms                                                                                                            | 601 ms: 1.07x faster                                                                                                    |
| asyncio_tcp                | 499 ms                                                                                                            | 492 ms: 1.01x faster                                                                                                    |
| asyncio_tcp_ssl            | 1.51 sec                                                                                                          | 1.50 sec: 1.01x faster                                                                                                  |
| Geometric mean             | (ref)                                                                                                             | 1.08x faster                                                                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-CLANG/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| nbody          | 98.6 ms                                                                                                           | 79.6 ms: 1.24x faster                                                                                                   |
| pidigits       | 210 ms                                                                                                            | 191 ms: 1.10x faster                                                                                                    |
| float          | 72.2 ms                                                                                                           | 69.4 ms: 1.04x faster                                                                                                   |
| Geometric mean | (ref)                                                                                                             | 1.12x faster                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-CLANG/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_compile  | 128 ms                                                                                                            | 123 ms: 1.04x faster                                                                                                    |
| regex_dna      | 181 ms                                                                                                            | 185 ms: 1.02x slower                                                                                                    |
| regex_effbot   | 2.82 ms                                                                                                           | 3.10 ms: 1.10x slower                                                                                                   |
| Geometric mean | (ref)                                                                                                             | 1.02x slower                                                                                                            |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-CLANG/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| unpickle_list        | 4.82 us                                                                                                           | 4.24 us: 1.14x faster                                                                                                   |
| tomli_loads          | 1.98 sec                                                                                                          | 1.80 sec: 1.10x faster                                                                                                  |
| xml_etree_process    | 60.3 ms                                                                                                           | 54.7 ms: 1.10x faster                                                                                                   |
| pickle_pure_python   | 322 us                                                                                                            | 294 us: 1.10x faster                                                                                                    |
| unpickle_pure_python | 221 us                                                                                                            | 202 us: 1.09x faster                                                                                                    |
| json_loads           | 27.9 us                                                                                                           | 26.1 us: 1.07x faster                                                                                                   |
| xml_etree_generate   | 85.2 ms                                                                                                           | 80.0 ms: 1.06x faster                                                                                                   |
| pickle               | 12.3 us                                                                                                           | 12.2 us: 1.01x faster                                                                                                   |
| pickle_list          | 4.92 us                                                                                                           | 4.97 us: 1.01x slower                                                                                                   |
| xml_etree_iterparse  | 92.9 ms                                                                                                           | 93.9 ms: 1.01x slower                                                                                                   |
| json_dumps           | 11.3 ms                                                                                                           | 11.5 ms: 1.02x slower                                                                                                   |
| pickle_dict          | 30.3 us                                                                                                           | 31.5 us: 1.04x slower                                                                                                   |
| xml_etree_parse      | 131 ms                                                                                                            | 144 ms: 1.10x slower                                                                                                    |
| Geometric mean       | (ref)                                                                                                             | 1.03x faster                                                                                                            |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-CLANG/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 14.9 ms                                                                                                           | 14.9 ms: 1.00x faster                                                                                                   |
| python_startup_no_site | 8.61 ms                                                                                                           | 8.60 ms: 1.00x faster                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.00x faster                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-CLANG/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_text     | 21.9 ms                                                                                                           | 19.4 ms: 1.13x faster                                                                                                   |
| django_template | 36.1 ms                                                                                                           | 32.4 ms: 1.11x faster                                                                                                   |
| genshi_xml      | 50.5 ms                                                                                                           | 45.6 ms: 1.11x faster                                                                                                   |
| mako            | 12.1 ms                                                                                                           | 11.3 ms: 1.07x faster                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.10x faster                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-CLANG/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| nbody                      | 98.6 ms                                                                                                           | 79.6 ms: 1.24x faster                                                                                                   |
| spectral_norm              | 92.8 ms                                                                                                           | 78.3 ms: 1.18x faster                                                                                                   |
| scimark_fft                | 332 ms                                                                                                            | 282 ms: 1.17x faster                                                                                                    |
| deepcopy_reduce            | 2.74 us                                                                                                           | 2.34 us: 1.17x faster                                                                                                   |
| scimark_monte_carlo        | 66.4 ms                                                                                                           | 56.6 ms: 1.17x faster                                                                                                   |
| logging_silent             | 97.7 ns                                                                                                           | 83.6 ns: 1.17x faster                                                                                                   |
| async_tree_cpu_io_mixed_tg | 524 ms                                                                                                            | 449 ms: 1.17x faster                                                                                                    |
| deepcopy                   | 264 us                                                                                                            | 229 us: 1.16x faster                                                                                                    |
| scimark_sor                | 115 ms                                                                                                            | 100 ms: 1.15x faster                                                                                                    |
| coroutines                 | 23.6 ms                                                                                                           | 20.6 ms: 1.15x faster                                                                                                   |
| async_tree_cpu_io_mixed    | 535 ms                                                                                                            | 468 ms: 1.14x faster                                                                                                    |
| comprehensions             | 16.8 us                                                                                                           | 14.7 us: 1.14x faster                                                                                                   |
| scimark_lu                 | 114 ms                                                                                                            | 100 ms: 1.14x faster                                                                                                    |
| unpickle_list              | 4.82 us                                                                                                           | 4.24 us: 1.14x faster                                                                                                   |
| chaos                      | 57.8 ms                                                                                                           | 50.9 ms: 1.13x faster                                                                                                   |
| nqueens                    | 81.8 ms                                                                                                           | 72.2 ms: 1.13x faster                                                                                                   |
| richards                   | 43.6 ms                                                                                                           | 38.6 ms: 1.13x faster                                                                                                   |
| genshi_text                | 21.9 ms                                                                                                           | 19.4 ms: 1.13x faster                                                                                                   |
| raytrace                   | 267 ms                                                                                                            | 237 ms: 1.13x faster                                                                                                    |
| scimark_sparse_mat_mult    | 4.53 ms                                                                                                           | 4.04 ms: 1.12x faster                                                                                                   |
| richards_super             | 50.0 ms                                                                                                           | 44.8 ms: 1.12x faster                                                                                                   |
| django_template            | 36.1 ms                                                                                                           | 32.4 ms: 1.11x faster                                                                                                   |
| generators                 | 29.7 ms                                                                                                           | 26.7 ms: 1.11x faster                                                                                                   |
| hexiom                     | 6.09 ms                                                                                                           | 5.49 ms: 1.11x faster                                                                                                   |
| genshi_xml                 | 50.5 ms                                                                                                           | 45.6 ms: 1.11x faster                                                                                                   |
| sqlglot_v2_parse           | 1.30 ms                                                                                                           | 1.17 ms: 1.11x faster                                                                                                   |
| deepcopy_memo              | 30.3 us                                                                                                           | 27.5 us: 1.10x faster                                                                                                   |
| tomli_loads                | 1.98 sec                                                                                                          | 1.80 sec: 1.10x faster                                                                                                  |
| xml_etree_process          | 60.3 ms                                                                                                           | 54.7 ms: 1.10x faster                                                                                                   |
| sqlglot_v2_transpile       | 1.61 ms                                                                                                           | 1.46 ms: 1.10x faster                                                                                                   |
| pidigits                   | 210 ms                                                                                                            | 191 ms: 1.10x faster                                                                                                    |
| pickle_pure_python         | 322 us                                                                                                            | 294 us: 1.10x faster                                                                                                    |
| typing_runtime_protocols   | 159 us                                                                                                            | 145 us: 1.10x faster                                                                                                    |
| logging_simple             | 6.12 us                                                                                                           | 5.58 us: 1.10x faster                                                                                                   |
| deltablue                  | 3.15 ms                                                                                                           | 2.88 ms: 1.10x faster                                                                                                   |
| unpickle_pure_python       | 221 us                                                                                                            | 202 us: 1.09x faster                                                                                                    |
| async_tree_none            | 279 ms                                                                                                            | 256 ms: 1.09x faster                                                                                                    |
| go                         | 113 ms                                                                                                            | 104 ms: 1.09x faster                                                                                                    |
| async_tree_memoization_tg  | 311 ms                                                                                                            | 285 ms: 1.09x faster                                                                                                    |
| async_tree_none_tg         | 261 ms                                                                                                            | 239 ms: 1.09x faster                                                                                                    |
| thrift                     | 786 us                                                                                                            | 722 us: 1.09x faster                                                                                                    |
| telco                      | 7.50 ms                                                                                                           | 6.89 ms: 1.09x faster                                                                                                   |
| async_tree_memoization     | 321 ms                                                                                                            | 295 ms: 1.09x faster                                                                                                    |
| pyflate                    | 418 ms                                                                                                            | 385 ms: 1.08x faster                                                                                                    |
| async_tree_io              | 632 ms                                                                                                            | 583 ms: 1.08x faster                                                                                                    |
| coverage                   | 79.5 ms                                                                                                           | 73.9 ms: 1.08x faster                                                                                                   |
| sympy_integrate            | 19.7 ms                                                                                                           | 18.4 ms: 1.07x faster                                                                                                   |
| sqlglot_v2_normalize       | 104 ms                                                                                                            | 96.6 ms: 1.07x faster                                                                                                   |
| logging_format             | 6.77 us                                                                                                           | 6.32 us: 1.07x faster                                                                                                   |
| mako                       | 12.1 ms                                                                                                           | 11.3 ms: 1.07x faster                                                                                                   |
| sqlglot_v2_optimize        | 52.4 ms                                                                                                           | 49.0 ms: 1.07x faster                                                                                                   |
| async_generators           | 337 ms                                                                                                            | 315 ms: 1.07x faster                                                                                                    |
| json_loads                 | 27.9 us                                                                                                           | 26.1 us: 1.07x faster                                                                                                   |
| async_tree_io_tg           | 641 ms                                                                                                            | 601 ms: 1.07x faster                                                                                                    |
| sympy_expand               | 466 ms                                                                                                            | 437 ms: 1.07x faster                                                                                                    |
| sympy_sum                  | 157 ms                                                                                                            | 147 ms: 1.07x faster                                                                                                    |
| xml_etree_generate         | 85.2 ms                                                                                                           | 80.0 ms: 1.06x faster                                                                                                   |
| sympy_str                  | 276 ms                                                                                                            | 260 ms: 1.06x faster                                                                                                    |
| pathlib                    | 19.4 ms                                                                                                           | 18.3 ms: 1.06x faster                                                                                                   |
| sqlalchemy_imperative      | 19.9 ms                                                                                                           | 18.7 ms: 1.06x faster                                                                                                   |
| bench_thread_pool          | 1.05 ms                                                                                                           | 998 us: 1.06x faster                                                                                                    |
| fannkuch                   | 401 ms                                                                                                            | 381 ms: 1.05x faster                                                                                                    |
| 2to3                       | 257 ms                                                                                                            | 244 ms: 1.05x faster                                                                                                    |
| pylint                     | 284 ms                                                                                                            | 270 ms: 1.05x faster                                                                                                    |
| pycparser                  | 1.13 sec                                                                                                          | 1.07 sec: 1.05x faster                                                                                                  |
| bpe_tokeniser              | 4.35 sec                                                                                                          | 4.14 sec: 1.05x faster                                                                                                  |
| sphinx                     | 1.01 sec                                                                                                          | 957 ms: 1.05x faster                                                                                                    |
| pprint_safe_repr           | 733 ms                                                                                                            | 698 ms: 1.05x faster                                                                                                    |
| pprint_pformat             | 1.49 sec                                                                                                          | 1.42 sec: 1.05x faster                                                                                                  |
| crypto_pyaes               | 70.9 ms                                                                                                           | 67.8 ms: 1.05x faster                                                                                                   |
| many_optionals             | 1.04 ms                                                                                                           | 999 us: 1.04x faster                                                                                                    |
| regex_compile              | 128 ms                                                                                                            | 123 ms: 1.04x faster                                                                                                    |
| unpack_sequence            | 52.7 ns                                                                                                           | 50.7 ns: 1.04x faster                                                                                                   |
| float                      | 72.2 ms                                                                                                           | 69.4 ms: 1.04x faster                                                                                                   |
| sqlalchemy_declarative     | 130 ms                                                                                                            | 125 ms: 1.04x faster                                                                                                    |
| docutils                   | 2.60 sec                                                                                                          | 2.51 sec: 1.04x faster                                                                                                  |
| subparsers                 | 22.5 ms                                                                                                           | 21.7 ms: 1.04x faster                                                                                                   |
| k_core                     | 2.06 sec                                                                                                          | 1.99 sec: 1.03x faster                                                                                                  |
| bench_mp_pool              | 89.5 ms                                                                                                           | 87.4 ms: 1.02x faster                                                                                                   |
| dulwich_log                | 66.9 ms                                                                                                           | 65.6 ms: 1.02x faster                                                                                                   |
| sqlite_synth               | 2.20 us                                                                                                           | 2.16 us: 1.02x faster                                                                                                   |
| json                       | 4.88 ms                                                                                                           | 4.80 ms: 1.02x faster                                                                                                   |
| asyncio_tcp                | 499 ms                                                                                                            | 492 ms: 1.01x faster                                                                                                    |
| gc_traversal               | 4.24 ms                                                                                                           | 4.19 ms: 1.01x faster                                                                                                   |
| pickle                     | 12.3 us                                                                                                           | 12.2 us: 1.01x faster                                                                                                   |
| asyncio_tcp_ssl            | 1.51 sec                                                                                                          | 1.50 sec: 1.01x faster                                                                                                  |
| python_startup             | 14.9 ms                                                                                                           | 14.9 ms: 1.00x faster                                                                                                   |
| python_startup_no_site     | 8.61 ms                                                                                                           | 8.60 ms: 1.00x faster                                                                                                   |
| meteor_contest             | 103 ms                                                                                                            | 103 ms: 1.00x slower                                                                                                    |
| pickle_list                | 4.92 us                                                                                                           | 4.97 us: 1.01x slower                                                                                                   |
| xml_etree_iterparse        | 92.9 ms                                                                                                           | 93.9 ms: 1.01x slower                                                                                                   |
| json_dumps                 | 11.3 ms                                                                                                           | 11.5 ms: 1.02x slower                                                                                                   |
| regex_dna                  | 181 ms                                                                                                            | 185 ms: 1.02x slower                                                                                                    |
| connected_components       | 398 ms                                                                                                            | 410 ms: 1.03x slower                                                                                                    |
| create_gc_cycles           | 1.87 ms                                                                                                           | 1.94 ms: 1.04x slower                                                                                                   |
| pickle_dict                | 30.3 us                                                                                                           | 31.5 us: 1.04x slower                                                                                                   |
| xml_etree_parse            | 131 ms                                                                                                            | 144 ms: 1.10x slower                                                                                                    |
| regex_effbot               | 2.82 ms                                                                                                           | 3.10 ms: 1.10x slower                                                                                                   |
| mdp                        | 2.33 sec                                                                                                          | 2.67 sec: 1.14x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                             | 1.07x faster                                                                                                            |

Benchmark hidden because not significant (4): regex_v8, asyncio_websockets, unpickle, shortest_path

- Geometric mean (including insignificant results): 1.069x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.03x