# Results vs. base

- fork: python
- ref: 7afe1adb0089d0f2df2a
- machine: linux-x86_64
- commit hash: 7afe1ad
- commit date: 2025-07-02
- overall geometric mean: 1.092x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250702-3.15.0a0-7afe1ad/bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad.json | results/bm-20250702-3.15.0a0-7afe1ad-NOGIL/bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 249 ms                                                                                                          | 283 ms: 1.14x slower                                                                                                  |
| docutils       | 2.54 sec                                                                                                        | 2.69 sec: 1.06x slower                                                                                                |
| html5lib       | 60.9 ms                                                                                                         | 65.0 ms: 1.07x slower                                                                                                 |
| sphinx         | 969 ms                                                                                                          | 1.04 sec: 1.07x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.08x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250702-3.15.0a0-7afe1ad/bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad.json | results/bm-20250702-3.15.0a0-7afe1ad-NOGIL/bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 617 ms                                                                                                          | 527 ms: 1.17x faster                                                                                                  |
| async_tree_none_tg         | 253 ms                                                                                                          | 228 ms: 1.11x faster                                                                                                  |
| async_tree_memoization_tg  | 312 ms                                                                                                          | 285 ms: 1.10x faster                                                                                                  |
| async_tree_io              | 599 ms                                                                                                          | 553 ms: 1.08x faster                                                                                                  |
| asyncio_websockets         | 517 ms                                                                                                          | 512 ms: 1.01x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 510 ms                                                                                                          | 522 ms: 1.02x slower                                                                                                  |
| coroutines                 | 22.9 ms                                                                                                         | 24.3 ms: 1.06x slower                                                                                                 |
| async_tree_cpu_io_mixed    | 505 ms                                                                                                          | 545 ms: 1.08x slower                                                                                                  |
| async_generators           | 338 ms                                                                                                          | 369 ms: 1.09x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.02x faster                                                                                                          |

