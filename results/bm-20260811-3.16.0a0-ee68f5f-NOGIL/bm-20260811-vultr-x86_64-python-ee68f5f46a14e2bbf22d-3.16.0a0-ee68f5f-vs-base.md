# Results vs. base

- fork: python
- ref: ee68f5f46a14e2bbf22d
- machine: linux-x86_64
- commit hash: ee68f5f
- commit date: 2026-08-11
- overall geometric mean: 1.097x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260811-3.16.0a0-ee68f5f/bm-20260811-vultr-x86_64-python-ee68f5f46a14e2bbf22d-3.16.0a0-ee68f5f.json | results/bm-20260811-3.16.0a0-ee68f5f-NOGIL/bm-20260811-vultr-x86_64-python-ee68f5f46a14e2bbf22d-3.16.0a0-ee68f5f.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                                                          | 293 ms: 1.13x slower                                                                                                  |
| docutils       | 2.38 sec                                                                                                        | 2.87 sec: 1.21x slower                                                                                                |
| html5lib       | 59.6 ms                                                                                                         | 66.3 ms: 1.11x slower                                                                                                 |
| sphinx         | 990 ms                                                                                                          | 1.10 sec: 1.11x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.14x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260811-3.16.0a0-ee68f5f/bm-20260811-vultr-x86_64-python-ee68f5f46a14e2bbf22d-3.16.0a0-ee68f5f.json | results/bm-20260811-3.16.0a0-ee68f5f-NOGIL/bm-20260811-vultr-x86_64-python-ee68f5f46a14e2bbf22d-3.16.0a0-ee68f5f.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 761 ms                                                                                                          | 680 ms: 1.12x faster                                                                                                  |
| asyncio_websockets         | 544 ms                                                                                                          | 510 ms: 1.07x faster                                                                                                  |
| async_tree_io              | 721 ms                                                                                                          | 697 ms: 1.03x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 560 ms                                                                                                          | 574 ms: 1.02x slower                                                                                                  |
| coroutines                 | 23.9 ms                                                                                                         | 25.0 ms: 1.05x slower                                                                                                 |
| async_tree_memoization_tg  | 365 ms                                                                                                          | 391 ms: 1.07x slower                                                                                                  |
| async_tree_none_tg         | 299 ms                                                                                                          | 324 ms: 1.08x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 544 ms                                                                                                          | 599 ms: 1.10x slower                                                                                                  |
| async_tree_memoization     | 378 ms                                                                                                          | 419 ms: 1.11x slower                                                                                                  |
| async_generators           | 348 ms                                                                                                          | 393 ms: 1.13x slower                                                                                                  |
| async_tree_none            | 295 ms                                                                                                          | 340 ms: 1.15x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.04x slower                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260811-3.16.0a0-ee68f5f/bm-20260811-vultr-x86_64-python-ee68f5f46a14e2bbf22d-3.16.0a0-ee68f5f.json | results/bm-20260811-3.16.0a0-ee68f5f-NOGIL/bm-20260811-vultr-x86_64-python-ee68f5f46a14e2bbf22d-3.16.0a0-ee68f5f.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 184 ms                                                                                                          | 187 ms: 1.02x slower                                                                                                  |
| float          | 72.6 ms                                                                                                         | 83.9 ms: 1.16x slower                                                                                                 |
| nbody          | 90.6 ms                                                                                                         | 119 ms: 1.31x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.15x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260811-3.16.0a0-ee68f5f/bm-20260811-vultr-x86_64-python-ee68f5f46a14e2bbf22d-3.16.0a0-ee68f5f.json | results/bm-20260811-3.16.0a0-ee68f5f-NOGIL/bm-20260811-vultr-x86_64-python-ee68f5f46a14e2bbf22d-3.16.0a0-ee68f5f.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.0 ms                                                                                                         | 20.5 ms: 1.02x faster                                                                                                 |
| regex_dna      | 182 ms                                                                                                          | 179 ms: 1.02x faster                                                                                                  |
| regex_compile  | 148 ms                                                                                                          | 168 ms: 1.13x slower                                                                                                  |
| regex_effbot   | 2.55 ms                                                                                                         | 2.93 ms: 1.15x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                           | 1.06x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260811-3.16.0a0-ee68f5f/bm-20260811-vultr-x86_64-python-ee68f5f46a14e2bbf22d-3.16.0a0-ee68f5f.json | results/bm-20260811-3.16.0a0-ee68f5f-NOGIL/bm-20260811-vultr-x86_64-python-ee68f5f46a14e2bbf22d-3.16.0a0-ee68f5f.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 143 ms                                                                                                          | 140 ms: 1.02x faster                                                                                                  |
| xml_etree_iterparse  | 91.2 ms                                                                                                         | 94.1 ms: 1.03x slower                                                                                                 |
| tomli_loads          | 1.85 sec                                                                                                        | 1.94 sec: 1.05x slower                                                                                                |
| json_dumps           | 9.33 ms                                                                                                         | 10.0 ms: 1.08x slower                                                                                                 |
| pickle_pure_python   | 304 us                                                                                                          | 331 us: 1.09x slower                                                                                                  |
| xml_etree_generate   | 88.0 ms                                                                                                         | 98.4 ms: 1.12x slower                                                                                                 |
| unpickle_pure_python | 212 us                                                                                                          | 239 us: 1.12x slower                                                                                                  |
| json_loads           | 27.0 us                                                                                                         | 30.4 us: 1.13x slower                                                                                                 |
| xml_etree_process    | 62.4 ms                                                                                                         | 74.4 ms: 1.19x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260811-3.16.0a0-ee68f5f/bm-20260811-vultr-x86_64-python-ee68f5f46a14e2bbf22d-3.16.0a0-ee68f5f.json | results/bm-20260811-3.16.0a0-ee68f5f-NOGIL/bm-20260811-vultr-x86_64-python-ee68f5f46a14e2bbf22d-3.16.0a0-ee68f5f.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.6 ms                                                                                                         | 15.7 ms: 1.25x slower                                                                                                 |
| python_startup_no_site | 7.09 ms                                                                                                         | 9.24 ms: 1.30x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.28x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260811-3.16.0a0-ee68f5f/bm-20260811-vultr-x86_64-python-ee68f5f46a14e2bbf22d-3.16.0a0-ee68f5f.json | results/bm-20260811-3.16.0a0-ee68f5f-NOGIL/bm-20260811-vultr-x86_64-python-ee68f5f46a14e2bbf22d-3.16.0a0-ee68f5f.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 36.3 ms                                                                                                         | 41.8 ms: 1.15x slower                                                                                                 |
| mako            | 12.0 ms                                                                                                         | 16.2 ms: 1.34x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.24x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20260811-3.16.0a0-ee68f5f/bm-20260811-vultr-x86_64-python-ee68f5f46a14e2bbf22d-3.16.0a0-ee68f5f.json | results/bm-20260811-3.16.0a0-ee68f5f-NOGIL/bm-20260811-vultr-x86_64-python-ee68f5f46a14e2bbf22d-3.16.0a0-ee68f5f.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 233 ms                                                                                                          | 6.68 ms: 34.90x faster                                                                                                |
| gc_traversal               | 3.72 ms                                                                                                         | 1.77 ms: 2.10x faster                                                                                                 |
| create_gc_cycles           | 1.67 ms                                                                                                         | 1.36 ms: 1.23x faster                                                                                                 |
| sqlite_synth               | 2.23 us                                                                                                         | 1.92 us: 1.16x faster                                                                                                 |
| async_tree_io_tg           | 761 ms                                                                                                          | 680 ms: 1.12x faster                                                                                                  |
| asyncio_websockets         | 544 ms                                                                                                          | 510 ms: 1.07x faster                                                                                                  |
| async_tree_io              | 721 ms                                                                                                          | 697 ms: 1.03x faster                                                                                                  |
| xml_etree_parse            | 143 ms                                                                                                          | 140 ms: 1.02x faster                                                                                                  |
| regex_v8                   | 21.0 ms                                                                                                         | 20.5 ms: 1.02x faster                                                                                                 |
| pathlib                    | 18.0 ms                                                                                                         | 17.6 ms: 1.02x faster                                                                                                 |
| regex_dna                  | 182 ms                                                                                                          | 179 ms: 1.02x faster                                                                                                  |
| pidigits                   | 184 ms                                                                                                          | 187 ms: 1.02x slower                                                                                                  |
| bpe_tokeniser              | 4.24 sec                                                                                                        | 4.34 sec: 1.02x slower                                                                                                |
| async_tree_cpu_io_mixed_tg | 560 ms                                                                                                          | 574 ms: 1.02x slower                                                                                                  |
| xml_etree_iterparse        | 91.2 ms                                                                                                         | 94.1 ms: 1.03x slower                                                                                                 |
| dulwich_log                | 67.7 ms                                                                                                         | 70.0 ms: 1.03x slower                                                                                                 |
| coroutines                 | 23.9 ms                                                                                                         | 25.0 ms: 1.05x slower                                                                                                 |
| tomli_loads                | 1.85 sec                                                                                                        | 1.94 sec: 1.05x slower                                                                                                |
| logging_silent             | 96.4 ns                                                                                                         | 102 ns: 1.05x slower                                                                                                  |
| async_tree_memoization_tg  | 365 ms                                                                                                          | 391 ms: 1.07x slower                                                                                                  |
| scimark_fft                | 311 ms                                                                                                          | 334 ms: 1.07x slower                                                                                                  |
| json_dumps                 | 9.33 ms                                                                                                         | 10.0 ms: 1.08x slower                                                                                                 |
| async_tree_none_tg         | 299 ms                                                                                                          | 324 ms: 1.08x slower                                                                                                  |
| k_core                     | 2.07 sec                                                                                                        | 2.24 sec: 1.08x slower                                                                                                |
| pprint_safe_repr           | 735 ms                                                                                                          | 800 ms: 1.09x slower                                                                                                  |
| telco                      | 162 ms                                                                                                          | 176 ms: 1.09x slower                                                                                                  |
| pickle_pure_python         | 304 us                                                                                                          | 331 us: 1.09x slower                                                                                                  |
| many_optionals             | 916 us                                                                                                          | 1.01 ms: 1.10x slower                                                                                                 |
| json                       | 4.87 ms                                                                                                         | 5.36 ms: 1.10x slower                                                                                                 |
| async_tree_cpu_io_mixed    | 544 ms                                                                                                          | 599 ms: 1.10x slower                                                                                                  |
| pprint_pformat             | 1.50 sec                                                                                                        | 1.66 sec: 1.10x slower                                                                                                |
| scimark_lu                 | 116 ms                                                                                                          | 128 ms: 1.11x slower                                                                                                  |
| sphinx                     | 990 ms                                                                                                          | 1.10 sec: 1.11x slower                                                                                                |
| bench_thread_pool          | 1.34 ms                                                                                                         | 1.49 ms: 1.11x slower                                                                                                 |
| async_tree_memoization     | 378 ms                                                                                                          | 419 ms: 1.11x slower                                                                                                  |
| deltablue                  | 3.32 ms                                                                                                         | 3.69 ms: 1.11x slower                                                                                                 |
| sqlglot_v2_normalize       | 102 ms                                                                                                          | 114 ms: 1.11x slower                                                                                                  |
| deepcopy                   | 237 us                                                                                                          | 264 us: 1.11x slower                                                                                                  |
| html5lib                   | 59.6 ms                                                                                                         | 66.3 ms: 1.11x slower                                                                                                 |
| sqlglot_v2_optimize        | 51.6 ms                                                                                                         | 57.5 ms: 1.11x slower                                                                                                 |
| scimark_sparse_mat_mult    | 4.55 ms                                                                                                         | 5.06 ms: 1.11x slower                                                                                                 |
| sympy_expand               | 474 ms                                                                                                          | 529 ms: 1.12x slower                                                                                                  |
| xml_etree_generate         | 88.0 ms                                                                                                         | 98.4 ms: 1.12x slower                                                                                                 |
| unpickle_pure_python       | 212 us                                                                                                          | 239 us: 1.12x slower                                                                                                  |
| logging_simple             | 6.22 us                                                                                                         | 7.00 us: 1.13x slower                                                                                                 |
| pylint                     | 115 ms                                                                                                          | 129 ms: 1.13x slower                                                                                                  |
| scimark_sor                | 106 ms                                                                                                          | 119 ms: 1.13x slower                                                                                                  |
| json_loads                 | 27.0 us                                                                                                         | 30.4 us: 1.13x slower                                                                                                 |
| async_generators           | 348 ms                                                                                                          | 393 ms: 1.13x slower                                                                                                  |
| regex_compile              | 148 ms                                                                                                          | 168 ms: 1.13x slower                                                                                                  |
| 2to3                       | 259 ms                                                                                                          | 293 ms: 1.13x slower                                                                                                  |
| hexiom                     | 5.74 ms                                                                                                         | 6.51 ms: 1.14x slower                                                                                                 |
| sympy_str                  | 278 ms                                                                                                          | 317 ms: 1.14x slower                                                                                                  |
| mdp                        | 1.14 sec                                                                                                        | 1.29 sec: 1.14x slower                                                                                                |
| richards                   | 44.9 ms                                                                                                         | 51.1 ms: 1.14x slower                                                                                                 |
| deepcopy_reduce            | 2.57 us                                                                                                         | 2.93 us: 1.14x slower                                                                                                 |
| spectral_norm              | 91.8 ms                                                                                                         | 105 ms: 1.14x slower                                                                                                  |
| chaos                      | 52.6 ms                                                                                                         | 60.1 ms: 1.14x slower                                                                                                 |
| comprehensions             | 15.6 us                                                                                                         | 17.8 us: 1.14x slower                                                                                                 |
| subparsers                 | 9.06 ms                                                                                                         | 10.4 ms: 1.14x slower                                                                                                 |
| sympy_integrate            | 19.1 ms                                                                                                         | 21.8 ms: 1.14x slower                                                                                                 |
| logging_format             | 7.00 us                                                                                                         | 8.01 us: 1.14x slower                                                                                                 |
| sympy_sum                  | 158 ms                                                                                                          | 181 ms: 1.15x slower                                                                                                  |
| regex_effbot               | 2.55 ms                                                                                                         | 2.93 ms: 1.15x slower                                                                                                 |
| django_template            | 36.3 ms                                                                                                         | 41.8 ms: 1.15x slower                                                                                                 |
| richards_super             | 51.1 ms                                                                                                         | 58.9 ms: 1.15x slower                                                                                                 |
| async_tree_none            | 295 ms                                                                                                          | 340 ms: 1.15x slower                                                                                                  |
| float                      | 72.6 ms                                                                                                         | 83.9 ms: 1.16x slower                                                                                                 |
| raytrace                   | 249 ms                                                                                                          | 289 ms: 1.16x slower                                                                                                  |
| pyflate                    | 394 ms                                                                                                          | 460 ms: 1.17x slower                                                                                                  |
| go                         | 103 ms                                                                                                          | 121 ms: 1.18x slower                                                                                                  |
| deepcopy_memo              | 26.4 us                                                                                                         | 31.1 us: 1.18x slower                                                                                                 |
| nqueens                    | 73.9 ms                                                                                                         | 87.4 ms: 1.18x slower                                                                                                 |
| sqlglot_v2_transpile       | 1.45 ms                                                                                                         | 1.72 ms: 1.19x slower                                                                                                 |
| xml_etree_process          | 62.4 ms                                                                                                         | 74.4 ms: 1.19x slower                                                                                                 |
| thrift                     | 778 us                                                                                                          | 929 us: 1.19x slower                                                                                                  |
| generators                 | 27.8 ms                                                                                                         | 33.6 ms: 1.21x slower                                                                                                 |
| docutils                   | 2.38 sec                                                                                                        | 2.87 sec: 1.21x slower                                                                                                |
| shortest_path              | 438 ms                                                                                                          | 532 ms: 1.21x slower                                                                                                  |
| sqlglot_v2_parse           | 1.15 ms                                                                                                         | 1.41 ms: 1.22x slower                                                                                                 |
| typing_runtime_protocols   | 120 us                                                                                                          | 147 us: 1.22x slower                                                                                                  |
| scimark_monte_carlo        | 62.7 ms                                                                                                         | 76.9 ms: 1.23x slower                                                                                                 |
| connected_components       | 396 ms                                                                                                          | 487 ms: 1.23x slower                                                                                                  |
| fannkuch                   | 372 ms                                                                                                          | 461 ms: 1.24x slower                                                                                                  |
| python_startup             | 12.6 ms                                                                                                         | 15.7 ms: 1.25x slower                                                                                                 |
| meteor_contest             | 103 ms                                                                                                          | 128 ms: 1.25x slower                                                                                                  |
| crypto_pyaes               | 67.3 ms                                                                                                         | 87.6 ms: 1.30x slower                                                                                                 |
| python_startup_no_site     | 7.09 ms                                                                                                         | 9.24 ms: 1.30x slower                                                                                                 |
| nbody                      | 90.6 ms                                                                                                         | 119 ms: 1.31x slower                                                                                                  |
| mako                       | 12.0 ms                                                                                                         | 16.2 ms: 1.34x slower                                                                                                 |
| coverage                   | 82.5 ms                                                                                                         | 115 ms: 1.39x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.06x slower                                                                                                          |

Benchmark hidden because not significant (1): pycparser

- Geometric mean (including insignificant results): 1.097x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.10x
- 99% likely to have a slowdown of 1.09x

# Memory
- memory change: 1.19x