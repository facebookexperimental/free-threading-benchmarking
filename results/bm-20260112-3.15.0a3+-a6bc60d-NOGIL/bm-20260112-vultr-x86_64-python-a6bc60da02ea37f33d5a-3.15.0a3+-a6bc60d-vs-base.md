# Results vs. base

- fork: python
- ref: a6bc60da02ea37f33d5a
- machine: linux-x86_64
- commit hash: a6bc60d
- commit date: 2026-01-12
- overall geometric mean: 1.101x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260112-3.15.0a3+-a6bc60d/bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d.json | results/bm-20260112-3.15.0a3+-a6bc60d-NOGIL/bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 249 ms                                                                                                            | 277 ms: 1.12x slower                                                                                                    |
| docutils       | 2.56 sec                                                                                                          | 2.74 sec: 1.07x slower                                                                                                  |
| html5lib       | 60.0 ms                                                                                                           | 64.4 ms: 1.07x slower                                                                                                   |
| sphinx         | 968 ms                                                                                                            | 1.05 sec: 1.09x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.09x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260112-3.15.0a3+-a6bc60d/bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d.json | results/bm-20260112-3.15.0a3+-a6bc60d-NOGIL/bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| asyncio_websockets         | 545 ms                                                                                                            | 512 ms: 1.07x faster                                                                                                    |
| coroutines                 | 23.8 ms                                                                                                           | 24.2 ms: 1.02x slower                                                                                                   |
| async_tree_none_tg         | 250 ms                                                                                                            | 262 ms: 1.05x slower                                                                                                    |
| async_tree_io_tg           | 561 ms                                                                                                            | 593 ms: 1.06x slower                                                                                                    |
| async_generators           | 345 ms                                                                                                            | 376 ms: 1.09x slower                                                                                                    |
| async_tree_cpu_io_mixed_tg | 487 ms                                                                                                            | 532 ms: 1.09x slower                                                                                                    |
| async_tree_memoization_tg  | 296 ms                                                                                                            | 324 ms: 1.10x slower                                                                                                    |
| async_tree_io              | 551 ms                                                                                                            | 611 ms: 1.11x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 483 ms                                                                                                            | 556 ms: 1.15x slower                                                                                                    |
| async_tree_memoization     | 301 ms                                                                                                            | 353 ms: 1.17x slower                                                                                                    |
| async_tree_none            | 243 ms                                                                                                            | 288 ms: 1.19x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.08x slower                                                                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260112-3.15.0a3+-a6bc60d/bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d.json | results/bm-20260112-3.15.0a3+-a6bc60d-NOGIL/bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 196 ms                                                                                                            | 194 ms: 1.01x faster                                                                                                    |
| float          | 70.1 ms                                                                                                           | 75.1 ms: 1.07x slower                                                                                                   |
| nbody          | 93.3 ms                                                                                                           | 125 ms: 1.34x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.13x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260112-3.15.0a3+-a6bc60d/bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d.json | results/bm-20260112-3.15.0a3+-a6bc60d-NOGIL/bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 23.1 ms                                                                                                           | 21.5 ms: 1.07x faster                                                                                                   |
| regex_effbot   | 2.84 ms                                                                                                           | 2.70 ms: 1.05x faster                                                                                                   |
| regex_dna      | 178 ms                                                                                                            | 173 ms: 1.03x faster                                                                                                    |
| regex_compile  | 123 ms                                                                                                            | 141 ms: 1.15x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.00x faster                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260112-3.15.0a3+-a6bc60d/bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d.json | results/bm-20260112-3.15.0a3+-a6bc60d-NOGIL/bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 84.8 ms                                                                                                           | 88.1 ms: 1.04x slower                                                                                                   |
| pickle_pure_python   | 313 us                                                                                                            | 334 us: 1.07x slower                                                                                                    |
| tomli_loads          | 1.84 sec                                                                                                          | 2.00 sec: 1.08x slower                                                                                                  |
| unpickle_pure_python | 212 us                                                                                                            | 238 us: 1.12x slower                                                                                                    |
| json_dumps           | 9.79 ms                                                                                                           | 11.1 ms: 1.13x slower                                                                                                   |
| xml_etree_generate   | 84.1 ms                                                                                                           | 96.0 ms: 1.14x slower                                                                                                   |
| json_loads           | 28.1 us                                                                                                           | 32.3 us: 1.15x slower                                                                                                   |
| xml_etree_process    | 59.0 ms                                                                                                           | 69.4 ms: 1.18x slower                                                                                                   |
| Geometric mean       | (ref)                                                                                                             | 1.10x slower                                                                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260112-3.15.0a3+-a6bc60d/bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d.json | results/bm-20260112-3.15.0a3+-a6bc60d-NOGIL/bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.4 ms                                                                                                           | 15.7 ms: 1.26x slower                                                                                                   |
| python_startup_no_site | 7.27 ms                                                                                                           | 9.67 ms: 1.33x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.30x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260112-3.15.0a3+-a6bc60d/bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d.json | results/bm-20260112-3.15.0a3+-a6bc60d-NOGIL/bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 36.3 ms                                                                                                           | 39.9 ms: 1.10x slower                                                                                                   |
| genshi_xml      | 49.9 ms                                                                                                           | 57.6 ms: 1.16x slower                                                                                                   |
| genshi_text     | 21.5 ms                                                                                                           | 27.2 ms: 1.27x slower                                                                                                   |
| mako            | 11.9 ms                                                                                                           | 15.7 ms: 1.32x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.21x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20260112-3.15.0a3+-a6bc60d/bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d.json | results/bm-20260112-3.15.0a3+-a6bc60d-NOGIL/bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 319 ms                                                                                                            | 7.04 ms: 45.21x faster                                                                                                  |
| gc_traversal               | 4.34 ms                                                                                                           | 1.93 ms: 2.25x faster                                                                                                   |
| create_gc_cycles           | 1.87 ms                                                                                                           | 1.51 ms: 1.24x faster                                                                                                   |
| sqlite_synth               | 2.29 us                                                                                                           | 2.06 us: 1.11x faster                                                                                                   |
| regex_v8                   | 23.1 ms                                                                                                           | 21.5 ms: 1.07x faster                                                                                                   |
| asyncio_websockets         | 545 ms                                                                                                            | 512 ms: 1.07x faster                                                                                                    |
| regex_effbot               | 2.84 ms                                                                                                           | 2.70 ms: 1.05x faster                                                                                                   |
| regex_dna                  | 178 ms                                                                                                            | 173 ms: 1.03x faster                                                                                                    |
| pidigits                   | 196 ms                                                                                                            | 194 ms: 1.01x faster                                                                                                    |
| pathlib                    | 18.0 ms                                                                                                           | 18.2 ms: 1.01x slower                                                                                                   |
| pycparser                  | 1.13 sec                                                                                                          | 1.14 sec: 1.01x slower                                                                                                  |
| coroutines                 | 23.8 ms                                                                                                           | 24.2 ms: 1.02x slower                                                                                                   |
| dulwich_log                | 69.1 ms                                                                                                           | 70.9 ms: 1.03x slower                                                                                                   |
| xml_etree_iterparse        | 84.8 ms                                                                                                           | 88.1 ms: 1.04x slower                                                                                                   |
| async_tree_none_tg         | 250 ms                                                                                                            | 262 ms: 1.05x slower                                                                                                    |
| async_tree_io_tg           | 561 ms                                                                                                            | 593 ms: 1.06x slower                                                                                                    |
| bpe_tokeniser              | 4.19 sec                                                                                                          | 4.44 sec: 1.06x slower                                                                                                  |
| logging_silent             | 99.8 ns                                                                                                           | 106 ns: 1.06x slower                                                                                                    |
| pylint                     | 284 ms                                                                                                            | 301 ms: 1.06x slower                                                                                                    |
| many_optionals             | 956 us                                                                                                            | 1.02 ms: 1.06x slower                                                                                                   |
| json                       | 5.12 ms                                                                                                           | 5.46 ms: 1.07x slower                                                                                                   |
| pickle_pure_python         | 313 us                                                                                                            | 334 us: 1.07x slower                                                                                                    |
| docutils                   | 2.56 sec                                                                                                          | 2.74 sec: 1.07x slower                                                                                                  |
| float                      | 70.1 ms                                                                                                           | 75.1 ms: 1.07x slower                                                                                                   |
| sympy_expand               | 492 ms                                                                                                            | 528 ms: 1.07x slower                                                                                                    |
| html5lib                   | 60.0 ms                                                                                                           | 64.4 ms: 1.07x slower                                                                                                   |
| tomli_loads                | 1.84 sec                                                                                                          | 2.00 sec: 1.08x slower                                                                                                  |
| pprint_safe_repr           | 707 ms                                                                                                            | 768 ms: 1.09x slower                                                                                                    |
| sphinx                     | 968 ms                                                                                                            | 1.05 sec: 1.09x slower                                                                                                  |
| async_generators           | 345 ms                                                                                                            | 376 ms: 1.09x slower                                                                                                    |
| deltablue                  | 3.31 ms                                                                                                           | 3.61 ms: 1.09x slower                                                                                                   |
| async_tree_cpu_io_mixed_tg | 487 ms                                                                                                            | 532 ms: 1.09x slower                                                                                                    |
| async_tree_memoization_tg  | 296 ms                                                                                                            | 324 ms: 1.10x slower                                                                                                    |
| django_template            | 36.3 ms                                                                                                           | 39.9 ms: 1.10x slower                                                                                                   |
| subparsers                 | 9.40 ms                                                                                                           | 10.4 ms: 1.10x slower                                                                                                   |
| telco                      | 160 ms                                                                                                            | 177 ms: 1.11x slower                                                                                                    |
| nqueens                    | 80.2 ms                                                                                                           | 88.8 ms: 1.11x slower                                                                                                   |
| pprint_pformat             | 1.44 sec                                                                                                          | 1.60 sec: 1.11x slower                                                                                                  |
| comprehensions             | 16.1 us                                                                                                           | 17.9 us: 1.11x slower                                                                                                   |
| async_tree_io              | 551 ms                                                                                                            | 611 ms: 1.11x slower                                                                                                    |
| deepcopy_reduce            | 2.62 us                                                                                                           | 2.91 us: 1.11x slower                                                                                                   |
| bench_thread_pool          | 1.32 ms                                                                                                           | 1.47 ms: 1.11x slower                                                                                                   |
| 2to3                       | 249 ms                                                                                                            | 277 ms: 1.12x slower                                                                                                    |
| sympy_str                  | 279 ms                                                                                                            | 313 ms: 1.12x slower                                                                                                    |
| unpickle_pure_python       | 212 us                                                                                                            | 238 us: 1.12x slower                                                                                                    |
| deepcopy                   | 236 us                                                                                                            | 265 us: 1.12x slower                                                                                                    |
| mdp                        | 1.17 sec                                                                                                          | 1.31 sec: 1.13x slower                                                                                                  |
| json_dumps                 | 9.79 ms                                                                                                           | 11.1 ms: 1.13x slower                                                                                                   |
| chaos                      | 56.9 ms                                                                                                           | 64.3 ms: 1.13x slower                                                                                                   |
| hexiom                     | 5.61 ms                                                                                                           | 6.38 ms: 1.14x slower                                                                                                   |
| sympy_integrate            | 19.3 ms                                                                                                           | 21.9 ms: 1.14x slower                                                                                                   |
| sympy_sum                  | 156 ms                                                                                                            | 178 ms: 1.14x slower                                                                                                    |
| xml_etree_generate         | 84.1 ms                                                                                                           | 96.0 ms: 1.14x slower                                                                                                   |
| pyflate                    | 412 ms                                                                                                            | 471 ms: 1.14x slower                                                                                                    |
| regex_compile              | 123 ms                                                                                                            | 141 ms: 1.15x slower                                                                                                    |
| scimark_fft                | 308 ms                                                                                                            | 353 ms: 1.15x slower                                                                                                    |
| logging_format             | 6.71 us                                                                                                           | 7.71 us: 1.15x slower                                                                                                   |
| json_loads                 | 28.1 us                                                                                                           | 32.3 us: 1.15x slower                                                                                                   |
| generators                 | 28.0 ms                                                                                                           | 32.2 ms: 1.15x slower                                                                                                   |
| async_tree_cpu_io_mixed    | 483 ms                                                                                                            | 556 ms: 1.15x slower                                                                                                    |
| sqlglot_v2_optimize        | 51.5 ms                                                                                                           | 59.2 ms: 1.15x slower                                                                                                   |
| sqlglot_v2_normalize       | 102 ms                                                                                                            | 117 ms: 1.15x slower                                                                                                    |
| genshi_xml                 | 49.9 ms                                                                                                           | 57.6 ms: 1.16x slower                                                                                                   |
| go                         | 105 ms                                                                                                            | 121 ms: 1.16x slower                                                                                                    |
| thrift                     | 773 us                                                                                                            | 899 us: 1.16x slower                                                                                                    |
| logging_simple             | 5.90 us                                                                                                           | 6.87 us: 1.16x slower                                                                                                   |
| scimark_sor                | 106 ms                                                                                                            | 123 ms: 1.17x slower                                                                                                    |
| deepcopy_memo              | 26.4 us                                                                                                           | 30.8 us: 1.17x slower                                                                                                   |
| async_tree_memoization     | 301 ms                                                                                                            | 353 ms: 1.17x slower                                                                                                    |
| sqlglot_v2_transpile       | 1.51 ms                                                                                                           | 1.77 ms: 1.17x slower                                                                                                   |
| xml_etree_process          | 59.0 ms                                                                                                           | 69.4 ms: 1.18x slower                                                                                                   |
| k_core                     | 1.86 sec                                                                                                          | 2.21 sec: 1.18x slower                                                                                                  |
| async_tree_none            | 243 ms                                                                                                            | 288 ms: 1.19x slower                                                                                                    |
| meteor_contest             | 101 ms                                                                                                            | 121 ms: 1.19x slower                                                                                                    |
| spectral_norm              | 95.1 ms                                                                                                           | 113 ms: 1.19x slower                                                                                                    |
| sqlglot_v2_parse           | 1.20 ms                                                                                                           | 1.44 ms: 1.20x slower                                                                                                   |
| raytrace                   | 253 ms                                                                                                            | 305 ms: 1.20x slower                                                                                                    |
| scimark_lu                 | 109 ms                                                                                                            | 132 ms: 1.21x slower                                                                                                    |
| typing_runtime_protocols   | 160 us                                                                                                            | 194 us: 1.21x slower                                                                                                    |
| fannkuch                   | 381 ms                                                                                                            | 464 ms: 1.22x slower                                                                                                    |
| shortest_path              | 431 ms                                                                                                            | 533 ms: 1.24x slower                                                                                                    |
| connected_components       | 392 ms                                                                                                            | 486 ms: 1.24x slower                                                                                                    |
| richards_super             | 48.0 ms                                                                                                           | 60.1 ms: 1.25x slower                                                                                                   |
| richards                   | 42.0 ms                                                                                                           | 52.8 ms: 1.26x slower                                                                                                   |
| crypto_pyaes               | 69.4 ms                                                                                                           | 87.4 ms: 1.26x slower                                                                                                   |
| python_startup             | 12.4 ms                                                                                                           | 15.7 ms: 1.26x slower                                                                                                   |
| genshi_text                | 21.5 ms                                                                                                           | 27.2 ms: 1.27x slower                                                                                                   |
| scimark_sparse_mat_mult    | 4.44 ms                                                                                                           | 5.64 ms: 1.27x slower                                                                                                   |
| scimark_monte_carlo        | 62.6 ms                                                                                                           | 79.5 ms: 1.27x slower                                                                                                   |
| mako                       | 11.9 ms                                                                                                           | 15.7 ms: 1.32x slower                                                                                                   |
| python_startup_no_site     | 7.27 ms                                                                                                           | 9.67 ms: 1.33x slower                                                                                                   |
| nbody                      | 93.3 ms                                                                                                           | 125 ms: 1.34x slower                                                                                                    |
| coverage                   | 82.0 ms                                                                                                           | 111 ms: 1.35x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.07x slower                                                                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

- Geometric mean (including insignificant results): 1.101x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.10x
- 99% likely to have a slowdown of 1.09x

# Memory
- memory change: 1.20x