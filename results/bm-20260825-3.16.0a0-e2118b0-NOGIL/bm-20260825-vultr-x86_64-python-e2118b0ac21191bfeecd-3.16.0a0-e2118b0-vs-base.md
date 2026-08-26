# Results vs. base

- fork: python
- ref: e2118b0ac21191bfeecd
- machine: linux-x86_64
- commit hash: e2118b0
- commit date: 2026-08-25
- overall geometric mean: 1.099x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260825-3.16.0a0-e2118b0/bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0.json | results/bm-20260825-3.16.0a0-e2118b0-NOGIL/bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                                                                          | 295 ms: 1.13x slower                                                                                                  |
| docutils       | 2.36 sec                                                                                                        | 2.91 sec: 1.23x slower                                                                                                |
| html5lib       | 58.1 ms                                                                                                         | 67.0 ms: 1.15x slower                                                                                                 |
| sphinx         | 985 ms                                                                                                          | 1.11 sec: 1.13x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.16x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260825-3.16.0a0-e2118b0/bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0.json | results/bm-20260825-3.16.0a0-e2118b0-NOGIL/bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 761 ms                                                                                                          | 694 ms: 1.10x faster                                                                                                  |
| asyncio_websockets         | 544 ms                                                                                                          | 512 ms: 1.06x faster                                                                                                  |
| async_tree_io              | 720 ms                                                                                                          | 704 ms: 1.02x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 558 ms                                                                                                          | 584 ms: 1.05x slower                                                                                                  |
| coroutines                 | 23.5 ms                                                                                                         | 24.7 ms: 1.05x slower                                                                                                 |
| async_tree_memoization_tg  | 366 ms                                                                                                          | 399 ms: 1.09x slower                                                                                                  |
| async_tree_memoization     | 378 ms                                                                                                          | 418 ms: 1.11x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 539 ms                                                                                                          | 597 ms: 1.11x slower                                                                                                  |
| async_tree_none_tg         | 296 ms                                                                                                          | 334 ms: 1.13x slower                                                                                                  |
| async_tree_none            | 291 ms                                                                                                          | 341 ms: 1.17x slower                                                                                                  |
| async_generators           | 347 ms                                                                                                          | 414 ms: 1.19x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.06x slower                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260825-3.16.0a0-e2118b0/bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0.json | results/bm-20260825-3.16.0a0-e2118b0-NOGIL/bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 187 ms                                                                                                          | 184 ms: 1.02x faster                                                                                                  |
| float          | 72.8 ms                                                                                                         | 83.9 ms: 1.15x slower                                                                                                 |
| nbody          | 91.5 ms                                                                                                         | 119 ms: 1.30x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.14x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260825-3.16.0a0-e2118b0/bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0.json | results/bm-20260825-3.16.0a0-e2118b0-NOGIL/bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.8 ms                                                                                                         | 21.0 ms: 1.04x faster                                                                                                 |
| regex_dna      | 177 ms                                                                                                          | 181 ms: 1.02x slower                                                                                                  |
| regex_compile  | 148 ms                                                                                                          | 169 ms: 1.14x slower                                                                                                  |
| regex_effbot   | 2.58 ms                                                                                                         | 2.98 ms: 1.16x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                           | 1.07x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260825-3.16.0a0-e2118b0/bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0.json | results/bm-20260825-3.16.0a0-e2118b0-NOGIL/bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 142 ms                                                                                                          | 140 ms: 1.01x faster                                                                                                  |
| xml_etree_iterparse  | 91.1 ms                                                                                                         | 95.3 ms: 1.05x slower                                                                                                 |
| tomli_loads          | 1.79 sec                                                                                                        | 1.92 sec: 1.07x slower                                                                                                |
| json_dumps           | 9.38 ms                                                                                                         | 10.1 ms: 1.08x slower                                                                                                 |
| pickle_pure_python   | 304 us                                                                                                          | 333 us: 1.09x slower                                                                                                  |
| unpickle_pure_python | 214 us                                                                                                          | 238 us: 1.11x slower                                                                                                  |
| json_loads           | 27.4 us                                                                                                         | 30.7 us: 1.12x slower                                                                                                 |
| xml_etree_generate   | 88.3 ms                                                                                                         | 102 ms: 1.15x slower                                                                                                  |
| xml_etree_process    | 62.8 ms                                                                                                         | 75.6 ms: 1.20x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260825-3.16.0a0-e2118b0/bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0.json | results/bm-20260825-3.16.0a0-e2118b0-NOGIL/bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.9 ms                                                                                                         | 16.1 ms: 1.25x slower                                                                                                 |
| python_startup_no_site | 7.70 ms                                                                                                         | 9.87 ms: 1.28x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.26x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260825-3.16.0a0-e2118b0/bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0.json | results/bm-20260825-3.16.0a0-e2118b0-NOGIL/bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 37.0 ms                                                                                                         | 41.1 ms: 1.11x slower                                                                                                 |
| mako            | 11.8 ms                                                                                                         | 15.8 ms: 1.34x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.22x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20260825-3.16.0a0-e2118b0/bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0.json | results/bm-20260825-3.16.0a0-e2118b0-NOGIL/bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 229 ms                                                                                                          | 6.71 ms: 34.09x faster                                                                                                |
| gc_traversal               | 3.76 ms                                                                                                         | 1.76 ms: 2.14x faster                                                                                                 |
| create_gc_cycles           | 1.64 ms                                                                                                         | 1.36 ms: 1.21x faster                                                                                                 |
| sqlite_synth               | 2.25 us                                                                                                         | 1.95 us: 1.16x faster                                                                                                 |
| async_tree_io_tg           | 761 ms                                                                                                          | 694 ms: 1.10x faster                                                                                                  |
| asyncio_websockets         | 544 ms                                                                                                          | 512 ms: 1.06x faster                                                                                                  |
| regex_v8                   | 21.8 ms                                                                                                         | 21.0 ms: 1.04x faster                                                                                                 |
| async_tree_io              | 720 ms                                                                                                          | 704 ms: 1.02x faster                                                                                                  |
| pidigits                   | 187 ms                                                                                                          | 184 ms: 1.02x faster                                                                                                  |
| xml_etree_parse            | 142 ms                                                                                                          | 140 ms: 1.01x faster                                                                                                  |
| dulwich_log                | 68.5 ms                                                                                                         | 69.7 ms: 1.02x slower                                                                                                 |
| regex_dna                  | 177 ms                                                                                                          | 181 ms: 1.02x slower                                                                                                  |
| pycparser                  | 1.13 sec                                                                                                        | 1.17 sec: 1.03x slower                                                                                                |
| bpe_tokeniser              | 4.23 sec                                                                                                        | 4.38 sec: 1.04x slower                                                                                                |
| logging_silent             | 99.1 ns                                                                                                         | 103 ns: 1.04x slower                                                                                                  |
| xml_etree_iterparse        | 91.1 ms                                                                                                         | 95.3 ms: 1.05x slower                                                                                                 |
| async_tree_cpu_io_mixed_tg | 558 ms                                                                                                          | 584 ms: 1.05x slower                                                                                                  |
| coroutines                 | 23.5 ms                                                                                                         | 24.7 ms: 1.05x slower                                                                                                 |
| tomli_loads                | 1.79 sec                                                                                                        | 1.92 sec: 1.07x slower                                                                                                |
| json_dumps                 | 9.38 ms                                                                                                         | 10.1 ms: 1.08x slower                                                                                                 |
| k_core                     | 2.08 sec                                                                                                        | 2.25 sec: 1.08x slower                                                                                                |
| deltablue                  | 3.39 ms                                                                                                         | 3.67 ms: 1.08x slower                                                                                                 |
| scimark_sor                | 109 ms                                                                                                          | 118 ms: 1.08x slower                                                                                                  |
| scimark_lu                 | 117 ms                                                                                                          | 127 ms: 1.08x slower                                                                                                  |
| bench_thread_pool          | 1.35 ms                                                                                                         | 1.47 ms: 1.09x slower                                                                                                 |
| telco                      | 161 ms                                                                                                          | 175 ms: 1.09x slower                                                                                                  |
| async_tree_memoization_tg  | 366 ms                                                                                                          | 399 ms: 1.09x slower                                                                                                  |
| generators                 | 29.2 ms                                                                                                         | 31.8 ms: 1.09x slower                                                                                                 |
| pickle_pure_python         | 304 us                                                                                                          | 333 us: 1.09x slower                                                                                                  |
| many_optionals             | 912 us                                                                                                          | 1.00 ms: 1.10x slower                                                                                                 |
| json                       | 4.90 ms                                                                                                         | 5.39 ms: 1.10x slower                                                                                                 |
| async_tree_memoization     | 378 ms                                                                                                          | 418 ms: 1.11x slower                                                                                                  |
| sqlglot_v2_normalize       | 103 ms                                                                                                          | 114 ms: 1.11x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 539 ms                                                                                                          | 597 ms: 1.11x slower                                                                                                  |
| unpickle_pure_python       | 214 us                                                                                                          | 238 us: 1.11x slower                                                                                                  |
| django_template            | 37.0 ms                                                                                                         | 41.1 ms: 1.11x slower                                                                                                 |
| sqlglot_v2_optimize        | 51.9 ms                                                                                                         | 57.6 ms: 1.11x slower                                                                                                 |
| pprint_safe_repr           | 724 ms                                                                                                          | 807 ms: 1.11x slower                                                                                                  |
| scimark_fft                | 304 ms                                                                                                          | 339 ms: 1.12x slower                                                                                                  |
| comprehensions             | 15.9 us                                                                                                         | 17.8 us: 1.12x slower                                                                                                 |
| json_loads                 | 27.4 us                                                                                                         | 30.7 us: 1.12x slower                                                                                                 |
| deepcopy                   | 236 us                                                                                                          | 265 us: 1.13x slower                                                                                                  |
| chaos                      | 53.8 ms                                                                                                         | 60.5 ms: 1.13x slower                                                                                                 |
| sphinx                     | 985 ms                                                                                                          | 1.11 sec: 1.13x slower                                                                                                |
| async_tree_none_tg         | 296 ms                                                                                                          | 334 ms: 1.13x slower                                                                                                  |
| subparsers                 | 9.18 ms                                                                                                         | 10.4 ms: 1.13x slower                                                                                                 |
| sympy_expand               | 476 ms                                                                                                          | 538 ms: 1.13x slower                                                                                                  |
| go                         | 105 ms                                                                                                          | 119 ms: 1.13x slower                                                                                                  |
| pyflate                    | 401 ms                                                                                                          | 454 ms: 1.13x slower                                                                                                  |
| 2to3                       | 260 ms                                                                                                          | 295 ms: 1.13x slower                                                                                                  |
| sympy_integrate            | 19.3 ms                                                                                                         | 22.0 ms: 1.14x slower                                                                                                 |
| pprint_pformat             | 1.47 sec                                                                                                        | 1.68 sec: 1.14x slower                                                                                                |
| sympy_str                  | 280 ms                                                                                                          | 320 ms: 1.14x slower                                                                                                  |
| raytrace                   | 255 ms                                                                                                          | 291 ms: 1.14x slower                                                                                                  |
| regex_compile              | 148 ms                                                                                                          | 169 ms: 1.14x slower                                                                                                  |
| sympy_sum                  | 160 ms                                                                                                          | 183 ms: 1.14x slower                                                                                                  |
| pylint                     | 114 ms                                                                                                          | 130 ms: 1.14x slower                                                                                                  |
| mdp                        | 1.13 sec                                                                                                        | 1.30 sec: 1.14x slower                                                                                                |
| hexiom                     | 5.67 ms                                                                                                         | 6.51 ms: 1.15x slower                                                                                                 |
| xml_etree_generate         | 88.3 ms                                                                                                         | 102 ms: 1.15x slower                                                                                                  |
| float                      | 72.8 ms                                                                                                         | 83.9 ms: 1.15x slower                                                                                                 |
| html5lib                   | 58.1 ms                                                                                                         | 67.0 ms: 1.15x slower                                                                                                 |
| deepcopy_reduce            | 2.62 us                                                                                                         | 3.03 us: 1.15x slower                                                                                                 |
| deepcopy_memo              | 27.0 us                                                                                                         | 31.1 us: 1.15x slower                                                                                                 |
| regex_effbot               | 2.58 ms                                                                                                         | 2.98 ms: 1.16x slower                                                                                                 |
| async_tree_none            | 291 ms                                                                                                          | 341 ms: 1.17x slower                                                                                                  |
| richards                   | 44.4 ms                                                                                                         | 52.2 ms: 1.17x slower                                                                                                 |
| thrift                     | 790 us                                                                                                          | 928 us: 1.17x slower                                                                                                  |
| sqlglot_v2_transpile       | 1.47 ms                                                                                                         | 1.72 ms: 1.18x slower                                                                                                 |
| richards_super             | 50.9 ms                                                                                                         | 60.1 ms: 1.18x slower                                                                                                 |
| logging_simple             | 6.00 us                                                                                                         | 7.10 us: 1.18x slower                                                                                                 |
| logging_format             | 6.83 us                                                                                                         | 8.08 us: 1.18x slower                                                                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                                                                         | 5.22 ms: 1.19x slower                                                                                                 |
| spectral_norm              | 90.1 ms                                                                                                         | 107 ms: 1.19x slower                                                                                                  |
| async_generators           | 347 ms                                                                                                          | 414 ms: 1.19x slower                                                                                                  |
| nqueens                    | 73.0 ms                                                                                                         | 87.2 ms: 1.20x slower                                                                                                 |
| typing_runtime_protocols   | 120 us                                                                                                          | 144 us: 1.20x slower                                                                                                  |
| xml_etree_process          | 62.8 ms                                                                                                         | 75.6 ms: 1.20x slower                                                                                                 |
| sqlglot_v2_parse           | 1.17 ms                                                                                                         | 1.41 ms: 1.21x slower                                                                                                 |
| scimark_monte_carlo        | 63.2 ms                                                                                                         | 76.6 ms: 1.21x slower                                                                                                 |
| shortest_path              | 438 ms                                                                                                          | 533 ms: 1.22x slower                                                                                                  |
| docutils                   | 2.36 sec                                                                                                        | 2.91 sec: 1.23x slower                                                                                                |
| connected_components       | 397 ms                                                                                                          | 489 ms: 1.23x slower                                                                                                  |
| meteor_contest             | 103 ms                                                                                                          | 128 ms: 1.24x slower                                                                                                  |
| fannkuch                   | 373 ms                                                                                                          | 464 ms: 1.24x slower                                                                                                  |
| python_startup             | 12.9 ms                                                                                                         | 16.1 ms: 1.25x slower                                                                                                 |
| python_startup_no_site     | 7.70 ms                                                                                                         | 9.87 ms: 1.28x slower                                                                                                 |
| nbody                      | 91.5 ms                                                                                                         | 119 ms: 1.30x slower                                                                                                  |
| crypto_pyaes               | 67.4 ms                                                                                                         | 88.9 ms: 1.32x slower                                                                                                 |
| mako                       | 11.8 ms                                                                                                         | 15.8 ms: 1.34x slower                                                                                                 |
| coverage                   | 85.4 ms                                                                                                         | 115 ms: 1.35x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.07x slower                                                                                                          |

Benchmark hidden because not significant (1): pathlib

- Geometric mean (including insignificant results): 1.099x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.19x