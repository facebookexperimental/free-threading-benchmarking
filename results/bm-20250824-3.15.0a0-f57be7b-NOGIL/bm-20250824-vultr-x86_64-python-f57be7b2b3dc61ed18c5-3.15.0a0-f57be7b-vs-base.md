# Results vs. base

- fork: python
- ref: f57be7b2b3dc61ed18c5
- machine: linux-x86_64
- commit hash: f57be7b
- commit date: 2025-08-24
- overall geometric mean: 1.097x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250824-3.15.0a0-f57be7b/bm-20250824-vultr-x86_64-python-f57be7b2b3dc61ed18c5-3.15.0a0-f57be7b.json | results/bm-20250824-3.15.0a0-f57be7b-NOGIL/bm-20250824-vultr-x86_64-python-f57be7b2b3dc61ed18c5-3.15.0a0-f57be7b.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 250 ms                                                                                                          | 284 ms: 1.14x slower                                                                                                  |
| docutils       | 2.54 sec                                                                                                        | 2.68 sec: 1.06x slower                                                                                                |
| html5lib       | 61.5 ms                                                                                                         | 66.9 ms: 1.09x slower                                                                                                 |
| sphinx         | 969 ms                                                                                                          | 1.06 sec: 1.09x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250824-3.15.0a0-f57be7b/bm-20250824-vultr-x86_64-python-f57be7b2b3dc61ed18c5-3.15.0a0-f57be7b.json | results/bm-20250824-3.15.0a0-f57be7b-NOGIL/bm-20250824-vultr-x86_64-python-f57be7b2b3dc61ed18c5-3.15.0a0-f57be7b.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 617 ms                                                                                                          | 514 ms: 1.20x faster                                                                                                  |
| async_tree_none_tg         | 254 ms                                                                                                          | 225 ms: 1.13x faster                                                                                                  |
| async_tree_memoization_tg  | 311 ms                                                                                                          | 281 ms: 1.11x faster                                                                                                  |
| async_tree_io              | 591 ms                                                                                                          | 542 ms: 1.09x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 512 ms                                                                                                          | 477 ms: 1.07x faster                                                                                                  |
| async_tree_memoization     | 313 ms                                                                                                          | 307 ms: 1.02x faster                                                                                                  |
| asyncio_websockets         | 517 ms                                                                                                          | 512 ms: 1.01x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 507 ms                                                                                                          | 504 ms: 1.01x faster                                                                                                  |
| coroutines                 | 23.8 ms                                                                                                         | 24.4 ms: 1.02x slower                                                                                                 |
| async_generators           | 343 ms                                                                                                          | 372 ms: 1.09x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.05x faster                                                                                                          |

