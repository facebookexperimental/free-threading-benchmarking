# Results vs. base

- fork: python
- ref: bcff99cb3f3b887a08c4
- machine: linux-x86_64
- commit hash: bcff99c
- commit date: 2026-03-23
- overall geometric mean: 1.094x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260323-3.15.0a7+-bcff99c/bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c.json | results/bm-20260323-3.15.0a7+-bcff99c-NOGIL/bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 252 ms                                                                                                            | 283 ms: 1.12x slower                                                                                                    |
| docutils       | 2.46 sec                                                                                                          | 2.66 sec: 1.08x slower                                                                                                  |
| html5lib       | 60.0 ms                                                                                                           | 65.7 ms: 1.09x slower                                                                                                   |
| sphinx         | 965 ms                                                                                                            | 1.04 sec: 1.08x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.09x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | results/bm-20260323-3.15.0a7+-bcff99c/bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c.json | results/bm-20260323-3.15.0a7+-bcff99c-NOGIL/bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c.json |
|---------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| asyncio_websockets        | 545 ms                                                                                                            | 513 ms: 1.06x faster                                                                                                    |
| coroutines                | 23.5 ms                                                                                                           | 23.9 ms: 1.02x slower                                                                                                   |
| async_tree_io             | 591 ms                                                                                                            | 612 ms: 1.04x slower                                                                                                    |
| async_tree_memoization_tg | 307 ms                                                                                                            | 320 ms: 1.04x slower                                                                                                    |
| async_tree_none_tg        | 246 ms                                                                                                            | 259 ms: 1.05x slower                                                                                                    |
| async_tree_io_tg          | 571 ms                                                                                                            | 602 ms: 1.05x slower                                                                                                    |
| async_tree_cpu_io_mixed   | 510 ms                                                                                                            | 547 ms: 1.07x slower                                                                                                    |
| async_generators          | 344 ms                                                                                                            | 372 ms: 1.08x slower                                                                                                    |
| async_tree_memoization    | 315 ms                                                                                                            | 350 ms: 1.11x slower                                                                                                    |
| async_tree_none           | 250 ms                                                                                                            | 284 ms: 1.13x slower                                                                                                    |
| Geometric mean            | (ref)                                                                                                             | 1.05x slower                                                                                                            |

