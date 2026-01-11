# Results vs. base

- fork: python
- ref: aa8578dc54df2af9daa3
- machine: linux-x86_64
- commit hash: aa8578d
- commit date: 2026-01-10
- overall geometric mean: 1.047x faster
- HPT reliability: 99.52%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260110-3.15.0a3+-aa8578d/bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d.json | results/bm-20260110-3.15.0a3+-aa8578d-JIT/bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| docutils       | 2.53 sec                                                                                                          | 2.66 sec: 1.05x slower                                                                                                |
| html5lib       | 60.5 ms                                                                                                           | 64.3 ms: 1.06x slower                                                                                                 |
| sphinx         | 960 ms                                                                                                            | 990 ms: 1.03x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.04x slower                                                                                                          |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | results/bm-20260110-3.15.0a3+-aa8578d/bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d.json | results/bm-20260110-3.15.0a3+-aa8578d-JIT/bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d.json |
|---------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_none           | 242 ms                                                                                                            | 236 ms: 1.03x faster                                                                                                  |
| coroutines                | 24.0 ms                                                                                                           | 23.7 ms: 1.01x faster                                                                                                 |
| asyncio_tcp               | 453 ms                                                                                                            | 449 ms: 1.01x faster                                                                                                  |
| async_tree_memoization_tg | 305 ms                                                                                                            | 303 ms: 1.01x faster                                                                                                  |
| async_tree_cpu_io_mixed   | 478 ms                                                                                                            | 482 ms: 1.01x slower                                                                                                  |
| asyncio_tcp_ssl           | 1.45 sec                                                                                                          | 1.47 sec: 1.01x slower                                                                                                |
| async_generators          | 337 ms                                                                                                            | 356 ms: 1.06x slower                                                                                                  |
| Geometric mean            | (ref)                                                                                                             | 1.00x slower                                                                                                          |

Benchmark hidden because not significant (6): async_tree_io, async_tree_none_tg, async_tree_memoization, async_tree_io_tg, asyncio_websockets, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260110-3.15.0a3+-aa8578d/bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d.json | results/bm-20260110-3.15.0a3+-aa8578d-JIT/bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| nbody          | 91.8 ms                                                                                                           | 72.9 ms: 1.26x faster                                                                                                 |
| float          | 70.9 ms                                                                                                           | 56.7 ms: 1.25x faster                                                                                                 |
| pidigits       | 193 ms                                                                                                            | 205 ms: 1.06x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.14x faster                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260110-3.15.0a3+-aa8578d/bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d.json | results/bm-20260110-3.15.0a3+-aa8578d-JIT/bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_effbot   | 3.03 ms                                                                                                           | 2.67 ms: 1.13x faster                                                                                                 |
| regex_dna      | 188 ms                                                                                                            | 170 ms: 1.11x faster                                                                                                  |
| regex_compile  | 124 ms                                                                                                            | 121 ms: 1.02x faster                                                                                                  |
| regex_v8       | 22.3 ms                                                                                                           | 22.1 ms: 1.01x faster                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.07x faster                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260110-3.15.0a3+-aa8578d/bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d.json | results/bm-20260110-3.15.0a3+-aa8578d-JIT/bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| unpickle_pure_python | 215 us                                                                                                            | 177 us: 1.21x faster                                                                                                  |
| tomli_loads          | 1.87 sec                                                                                                          | 1.66 sec: 1.13x faster                                                                                                |
| pickle_pure_python   | 308 us                                                                                                            | 281 us: 1.10x faster                                                                                                  |
| json_dumps           | 10.0 ms                                                                                                           | 9.36 ms: 1.07x faster                                                                                                 |
| xml_etree_generate   | 83.1 ms                                                                                                           | 77.7 ms: 1.07x faster                                                                                                 |
| xml_etree_process    | 58.0 ms                                                                                                           | 54.3 ms: 1.07x faster                                                                                                 |
| unpickle_list        | 5.30 us                                                                                                           | 5.15 us: 1.03x faster                                                                                                 |
| xml_etree_parse      | 130 ms                                                                                                            | 128 ms: 1.02x faster                                                                                                  |
| xml_etree_iterparse  | 84.1 ms                                                                                                           | 83.1 ms: 1.01x faster                                                                                                 |
| unpickle             | 14.9 us                                                                                                           | 14.7 us: 1.01x faster                                                                                                 |
| pickle_list          | 5.12 us                                                                                                           | 5.07 us: 1.01x faster                                                                                                 |
| pickle_dict          | 31.6 us                                                                                                           | 31.7 us: 1.00x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                             | 1.05x faster                                                                                                          |