Benchmark hidden because not significant (1): async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250824-3.15.0a0-f57be7b/bm-20250824-vultr-x86_64-python-f57be7b2b3dc61ed18c5-3.15.0a0-f57be7b.json | results/bm-20250824-3.15.0a0-f57be7b-NOGIL/bm-20250824-vultr-x86_64-python-f57be7b2b3dc61ed18c5-3.15.0a0-f57be7b.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 194 ms                                                                                                          | 187 ms: 1.04x faster                                                                                                  |
| float          | 72.2 ms                                                                                                         | 69.8 ms: 1.03x faster                                                                                                 |
| nbody          | 87.5 ms                                                                                                         | 126 ms: 1.44x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.10x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250824-3.15.0a0-f57be7b/bm-20250824-vultr-x86_64-python-f57be7b2b3dc61ed18c5-3.15.0a0-f57be7b.json | results/bm-20250824-3.15.0a0-f57be7b-NOGIL/bm-20250824-vultr-x86_64-python-f57be7b2b3dc61ed18c5-3.15.0a0-f57be7b.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.0 ms                                                                                                         | 20.8 ms: 1.01x faster                                                                                                 |
| regex_dna      | 165 ms                                                                                                          | 178 ms: 1.08x slower                                                                                                  |
| regex_effbot   | 2.58 ms                                                                                                         | 2.82 ms: 1.09x slower                                                                                                 |
| regex_compile  | 123 ms                                                                                                          | 143 ms: 1.16x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.08x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250824-3.15.0a0-f57be7b/bm-20250824-vultr-x86_64-python-f57be7b2b3dc61ed18c5-3.15.0a0-f57be7b.json | results/bm-20250824-3.15.0a0-f57be7b-NOGIL/bm-20250824-vultr-x86_64-python-f57be7b2b3dc61ed18c5-3.15.0a0-f57be7b.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 92.7 ms                                                                                                         | 87.1 ms: 1.06x faster                                                                                                 |
| pickle_pure_python   | 312 us                                                                                                          | 339 us: 1.09x slower                                                                                                  |
| json_dumps           | 9.69 ms                                                                                                         | 10.7 ms: 1.10x slower                                                                                                 |
| tomli_loads          | 1.93 sec                                                                                                        | 2.13 sec: 1.11x slower                                                                                                |
| json_loads           | 29.1 us                                                                                                         | 32.2 us: 1.11x slower                                                                                                 |
| unpickle_pure_python | 206 us                                                                                                          | 236 us: 1.15x slower                                                                                                  |
| xml_etree_generate   | 82.5 ms                                                                                                         | 96.2 ms: 1.17x slower                                                                                                 |
| xml_etree_process    | 58.3 ms                                                                                                         | 70.2 ms: 1.20x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250824-3.15.0a0-f57be7b/bm-20250824-vultr-x86_64-python-f57be7b2b3dc61ed18c5-3.15.0a0-f57be7b.json | results/bm-20250824-3.15.0a0-f57be7b-NOGIL/bm-20250824-vultr-x86_64-python-f57be7b2b3dc61ed18c5-3.15.0a0-f57be7b.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.5 ms                                                                                                         | 15.7 ms: 1.26x slower                                                                                                 |
| python_startup_no_site | 7.20 ms                                                                                                         | 9.53 ms: 1.32x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.29x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250824-3.15.0a0-f57be7b/bm-20250824-vultr-x86_64-python-f57be7b2b3dc61ed18c5-3.15.0a0-f57be7b.json | results/bm-20250824-3.15.0a0-f57be7b-NOGIL/bm-20250824-vultr-x86_64-python-f57be7b2b3dc61ed18c5-3.15.0a0-f57be7b.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 34.3 ms                                                                                                         | 40.1 ms: 1.17x slower                                                                                                 |
| genshi_xml      | 47.8 ms                                                                                                         | 58.6 ms: 1.23x slower                                                                                                 |
| genshi_text     | 20.7 ms                                                                                                         | 26.9 ms: 1.30x slower                                                                                                 |
| mako            | 11.8 ms                                                                                                         | 15.7 ms: 1.33x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.25x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20250824-3.15.0a0-f57be7b/bm-20250824-vultr-x86_64-python-f57be7b2b3dc61ed18c5-3.15.0a0-f57be7b.json | results/bm-20250824-3.15.0a0-f57be7b-NOGIL/bm-20250824-vultr-x86_64-python-f57be7b2b3dc61ed18c5-3.15.0a0-f57be7b.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.42 ms                                                                                                         | 1.95 ms: 2.27x faster                                                                                                 |
| create_gc_cycles           | 1.93 ms                                                                                                         | 1.52 ms: 1.27x faster                                                                                                 |
| async_tree_io_tg           | 617 ms                                                                                                          | 514 ms: 1.20x faster                                                                                                  |
| async_tree_none_tg         | 254 ms                                                                                                          | 225 ms: 1.13x faster                                                                                                  |
| async_tree_memoization_tg  | 311 ms                                                                                                          | 281 ms: 1.11x faster                                                                                                  |
| async_tree_io              | 591 ms                                                                                                          | 542 ms: 1.09x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 512 ms                                                                                                          | 477 ms: 1.07x faster                                                                                                  |
| sqlite_synth               | 2.22 us                                                                                                         | 2.07 us: 1.07x faster                                                                                                 |
| xml_etree_iterparse        | 92.7 ms                                                                                                         | 87.1 ms: 1.06x faster                                                                                                 |
| pidigits                   | 194 ms                                                                                                          | 187 ms: 1.04x faster                                                                                                  |
| float                      | 72.2 ms                                                                                                         | 69.8 ms: 1.03x faster                                                                                                 |
| async_tree_memoization     | 313 ms                                                                                                          | 307 ms: 1.02x faster                                                                                                  |
| asyncio_websockets         | 517 ms                                                                                                          | 512 ms: 1.01x faster                                                                                                  |
| regex_v8                   | 21.0 ms                                                                                                         | 20.8 ms: 1.01x faster                                                                                                 |
| async_tree_cpu_io_mixed    | 507 ms                                                                                                          | 504 ms: 1.01x faster                                                                                                  |
| logging_silent             | 99.2 ns                                                                                                         | 101 ns: 1.02x slower                                                                                                  |
| pathlib                    | 18.8 ms                                                                                                         | 19.2 ms: 1.02x slower                                                                                                 |
| coroutines                 | 23.8 ms                                                                                                         | 24.4 ms: 1.02x slower                                                                                                 |
| json                       | 5.30 ms                                                                                                         | 5.46 ms: 1.03x slower                                                                                                 |
| bpe_tokeniser              | 4.23 sec                                                                                                        | 4.40 sec: 1.04x slower                                                                                                |
| docutils                   | 2.54 sec                                                                                                        | 2.68 sec: 1.06x slower                                                                                                |
| bench_mp_pool              | 103 ms                                                                                                          | 109 ms: 1.06x slower                                                                                                  |
| dulwich_log                | 66.5 ms                                                                                                         | 70.9 ms: 1.07x slower                                                                                                 |
| regex_dna                  | 165 ms                                                                                                          | 178 ms: 1.08x slower                                                                                                  |
| pickle_pure_python         | 312 us                                                                                                          | 339 us: 1.09x slower                                                                                                  |
| html5lib                   | 61.5 ms                                                                                                         | 66.9 ms: 1.09x slower                                                                                                 |
| pycparser                  | 1.08 sec                                                                                                        | 1.18 sec: 1.09x slower                                                                                                |
| async_generators           | 343 ms                                                                                                          | 372 ms: 1.09x slower                                                                                                  |
| regex_effbot               | 2.58 ms                                                                                                         | 2.82 ms: 1.09x slower                                                                                                 |
| sphinx                     | 969 ms                                                                                                          | 1.06 sec: 1.09x slower                                                                                                |
| pylint                     | 280 ms                                                                                                          | 308 ms: 1.10x slower                                                                                                  |
| telco                      | 159 ms                                                                                                          | 175 ms: 1.10x slower                                                                                                  |
| json_dumps                 | 9.69 ms                                                                                                         | 10.7 ms: 1.10x slower                                                                                                 |
| tomli_loads                | 1.93 sec                                                                                                        | 2.13 sec: 1.11x slower                                                                                                |
| json_loads                 | 29.1 us                                                                                                         | 32.2 us: 1.11x slower                                                                                                 |
| k_core                     | 2.02 sec                                                                                                        | 2.24 sec: 1.11x slower                                                                                                |
| scimark_sor                | 110 ms                                                                                                          | 122 ms: 1.11x slower                                                                                                  |
| many_optionals             | 1.20 ms                                                                                                         | 1.33 ms: 1.11x slower                                                                                                 |
| scimark_fft                | 333 ms                                                                                                          | 372 ms: 1.12x slower                                                                                                  |
| chaos                      | 56.2 ms                                                                                                         | 63.8 ms: 1.14x slower                                                                                                 |
| 2to3                       | 250 ms                                                                                                          | 284 ms: 1.14x slower                                                                                                  |
| generators                 | 28.4 ms                                                                                                         | 32.5 ms: 1.14x slower                                                                                                 |
| sympy_expand               | 458 ms                                                                                                          | 523 ms: 1.14x slower                                                                                                  |
| mdp                        | 1.15 sec                                                                                                        | 1.32 sec: 1.14x slower                                                                                                |
| hexiom                     | 5.65 ms                                                                                                         | 6.46 ms: 1.14x slower                                                                                                 |
| unpickle_pure_python       | 206 us                                                                                                          | 236 us: 1.15x slower                                                                                                  |
| pyflate                    | 404 ms                                                                                                          | 463 ms: 1.15x slower                                                                                                  |
| nqueens                    | 77.8 ms                                                                                                         | 89.2 ms: 1.15x slower                                                                                                 |
| comprehensions             | 15.5 us                                                                                                         | 17.9 us: 1.15x slower                                                                                                 |
| sqlglot_v2_optimize        | 50.1 ms                                                                                                         | 57.9 ms: 1.15x slower                                                                                                 |
| pprint_safe_repr           | 683 ms                                                                                                          | 790 ms: 1.16x slower                                                                                                  |
| subparsers                 | 42.4 ms                                                                                                         | 49.1 ms: 1.16x slower                                                                                                 |
| regex_compile              | 123 ms                                                                                                          | 143 ms: 1.16x slower                                                                                                  |
| spectral_norm              | 95.6 ms                                                                                                         | 111 ms: 1.16x slower                                                                                                  |
| sympy_str                  | 270 ms                                                                                                          | 313 ms: 1.16x slower                                                                                                  |
| sqlglot_v2_normalize       | 98.8 ms                                                                                                         | 115 ms: 1.16x slower                                                                                                  |
| pprint_pformat             | 1.40 sec                                                                                                        | 1.63 sec: 1.16x slower                                                                                                |
| deltablue                  | 3.07 ms                                                                                                         | 3.58 ms: 1.16x slower                                                                                                 |
| thrift                     | 742 us                                                                                                          | 864 us: 1.16x slower                                                                                                  |
| xml_etree_generate         | 82.5 ms                                                                                                         | 96.2 ms: 1.17x slower                                                                                                 |
| logging_format             | 6.60 us                                                                                                         | 7.71 us: 1.17x slower                                                                                                 |
| go                         | 104 ms                                                                                                          | 122 ms: 1.17x slower                                                                                                  |
| django_template            | 34.3 ms                                                                                                         | 40.1 ms: 1.17x slower                                                                                                 |
| sympy_sum                  | 153 ms                                                                                                          | 179 ms: 1.17x slower                                                                                                  |
| logging_simple             | 5.81 us                                                                                                         | 6.81 us: 1.17x slower                                                                                                 |
| fannkuch                   | 385 ms                                                                                                          | 453 ms: 1.18x slower                                                                                                  |
| sympy_integrate            | 18.8 ms                                                                                                         | 22.1 ms: 1.18x slower                                                                                                 |
| deepcopy_reduce            | 2.63 us                                                                                                         | 3.11 us: 1.18x slower                                                                                                 |
| deepcopy                   | 253 us                                                                                                          | 300 us: 1.19x slower                                                                                                  |
| raytrace                   | 249 ms                                                                                                          | 299 ms: 1.20x slower                                                                                                  |
| sqlglot_v2_transpile       | 1.53 ms                                                                                                         | 1.84 ms: 1.20x slower                                                                                                 |
| xml_etree_process          | 58.3 ms                                                                                                         | 70.2 ms: 1.20x slower                                                                                                 |
| scimark_lu                 | 109 ms                                                                                                          | 133 ms: 1.21x slower                                                                                                  |
| meteor_contest             | 98.8 ms                                                                                                         | 120 ms: 1.21x slower                                                                                                  |
| shortest_path              | 438 ms                                                                                                          | 534 ms: 1.22x slower                                                                                                  |
| sqlglot_v2_parse           | 1.22 ms                                                                                                         | 1.50 ms: 1.22x slower                                                                                                 |
| scimark_sparse_mat_mult    | 4.57 ms                                                                                                         | 5.59 ms: 1.22x slower                                                                                                 |
| genshi_xml                 | 47.8 ms                                                                                                         | 58.6 ms: 1.23x slower                                                                                                 |
| deepcopy_memo              | 28.9 us                                                                                                         | 35.5 us: 1.23x slower                                                                                                 |
| connected_components       | 396 ms                                                                                                          | 490 ms: 1.24x slower                                                                                                  |
| typing_runtime_protocols   | 152 us                                                                                                          | 189 us: 1.24x slower                                                                                                  |
| python_startup             | 12.5 ms                                                                                                         | 15.7 ms: 1.26x slower                                                                                                 |
| crypto_pyaes               | 68.5 ms                                                                                                         | 86.2 ms: 1.26x slower                                                                                                 |
| richards                   | 40.9 ms                                                                                                         | 52.3 ms: 1.28x slower                                                                                                 |
| scimark_monte_carlo        | 61.5 ms                                                                                                         | 78.9 ms: 1.28x slower                                                                                                 |
| richards_super             | 46.7 ms                                                                                                         | 60.7 ms: 1.30x slower                                                                                                 |
| genshi_text                | 20.7 ms                                                                                                         | 26.9 ms: 1.30x slower                                                                                                 |
| python_startup_no_site     | 7.20 ms                                                                                                         | 9.53 ms: 1.32x slower                                                                                                 |
| mako                       | 11.8 ms                                                                                                         | 15.7 ms: 1.33x slower                                                                                                 |
| coverage                   | 82.1 ms                                                                                                         | 112 ms: 1.36x slower                                                                                                  |
| nbody                      | 87.5 ms                                                                                                         | 126 ms: 1.44x slower                                                                                                  |
| bench_thread_pool          | 1.01 ms                                                                                                         | 3.11 ms: 3.09x slower                                                                                                 |
| Geometric mean             | (ref)                                                                                                           | 1.12x slower                                                                                                          |

Benchmark hidden because not significant (2): async_tree_none, xml_etree_parse

- Geometric mean (including insignificant results): 1.097x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.20x