Benchmark hidden because not significant (1): async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260323-3.15.0a7+-bcff99c/bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c.json | results/bm-20260323-3.15.0a7+-bcff99c-NOGIL/bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 204 ms                                                                                                            | 187 ms: 1.09x faster                                                                                                    |
| float          | 69.8 ms                                                                                                           | 73.3 ms: 1.05x slower                                                                                                   |
| nbody          | 94.9 ms                                                                                                           | 122 ms: 1.29x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.08x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260323-3.15.0a7+-bcff99c/bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c.json | results/bm-20260323-3.15.0a7+-bcff99c-NOGIL/bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.1 ms                                                                                                           | 21.8 ms: 1.03x slower                                                                                                   |
| regex_effbot   | 2.68 ms                                                                                                           | 3.00 ms: 1.12x slower                                                                                                   |
| regex_dna      | 165 ms                                                                                                            | 186 ms: 1.13x slower                                                                                                    |
| regex_compile  | 125 ms                                                                                                            | 142 ms: 1.14x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.11x slower                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260323-3.15.0a7+-bcff99c/bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c.json | results/bm-20260323-3.15.0a7+-bcff99c-NOGIL/bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 85.2 ms                                                                                                           | 88.0 ms: 1.03x slower                                                                                                   |
| tomli_loads          | 1.84 sec                                                                                                          | 1.97 sec: 1.07x slower                                                                                                  |
| json_dumps           | 10.1 ms                                                                                                           | 10.9 ms: 1.07x slower                                                                                                   |
| pickle_pure_python   | 308 us                                                                                                            | 335 us: 1.09x slower                                                                                                    |
| unpickle_pure_python | 215 us                                                                                                            | 236 us: 1.10x slower                                                                                                    |
| json_loads           | 27.8 us                                                                                                           | 31.3 us: 1.13x slower                                                                                                   |
| xml_etree_generate   | 85.2 ms                                                                                                           | 96.5 ms: 1.13x slower                                                                                                   |
| xml_etree_process    | 59.6 ms                                                                                                           | 68.2 ms: 1.14x slower                                                                                                   |
| Geometric mean       | (ref)                                                                                                             | 1.08x slower                                                                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260323-3.15.0a7+-bcff99c/bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c.json | results/bm-20260323-3.15.0a7+-bcff99c-NOGIL/bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.6 ms                                                                                                           | 15.9 ms: 1.26x slower                                                                                                   |
| python_startup_no_site | 7.42 ms                                                                                                           | 9.77 ms: 1.32x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.29x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260323-3.15.0a7+-bcff99c/bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c.json | results/bm-20260323-3.15.0a7+-bcff99c-NOGIL/bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 51.2 ms                                                                                                           | 55.4 ms: 1.08x slower                                                                                                   |
| django_template | 35.5 ms                                                                                                           | 39.9 ms: 1.12x slower                                                                                                   |
| genshi_text     | 21.4 ms                                                                                                           | 26.2 ms: 1.22x slower                                                                                                   |
| mako            | 12.0 ms                                                                                                           | 15.5 ms: 1.29x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.18x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                 | results/bm-20260323-3.15.0a7+-bcff99c/bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c.json | results/bm-20260323-3.15.0a7+-bcff99c-NOGIL/bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c.json |
|---------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool             | 298 ms                                                                                                            | 7.02 ms: 42.50x faster                                                                                                  |
| gc_traversal              | 4.46 ms                                                                                                           | 1.92 ms: 2.32x faster                                                                                                   |
| create_gc_cycles          | 1.83 ms                                                                                                           | 1.49 ms: 1.23x faster                                                                                                   |
| sqlite_synth              | 2.22 us                                                                                                           | 1.92 us: 1.16x faster                                                                                                   |
| pidigits                  | 204 ms                                                                                                            | 187 ms: 1.09x faster                                                                                                    |
| asyncio_websockets        | 545 ms                                                                                                            | 513 ms: 1.06x faster                                                                                                    |
| pathlib                   | 17.8 ms                                                                                                           | 17.7 ms: 1.01x faster                                                                                                   |
| dulwich_log               | 68.5 ms                                                                                                           | 69.5 ms: 1.01x slower                                                                                                   |
| coroutines                | 23.5 ms                                                                                                           | 23.9 ms: 1.02x slower                                                                                                   |
| pycparser                 | 1.09 sec                                                                                                          | 1.12 sec: 1.02x slower                                                                                                  |
| xml_etree_iterparse       | 85.2 ms                                                                                                           | 88.0 ms: 1.03x slower                                                                                                   |
| regex_v8                  | 21.1 ms                                                                                                           | 21.8 ms: 1.03x slower                                                                                                   |
| async_tree_io             | 591 ms                                                                                                            | 612 ms: 1.04x slower                                                                                                    |
| sympy_expand              | 495 ms                                                                                                            | 516 ms: 1.04x slower                                                                                                    |
| async_tree_memoization_tg | 307 ms                                                                                                            | 320 ms: 1.04x slower                                                                                                    |
| bpe_tokeniser             | 4.16 sec                                                                                                          | 4.36 sec: 1.05x slower                                                                                                  |
| float                     | 69.8 ms                                                                                                           | 73.3 ms: 1.05x slower                                                                                                   |
| async_tree_none_tg        | 246 ms                                                                                                            | 259 ms: 1.05x slower                                                                                                    |
| async_tree_io_tg          | 571 ms                                                                                                            | 602 ms: 1.05x slower                                                                                                    |
| pylint                    | 283 ms                                                                                                            | 300 ms: 1.06x slower                                                                                                    |
| deltablue                 | 3.31 ms                                                                                                           | 3.51 ms: 1.06x slower                                                                                                   |
| json                      | 5.11 ms                                                                                                           | 5.44 ms: 1.06x slower                                                                                                   |
| tomli_loads               | 1.84 sec                                                                                                          | 1.97 sec: 1.07x slower                                                                                                  |
| telco                     | 161 ms                                                                                                            | 172 ms: 1.07x slower                                                                                                    |
| json_dumps                | 10.1 ms                                                                                                           | 10.9 ms: 1.07x slower                                                                                                   |
| logging_silent            | 97.1 ns                                                                                                           | 104 ns: 1.07x slower                                                                                                    |
| async_tree_cpu_io_mixed   | 510 ms                                                                                                            | 547 ms: 1.07x slower                                                                                                    |
| docutils                  | 2.46 sec                                                                                                          | 2.66 sec: 1.08x slower                                                                                                  |
| many_optionals            | 939 us                                                                                                            | 1.02 ms: 1.08x slower                                                                                                   |
| sphinx                    | 965 ms                                                                                                            | 1.04 sec: 1.08x slower                                                                                                  |
| genshi_xml                | 51.2 ms                                                                                                           | 55.4 ms: 1.08x slower                                                                                                   |
| async_generators          | 344 ms                                                                                                            | 372 ms: 1.08x slower                                                                                                    |
| generators                | 29.5 ms                                                                                                           | 32.0 ms: 1.09x slower                                                                                                   |
| pickle_pure_python        | 308 us                                                                                                            | 335 us: 1.09x slower                                                                                                    |
| html5lib                  | 60.0 ms                                                                                                           | 65.7 ms: 1.09x slower                                                                                                   |
| unpickle_pure_python      | 215 us                                                                                                            | 236 us: 1.10x slower                                                                                                    |
| sympy_str                 | 282 ms                                                                                                            | 310 ms: 1.10x slower                                                                                                    |
| sqlglot_v2_normalize      | 105 ms                                                                                                            | 115 ms: 1.10x slower                                                                                                    |
| scimark_sor               | 110 ms                                                                                                            | 121 ms: 1.10x slower                                                                                                    |
| pprint_safe_repr          | 723 ms                                                                                                            | 801 ms: 1.11x slower                                                                                                    |
| async_tree_memoization    | 315 ms                                                                                                            | 350 ms: 1.11x slower                                                                                                    |
| subparsers                | 9.15 ms                                                                                                           | 10.2 ms: 1.11x slower                                                                                                   |
| comprehensions            | 16.5 us                                                                                                           | 18.4 us: 1.11x slower                                                                                                   |
| sympy_integrate           | 19.3 ms                                                                                                           | 21.6 ms: 1.12x slower                                                                                                   |
| bench_thread_pool         | 1.33 ms                                                                                                           | 1.49 ms: 1.12x slower                                                                                                   |
| sympy_sum                 | 159 ms                                                                                                            | 178 ms: 1.12x slower                                                                                                    |
| scimark_fft               | 316 ms                                                                                                            | 354 ms: 1.12x slower                                                                                                    |
| 2to3                      | 252 ms                                                                                                            | 283 ms: 1.12x slower                                                                                                    |
| regex_effbot              | 2.68 ms                                                                                                           | 3.00 ms: 1.12x slower                                                                                                   |
| pprint_pformat            | 1.48 sec                                                                                                          | 1.66 sec: 1.12x slower                                                                                                  |
| chaos                     | 54.9 ms                                                                                                           | 61.7 ms: 1.12x slower                                                                                                   |
| django_template           | 35.5 ms                                                                                                           | 39.9 ms: 1.12x slower                                                                                                   |
| json_loads                | 27.8 us                                                                                                           | 31.3 us: 1.13x slower                                                                                                   |
| hexiom                    | 5.75 ms                                                                                                           | 6.48 ms: 1.13x slower                                                                                                   |
| regex_dna                 | 165 ms                                                                                                            | 186 ms: 1.13x slower                                                                                                    |
| sqlglot_v2_optimize       | 51.3 ms                                                                                                           | 58.1 ms: 1.13x slower                                                                                                   |
| nqueens                   | 76.3 ms                                                                                                           | 86.4 ms: 1.13x slower                                                                                                   |
| xml_etree_generate        | 85.2 ms                                                                                                           | 96.5 ms: 1.13x slower                                                                                                   |
| async_tree_none           | 250 ms                                                                                                            | 284 ms: 1.13x slower                                                                                                    |
| mdp                       | 1.15 sec                                                                                                          | 1.31 sec: 1.13x slower                                                                                                  |
| regex_compile             | 125 ms                                                                                                            | 142 ms: 1.14x slower                                                                                                    |
| go                        | 104 ms                                                                                                            | 119 ms: 1.14x slower                                                                                                    |
| xml_etree_process         | 59.6 ms                                                                                                           | 68.2 ms: 1.14x slower                                                                                                   |
| pyflate                   | 407 ms                                                                                                            | 466 ms: 1.15x slower                                                                                                    |
| deepcopy                  | 234 us                                                                                                            | 268 us: 1.15x slower                                                                                                    |
| deepcopy_reduce           | 2.57 us                                                                                                           | 2.95 us: 1.15x slower                                                                                                   |
| sqlglot_v2_transpile      | 1.52 ms                                                                                                           | 1.77 ms: 1.17x slower                                                                                                   |
| thrift                    | 780 us                                                                                                            | 911 us: 1.17x slower                                                                                                    |
| scimark_lu                | 109 ms                                                                                                            | 128 ms: 1.17x slower                                                                                                    |
| sqlglot_v2_parse          | 1.22 ms                                                                                                           | 1.44 ms: 1.18x slower                                                                                                   |
| logging_simple            | 5.78 us                                                                                                           | 6.84 us: 1.18x slower                                                                                                   |
| deepcopy_memo             | 26.5 us                                                                                                           | 31.3 us: 1.18x slower                                                                                                   |
| logging_format            | 6.71 us                                                                                                           | 7.94 us: 1.18x slower                                                                                                   |
| raytrace                  | 254 ms                                                                                                            | 302 ms: 1.19x slower                                                                                                    |
| k_core                    | 1.87 sec                                                                                                          | 2.23 sec: 1.19x slower                                                                                                  |
| fannkuch                  | 382 ms                                                                                                            | 460 ms: 1.20x slower                                                                                                    |
| typing_runtime_protocols  | 160 us                                                                                                            | 193 us: 1.21x slower                                                                                                    |
| spectral_norm             | 93.1 ms                                                                                                           | 112 ms: 1.21x slower                                                                                                    |
| genshi_text               | 21.4 ms                                                                                                           | 26.2 ms: 1.22x slower                                                                                                   |
| richards_super            | 48.5 ms                                                                                                           | 59.5 ms: 1.23x slower                                                                                                   |
| shortest_path             | 436 ms                                                                                                            | 535 ms: 1.23x slower                                                                                                    |
| scimark_sparse_mat_mult   | 4.60 ms                                                                                                           | 5.69 ms: 1.24x slower                                                                                                   |
| meteor_contest            | 101 ms                                                                                                            | 126 ms: 1.25x slower                                                                                                    |
| crypto_pyaes              | 70.0 ms                                                                                                           | 87.7 ms: 1.25x slower                                                                                                   |
| connected_components      | 389 ms                                                                                                            | 487 ms: 1.25x slower                                                                                                    |
| richards                  | 42.3 ms                                                                                                           | 53.2 ms: 1.26x slower                                                                                                   |
| python_startup            | 12.6 ms                                                                                                           | 15.9 ms: 1.26x slower                                                                                                   |
| scimark_monte_carlo       | 62.2 ms                                                                                                           | 78.9 ms: 1.27x slower                                                                                                   |
| nbody                     | 94.9 ms                                                                                                           | 122 ms: 1.29x slower                                                                                                    |
| mako                      | 12.0 ms                                                                                                           | 15.5 ms: 1.29x slower                                                                                                   |
| python_startup_no_site    | 7.42 ms                                                                                                           | 9.77 ms: 1.32x slower                                                                                                   |
| coverage                  | 83.3 ms                                                                                                           | 113 ms: 1.35x slower                                                                                                    |
| Geometric mean            | (ref)                                                                                                             | 1.06x slower                                                                                                            |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed_tg, xml_etree_parse

- Geometric mean (including insignificant results): 1.094x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.21x