# Results vs. base

- fork: python
- ref: 3e06cfcaeee31c2a6e9b
- machine: linux-x86_64
- commit hash: 3e06cfc
- commit date: 2025-09-14
- overall geometric mean: 1.094x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250914-3.15.0a0-3e06cfc/bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc.json | results/bm-20250914-3.15.0a0-3e06cfc-NOGIL/bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 251 ms                                                                                                          | 281 ms: 1.12x slower                                                                                                  |
| docutils       | 2.53 sec                                                                                                        | 2.68 sec: 1.06x slower                                                                                                |
| html5lib       | 61.3 ms                                                                                                         | 66.8 ms: 1.09x slower                                                                                                 |
| sphinx         | 960 ms                                                                                                          | 1.04 sec: 1.08x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250914-3.15.0a0-3e06cfc/bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc.json | results/bm-20250914-3.15.0a0-3e06cfc-NOGIL/bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 621 ms                                                                                                          | 517 ms: 1.20x faster                                                                                                  |
| async_tree_none_tg         | 253 ms                                                                                                          | 223 ms: 1.14x faster                                                                                                  |
| async_tree_memoization_tg  | 316 ms                                                                                                          | 280 ms: 1.13x faster                                                                                                  |
| async_tree_io              | 605 ms                                                                                                          | 543 ms: 1.11x faster                                                                                                  |
| async_tree_none            | 267 ms                                                                                                          | 257 ms: 1.04x faster                                                                                                  |
| async_tree_memoization     | 314 ms                                                                                                          | 308 ms: 1.02x faster                                                                                                  |
| asyncio_websockets         | 522 ms                                                                                                          | 512 ms: 1.02x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 494 ms                                                                                                          | 487 ms: 1.02x faster                                                                                                  |
| coroutines                 | 23.2 ms                                                                                                         | 24.2 ms: 1.04x slower                                                                                                 |
| async_tree_cpu_io_mixed    | 493 ms                                                                                                          | 515 ms: 1.04x slower                                                                                                  |
| async_generators           | 347 ms                                                                                                          | 368 ms: 1.06x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.05x faster                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250914-3.15.0a0-3e06cfc/bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc.json | results/bm-20250914-3.15.0a0-3e06cfc-NOGIL/bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| float          | 71.5 ms                                                                                                         | 70.1 ms: 1.02x faster                                                                                                 |
| pidigits       | 193 ms                                                                                                          | 194 ms: 1.01x slower                                                                                                  |
| nbody          | 89.3 ms                                                                                                         | 124 ms: 1.38x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.11x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250914-3.15.0a0-3e06cfc/bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc.json | results/bm-20250914-3.15.0a0-3e06cfc-NOGIL/bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_dna      | 166 ms                                                                                                          | 159 ms: 1.05x faster                                                                                                  |
| regex_v8       | 20.7 ms                                                                                                         | 20.1 ms: 1.03x faster                                                                                                 |
| regex_effbot   | 2.56 ms                                                                                                         | 2.51 ms: 1.02x faster                                                                                                 |
| regex_compile  | 123 ms                                                                                                          | 143 ms: 1.16x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.01x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250914-3.15.0a0-3e06cfc/bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc.json | results/bm-20250914-3.15.0a0-3e06cfc-NOGIL/bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 92.8 ms                                                                                                         | 87.0 ms: 1.07x faster                                                                                                 |
| tomli_loads          | 1.89 sec                                                                                                        | 2.01 sec: 1.06x slower                                                                                                |
| unpickle_pure_python | 208 us                                                                                                          | 232 us: 1.12x slower                                                                                                  |
| json_loads           | 28.0 us                                                                                                         | 31.4 us: 1.12x slower                                                                                                 |
| json_dumps           | 9.57 ms                                                                                                         | 11.0 ms: 1.15x slower                                                                                                 |
| pickle_pure_python   | 301 us                                                                                                          | 347 us: 1.15x slower                                                                                                  |
| xml_etree_generate   | 83.7 ms                                                                                                         | 98.7 ms: 1.18x slower                                                                                                 |
| xml_etree_process    | 58.2 ms                                                                                                         | 70.9 ms: 1.22x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.10x slower                                                                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250914-3.15.0a0-3e06cfc/bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc.json | results/bm-20250914-3.15.0a0-3e06cfc-NOGIL/bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.5 ms                                                                                                         | 15.7 ms: 1.26x slower                                                                                                 |
| python_startup_no_site | 7.24 ms                                                                                                         | 9.57 ms: 1.32x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.29x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250914-3.15.0a0-3e06cfc/bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc.json | results/bm-20250914-3.15.0a0-3e06cfc-NOGIL/bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                                                         | 41.1 ms: 1.20x slower                                                                                                 |
| genshi_xml      | 48.4 ms                                                                                                         | 59.0 ms: 1.22x slower                                                                                                 |
| genshi_text     | 20.6 ms                                                                                                         | 26.6 ms: 1.29x slower                                                                                                 |
| mako            | 11.6 ms                                                                                                         | 15.7 ms: 1.36x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.26x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20250914-3.15.0a0-3e06cfc/bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc.json | results/bm-20250914-3.15.0a0-3e06cfc-NOGIL/bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.68 ms                                                                                                         | 1.95 ms: 2.40x faster                                                                                                 |
| create_gc_cycles           | 1.92 ms                                                                                                         | 1.52 ms: 1.26x faster                                                                                                 |
| async_tree_io_tg           | 621 ms                                                                                                          | 517 ms: 1.20x faster                                                                                                  |
| async_tree_none_tg         | 253 ms                                                                                                          | 223 ms: 1.14x faster                                                                                                  |
| async_tree_memoization_tg  | 316 ms                                                                                                          | 280 ms: 1.13x faster                                                                                                  |
| async_tree_io              | 605 ms                                                                                                          | 543 ms: 1.11x faster                                                                                                  |
| sqlite_synth               | 2.31 us                                                                                                         | 2.09 us: 1.11x faster                                                                                                 |
| xml_etree_iterparse        | 92.8 ms                                                                                                         | 87.0 ms: 1.07x faster                                                                                                 |
| regex_dna                  | 166 ms                                                                                                          | 159 ms: 1.05x faster                                                                                                  |
| async_tree_none            | 267 ms                                                                                                          | 257 ms: 1.04x faster                                                                                                  |
| regex_v8                   | 20.7 ms                                                                                                         | 20.1 ms: 1.03x faster                                                                                                 |
| regex_effbot               | 2.56 ms                                                                                                         | 2.51 ms: 1.02x faster                                                                                                 |
| async_tree_memoization     | 314 ms                                                                                                          | 308 ms: 1.02x faster                                                                                                  |
| asyncio_websockets         | 522 ms                                                                                                          | 512 ms: 1.02x faster                                                                                                  |
| float                      | 71.5 ms                                                                                                         | 70.1 ms: 1.02x faster                                                                                                 |
| async_tree_cpu_io_mixed_tg | 494 ms                                                                                                          | 487 ms: 1.02x faster                                                                                                  |
| pidigits                   | 193 ms                                                                                                          | 194 ms: 1.01x slower                                                                                                  |
| pathlib                    | 18.0 ms                                                                                                         | 18.1 ms: 1.01x slower                                                                                                 |
| coroutines                 | 23.2 ms                                                                                                         | 24.2 ms: 1.04x slower                                                                                                 |
| async_tree_cpu_io_mixed    | 493 ms                                                                                                          | 515 ms: 1.04x slower                                                                                                  |
| bpe_tokeniser              | 4.18 sec                                                                                                        | 4.40 sec: 1.05x slower                                                                                                |
| docutils                   | 2.53 sec                                                                                                        | 2.68 sec: 1.06x slower                                                                                                |
| async_generators           | 347 ms                                                                                                          | 368 ms: 1.06x slower                                                                                                  |
| tomli_loads                | 1.89 sec                                                                                                        | 2.01 sec: 1.06x slower                                                                                                |
| json                       | 5.06 ms                                                                                                         | 5.40 ms: 1.07x slower                                                                                                 |
| pycparser                  | 1.10 sec                                                                                                        | 1.17 sec: 1.07x slower                                                                                                |
| logging_silent             | 96.1 ns                                                                                                         | 103 ns: 1.07x slower                                                                                                  |
| sphinx                     | 960 ms                                                                                                          | 1.04 sec: 1.08x slower                                                                                                |
| dulwich_log                | 66.5 ms                                                                                                         | 72.1 ms: 1.08x slower                                                                                                 |
| scimark_fft                | 339 ms                                                                                                          | 369 ms: 1.09x slower                                                                                                  |
| html5lib                   | 61.3 ms                                                                                                         | 66.8 ms: 1.09x slower                                                                                                 |
| k_core                     | 2.03 sec                                                                                                        | 2.23 sec: 1.10x slower                                                                                                |
| pylint                     | 279 ms                                                                                                          | 307 ms: 1.10x slower                                                                                                  |
| deltablue                  | 3.24 ms                                                                                                         | 3.58 ms: 1.10x slower                                                                                                 |
| chaos                      | 57.4 ms                                                                                                         | 63.5 ms: 1.11x slower                                                                                                 |
| telco                      | 157 ms                                                                                                          | 175 ms: 1.11x slower                                                                                                  |
| unpickle_pure_python       | 208 us                                                                                                          | 232 us: 1.12x slower                                                                                                  |
| generators                 | 27.7 ms                                                                                                         | 30.9 ms: 1.12x slower                                                                                                 |
| json_loads                 | 28.0 us                                                                                                         | 31.4 us: 1.12x slower                                                                                                 |
| 2to3                       | 251 ms                                                                                                          | 281 ms: 1.12x slower                                                                                                  |
| many_optionals             | 1.20 ms                                                                                                         | 1.35 ms: 1.13x slower                                                                                                 |
| nqueens                    | 77.7 ms                                                                                                         | 87.7 ms: 1.13x slower                                                                                                 |
| comprehensions             | 15.5 us                                                                                                         | 17.6 us: 1.13x slower                                                                                                 |
| mdp                        | 1.15 sec                                                                                                        | 1.31 sec: 1.13x slower                                                                                                |
| pyflate                    | 404 ms                                                                                                          | 459 ms: 1.14x slower                                                                                                  |
| scimark_sor                | 109 ms                                                                                                          | 125 ms: 1.15x slower                                                                                                  |
| json_dumps                 | 9.57 ms                                                                                                         | 11.0 ms: 1.15x slower                                                                                                 |
| pickle_pure_python         | 301 us                                                                                                          | 347 us: 1.15x slower                                                                                                  |
| go                         | 105 ms                                                                                                          | 121 ms: 1.15x slower                                                                                                  |
| sympy_expand               | 450 ms                                                                                                          | 519 ms: 1.15x slower                                                                                                  |
| regex_compile              | 123 ms                                                                                                          | 143 ms: 1.16x slower                                                                                                  |
| deepcopy                   | 240 us                                                                                                          | 279 us: 1.16x slower                                                                                                  |
| deepcopy_reduce            | 2.57 us                                                                                                         | 2.99 us: 1.16x slower                                                                                                 |
| scimark_sparse_mat_mult    | 4.70 ms                                                                                                         | 5.48 ms: 1.17x slower                                                                                                 |
| pprint_safe_repr           | 684 ms                                                                                                          | 798 ms: 1.17x slower                                                                                                  |
| thrift                     | 756 us                                                                                                          | 885 us: 1.17x slower                                                                                                  |
| sympy_sum                  | 152 ms                                                                                                          | 178 ms: 1.17x slower                                                                                                  |
| sqlglot_v2_optimize        | 49.9 ms                                                                                                         | 58.5 ms: 1.17x slower                                                                                                 |
| subparsers                 | 42.4 ms                                                                                                         | 49.8 ms: 1.17x slower                                                                                                 |
| deepcopy_memo              | 26.1 us                                                                                                         | 30.7 us: 1.17x slower                                                                                                 |
| sympy_str                  | 265 ms                                                                                                          | 312 ms: 1.17x slower                                                                                                  |
| sqlglot_v2_normalize       | 99.1 ms                                                                                                         | 117 ms: 1.18x slower                                                                                                  |
| pprint_pformat             | 1.40 sec                                                                                                        | 1.65 sec: 1.18x slower                                                                                                |
| logging_simple             | 5.88 us                                                                                                         | 6.93 us: 1.18x slower                                                                                                 |
| xml_etree_generate         | 83.7 ms                                                                                                         | 98.7 ms: 1.18x slower                                                                                                 |
| sympy_integrate            | 18.7 ms                                                                                                         | 22.0 ms: 1.18x slower                                                                                                 |
| raytrace                   | 255 ms                                                                                                          | 301 ms: 1.18x slower                                                                                                  |
| hexiom                     | 5.54 ms                                                                                                         | 6.55 ms: 1.18x slower                                                                                                 |
| meteor_contest             | 98.5 ms                                                                                                         | 117 ms: 1.19x slower                                                                                                  |
| sqlglot_v2_transpile       | 1.51 ms                                                                                                         | 1.80 ms: 1.19x slower                                                                                                 |
| fannkuch                   | 384 ms                                                                                                          | 459 ms: 1.19x slower                                                                                                  |
| scimark_lu                 | 109 ms                                                                                                          | 130 ms: 1.20x slower                                                                                                  |
| django_template            | 34.2 ms                                                                                                         | 41.1 ms: 1.20x slower                                                                                                 |
| logging_format             | 6.54 us                                                                                                         | 7.87 us: 1.20x slower                                                                                                 |
| shortest_path              | 444 ms                                                                                                          | 535 ms: 1.21x slower                                                                                                  |
| spectral_norm              | 94.5 ms                                                                                                         | 115 ms: 1.22x slower                                                                                                  |
| genshi_xml                 | 48.4 ms                                                                                                         | 59.0 ms: 1.22x slower                                                                                                 |
| xml_etree_process          | 58.2 ms                                                                                                         | 70.9 ms: 1.22x slower                                                                                                 |
| sqlglot_v2_parse           | 1.21 ms                                                                                                         | 1.48 ms: 1.22x slower                                                                                                 |
| connected_components       | 401 ms                                                                                                          | 494 ms: 1.23x slower                                                                                                  |
| bench_mp_pool              | 12.3 ms                                                                                                         | 15.3 ms: 1.25x slower                                                                                                 |
| python_startup             | 12.5 ms                                                                                                         | 15.7 ms: 1.26x slower                                                                                                 |
| richards                   | 41.1 ms                                                                                                         | 51.7 ms: 1.26x slower                                                                                                 |
| scimark_monte_carlo        | 62.2 ms                                                                                                         | 78.6 ms: 1.26x slower                                                                                                 |
| typing_runtime_protocols   | 149 us                                                                                                          | 190 us: 1.27x slower                                                                                                  |
| richards_super             | 46.9 ms                                                                                                         | 59.7 ms: 1.27x slower                                                                                                 |
| crypto_pyaes               | 68.1 ms                                                                                                         | 86.8 ms: 1.27x slower                                                                                                 |
| genshi_text                | 20.6 ms                                                                                                         | 26.6 ms: 1.29x slower                                                                                                 |
| python_startup_no_site     | 7.24 ms                                                                                                         | 9.57 ms: 1.32x slower                                                                                                 |
| coverage                   | 82.8 ms                                                                                                         | 110 ms: 1.33x slower                                                                                                  |
| mako                       | 11.6 ms                                                                                                         | 15.7 ms: 1.36x slower                                                                                                 |
| nbody                      | 89.3 ms                                                                                                         | 124 ms: 1.38x slower                                                                                                  |
| bench_thread_pool          | 1.00 ms                                                                                                         | 3.11 ms: 3.10x slower                                                                                                 |
| Geometric mean             | (ref)                                                                                                           | 1.12x slower                                                                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

- Geometric mean (including insignificant results): 1.094x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.21x