Benchmark hidden because not significant (2): json_loads, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260110-3.15.0a3+-aa8578d/bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d.json | results/bm-20260110-3.15.0a3+-aa8578d-JIT/bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.4 ms                                                                                                           | 12.5 ms: 1.01x slower                                                                                                 |
| python_startup_no_site | 7.25 ms                                                                                                           | 7.36 ms: 1.01x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                             | 1.01x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260110-3.15.0a3+-aa8578d/bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d.json | results/bm-20260110-3.15.0a3+-aa8578d-JIT/bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| mako            | 12.2 ms                                                                                                           | 10.4 ms: 1.17x faster                                                                                                 |
| genshi_text     | 21.4 ms                                                                                                           | 20.8 ms: 1.03x faster                                                                                                 |
| django_template | 35.4 ms                                                                                                           | 34.9 ms: 1.01x faster                                                                                                 |
| genshi_xml      | 48.6 ms                                                                                                           | 52.2 ms: 1.07x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                             | 1.03x faster                                                                                                          |

All benchmarks:
===============

| Benchmark                 | results/bm-20260110-3.15.0a3+-aa8578d/bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d.json | results/bm-20260110-3.15.0a3+-aa8578d-JIT/bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d.json |
|---------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| richards                  | 41.5 ms                                                                                                           | 17.7 ms: 2.34x faster                                                                                                 |
| richards_super            | 47.5 ms                                                                                                           | 21.6 ms: 2.20x faster                                                                                                 |
| bench_mp_pool             | 328 ms                                                                                                            | 239 ms: 1.38x faster                                                                                                  |
| nbody                     | 91.8 ms                                                                                                           | 72.9 ms: 1.26x faster                                                                                                 |
| float                     | 70.9 ms                                                                                                           | 56.7 ms: 1.25x faster                                                                                                 |
| deltablue                 | 3.29 ms                                                                                                           | 2.69 ms: 1.22x faster                                                                                                 |
| unpickle_pure_python      | 215 us                                                                                                            | 177 us: 1.21x faster                                                                                                  |
| scimark_monte_carlo       | 63.1 ms                                                                                                           | 52.2 ms: 1.21x faster                                                                                                 |
| logging_silent            | 101 ns                                                                                                            | 83.7 ns: 1.20x faster                                                                                                 |
| mako                      | 12.2 ms                                                                                                           | 10.4 ms: 1.17x faster                                                                                                 |
| scimark_fft               | 306 ms                                                                                                            | 262 ms: 1.17x faster                                                                                                  |
| go                        | 106 ms                                                                                                            | 91.9 ms: 1.16x faster                                                                                                 |
| pyflate                   | 411 ms                                                                                                            | 362 ms: 1.14x faster                                                                                                  |
| regex_effbot              | 3.03 ms                                                                                                           | 2.67 ms: 1.13x faster                                                                                                 |
| tomli_loads               | 1.87 sec                                                                                                          | 1.66 sec: 1.13x faster                                                                                                |
| pprint_safe_repr          | 709 ms                                                                                                            | 630 ms: 1.13x faster                                                                                                  |
| fannkuch                  | 390 ms                                                                                                            | 350 ms: 1.11x faster                                                                                                  |
| regex_dna                 | 188 ms                                                                                                            | 170 ms: 1.11x faster                                                                                                  |
| pprint_pformat            | 1.45 sec                                                                                                          | 1.31 sec: 1.11x faster                                                                                                |
| spectral_norm             | 92.5 ms                                                                                                           | 84.0 ms: 1.10x faster                                                                                                 |
| pickle_pure_python        | 308 us                                                                                                            | 281 us: 1.10x faster                                                                                                  |
| scimark_lu                | 109 ms                                                                                                            | 100 ms: 1.08x faster                                                                                                  |
| deepcopy_memo             | 26.5 us                                                                                                           | 24.6 us: 1.08x faster                                                                                                 |
| json_dumps                | 10.0 ms                                                                                                           | 9.36 ms: 1.07x faster                                                                                                 |
| scimark_sparse_mat_mult   | 4.56 ms                                                                                                           | 4.26 ms: 1.07x faster                                                                                                 |
| xml_etree_generate        | 83.1 ms                                                                                                           | 77.7 ms: 1.07x faster                                                                                                 |
| json                      | 5.20 ms                                                                                                           | 4.87 ms: 1.07x faster                                                                                                 |
| xml_etree_process         | 58.0 ms                                                                                                           | 54.3 ms: 1.07x faster                                                                                                 |
| sqlite_synth              | 2.33 us                                                                                                           | 2.18 us: 1.07x faster                                                                                                 |
| scimark_sor               | 106 ms                                                                                                            | 99.9 ms: 1.06x faster                                                                                                 |
| bpe_tokeniser             | 4.23 sec                                                                                                          | 4.01 sec: 1.05x faster                                                                                                |
| crypto_pyaes              | 69.1 ms                                                                                                           | 66.1 ms: 1.05x faster                                                                                                 |
| chaos                     | 55.6 ms                                                                                                           | 53.2 ms: 1.04x faster                                                                                                 |
| deepcopy                  | 232 us                                                                                                            | 223 us: 1.04x faster                                                                                                  |
| thrift                    | 775 us                                                                                                            | 749 us: 1.03x faster                                                                                                  |
| connected_components      | 392 ms                                                                                                            | 380 ms: 1.03x faster                                                                                                  |
| deepcopy_reduce           | 2.52 us                                                                                                           | 2.43 us: 1.03x faster                                                                                                 |
| meteor_contest            | 102 ms                                                                                                            | 98.9 ms: 1.03x faster                                                                                                 |
| sqlglot_v2_parse          | 1.21 ms                                                                                                           | 1.17 ms: 1.03x faster                                                                                                 |
| genshi_text               | 21.4 ms                                                                                                           | 20.8 ms: 1.03x faster                                                                                                 |
| pycparser                 | 1.11 sec                                                                                                          | 1.08 sec: 1.03x faster                                                                                                |
| unpickle_list             | 5.30 us                                                                                                           | 5.15 us: 1.03x faster                                                                                                 |
| async_tree_none           | 242 ms                                                                                                            | 236 ms: 1.03x faster                                                                                                  |
| gc_traversal              | 4.35 ms                                                                                                           | 4.24 ms: 1.03x faster                                                                                                 |
| regex_compile             | 124 ms                                                                                                            | 121 ms: 1.02x faster                                                                                                  |
| xml_etree_parse           | 130 ms                                                                                                            | 128 ms: 1.02x faster                                                                                                  |
| k_core                    | 1.89 sec                                                                                                          | 1.86 sec: 1.02x faster                                                                                                |
| django_template           | 35.4 ms                                                                                                           | 34.9 ms: 1.01x faster                                                                                                 |
| comprehensions            | 16.3 us                                                                                                           | 16.1 us: 1.01x faster                                                                                                 |
| coroutines                | 24.0 ms                                                                                                           | 23.7 ms: 1.01x faster                                                                                                 |
| xml_etree_iterparse       | 84.1 ms                                                                                                           | 83.1 ms: 1.01x faster                                                                                                 |
| logging_format            | 6.74 us                                                                                                           | 6.67 us: 1.01x faster                                                                                                 |
| unpickle                  | 14.9 us                                                                                                           | 14.7 us: 1.01x faster                                                                                                 |
| pickle_list               | 5.12 us                                                                                                           | 5.07 us: 1.01x faster                                                                                                 |
| regex_v8                  | 22.3 ms                                                                                                           | 22.1 ms: 1.01x faster                                                                                                 |
| shortest_path             | 431 ms                                                                                                            | 427 ms: 1.01x faster                                                                                                  |
| coverage                  | 81.6 ms                                                                                                           | 81.0 ms: 1.01x faster                                                                                                 |
| asyncio_tcp               | 453 ms                                                                                                            | 449 ms: 1.01x faster                                                                                                  |
| async_tree_memoization_tg | 305 ms                                                                                                            | 303 ms: 1.01x faster                                                                                                  |
| logging_simple            | 5.95 us                                                                                                           | 5.91 us: 1.01x faster                                                                                                 |
| pickle_dict               | 31.6 us                                                                                                           | 31.7 us: 1.00x slower                                                                                                 |
| python_startup            | 12.4 ms                                                                                                           | 12.5 ms: 1.01x slower                                                                                                 |
| async_tree_cpu_io_mixed   | 478 ms                                                                                                            | 482 ms: 1.01x slower                                                                                                  |
| nqueens                   | 79.5 ms                                                                                                           | 80.4 ms: 1.01x slower                                                                                                 |
| asyncio_tcp_ssl           | 1.45 sec                                                                                                          | 1.47 sec: 1.01x slower                                                                                                |
| python_startup_no_site    | 7.25 ms                                                                                                           | 7.36 ms: 1.01x slower                                                                                                 |
| telco                     | 160 ms                                                                                                            | 162 ms: 1.02x slower                                                                                                  |
| create_gc_cycles          | 1.89 ms                                                                                                           | 1.94 ms: 1.03x slower                                                                                                 |
| sphinx                    | 960 ms                                                                                                            | 990 ms: 1.03x slower                                                                                                  |
| pathlib                   | 17.2 ms                                                                                                           | 17.8 ms: 1.04x slower                                                                                                 |
| raytrace                  | 253 ms                                                                                                            | 264 ms: 1.04x slower                                                                                                  |
| sqlglot_v2_normalize      | 101 ms                                                                                                            | 106 ms: 1.05x slower                                                                                                  |
| dulwich_log               | 67.3 ms                                                                                                           | 70.6 ms: 1.05x slower                                                                                                 |
| sympy_expand              | 483 ms                                                                                                            | 507 ms: 1.05x slower                                                                                                  |
| sympy_integrate           | 19.2 ms                                                                                                           | 20.2 ms: 1.05x slower                                                                                                 |
| sqlglot_v2_optimize       | 51.0 ms                                                                                                           | 53.5 ms: 1.05x slower                                                                                                 |
| docutils                  | 2.53 sec                                                                                                          | 2.66 sec: 1.05x slower                                                                                                |
| async_generators          | 337 ms                                                                                                            | 356 ms: 1.06x slower                                                                                                  |
| many_optionals            | 942 us                                                                                                            | 995 us: 1.06x slower                                                                                                  |
| generators                | 28.4 ms                                                                                                           | 30.0 ms: 1.06x slower                                                                                                 |
| pidigits                  | 193 ms                                                                                                            | 205 ms: 1.06x slower                                                                                                  |
| hexiom                    | 5.69 ms                                                                                                           | 6.03 ms: 1.06x slower                                                                                                 |
| html5lib                  | 60.5 ms                                                                                                           | 64.3 ms: 1.06x slower                                                                                                 |
| genshi_xml                | 48.6 ms                                                                                                           | 52.2 ms: 1.07x slower                                                                                                 |
| sympy_sum                 | 156 ms                                                                                                            | 168 ms: 1.08x slower                                                                                                  |
| pylint                    | 282 ms                                                                                                            | 306 ms: 1.08x slower                                                                                                  |
| sympy_str                 | 277 ms                                                                                                            | 307 ms: 1.11x slower                                                                                                  |
| mdp                       | 1.16 sec                                                                                                          | 1.35 sec: 1.16x slower                                                                                                |
| unpack_sequence           | 46.7 ns                                                                                                           | 69.0 ns: 1.48x slower                                                                                                 |
| Geometric mean            | (ref)                                                                                                             | 1.04x faster                                                                                                          |

Benchmark hidden because not significant (13): async_tree_io, async_tree_none_tg, bench_thread_pool, json_loads, sqlglot_v2_transpile, async_tree_memoization, async_tree_io_tg, subparsers, asyncio_websockets, 2to3, pickle, typing_runtime_protocols, async_tree_cpu_io_mixed_tg

- Geometric mean (including insignificant results): 1.047x faster

# HPT report

- Reliability score: 99.52% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x