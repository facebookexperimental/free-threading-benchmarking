# Results vs. base

- fork: python
- ref: 9e863fab283eddca9c2a
- machine: linux-x86_64
- commit hash: 9e863fa
- commit date: 2026-06-17
- overall geometric mean: 1.097x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260617-3.16.0a0-9e863fa/bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa.json | results/bm-20260617-3.16.0a0-9e863fa-NOGIL/bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 257 ms                                                                                                          | 295 ms: 1.15x slower                                                                                                  |
| docutils       | 2.43 sec                                                                                                        | 2.94 sec: 1.21x slower                                                                                                |
| html5lib       | 58.9 ms                                                                                                         | 68.5 ms: 1.16x slower                                                                                                 |
| sphinx         | 982 ms                                                                                                          | 1.11 sec: 1.13x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.16x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260617-3.16.0a0-9e863fa/bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa.json | results/bm-20260617-3.16.0a0-9e863fa-NOGIL/bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 760 ms                                                                                                          | 677 ms: 1.12x faster                                                                                                  |
| asyncio_websockets         | 544 ms                                                                                                          | 514 ms: 1.06x faster                                                                                                  |
| async_tree_io              | 719 ms                                                                                                          | 698 ms: 1.03x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 556 ms                                                                                                          | 579 ms: 1.04x slower                                                                                                  |
| coroutines                 | 23.2 ms                                                                                                         | 24.7 ms: 1.06x slower                                                                                                 |
| async_tree_none_tg         | 298 ms                                                                                                          | 319 ms: 1.07x slower                                                                                                  |
| async_tree_memoization_tg  | 362 ms                                                                                                          | 390 ms: 1.08x slower                                                                                                  |
| async_tree_memoization     | 378 ms                                                                                                          | 417 ms: 1.10x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 540 ms                                                                                                          | 606 ms: 1.12x slower                                                                                                  |
| async_generators           | 341 ms                                                                                                          | 388 ms: 1.14x slower                                                                                                  |
| async_tree_none            | 293 ms                                                                                                          | 340 ms: 1.16x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.05x slower                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260617-3.16.0a0-9e863fa/bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa.json | results/bm-20260617-3.16.0a0-9e863fa-NOGIL/bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 195 ms                                                                                                          | 180 ms: 1.08x faster                                                                                                  |
| float          | 75.6 ms                                                                                                         | 86.4 ms: 1.14x slower                                                                                                 |
| nbody          | 97.6 ms                                                                                                         | 127 ms: 1.30x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.11x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260617-3.16.0a0-9e863fa/bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa.json | results/bm-20260617-3.16.0a0-9e863fa-NOGIL/bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.6 ms                                                                                                         | 20.1 ms: 1.08x faster                                                                                                 |
| regex_dna      | 177 ms                                                                                                          | 177 ms: 1.00x slower                                                                                                  |
| regex_effbot   | 2.64 ms                                                                                                         | 3.02 ms: 1.14x slower                                                                                                 |
| regex_compile  | 123 ms                                                                                                          | 141 ms: 1.15x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.05x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260617-3.16.0a0-9e863fa/bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa.json | results/bm-20260617-3.16.0a0-9e863fa-NOGIL/bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 142 ms                                                                                                          | 141 ms: 1.01x faster                                                                                                  |
| xml_etree_iterparse  | 90.0 ms                                                                                                         | 94.9 ms: 1.05x slower                                                                                                 |
| tomli_loads          | 1.86 sec                                                                                                        | 1.97 sec: 1.06x slower                                                                                                |
| pickle_pure_python   | 314 us                                                                                                          | 337 us: 1.07x slower                                                                                                  |
| json_dumps           | 9.68 ms                                                                                                         | 10.6 ms: 1.09x slower                                                                                                 |
| unpickle_pure_python | 215 us                                                                                                          | 239 us: 1.11x slower                                                                                                  |
| json_loads           | 26.7 us                                                                                                         | 30.5 us: 1.14x slower                                                                                                 |
| xml_etree_generate   | 86.1 ms                                                                                                         | 99.2 ms: 1.15x slower                                                                                                 |
| xml_etree_process    | 60.8 ms                                                                                                         | 74.4 ms: 1.22x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.10x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260617-3.16.0a0-9e863fa/bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa.json | results/bm-20260617-3.16.0a0-9e863fa-NOGIL/bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.3 ms                                                                                                         | 15.4 ms: 1.25x slower                                                                                                 |
| python_startup_no_site | 6.95 ms                                                                                                         | 9.15 ms: 1.32x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.28x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260617-3.16.0a0-9e863fa/bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa.json | results/bm-20260617-3.16.0a0-9e863fa-NOGIL/bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 35.7 ms                                                                                                         | 40.1 ms: 1.12x slower                                                                                                 |
| mako            | 11.8 ms                                                                                                         | 15.9 ms: 1.34x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.23x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20260617-3.16.0a0-9e863fa/bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa.json | results/bm-20260617-3.16.0a0-9e863fa-NOGIL/bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 311 ms                                                                                                          | 6.79 ms: 45.72x faster                                                                                                |
| gc_traversal               | 4.02 ms                                                                                                         | 1.77 ms: 2.28x faster                                                                                                 |
| create_gc_cycles           | 1.68 ms                                                                                                         | 1.36 ms: 1.23x faster                                                                                                 |
| sqlite_synth               | 2.24 us                                                                                                         | 1.94 us: 1.16x faster                                                                                                 |
| async_tree_io_tg           | 760 ms                                                                                                          | 677 ms: 1.12x faster                                                                                                  |
| pidigits                   | 195 ms                                                                                                          | 180 ms: 1.08x faster                                                                                                  |
| regex_v8                   | 21.6 ms                                                                                                         | 20.1 ms: 1.08x faster                                                                                                 |
| asyncio_websockets         | 544 ms                                                                                                          | 514 ms: 1.06x faster                                                                                                  |
| pycparser                  | 1.18 sec                                                                                                        | 1.14 sec: 1.03x faster                                                                                                |
| async_tree_io              | 719 ms                                                                                                          | 698 ms: 1.03x faster                                                                                                  |
| xml_etree_parse            | 142 ms                                                                                                          | 141 ms: 1.01x faster                                                                                                  |
| regex_dna                  | 177 ms                                                                                                          | 177 ms: 1.00x slower                                                                                                  |
| dulwich_log                | 69.0 ms                                                                                                         | 71.0 ms: 1.03x slower                                                                                                 |
| bpe_tokeniser              | 4.21 sec                                                                                                        | 4.37 sec: 1.04x slower                                                                                                |
| async_tree_cpu_io_mixed_tg | 556 ms                                                                                                          | 579 ms: 1.04x slower                                                                                                  |
| xml_etree_iterparse        | 90.0 ms                                                                                                         | 94.9 ms: 1.05x slower                                                                                                 |
| json                       | 4.96 ms                                                                                                         | 5.23 ms: 1.06x slower                                                                                                 |
| tomli_loads                | 1.86 sec                                                                                                        | 1.97 sec: 1.06x slower                                                                                                |
| coroutines                 | 23.2 ms                                                                                                         | 24.7 ms: 1.06x slower                                                                                                 |
| scimark_fft                | 327 ms                                                                                                          | 351 ms: 1.07x slower                                                                                                  |
| async_tree_none_tg         | 298 ms                                                                                                          | 319 ms: 1.07x slower                                                                                                  |
| deltablue                  | 3.44 ms                                                                                                         | 3.69 ms: 1.07x slower                                                                                                 |
| pickle_pure_python         | 314 us                                                                                                          | 337 us: 1.07x slower                                                                                                  |
| async_tree_memoization_tg  | 362 ms                                                                                                          | 390 ms: 1.08x slower                                                                                                  |
| logging_silent             | 98.9 ns                                                                                                         | 107 ns: 1.08x slower                                                                                                  |
| many_optionals             | 916 us                                                                                                          | 998 us: 1.09x slower                                                                                                  |
| json_dumps                 | 9.68 ms                                                                                                         | 10.6 ms: 1.09x slower                                                                                                 |
| pprint_safe_repr           | 727 ms                                                                                                          | 795 ms: 1.09x slower                                                                                                  |
| telco                      | 160 ms                                                                                                          | 175 ms: 1.10x slower                                                                                                  |
| bench_thread_pool          | 1.34 ms                                                                                                         | 1.47 ms: 1.10x slower                                                                                                 |
| async_tree_memoization     | 378 ms                                                                                                          | 417 ms: 1.10x slower                                                                                                  |
| pyflate                    | 413 ms                                                                                                          | 457 ms: 1.11x slower                                                                                                  |
| scimark_sor                | 111 ms                                                                                                          | 123 ms: 1.11x slower                                                                                                  |
| unpickle_pure_python       | 215 us                                                                                                          | 239 us: 1.11x slower                                                                                                  |
| pprint_pformat             | 1.48 sec                                                                                                        | 1.65 sec: 1.11x slower                                                                                                |
| k_core                     | 2.03 sec                                                                                                        | 2.26 sec: 1.11x slower                                                                                                |
| sympy_expand               | 462 ms                                                                                                          | 518 ms: 1.12x slower                                                                                                  |
| django_template            | 35.7 ms                                                                                                         | 40.1 ms: 1.12x slower                                                                                                 |
| async_tree_cpu_io_mixed    | 540 ms                                                                                                          | 606 ms: 1.12x slower                                                                                                  |
| sympy_str                  | 275 ms                                                                                                          | 309 ms: 1.12x slower                                                                                                  |
| comprehensions             | 15.8 us                                                                                                         | 17.8 us: 1.12x slower                                                                                                 |
| deepcopy_reduce            | 2.57 us                                                                                                         | 2.90 us: 1.12x slower                                                                                                 |
| subparsers                 | 9.36 ms                                                                                                         | 10.5 ms: 1.13x slower                                                                                                 |
| sqlglot_v2_optimize        | 51.1 ms                                                                                                         | 57.5 ms: 1.13x slower                                                                                                 |
| sympy_sum                  | 158 ms                                                                                                          | 178 ms: 1.13x slower                                                                                                  |
| sphinx                     | 982 ms                                                                                                          | 1.11 sec: 1.13x slower                                                                                                |
| scimark_lu                 | 115 ms                                                                                                          | 130 ms: 1.13x slower                                                                                                  |
| sqlglot_v2_normalize       | 101 ms                                                                                                          | 114 ms: 1.13x slower                                                                                                  |
| logging_simple             | 6.00 us                                                                                                         | 6.81 us: 1.14x slower                                                                                                 |
| async_generators           | 341 ms                                                                                                          | 388 ms: 1.14x slower                                                                                                  |
| sympy_integrate            | 19.1 ms                                                                                                         | 21.8 ms: 1.14x slower                                                                                                 |
| json_loads                 | 26.7 us                                                                                                         | 30.5 us: 1.14x slower                                                                                                 |
| go                         | 107 ms                                                                                                          | 122 ms: 1.14x slower                                                                                                  |
| chaos                      | 55.1 ms                                                                                                         | 62.9 ms: 1.14x slower                                                                                                 |
| logging_format             | 6.80 us                                                                                                         | 7.77 us: 1.14x slower                                                                                                 |
| regex_effbot               | 2.64 ms                                                                                                         | 3.02 ms: 1.14x slower                                                                                                 |
| float                      | 75.6 ms                                                                                                         | 86.4 ms: 1.14x slower                                                                                                 |
| regex_compile              | 123 ms                                                                                                          | 141 ms: 1.15x slower                                                                                                  |
| 2to3                       | 257 ms                                                                                                          | 295 ms: 1.15x slower                                                                                                  |
| pylint                     | 115 ms                                                                                                          | 132 ms: 1.15x slower                                                                                                  |
| xml_etree_generate         | 86.1 ms                                                                                                         | 99.2 ms: 1.15x slower                                                                                                 |
| deepcopy                   | 230 us                                                                                                          | 265 us: 1.15x slower                                                                                                  |
| thrift                     | 782 us                                                                                                          | 902 us: 1.15x slower                                                                                                  |
| scimark_sparse_mat_mult    | 4.68 ms                                                                                                         | 5.42 ms: 1.16x slower                                                                                                 |
| hexiom                     | 5.78 ms                                                                                                         | 6.71 ms: 1.16x slower                                                                                                 |
| async_tree_none            | 293 ms                                                                                                          | 340 ms: 1.16x slower                                                                                                  |
| html5lib                   | 58.9 ms                                                                                                         | 68.5 ms: 1.16x slower                                                                                                 |
| mdp                        | 1.13 sec                                                                                                        | 1.32 sec: 1.16x slower                                                                                                |
| raytrace                   | 259 ms                                                                                                          | 304 ms: 1.17x slower                                                                                                  |
| sqlglot_v2_transpile       | 1.47 ms                                                                                                         | 1.72 ms: 1.17x slower                                                                                                 |
| deepcopy_memo              | 26.5 us                                                                                                         | 31.1 us: 1.18x slower                                                                                                 |
| nqueens                    | 74.1 ms                                                                                                         | 87.7 ms: 1.18x slower                                                                                                 |
| spectral_norm              | 93.7 ms                                                                                                         | 112 ms: 1.20x slower                                                                                                  |
| generators                 | 27.8 ms                                                                                                         | 33.4 ms: 1.20x slower                                                                                                 |
| docutils                   | 2.43 sec                                                                                                        | 2.94 sec: 1.21x slower                                                                                                |
| sqlglot_v2_parse           | 1.16 ms                                                                                                         | 1.40 ms: 1.21x slower                                                                                                 |
| shortest_path              | 440 ms                                                                                                          | 536 ms: 1.22x slower                                                                                                  |
| richards_super             | 49.4 ms                                                                                                         | 60.2 ms: 1.22x slower                                                                                                 |
| connected_components       | 399 ms                                                                                                          | 487 ms: 1.22x slower                                                                                                  |
| xml_etree_process          | 60.8 ms                                                                                                         | 74.4 ms: 1.22x slower                                                                                                 |
| richards                   | 43.5 ms                                                                                                         | 53.2 ms: 1.22x slower                                                                                                 |
| fannkuch                   | 379 ms                                                                                                          | 470 ms: 1.24x slower                                                                                                  |
| meteor_contest             | 100.0 ms                                                                                                        | 124 ms: 1.24x slower                                                                                                  |
| scimark_monte_carlo        | 64.1 ms                                                                                                         | 79.5 ms: 1.24x slower                                                                                                 |
| typing_runtime_protocols   | 119 us                                                                                                          | 148 us: 1.25x slower                                                                                                  |
| python_startup             | 12.3 ms                                                                                                         | 15.4 ms: 1.25x slower                                                                                                 |
| crypto_pyaes               | 69.7 ms                                                                                                         | 89.6 ms: 1.28x slower                                                                                                 |
| nbody                      | 97.6 ms                                                                                                         | 127 ms: 1.30x slower                                                                                                  |
| python_startup_no_site     | 6.95 ms                                                                                                         | 9.15 ms: 1.32x slower                                                                                                 |
| mako                       | 11.8 ms                                                                                                         | 15.9 ms: 1.34x slower                                                                                                 |
| coverage                   | 83.8 ms                                                                                                         | 114 ms: 1.37x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.06x slower                                                                                                          |

Benchmark hidden because not significant (1): pathlib

- Geometric mean (including insignificant results): 1.097x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.18x