Benchmark hidden because not significant (2): async_tree_memoization, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250702-3.15.0a0-7afe1ad/bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad.json | results/bm-20250702-3.15.0a0-7afe1ad-NOGIL/bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| float          | 72.4 ms                                                                                                         | 69.5 ms: 1.04x faster                                                                                                 |
| pidigits       | 194 ms                                                                                                          | 206 ms: 1.06x slower                                                                                                  |
| nbody          | 89.3 ms                                                                                                         | 124 ms: 1.39x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.12x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250702-3.15.0a0-7afe1ad/bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad.json | results/bm-20250702-3.15.0a0-7afe1ad-NOGIL/bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.0 ms                                                                                                         | 20.5 ms: 1.02x faster                                                                                                 |
| regex_dna      | 164 ms                                                                                                          | 172 ms: 1.05x slower                                                                                                  |
| regex_effbot   | 2.57 ms                                                                                                         | 2.75 ms: 1.07x slower                                                                                                 |
| regex_compile  | 124 ms                                                                                                          | 142 ms: 1.15x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.06x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250702-3.15.0a0-7afe1ad/bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad.json | results/bm-20250702-3.15.0a0-7afe1ad-NOGIL/bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 93.7 ms                                                                                                         | 87.1 ms: 1.08x faster                                                                                                 |
| xml_etree_parse      | 133 ms                                                                                                          | 130 ms: 1.02x faster                                                                                                  |
| json_loads           | 28.8 us                                                                                                         | 31.1 us: 1.08x slower                                                                                                 |
| pickle_pure_python   | 307 us                                                                                                          | 335 us: 1.09x slower                                                                                                  |
| unpickle_pure_python | 208 us                                                                                                          | 230 us: 1.11x slower                                                                                                  |
| tomli_loads          | 1.91 sec                                                                                                        | 2.15 sec: 1.13x slower                                                                                                |
| xml_etree_generate   | 83.3 ms                                                                                                         | 94.9 ms: 1.14x slower                                                                                                 |
| json_dumps           | 10.8 ms                                                                                                         | 12.3 ms: 1.14x slower                                                                                                 |
| xml_etree_process    | 57.8 ms                                                                                                         | 68.8 ms: 1.19x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.08x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250702-3.15.0a0-7afe1ad/bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad.json | results/bm-20250702-3.15.0a0-7afe1ad-NOGIL/bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.6 ms                                                                                                         | 15.9 ms: 1.26x slower                                                                                                 |
| python_startup_no_site | 7.32 ms                                                                                                         | 9.53 ms: 1.30x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.28x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250702-3.15.0a0-7afe1ad/bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad.json | results/bm-20250702-3.15.0a0-7afe1ad-NOGIL/bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 34.4 ms                                                                                                         | 39.0 ms: 1.13x slower                                                                                                 |
| genshi_xml      | 48.6 ms                                                                                                         | 57.4 ms: 1.18x slower                                                                                                 |
| genshi_text     | 20.8 ms                                                                                                         | 26.2 ms: 1.26x slower                                                                                                 |
| mako            | 11.5 ms                                                                                                         | 15.7 ms: 1.37x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.23x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20250702-3.15.0a0-7afe1ad/bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad.json | results/bm-20250702-3.15.0a0-7afe1ad-NOGIL/bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.41 ms                                                                                                         | 1.87 ms: 2.36x faster                                                                                                 |
| create_gc_cycles           | 1.95 ms                                                                                                         | 1.44 ms: 1.36x faster                                                                                                 |
| async_tree_io_tg           | 617 ms                                                                                                          | 527 ms: 1.17x faster                                                                                                  |
| async_tree_none_tg         | 253 ms                                                                                                          | 228 ms: 1.11x faster                                                                                                  |
| async_tree_memoization_tg  | 312 ms                                                                                                          | 285 ms: 1.10x faster                                                                                                  |
| sqlite_synth               | 2.24 us                                                                                                         | 2.04 us: 1.09x faster                                                                                                 |
| async_tree_io              | 599 ms                                                                                                          | 553 ms: 1.08x faster                                                                                                  |
| xml_etree_iterparse        | 93.7 ms                                                                                                         | 87.1 ms: 1.08x faster                                                                                                 |
| float                      | 72.4 ms                                                                                                         | 69.5 ms: 1.04x faster                                                                                                 |
| regex_v8                   | 21.0 ms                                                                                                         | 20.5 ms: 1.02x faster                                                                                                 |
| xml_etree_parse            | 133 ms                                                                                                          | 130 ms: 1.02x faster                                                                                                  |
| asyncio_websockets         | 517 ms                                                                                                          | 512 ms: 1.01x faster                                                                                                  |
| pathlib                    | 19.4 ms                                                                                                         | 19.2 ms: 1.01x faster                                                                                                 |
| async_tree_cpu_io_mixed_tg | 510 ms                                                                                                          | 522 ms: 1.02x slower                                                                                                  |
| json                       | 5.15 ms                                                                                                         | 5.33 ms: 1.03x slower                                                                                                 |
| pycparser                  | 1.09 sec                                                                                                        | 1.14 sec: 1.05x slower                                                                                                |
| bench_mp_pool              | 102 ms                                                                                                          | 108 ms: 1.05x slower                                                                                                  |
| bpe_tokeniser              | 4.19 sec                                                                                                        | 4.40 sec: 1.05x slower                                                                                                |
| regex_dna                  | 164 ms                                                                                                          | 172 ms: 1.05x slower                                                                                                  |
| docutils                   | 2.54 sec                                                                                                        | 2.69 sec: 1.06x slower                                                                                                |
| pidigits                   | 194 ms                                                                                                          | 206 ms: 1.06x slower                                                                                                  |
| coroutines                 | 22.9 ms                                                                                                         | 24.3 ms: 1.06x slower                                                                                                 |
| html5lib                   | 60.9 ms                                                                                                         | 65.0 ms: 1.07x slower                                                                                                 |
| regex_effbot               | 2.57 ms                                                                                                         | 2.75 ms: 1.07x slower                                                                                                 |
| dulwich_log                | 66.8 ms                                                                                                         | 71.7 ms: 1.07x slower                                                                                                 |
| sphinx                     | 969 ms                                                                                                          | 1.04 sec: 1.07x slower                                                                                                |
| async_tree_cpu_io_mixed    | 505 ms                                                                                                          | 545 ms: 1.08x slower                                                                                                  |
| json_loads                 | 28.8 us                                                                                                         | 31.1 us: 1.08x slower                                                                                                 |
| scimark_sparse_mat_mult    | 4.96 ms                                                                                                         | 5.38 ms: 1.08x slower                                                                                                 |
| pickle_pure_python         | 307 us                                                                                                          | 335 us: 1.09x slower                                                                                                  |
| async_generators           | 338 ms                                                                                                          | 369 ms: 1.09x slower                                                                                                  |
| many_optionals             | 1.04 ms                                                                                                         | 1.14 ms: 1.09x slower                                                                                                 |
| k_core                     | 2.03 sec                                                                                                        | 2.23 sec: 1.10x slower                                                                                                |
| pylint                     | 280 ms                                                                                                          | 308 ms: 1.10x slower                                                                                                  |
| scimark_fft                | 333 ms                                                                                                          | 367 ms: 1.10x slower                                                                                                  |
| unpickle_pure_python       | 208 us                                                                                                          | 230 us: 1.11x slower                                                                                                  |
| telco                      | 158 ms                                                                                                          | 175 ms: 1.11x slower                                                                                                  |
| pprint_safe_repr           | 695 ms                                                                                                          | 777 ms: 1.12x slower                                                                                                  |
| logging_silent             | 93.4 ns                                                                                                         | 105 ns: 1.12x slower                                                                                                  |
| chaos                      | 55.8 ms                                                                                                         | 62.7 ms: 1.12x slower                                                                                                 |
| hexiom                     | 5.67 ms                                                                                                         | 6.38 ms: 1.13x slower                                                                                                 |
| tomli_loads                | 1.91 sec                                                                                                        | 2.15 sec: 1.13x slower                                                                                                |
| pprint_pformat             | 1.42 sec                                                                                                        | 1.60 sec: 1.13x slower                                                                                                |
| spectral_norm              | 97.1 ms                                                                                                         | 110 ms: 1.13x slower                                                                                                  |
| nqueens                    | 77.3 ms                                                                                                         | 87.7 ms: 1.13x slower                                                                                                 |
| django_template            | 34.4 ms                                                                                                         | 39.0 ms: 1.13x slower                                                                                                 |
| mdp                        | 1.15 sec                                                                                                        | 1.31 sec: 1.14x slower                                                                                                |
| pyflate                    | 402 ms                                                                                                          | 457 ms: 1.14x slower                                                                                                  |
| 2to3                       | 249 ms                                                                                                          | 283 ms: 1.14x slower                                                                                                  |
| xml_etree_generate         | 83.3 ms                                                                                                         | 94.9 ms: 1.14x slower                                                                                                 |
| json_dumps                 | 10.8 ms                                                                                                         | 12.3 ms: 1.14x slower                                                                                                 |
| thrift                     | 765 us                                                                                                          | 874 us: 1.14x slower                                                                                                  |
| comprehensions             | 15.4 us                                                                                                         | 17.6 us: 1.14x slower                                                                                                 |
| scimark_sor                | 107 ms                                                                                                          | 123 ms: 1.14x slower                                                                                                  |
| subparsers                 | 25.2 ms                                                                                                         | 28.9 ms: 1.14x slower                                                                                                 |
| sympy_expand               | 459 ms                                                                                                          | 525 ms: 1.14x slower                                                                                                  |
| regex_compile              | 124 ms                                                                                                          | 142 ms: 1.15x slower                                                                                                  |
| logging_simple             | 5.97 us                                                                                                         | 6.85 us: 1.15x slower                                                                                                 |
| deepcopy                   | 251 us                                                                                                          | 290 us: 1.16x slower                                                                                                  |
| sqlglot_v2_optimize        | 50.2 ms                                                                                                         | 58.0 ms: 1.16x slower                                                                                                 |
| sympy_integrate            | 19.0 ms                                                                                                         | 22.0 ms: 1.16x slower                                                                                                 |
| sympy_str                  | 270 ms                                                                                                          | 313 ms: 1.16x slower                                                                                                  |
| scimark_lu                 | 112 ms                                                                                                          | 129 ms: 1.16x slower                                                                                                  |
| sympy_sum                  | 155 ms                                                                                                          | 180 ms: 1.16x slower                                                                                                  |
| sqlglot_v2_normalize       | 99.2 ms                                                                                                         | 115 ms: 1.16x slower                                                                                                  |
| logging_format             | 6.79 us                                                                                                         | 7.92 us: 1.17x slower                                                                                                 |
| deepcopy_reduce            | 2.63 us                                                                                                         | 3.07 us: 1.17x slower                                                                                                 |
| generators                 | 27.1 ms                                                                                                         | 31.7 ms: 1.17x slower                                                                                                 |
| fannkuch                   | 385 ms                                                                                                          | 454 ms: 1.18x slower                                                                                                  |
| genshi_xml                 | 48.6 ms                                                                                                         | 57.4 ms: 1.18x slower                                                                                                 |
| deepcopy_memo              | 29.0 us                                                                                                         | 34.3 us: 1.18x slower                                                                                                 |
| go                         | 102 ms                                                                                                          | 121 ms: 1.19x slower                                                                                                  |
| xml_etree_process          | 57.8 ms                                                                                                         | 68.8 ms: 1.19x slower                                                                                                 |
| deltablue                  | 2.99 ms                                                                                                         | 3.57 ms: 1.19x slower                                                                                                 |
| sqlglot_v2_transpile       | 1.52 ms                                                                                                         | 1.81 ms: 1.20x slower                                                                                                 |
| sqlglot_v2_parse           | 1.22 ms                                                                                                         | 1.46 ms: 1.20x slower                                                                                                 |
| meteor_contest             | 98.9 ms                                                                                                         | 119 ms: 1.21x slower                                                                                                  |
| shortest_path              | 441 ms                                                                                                          | 534 ms: 1.21x slower                                                                                                  |
| raytrace                   | 250 ms                                                                                                          | 303 ms: 1.21x slower                                                                                                  |
| typing_runtime_protocols   | 152 us                                                                                                          | 186 us: 1.22x slower                                                                                                  |
| connected_components       | 399 ms                                                                                                          | 494 ms: 1.24x slower                                                                                                  |
| scimark_monte_carlo        | 61.9 ms                                                                                                         | 77.8 ms: 1.26x slower                                                                                                 |
| genshi_text                | 20.8 ms                                                                                                         | 26.2 ms: 1.26x slower                                                                                                 |
| python_startup             | 12.6 ms                                                                                                         | 15.9 ms: 1.26x slower                                                                                                 |
| richards                   | 40.5 ms                                                                                                         | 51.3 ms: 1.27x slower                                                                                                 |
| crypto_pyaes               | 68.7 ms                                                                                                         | 87.0 ms: 1.27x slower                                                                                                 |
| richards_super             | 46.3 ms                                                                                                         | 59.0 ms: 1.27x slower                                                                                                 |
| python_startup_no_site     | 7.32 ms                                                                                                         | 9.53 ms: 1.30x slower                                                                                                 |
| coverage                   | 83.5 ms                                                                                                         | 111 ms: 1.33x slower                                                                                                  |
| mako                       | 11.5 ms                                                                                                         | 15.7 ms: 1.37x slower                                                                                                 |
| nbody                      | 89.3 ms                                                                                                         | 124 ms: 1.39x slower                                                                                                  |
| bench_thread_pool          | 1.06 ms                                                                                                         | 3.18 ms: 3.00x slower                                                                                                 |
| Geometric mean             | (ref)                                                                                                           | 1.11x slower                                                                                                          |

Benchmark hidden because not significant (2): async_tree_memoization, async_tree_none

- Geometric mean (including insignificant results): 1.092x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.20x