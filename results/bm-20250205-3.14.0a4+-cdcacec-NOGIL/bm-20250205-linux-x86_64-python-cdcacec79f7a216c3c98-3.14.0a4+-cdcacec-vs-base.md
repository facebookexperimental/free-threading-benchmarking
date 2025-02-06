# Results vs. base

- fork: python
- ref: cdcacec79f7a216c3c98
- machine: linux-x86_64
- commit hash: cdcacec
- commit date: 2025-02-05
- overall geometric mean: 1.132x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250205-3.14.0a4+-cdcacec/bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json | results/bm-20250205-3.14.0a4+-cdcacec-NOGIL/bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 470 ms                                                                                                            | 554 ms: 1.18x slower                                                                                                    |
| docutils       | 3.67 sec                                                                                                          | 4.02 sec: 1.10x slower                                                                                                  |
| html5lib       | 78.4 ms                                                                                                           | 93.9 ms: 1.20x slower                                                                                                   |
| sphinx         | 1.44 sec                                                                                                          | 1.62 sec: 1.12x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.15x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250205-3.14.0a4+-cdcacec/bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json | results/bm-20250205-3.14.0a4+-cdcacec-NOGIL/bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_none_tg         | 383 ms                                                                                                            | 343 ms: 1.11x faster                                                                                                    |
| async_tree_io_tg           | 914 ms                                                                                                            | 825 ms: 1.11x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 699 ms                                                                                                            | 654 ms: 1.07x faster                                                                                                    |
| async_tree_io              | 902 ms                                                                                                            | 854 ms: 1.06x faster                                                                                                    |
| coroutines                 | 30.5 ms                                                                                                           | 32.3 ms: 1.06x slower                                                                                                   |
| asyncio_websockets         | 704 ms                                                                                                            | 757 ms: 1.08x slower                                                                                                    |
| async_generators           | 522 ms                                                                                                            | 564 ms: 1.08x slower                                                                                                    |
| async_tree_none            | 386 ms                                                                                                            | 428 ms: 1.11x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.00x faster                                                                                                            |

