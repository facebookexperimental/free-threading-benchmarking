# Results vs. base

- fork: python
- ref: cb59eaefeda5ff44ac0c
- machine: linux-x86_64
- commit hash: cb59eae
- commit date: 2025-07-15
- overall geometric mean: 1.093x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250715-3.15.0a0-cb59eae/bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae.json | results/bm-20250715-3.15.0a0-cb59eae-NOGIL/bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 251 ms                                                                                                          | 283 ms: 1.13x slower                                                                                                  |
| docutils       | 2.57 sec                                                                                                        | 2.69 sec: 1.05x slower                                                                                                |
| html5lib       | 61.2 ms                                                                                                         | 65.8 ms: 1.07x slower                                                                                                 |
| sphinx         | 972 ms                                                                                                          | 1.05 sec: 1.08x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.08x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250715-3.15.0a0-cb59eae/bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae.json | results/bm-20250715-3.15.0a0-cb59eae-NOGIL/bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 615 ms                                                                                                          | 527 ms: 1.17x faster                                                                                                  |
| async_tree_none_tg         | 255 ms                                                                                                          | 229 ms: 1.11x faster                                                                                                  |
| async_tree_memoization_tg  | 313 ms                                                                                                          | 286 ms: 1.09x faster                                                                                                  |
| async_tree_io              | 594 ms                                                                                                          | 556 ms: 1.07x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 505 ms                                                                                                          | 480 ms: 1.05x faster                                                                                                  |
| asyncio_websockets         | 517 ms                                                                                                          | 512 ms: 1.01x faster                                                                                                  |
| async_tree_memoization     | 315 ms                                                                                                          | 312 ms: 1.01x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 500 ms                                                                                                          | 506 ms: 1.01x slower                                                                                                  |
| async_tree_none            | 255 ms                                                                                                          | 259 ms: 1.02x slower                                                                                                  |
| coroutines                 | 23.2 ms                                                                                                         | 24.7 ms: 1.06x slower                                                                                                 |
| async_generators           | 342 ms                                                                                                          | 371 ms: 1.09x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.03x faster                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250715-3.15.0a0-cb59eae/bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae.json | results/bm-20250715-3.15.0a0-cb59eae-NOGIL/bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 203 ms                                                                                                          | 195 ms: 1.04x faster                                                                                                  |
| float          | 72.6 ms                                                                                                         | 70.1 ms: 1.04x faster                                                                                                 |
| nbody          | 87.8 ms                                                                                                         | 124 ms: 1.41x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250715-3.15.0a0-cb59eae/bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae.json | results/bm-20250715-3.15.0a0-cb59eae-NOGIL/bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.5 ms                                                                                                         | 21.4 ms: 1.01x faster                                                                                                 |
| regex_dna      | 174 ms                                                                                                          | 180 ms: 1.03x slower                                                                                                  |
| regex_effbot   | 2.62 ms                                                                                                         | 2.90 ms: 1.11x slower                                                                                                 |
| regex_compile  | 124 ms                                                                                                          | 143 ms: 1.15x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.07x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250715-3.15.0a0-cb59eae/bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae.json | results/bm-20250715-3.15.0a0-cb59eae-NOGIL/bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 92.5 ms                                                                                                         | 86.8 ms: 1.07x faster                                                                                                 |
| xml_etree_parse      | 131 ms                                                                                                          | 130 ms: 1.01x faster                                                                                                  |
| unpickle_pure_python | 209 us                                                                                                          | 231 us: 1.11x slower                                                                                                  |
| tomli_loads          | 1.92 sec                                                                                                        | 2.13 sec: 1.11x slower                                                                                                |
| json_loads           | 27.9 us                                                                                                         | 31.1 us: 1.11x slower                                                                                                 |
| pickle_pure_python   | 304 us                                                                                                          | 340 us: 1.12x slower                                                                                                  |
| json_dumps           | 10.8 ms                                                                                                         | 12.2 ms: 1.13x slower                                                                                                 |
| xml_etree_generate   | 83.6 ms                                                                                                         | 95.9 ms: 1.15x slower                                                                                                 |
| xml_etree_process    | 58.0 ms                                                                                                         | 69.3 ms: 1.19x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250715-3.15.0a0-cb59eae/bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae.json | results/bm-20250715-3.15.0a0-cb59eae-NOGIL/bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.4 ms                                                                                                         | 15.8 ms: 1.27x slower                                                                                                 |
| python_startup_no_site | 7.15 ms                                                                                                         | 9.37 ms: 1.31x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.29x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250715-3.15.0a0-cb59eae/bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae.json | results/bm-20250715-3.15.0a0-cb59eae-NOGIL/bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 34.5 ms                                                                                                         | 40.1 ms: 1.16x slower                                                                                                 |
| genshi_xml      | 48.7 ms                                                                                                         | 57.4 ms: 1.18x slower                                                                                                 |
| genshi_text     | 20.6 ms                                                                                                         | 26.7 ms: 1.30x slower                                                                                                 |
| mako            | 11.5 ms                                                                                                         | 15.4 ms: 1.34x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.24x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20250715-3.15.0a0-cb59eae/bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae.json | results/bm-20250715-3.15.0a0-cb59eae-NOGIL/bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.30 ms                                                                                                         | 1.90 ms: 2.26x faster                                                                                                 |
| create_gc_cycles           | 1.93 ms                                                                                                         | 1.48 ms: 1.30x faster                                                                                                 |
| async_tree_io_tg           | 615 ms                                                                                                          | 527 ms: 1.17x faster                                                                                                  |
| async_tree_none_tg         | 255 ms                                                                                                          | 229 ms: 1.11x faster                                                                                                  |
| sqlite_synth               | 2.27 us                                                                                                         | 2.07 us: 1.10x faster                                                                                                 |
| async_tree_memoization_tg  | 313 ms                                                                                                          | 286 ms: 1.09x faster                                                                                                  |
| async_tree_io              | 594 ms                                                                                                          | 556 ms: 1.07x faster                                                                                                  |
| xml_etree_iterparse        | 92.5 ms                                                                                                         | 86.8 ms: 1.07x faster                                                                                                 |
| async_tree_cpu_io_mixed_tg | 505 ms                                                                                                          | 480 ms: 1.05x faster                                                                                                  |
| pidigits                   | 203 ms                                                                                                          | 195 ms: 1.04x faster                                                                                                  |
| float                      | 72.6 ms                                                                                                         | 70.1 ms: 1.04x faster                                                                                                 |
| pathlib                    | 19.6 ms                                                                                                         | 19.2 ms: 1.02x faster                                                                                                 |
| asyncio_websockets         | 517 ms                                                                                                          | 512 ms: 1.01x faster                                                                                                  |
| async_tree_memoization     | 315 ms                                                                                                          | 312 ms: 1.01x faster                                                                                                  |
| regex_v8                   | 21.5 ms                                                                                                         | 21.4 ms: 1.01x faster                                                                                                 |
| xml_etree_parse            | 131 ms                                                                                                          | 130 ms: 1.01x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 500 ms                                                                                                          | 506 ms: 1.01x slower                                                                                                  |
| async_tree_none            | 255 ms                                                                                                          | 259 ms: 1.02x slower                                                                                                  |
| regex_dna                  | 174 ms                                                                                                          | 180 ms: 1.03x slower                                                                                                  |
| json                       | 5.13 ms                                                                                                         | 5.33 ms: 1.04x slower                                                                                                 |
| bpe_tokeniser              | 4.22 sec                                                                                                        | 4.39 sec: 1.04x slower                                                                                                |
| docutils                   | 2.57 sec                                                                                                        | 2.69 sec: 1.05x slower                                                                                                |
| pycparser                  | 1.10 sec                                                                                                        | 1.15 sec: 1.05x slower                                                                                                |
| bench_mp_pool              | 103 ms                                                                                                          | 108 ms: 1.05x slower                                                                                                  |
| coroutines                 | 23.2 ms                                                                                                         | 24.7 ms: 1.06x slower                                                                                                 |
| many_optionals             | 1.05 ms                                                                                                         | 1.13 ms: 1.07x slower                                                                                                 |
| dulwich_log                | 66.5 ms                                                                                                         | 71.4 ms: 1.07x slower                                                                                                 |
| html5lib                   | 61.2 ms                                                                                                         | 65.8 ms: 1.07x slower                                                                                                 |
| sphinx                     | 972 ms                                                                                                          | 1.05 sec: 1.08x slower                                                                                                |
| scimark_fft                | 338 ms                                                                                                          | 364 ms: 1.08x slower                                                                                                  |
| logging_silent             | 99.0 ns                                                                                                         | 107 ns: 1.08x slower                                                                                                  |
| async_generators           | 342 ms                                                                                                          | 371 ms: 1.09x slower                                                                                                  |
| telco                      | 159 ms                                                                                                          | 174 ms: 1.09x slower                                                                                                  |
| generators                 | 28.4 ms                                                                                                         | 31.2 ms: 1.10x slower                                                                                                 |
| pprint_safe_repr           | 707 ms                                                                                                          | 777 ms: 1.10x slower                                                                                                  |
| pylint                     | 279 ms                                                                                                          | 307 ms: 1.10x slower                                                                                                  |
| k_core                     | 2.03 sec                                                                                                        | 2.24 sec: 1.10x slower                                                                                                |
| unpickle_pure_python       | 209 us                                                                                                          | 231 us: 1.11x slower                                                                                                  |
| regex_effbot               | 2.62 ms                                                                                                         | 2.90 ms: 1.11x slower                                                                                                 |
| tomli_loads                | 1.92 sec                                                                                                        | 2.13 sec: 1.11x slower                                                                                                |
| subparsers                 | 25.3 ms                                                                                                         | 28.2 ms: 1.11x slower                                                                                                 |
| json_loads                 | 27.9 us                                                                                                         | 31.1 us: 1.11x slower                                                                                                 |
| pprint_pformat             | 1.44 sec                                                                                                        | 1.60 sec: 1.11x slower                                                                                                |
| deepcopy_reduce            | 2.68 us                                                                                                         | 3.00 us: 1.12x slower                                                                                                 |
| pickle_pure_python         | 304 us                                                                                                          | 340 us: 1.12x slower                                                                                                  |
| chaos                      | 56.3 ms                                                                                                         | 63.3 ms: 1.12x slower                                                                                                 |
| json_dumps                 | 10.8 ms                                                                                                         | 12.2 ms: 1.13x slower                                                                                                 |
| 2to3                       | 251 ms                                                                                                          | 283 ms: 1.13x slower                                                                                                  |
| sympy_expand               | 460 ms                                                                                                          | 521 ms: 1.13x slower                                                                                                  |
| nqueens                    | 78.2 ms                                                                                                         | 88.7 ms: 1.13x slower                                                                                                 |
| pyflate                    | 407 ms                                                                                                          | 465 ms: 1.14x slower                                                                                                  |
| mdp                        | 1.15 sec                                                                                                        | 1.31 sec: 1.14x slower                                                                                                |
| xml_etree_generate         | 83.6 ms                                                                                                         | 95.9 ms: 1.15x slower                                                                                                 |
| scimark_sparse_mat_mult    | 4.82 ms                                                                                                         | 5.53 ms: 1.15x slower                                                                                                 |
| regex_compile              | 124 ms                                                                                                          | 143 ms: 1.15x slower                                                                                                  |
| hexiom                     | 5.60 ms                                                                                                         | 6.43 ms: 1.15x slower                                                                                                 |
| comprehensions             | 15.4 us                                                                                                         | 17.8 us: 1.15x slower                                                                                                 |
| scimark_lu                 | 111 ms                                                                                                          | 129 ms: 1.16x slower                                                                                                  |
| sympy_str                  | 268 ms                                                                                                          | 311 ms: 1.16x slower                                                                                                  |
| sympy_sum                  | 154 ms                                                                                                          | 178 ms: 1.16x slower                                                                                                  |
| sqlglot_v2_optimize        | 49.9 ms                                                                                                         | 58.0 ms: 1.16x slower                                                                                                 |
| deepcopy                   | 252 us                                                                                                          | 293 us: 1.16x slower                                                                                                  |
| scimark_sor                | 109 ms                                                                                                          | 127 ms: 1.16x slower                                                                                                  |
| django_template            | 34.5 ms                                                                                                         | 40.1 ms: 1.16x slower                                                                                                 |
| sympy_integrate            | 18.8 ms                                                                                                         | 22.0 ms: 1.17x slower                                                                                                 |
| sqlglot_v2_normalize       | 98.5 ms                                                                                                         | 115 ms: 1.17x slower                                                                                                  |
| spectral_norm              | 96.4 ms                                                                                                         | 113 ms: 1.17x slower                                                                                                  |
| logging_format             | 6.77 us                                                                                                         | 7.95 us: 1.17x slower                                                                                                 |
| thrift                     | 740 us                                                                                                          | 871 us: 1.18x slower                                                                                                  |
| genshi_xml                 | 48.7 ms                                                                                                         | 57.4 ms: 1.18x slower                                                                                                 |
| fannkuch                   | 385 ms                                                                                                          | 454 ms: 1.18x slower                                                                                                  |
| go                         | 103 ms                                                                                                          | 122 ms: 1.18x slower                                                                                                  |
| logging_simple             | 5.87 us                                                                                                         | 6.94 us: 1.18x slower                                                                                                 |
| deltablue                  | 3.06 ms                                                                                                         | 3.63 ms: 1.18x slower                                                                                                 |
| meteor_contest             | 99.6 ms                                                                                                         | 118 ms: 1.19x slower                                                                                                  |
| deepcopy_memo              | 29.3 us                                                                                                         | 34.9 us: 1.19x slower                                                                                                 |
| xml_etree_process          | 58.0 ms                                                                                                         | 69.3 ms: 1.19x slower                                                                                                 |
| sqlglot_v2_transpile       | 1.51 ms                                                                                                         | 1.82 ms: 1.21x slower                                                                                                 |
| raytrace                   | 252 ms                                                                                                          | 305 ms: 1.21x slower                                                                                                  |
| sqlglot_v2_parse           | 1.21 ms                                                                                                         | 1.46 ms: 1.21x slower                                                                                                 |
| shortest_path              | 442 ms                                                                                                          | 542 ms: 1.23x slower                                                                                                  |
| connected_components       | 398 ms                                                                                                          | 493 ms: 1.24x slower                                                                                                  |
| crypto_pyaes               | 69.1 ms                                                                                                         | 85.8 ms: 1.24x slower                                                                                                 |
| typing_runtime_protocols   | 152 us                                                                                                          | 191 us: 1.26x slower                                                                                                  |
| richards                   | 40.9 ms                                                                                                         | 52.0 ms: 1.27x slower                                                                                                 |
| python_startup             | 12.4 ms                                                                                                         | 15.8 ms: 1.27x slower                                                                                                 |
| richards_super             | 46.6 ms                                                                                                         | 59.3 ms: 1.27x slower                                                                                                 |
| scimark_monte_carlo        | 61.0 ms                                                                                                         | 78.3 ms: 1.28x slower                                                                                                 |
| genshi_text                | 20.6 ms                                                                                                         | 26.7 ms: 1.30x slower                                                                                                 |
| python_startup_no_site     | 7.15 ms                                                                                                         | 9.37 ms: 1.31x slower                                                                                                 |
| mako                       | 11.5 ms                                                                                                         | 15.4 ms: 1.34x slower                                                                                                 |
| coverage                   | 81.6 ms                                                                                                         | 112 ms: 1.37x slower                                                                                                  |
| nbody                      | 87.8 ms                                                                                                         | 124 ms: 1.41x slower                                                                                                  |
| bench_thread_pool          | 1.05 ms                                                                                                         | 3.15 ms: 3.01x slower                                                                                                 |
| Geometric mean             | (ref)                                                                                                           | 1.11x slower                                                                                                          |

- Geometric mean (including insignificant results): 1.093x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.20x