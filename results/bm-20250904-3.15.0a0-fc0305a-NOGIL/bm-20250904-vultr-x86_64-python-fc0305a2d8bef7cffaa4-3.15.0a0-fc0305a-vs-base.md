# Results vs. base

- fork: python
- ref: fc0305a2d8bef7cffaa4
- machine: linux-x86_64
- commit hash: fc0305a
- commit date: 2025-09-04
- overall geometric mean: 1.093x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250904-3.15.0a0-fc0305a/bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a.json | results/bm-20250904-3.15.0a0-fc0305a-NOGIL/bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 251 ms                                                                                                          | 283 ms: 1.13x slower                                                                                                  |
| docutils       | 2.55 sec                                                                                                        | 2.70 sec: 1.06x slower                                                                                                |
| html5lib       | 61.5 ms                                                                                                         | 68.3 ms: 1.11x slower                                                                                                 |
| sphinx         | 970 ms                                                                                                          | 1.05 sec: 1.08x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250904-3.15.0a0-fc0305a/bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a.json | results/bm-20250904-3.15.0a0-fc0305a-NOGIL/bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 622 ms                                                                                                          | 511 ms: 1.22x faster                                                                                                  |
| async_tree_io              | 609 ms                                                                                                          | 540 ms: 1.13x faster                                                                                                  |
| async_tree_memoization_tg  | 316 ms                                                                                                          | 281 ms: 1.12x faster                                                                                                  |
| async_tree_none_tg         | 252 ms                                                                                                          | 234 ms: 1.08x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 509 ms                                                                                                          | 481 ms: 1.06x faster                                                                                                  |
| async_tree_none            | 268 ms                                                                                                          | 254 ms: 1.05x faster                                                                                                  |
| async_tree_memoization     | 313 ms                                                                                                          | 308 ms: 1.02x faster                                                                                                  |
| asyncio_websockets         | 517 ms                                                                                                          | 512 ms: 1.01x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 511 ms                                                                                                          | 507 ms: 1.01x faster                                                                                                  |
| coroutines                 | 22.9 ms                                                                                                         | 24.2 ms: 1.06x slower                                                                                                 |
| async_generators           | 343 ms                                                                                                          | 372 ms: 1.08x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.05x faster                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250904-3.15.0a0-fc0305a/bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a.json | results/bm-20250904-3.15.0a0-fc0305a-NOGIL/bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 207 ms                                                                                                          | 199 ms: 1.04x faster                                                                                                  |
| float          | 72.4 ms                                                                                                         | 71.4 ms: 1.01x faster                                                                                                 |
| nbody          | 92.4 ms                                                                                                         | 123 ms: 1.33x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.08x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250904-3.15.0a0-fc0305a/bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a.json | results/bm-20250904-3.15.0a0-fc0305a-NOGIL/bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.8 ms                                                                                                         | 20.4 ms: 1.07x faster                                                                                                 |
| regex_dna      | 168 ms                                                                                                          | 180 ms: 1.07x slower                                                                                                  |
| regex_effbot   | 2.57 ms                                                                                                         | 2.76 ms: 1.07x slower                                                                                                 |
| regex_compile  | 123 ms                                                                                                          | 144 ms: 1.17x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.06x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250904-3.15.0a0-fc0305a/bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a.json | results/bm-20250904-3.15.0a0-fc0305a-NOGIL/bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 92.8 ms                                                                                                         | 87.0 ms: 1.07x faster                                                                                                 |
| xml_etree_parse      | 132 ms                                                                                                          | 130 ms: 1.02x faster                                                                                                  |
| tomli_loads          | 1.89 sec                                                                                                        | 2.06 sec: 1.09x slower                                                                                                |
| pickle_pure_python   | 305 us                                                                                                          | 337 us: 1.10x slower                                                                                                  |
| unpickle_pure_python | 209 us                                                                                                          | 232 us: 1.11x slower                                                                                                  |
| json_loads           | 28.0 us                                                                                                         | 31.5 us: 1.13x slower                                                                                                 |
| json_dumps           | 9.59 ms                                                                                                         | 11.0 ms: 1.15x slower                                                                                                 |
| xml_etree_generate   | 82.8 ms                                                                                                         | 96.1 ms: 1.16x slower                                                                                                 |
| xml_etree_process    | 58.1 ms                                                                                                         | 69.2 ms: 1.19x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250904-3.15.0a0-fc0305a/bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a.json | results/bm-20250904-3.15.0a0-fc0305a-NOGIL/bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.5 ms                                                                                                         | 15.7 ms: 1.26x slower                                                                                                 |
| python_startup_no_site | 7.27 ms                                                                                                         | 9.57 ms: 1.32x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.29x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250904-3.15.0a0-fc0305a/bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a.json | results/bm-20250904-3.15.0a0-fc0305a-NOGIL/bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 34.6 ms                                                                                                         | 40.0 ms: 1.16x slower                                                                                                 |
| genshi_xml      | 48.7 ms                                                                                                         | 59.1 ms: 1.21x slower                                                                                                 |
| genshi_text     | 20.4 ms                                                                                                         | 27.0 ms: 1.32x slower                                                                                                 |
| mako            | 11.5 ms                                                                                                         | 15.8 ms: 1.38x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.27x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20250904-3.15.0a0-fc0305a/bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a.json | results/bm-20250904-3.15.0a0-fc0305a-NOGIL/bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.65 ms                                                                                                         | 1.94 ms: 2.40x faster                                                                                                 |
| create_gc_cycles           | 1.93 ms                                                                                                         | 1.51 ms: 1.28x faster                                                                                                 |
| async_tree_io_tg           | 622 ms                                                                                                          | 511 ms: 1.22x faster                                                                                                  |
| async_tree_io              | 609 ms                                                                                                          | 540 ms: 1.13x faster                                                                                                  |
| async_tree_memoization_tg  | 316 ms                                                                                                          | 281 ms: 1.12x faster                                                                                                  |
| sqlite_synth               | 2.31 us                                                                                                         | 2.06 us: 1.12x faster                                                                                                 |
| async_tree_none_tg         | 252 ms                                                                                                          | 234 ms: 1.08x faster                                                                                                  |
| regex_v8                   | 21.8 ms                                                                                                         | 20.4 ms: 1.07x faster                                                                                                 |
| xml_etree_iterparse        | 92.8 ms                                                                                                         | 87.0 ms: 1.07x faster                                                                                                 |
| async_tree_cpu_io_mixed_tg | 509 ms                                                                                                          | 481 ms: 1.06x faster                                                                                                  |
| async_tree_none            | 268 ms                                                                                                          | 254 ms: 1.05x faster                                                                                                  |
| pidigits                   | 207 ms                                                                                                          | 199 ms: 1.04x faster                                                                                                  |
| xml_etree_parse            | 132 ms                                                                                                          | 130 ms: 1.02x faster                                                                                                  |
| async_tree_memoization     | 313 ms                                                                                                          | 308 ms: 1.02x faster                                                                                                  |
| float                      | 72.4 ms                                                                                                         | 71.4 ms: 1.01x faster                                                                                                 |
| asyncio_websockets         | 517 ms                                                                                                          | 512 ms: 1.01x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 511 ms                                                                                                          | 507 ms: 1.01x faster                                                                                                  |
| pathlib                    | 18.8 ms                                                                                                         | 19.2 ms: 1.02x slower                                                                                                 |
| bench_mp_pool              | 97.8 ms                                                                                                         | 102 ms: 1.04x slower                                                                                                  |
| pycparser                  | 1.09 sec                                                                                                        | 1.14 sec: 1.05x slower                                                                                                |
| coroutines                 | 22.9 ms                                                                                                         | 24.2 ms: 1.06x slower                                                                                                 |
| bpe_tokeniser              | 4.18 sec                                                                                                        | 4.42 sec: 1.06x slower                                                                                                |
| docutils                   | 2.55 sec                                                                                                        | 2.70 sec: 1.06x slower                                                                                                |
| regex_dna                  | 168 ms                                                                                                          | 180 ms: 1.07x slower                                                                                                  |
| dulwich_log                | 66.6 ms                                                                                                         | 71.5 ms: 1.07x slower                                                                                                 |
| deltablue                  | 3.29 ms                                                                                                         | 3.53 ms: 1.07x slower                                                                                                 |
| regex_effbot               | 2.57 ms                                                                                                         | 2.76 ms: 1.07x slower                                                                                                 |
| sphinx                     | 970 ms                                                                                                          | 1.05 sec: 1.08x slower                                                                                                |
| logging_silent             | 97.8 ns                                                                                                         | 106 ns: 1.08x slower                                                                                                  |
| async_generators           | 343 ms                                                                                                          | 372 ms: 1.08x slower                                                                                                  |
| json                       | 5.01 ms                                                                                                         | 5.46 ms: 1.09x slower                                                                                                 |
| tomli_loads                | 1.89 sec                                                                                                        | 2.06 sec: 1.09x slower                                                                                                |
| pylint                     | 280 ms                                                                                                          | 309 ms: 1.10x slower                                                                                                  |
| pickle_pure_python         | 305 us                                                                                                          | 337 us: 1.10x slower                                                                                                  |
| unpickle_pure_python       | 209 us                                                                                                          | 232 us: 1.11x slower                                                                                                  |
| k_core                     | 2.02 sec                                                                                                        | 2.24 sec: 1.11x slower                                                                                                |
| html5lib                   | 61.5 ms                                                                                                         | 68.3 ms: 1.11x slower                                                                                                 |
| telco                      | 158 ms                                                                                                          | 175 ms: 1.11x slower                                                                                                  |
| scimark_fft                | 331 ms                                                                                                          | 371 ms: 1.12x slower                                                                                                  |
| scimark_sor                | 109 ms                                                                                                          | 123 ms: 1.12x slower                                                                                                  |
| pprint_safe_repr           | 696 ms                                                                                                          | 782 ms: 1.12x slower                                                                                                  |
| many_optionals             | 1.21 ms                                                                                                         | 1.36 ms: 1.12x slower                                                                                                 |
| 2to3                       | 251 ms                                                                                                          | 283 ms: 1.13x slower                                                                                                  |
| json_loads                 | 28.0 us                                                                                                         | 31.5 us: 1.13x slower                                                                                                 |
| chaos                      | 56.5 ms                                                                                                         | 63.6 ms: 1.13x slower                                                                                                 |
| sympy_expand               | 462 ms                                                                                                          | 521 ms: 1.13x slower                                                                                                  |
| comprehensions             | 15.7 us                                                                                                         | 17.8 us: 1.13x slower                                                                                                 |
| generators                 | 28.9 ms                                                                                                         | 32.8 ms: 1.13x slower                                                                                                 |
| pyflate                    | 402 ms                                                                                                          | 459 ms: 1.14x slower                                                                                                  |
| scimark_sparse_mat_mult    | 4.77 ms                                                                                                         | 5.45 ms: 1.14x slower                                                                                                 |
| nqueens                    | 77.1 ms                                                                                                         | 88.2 ms: 1.14x slower                                                                                                 |
| hexiom                     | 5.59 ms                                                                                                         | 6.41 ms: 1.15x slower                                                                                                 |
| json_dumps                 | 9.59 ms                                                                                                         | 11.0 ms: 1.15x slower                                                                                                 |
| pprint_pformat             | 1.41 sec                                                                                                        | 1.62 sec: 1.15x slower                                                                                                |
| mdp                        | 1.15 sec                                                                                                        | 1.32 sec: 1.15x slower                                                                                                |
| subparsers                 | 42.7 ms                                                                                                         | 49.2 ms: 1.15x slower                                                                                                 |
| django_template            | 34.6 ms                                                                                                         | 40.0 ms: 1.16x slower                                                                                                 |
| deepcopy                   | 242 us                                                                                                          | 280 us: 1.16x slower                                                                                                  |
| sympy_sum                  | 154 ms                                                                                                          | 178 ms: 1.16x slower                                                                                                  |
| sympy_str                  | 269 ms                                                                                                          | 312 ms: 1.16x slower                                                                                                  |
| xml_etree_generate         | 82.8 ms                                                                                                         | 96.1 ms: 1.16x slower                                                                                                 |
| go                         | 104 ms                                                                                                          | 121 ms: 1.16x slower                                                                                                  |
| deepcopy_memo              | 26.6 us                                                                                                         | 31.1 us: 1.17x slower                                                                                                 |
| sympy_integrate            | 18.9 ms                                                                                                         | 22.0 ms: 1.17x slower                                                                                                 |
| regex_compile              | 123 ms                                                                                                          | 144 ms: 1.17x slower                                                                                                  |
| sqlglot_v2_optimize        | 49.9 ms                                                                                                         | 58.5 ms: 1.17x slower                                                                                                 |
| deepcopy_reduce            | 2.57 us                                                                                                         | 3.01 us: 1.17x slower                                                                                                 |
| sqlglot_v2_normalize       | 99.4 ms                                                                                                         | 117 ms: 1.18x slower                                                                                                  |
| scimark_lu                 | 109 ms                                                                                                          | 129 ms: 1.18x slower                                                                                                  |
| logging_simple             | 5.81 us                                                                                                         | 6.88 us: 1.19x slower                                                                                                 |
| thrift                     | 750 us                                                                                                          | 889 us: 1.19x slower                                                                                                  |
| xml_etree_process          | 58.1 ms                                                                                                         | 69.2 ms: 1.19x slower                                                                                                 |
| fannkuch                   | 380 ms                                                                                                          | 454 ms: 1.19x slower                                                                                                  |
| meteor_contest             | 99.8 ms                                                                                                         | 119 ms: 1.19x slower                                                                                                  |
| sqlglot_v2_transpile       | 1.51 ms                                                                                                         | 1.81 ms: 1.20x slower                                                                                                 |
| logging_format             | 6.50 us                                                                                                         | 7.81 us: 1.20x slower                                                                                                 |
| raytrace                   | 253 ms                                                                                                          | 305 ms: 1.21x slower                                                                                                  |
| genshi_xml                 | 48.7 ms                                                                                                         | 59.1 ms: 1.21x slower                                                                                                 |
| shortest_path              | 442 ms                                                                                                          | 539 ms: 1.22x slower                                                                                                  |
| sqlglot_v2_parse           | 1.21 ms                                                                                                         | 1.48 ms: 1.22x slower                                                                                                 |
| spectral_norm              | 92.9 ms                                                                                                         | 115 ms: 1.23x slower                                                                                                  |
| typing_runtime_protocols   | 152 us                                                                                                          | 189 us: 1.24x slower                                                                                                  |
| connected_components       | 402 ms                                                                                                          | 501 ms: 1.25x slower                                                                                                  |
| richards                   | 41.5 ms                                                                                                         | 51.9 ms: 1.25x slower                                                                                                 |
| richards_super             | 47.4 ms                                                                                                         | 59.6 ms: 1.26x slower                                                                                                 |
| python_startup             | 12.5 ms                                                                                                         | 15.7 ms: 1.26x slower                                                                                                 |
| scimark_monte_carlo        | 61.5 ms                                                                                                         | 77.9 ms: 1.27x slower                                                                                                 |
| crypto_pyaes               | 67.7 ms                                                                                                         | 86.4 ms: 1.28x slower                                                                                                 |
| python_startup_no_site     | 7.27 ms                                                                                                         | 9.57 ms: 1.32x slower                                                                                                 |
| genshi_text                | 20.4 ms                                                                                                         | 27.0 ms: 1.32x slower                                                                                                 |
| nbody                      | 92.4 ms                                                                                                         | 123 ms: 1.33x slower                                                                                                  |
| coverage                   | 81.0 ms                                                                                                         | 111 ms: 1.37x slower                                                                                                  |
| mako                       | 11.5 ms                                                                                                         | 15.8 ms: 1.38x slower                                                                                                 |
| bench_thread_pool          | 1.01 ms                                                                                                         | 3.10 ms: 3.06x slower                                                                                                 |
| Geometric mean             | (ref)                                                                                                           | 1.11x slower                                                                                                          |

- Geometric mean (including insignificant results): 1.093x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.21x