Benchmark hidden because not significant (3): async_tree_memoization_tg, async_tree_cpu_io_mixed, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250205-3.14.0a4+-cdcacec/bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json | results/bm-20250205-3.14.0a4+-cdcacec-NOGIL/bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| float          | 114 ms                                                                                                            | 107 ms: 1.06x faster                                                                                                    |
| pidigits       | 232 ms                                                                                                            | 245 ms: 1.06x slower                                                                                                    |
| nbody          | 123 ms                                                                                                            | 202 ms: 1.64x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.18x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250205-3.14.0a4+-cdcacec/bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json | results/bm-20250205-3.14.0a4+-cdcacec-NOGIL/bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_dna      | 277 ms                                                                                                            | 312 ms: 1.13x slower                                                                                                    |
| regex_compile  | 157 ms                                                                                                            | 197 ms: 1.26x slower                                                                                                    |
| regex_effbot   | 4.18 ms                                                                                                           | 5.30 ms: 1.27x slower                                                                                                   |
| Geometric mean | (ref)                                                                                                             | 1.16x slower                                                                                                            |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250205-3.14.0a4+-cdcacec/bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json | results/bm-20250205-3.14.0a4+-cdcacec-NOGIL/bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 166 ms                                                                                                            | 144 ms: 1.15x faster                                                                                                    |
| xml_etree_parse      | 196 ms                                                                                                            | 213 ms: 1.08x slower                                                                                                    |
| json_dumps           | 16.1 ms                                                                                                           | 17.7 ms: 1.10x slower                                                                                                   |
| json_loads           | 39.6 us                                                                                                           | 45.6 us: 1.15x slower                                                                                                   |
| xml_etree_generate   | 112 ms                                                                                                            | 130 ms: 1.16x slower                                                                                                    |
| unpickle_pure_python | 271 us                                                                                                            | 327 us: 1.21x slower                                                                                                    |
| xml_etree_process    | 80.8 ms                                                                                                           | 98.1 ms: 1.21x slower                                                                                                   |
| tomli_loads          | 2.44 sec                                                                                                          | 2.99 sec: 1.23x slower                                                                                                  |
| pickle_pure_python   | 389 us                                                                                                            | 491 us: 1.26x slower                                                                                                    |
| Geometric mean       | (ref)                                                                                                             | 1.14x slower                                                                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250205-3.14.0a4+-cdcacec/bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json | results/bm-20250205-3.14.0a4+-cdcacec-NOGIL/bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 26.7 ms                                                                                                           | 32.4 ms: 1.21x slower                                                                                                   |
| python_startup_no_site | 15.5 ms                                                                                                           | 20.0 ms: 1.29x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.25x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250205-3.14.0a4+-cdcacec/bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json | results/bm-20250205-3.14.0a4+-cdcacec-NOGIL/bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 44.4 ms                                                                                                           | 52.7 ms: 1.19x slower                                                                                                   |
| genshi_xml      | 68.4 ms                                                                                                           | 82.6 ms: 1.21x slower                                                                                                   |
| genshi_text     | 28.1 ms                                                                                                           | 36.8 ms: 1.31x slower                                                                                                   |
| mako            | 16.3 ms                                                                                                           | 25.2 ms: 1.55x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.30x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20250205-3.14.0a4+-cdcacec/bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json | results/bm-20250205-3.14.0a4+-cdcacec-NOGIL/bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 8.83 ms                                                                                                           | 3.76 ms: 2.35x faster                                                                                                   |
| create_gc_cycles           | 3.81 ms                                                                                                           | 2.97 ms: 1.28x faster                                                                                                   |
| xml_etree_iterparse        | 166 ms                                                                                                            | 144 ms: 1.15x faster                                                                                                    |
| async_tree_none_tg         | 383 ms                                                                                                            | 343 ms: 1.11x faster                                                                                                    |
| bench_mp_pool              | 97.0 ms                                                                                                           | 87.5 ms: 1.11x faster                                                                                                   |
| async_tree_io_tg           | 914 ms                                                                                                            | 825 ms: 1.11x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 699 ms                                                                                                            | 654 ms: 1.07x faster                                                                                                    |
| float                      | 114 ms                                                                                                            | 107 ms: 1.06x faster                                                                                                    |
| async_tree_io              | 902 ms                                                                                                            | 854 ms: 1.06x faster                                                                                                    |
| pycparser                  | 1.55 sec                                                                                                          | 1.60 sec: 1.03x slower                                                                                                  |
| pidigits                   | 232 ms                                                                                                            | 245 ms: 1.06x slower                                                                                                    |
| coroutines                 | 30.5 ms                                                                                                           | 32.3 ms: 1.06x slower                                                                                                   |
| thrift                     | 1.18 ms                                                                                                           | 1.26 ms: 1.06x slower                                                                                                   |
| telco                      | 10.9 ms                                                                                                           | 11.7 ms: 1.07x slower                                                                                                   |
| asyncio_websockets         | 704 ms                                                                                                            | 757 ms: 1.08x slower                                                                                                    |
| k_core                     | 4.15 sec                                                                                                          | 4.48 sec: 1.08x slower                                                                                                  |
| async_generators           | 522 ms                                                                                                            | 564 ms: 1.08x slower                                                                                                    |
| xml_etree_parse            | 196 ms                                                                                                            | 213 ms: 1.08x slower                                                                                                    |
| sympy_sum                  | 219 ms                                                                                                            | 238 ms: 1.09x slower                                                                                                    |
| docutils                   | 3.67 sec                                                                                                          | 4.02 sec: 1.10x slower                                                                                                  |
| json_dumps                 | 16.1 ms                                                                                                           | 17.7 ms: 1.10x slower                                                                                                   |
| async_tree_none            | 386 ms                                                                                                            | 428 ms: 1.11x slower                                                                                                    |
| pathlib                    | 28.2 ms                                                                                                           | 31.4 ms: 1.11x slower                                                                                                   |
| logging_silent             | 128 ns                                                                                                            | 143 ns: 1.12x slower                                                                                                    |
| json                       | 7.02 ms                                                                                                           | 7.83 ms: 1.12x slower                                                                                                   |
| connected_components       | 842 ms                                                                                                            | 943 ms: 1.12x slower                                                                                                    |
| sphinx                     | 1.44 sec                                                                                                          | 1.62 sec: 1.12x slower                                                                                                  |
| regex_dna                  | 277 ms                                                                                                            | 312 ms: 1.13x slower                                                                                                    |
| shortest_path              | 942 ms                                                                                                            | 1.07 sec: 1.14x slower                                                                                                  |
| generators                 | 39.9 ms                                                                                                           | 45.9 ms: 1.15x slower                                                                                                   |
| json_loads                 | 39.6 us                                                                                                           | 45.6 us: 1.15x slower                                                                                                   |
| sympy_integrate            | 28.4 ms                                                                                                           | 32.9 ms: 1.16x slower                                                                                                   |
| spectral_norm              | 127 ms                                                                                                            | 148 ms: 1.16x slower                                                                                                    |
| xml_etree_generate         | 112 ms                                                                                                            | 130 ms: 1.16x slower                                                                                                    |
| coverage                   | 119 ms                                                                                                            | 139 ms: 1.16x slower                                                                                                    |
| pprint_safe_repr           | 947 ms                                                                                                            | 1.11 sec: 1.17x slower                                                                                                  |
| logging_simple             | 9.14 us                                                                                                           | 10.7 us: 1.17x slower                                                                                                   |
| 2to3                       | 470 ms                                                                                                            | 554 ms: 1.18x slower                                                                                                    |
| pylint                     | 393 ms                                                                                                            | 464 ms: 1.18x slower                                                                                                    |
| django_template            | 44.4 ms                                                                                                           | 52.7 ms: 1.19x slower                                                                                                   |
| mdp                        | 3.55 sec                                                                                                          | 4.23 sec: 1.19x slower                                                                                                  |
| pprint_pformat             | 1.86 sec                                                                                                          | 2.21 sec: 1.19x slower                                                                                                  |
| html5lib                   | 78.4 ms                                                                                                           | 93.9 ms: 1.20x slower                                                                                                   |
| pyflate                    | 628 ms                                                                                                            | 753 ms: 1.20x slower                                                                                                    |
| fannkuch                   | 527 ms                                                                                                            | 632 ms: 1.20x slower                                                                                                    |
| unpickle_pure_python       | 271 us                                                                                                            | 327 us: 1.21x slower                                                                                                    |
| deepcopy_reduce            | 3.38 us                                                                                                           | 4.08 us: 1.21x slower                                                                                                   |
| genshi_xml                 | 68.4 ms                                                                                                           | 82.6 ms: 1.21x slower                                                                                                   |
| python_startup             | 26.7 ms                                                                                                           | 32.4 ms: 1.21x slower                                                                                                   |
| xml_etree_process          | 80.8 ms                                                                                                           | 98.1 ms: 1.21x slower                                                                                                   |
| tomli_loads                | 2.44 sec                                                                                                          | 2.99 sec: 1.23x slower                                                                                                  |
| sqlglot_optimize           | 68.7 ms                                                                                                           | 84.4 ms: 1.23x slower                                                                                                   |
| scimark_fft                | 442 ms                                                                                                            | 543 ms: 1.23x slower                                                                                                    |
| many_optionals             | 1.26 ms                                                                                                           | 1.55 ms: 1.23x slower                                                                                                   |
| sympy_expand               | 592 ms                                                                                                            | 730 ms: 1.23x slower                                                                                                    |
| deepcopy_memo              | 38.6 us                                                                                                           | 47.8 us: 1.24x slower                                                                                                   |
| sqlglot_parse              | 1.88 ms                                                                                                           | 2.33 ms: 1.24x slower                                                                                                   |
| sqlalchemy_declarative     | 162 ms                                                                                                            | 203 ms: 1.25x slower                                                                                                    |
| sqlglot_transpile          | 2.13 ms                                                                                                           | 2.67 ms: 1.26x slower                                                                                                   |
| regex_compile              | 157 ms                                                                                                            | 197 ms: 1.26x slower                                                                                                    |
| sympy_str                  | 353 ms                                                                                                            | 445 ms: 1.26x slower                                                                                                    |
| pickle_pure_python         | 389 us                                                                                                            | 491 us: 1.26x slower                                                                                                    |
| scimark_sor                | 155 ms                                                                                                            | 196 ms: 1.26x slower                                                                                                    |
| nqueens                    | 111 ms                                                                                                            | 140 ms: 1.26x slower                                                                                                    |
| sqlalchemy_imperative      | 25.4 ms                                                                                                           | 32.2 ms: 1.27x slower                                                                                                   |
| go                         | 153 ms                                                                                                            | 194 ms: 1.27x slower                                                                                                    |
| regex_effbot               | 4.18 ms                                                                                                           | 5.30 ms: 1.27x slower                                                                                                   |
| meteor_contest             | 140 ms                                                                                                            | 178 ms: 1.27x slower                                                                                                    |
| richards                   | 56.8 ms                                                                                                           | 72.7 ms: 1.28x slower                                                                                                   |
| richards_super             | 65.1 ms                                                                                                           | 83.6 ms: 1.29x slower                                                                                                   |
| python_startup_no_site     | 15.5 ms                                                                                                           | 20.0 ms: 1.29x slower                                                                                                   |
| deepcopy                   | 340 us                                                                                                            | 439 us: 1.29x slower                                                                                                    |
| bpe_tokeniser              | 5.60 sec                                                                                                          | 7.27 sec: 1.30x slower                                                                                                  |
| crypto_pyaes               | 92.7 ms                                                                                                           | 121 ms: 1.30x slower                                                                                                    |
| genshi_text                | 28.1 ms                                                                                                           | 36.8 ms: 1.31x slower                                                                                                   |
| scimark_lu                 | 142 ms                                                                                                            | 187 ms: 1.32x slower                                                                                                    |
| comprehensions             | 20.7 us                                                                                                           | 27.4 us: 1.32x slower                                                                                                   |
| bench_thread_pool          | 3.26 ms                                                                                                           | 4.32 ms: 1.32x slower                                                                                                   |
| logging_format             | 8.39 us                                                                                                           | 11.1 us: 1.33x slower                                                                                                   |
| hexiom                     | 8.03 ms                                                                                                           | 10.8 ms: 1.34x slower                                                                                                   |
| subparsers                 | 29.8 ms                                                                                                           | 40.3 ms: 1.35x slower                                                                                                   |
| scimark_sparse_mat_mult    | 6.04 ms                                                                                                           | 8.33 ms: 1.38x slower                                                                                                   |
| scimark_monte_carlo        | 84.1 ms                                                                                                           | 116 ms: 1.38x slower                                                                                                    |
| raytrace                   | 338 ms                                                                                                            | 474 ms: 1.40x slower                                                                                                    |
| deltablue                  | 4.34 ms                                                                                                           | 6.28 ms: 1.45x slower                                                                                                   |
| typing_runtime_protocols   | 204 us                                                                                                            | 296 us: 1.45x slower                                                                                                    |
| chaos                      | 78.3 ms                                                                                                           | 120 ms: 1.54x slower                                                                                                    |
| mako                       | 16.3 ms                                                                                                           | 25.2 ms: 1.55x slower                                                                                                   |
| nbody                      | 123 ms                                                                                                            | 202 ms: 1.64x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.16x slower                                                                                                            |

Benchmark hidden because not significant (7): dulwich_log, async_tree_memoization_tg, async_tree_cpu_io_mixed, sqlite_synth, regex_v8, async_tree_memoization, sqlglot_normalize

- Geometric mean (including insignificant results): 1.132x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.14x
- 95% likely to have a slowdown of 1.13x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.19x