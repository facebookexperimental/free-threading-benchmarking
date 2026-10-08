# Results vs. base

- fork: python
- ref: cdfdf7bb73a5751ecec7
- machine: linux-x86_64
- commit hash: cdfdf7b
- commit date: 2026-10-08
- overall geometric mean: 1.107x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20261008-3.16.0a0-cdfdf7b/bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b.json | results/bm-20261008-3.16.0a0-cdfdf7b-NOGIL/bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 257 ms                                                                                                          | 296 ms: 1.15x slower                                                                                                  |
| docutils       | 2.37 sec                                                                                                        | 2.90 sec: 1.22x slower                                                                                                |
| html5lib       | 57.9 ms                                                                                                         | 67.4 ms: 1.16x slower                                                                                                 |
| sphinx         | 984 ms                                                                                                          | 1.11 sec: 1.13x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.17x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20261008-3.16.0a0-cdfdf7b/bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b.json | results/bm-20261008-3.16.0a0-cdfdf7b-NOGIL/bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 763 ms                                                                                                          | 698 ms: 1.09x faster                                                                                                  |
| asyncio_websockets         | 544 ms                                                                                                          | 506 ms: 1.08x faster                                                                                                  |
| async_tree_io              | 720 ms                                                                                                          | 708 ms: 1.02x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 564 ms                                                                                                          | 612 ms: 1.09x slower                                                                                                  |
| async_tree_memoization_tg  | 367 ms                                                                                                          | 400 ms: 1.09x slower                                                                                                  |
| async_tree_none_tg         | 301 ms                                                                                                          | 333 ms: 1.11x slower                                                                                                  |
| async_tree_memoization     | 376 ms                                                                                                          | 423 ms: 1.12x slower                                                                                                  |
| async_tree_none            | 295 ms                                                                                                          | 343 ms: 1.16x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 543 ms                                                                                                          | 632 ms: 1.16x slower                                                                                                  |
| coroutines                 | 22.9 ms                                                                                                         | 27.1 ms: 1.18x slower                                                                                                 |
| async_generators           | 347 ms                                                                                                          | 421 ms: 1.22x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.08x slower                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20261008-3.16.0a0-cdfdf7b/bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b.json | results/bm-20261008-3.16.0a0-cdfdf7b-NOGIL/bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 187 ms                                                                                                          | 197 ms: 1.05x slower                                                                                                  |
| float          | 71.7 ms                                                                                                         | 85.2 ms: 1.19x slower                                                                                                 |
| nbody          | 89.7 ms                                                                                                         | 117 ms: 1.30x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.17x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20261008-3.16.0a0-cdfdf7b/bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b.json | results/bm-20261008-3.16.0a0-cdfdf7b-NOGIL/bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.4 ms                                                                                                         | 21.1 ms: 1.02x faster                                                                                                 |
| regex_dna      | 176 ms                                                                                                          | 178 ms: 1.01x slower                                                                                                  |
| regex_effbot   | 2.65 ms                                                                                                         | 2.98 ms: 1.12x slower                                                                                                 |
| regex_compile  | 148 ms                                                                                                          | 169 ms: 1.14x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.06x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20261008-3.16.0a0-cdfdf7b/bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b.json | results/bm-20261008-3.16.0a0-cdfdf7b-NOGIL/bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 144 ms                                                                                                          | 140 ms: 1.03x faster                                                                                                  |
| xml_etree_iterparse  | 92.3 ms                                                                                                         | 96.1 ms: 1.04x slower                                                                                                 |
| tomli_loads          | 1.82 sec                                                                                                        | 1.96 sec: 1.07x slower                                                                                                |
| json_dumps           | 9.26 ms                                                                                                         | 9.99 ms: 1.08x slower                                                                                                 |
| pickle_pure_python   | 301 us                                                                                                          | 335 us: 1.11x slower                                                                                                  |
| json_loads           | 27.0 us                                                                                                         | 30.5 us: 1.13x slower                                                                                                 |
| xml_etree_generate   | 89.3 ms                                                                                                         | 101 ms: 1.13x slower                                                                                                  |
| unpickle_pure_python | 211 us                                                                                                          | 240 us: 1.14x slower                                                                                                  |
| xml_etree_process    | 63.0 ms                                                                                                         | 75.5 ms: 1.20x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.10x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20261008-3.16.0a0-cdfdf7b/bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b.json | results/bm-20261008-3.16.0a0-cdfdf7b-NOGIL/bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup_no_site | 7.71 ms                                                                                                         | 9.70 ms: 1.26x slower                                                                                                 |
| python_startup         | 12.9 ms                                                                                                         | 16.3 ms: 1.26x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.26x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20261008-3.16.0a0-cdfdf7b/bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b.json | results/bm-20261008-3.16.0a0-cdfdf7b-NOGIL/bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 36.8 ms                                                                                                         | 41.5 ms: 1.13x slower                                                                                                 |
| mako            | 11.8 ms                                                                                                         | 15.9 ms: 1.35x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.23x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20261008-3.16.0a0-cdfdf7b/bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b.json | results/bm-20261008-3.16.0a0-cdfdf7b-NOGIL/bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 262 ms                                                                                                          | 6.75 ms: 38.79x faster                                                                                                |
| gc_traversal               | 4.01 ms                                                                                                         | 1.77 ms: 2.27x faster                                                                                                 |
| create_gc_cycles           | 1.63 ms                                                                                                         | 1.36 ms: 1.20x faster                                                                                                 |
| sqlite_synth               | 2.16 us                                                                                                         | 1.91 us: 1.13x faster                                                                                                 |
| async_tree_io_tg           | 763 ms                                                                                                          | 698 ms: 1.09x faster                                                                                                  |
| asyncio_websockets         | 544 ms                                                                                                          | 506 ms: 1.08x faster                                                                                                  |
| pycparser                  | 1.19 sec                                                                                                        | 1.14 sec: 1.04x faster                                                                                                |
| xml_etree_parse            | 144 ms                                                                                                          | 140 ms: 1.03x faster                                                                                                  |
| regex_v8                   | 21.4 ms                                                                                                         | 21.1 ms: 1.02x faster                                                                                                 |
| async_tree_io              | 720 ms                                                                                                          | 708 ms: 1.02x faster                                                                                                  |
| regex_dna                  | 176 ms                                                                                                          | 178 ms: 1.01x slower                                                                                                  |
| bpe_tokeniser              | 4.27 sec                                                                                                        | 4.44 sec: 1.04x slower                                                                                                |
| xml_etree_iterparse        | 92.3 ms                                                                                                         | 96.1 ms: 1.04x slower                                                                                                 |
| pidigits                   | 187 ms                                                                                                          | 197 ms: 1.05x slower                                                                                                  |
| dulwich_log                | 66.7 ms                                                                                                         | 70.1 ms: 1.05x slower                                                                                                 |
| json                       | 5.04 ms                                                                                                         | 5.41 ms: 1.07x slower                                                                                                 |
| tomli_loads                | 1.82 sec                                                                                                        | 1.96 sec: 1.07x slower                                                                                                |
| telco                      | 164 ms                                                                                                          | 176 ms: 1.08x slower                                                                                                  |
| json_dumps                 | 9.26 ms                                                                                                         | 9.99 ms: 1.08x slower                                                                                                 |
| async_tree_cpu_io_mixed_tg | 564 ms                                                                                                          | 612 ms: 1.09x slower                                                                                                  |
| async_tree_memoization_tg  | 367 ms                                                                                                          | 400 ms: 1.09x slower                                                                                                  |
| k_core                     | 2.08 sec                                                                                                        | 2.27 sec: 1.09x slower                                                                                                |
| scimark_lu                 | 119 ms                                                                                                          | 130 ms: 1.09x slower                                                                                                  |
| pprint_safe_repr           | 738 ms                                                                                                          | 808 ms: 1.10x slower                                                                                                  |
| scimark_fft                | 298 ms                                                                                                          | 327 ms: 1.10x slower                                                                                                  |
| chaos                      | 54.0 ms                                                                                                         | 59.6 ms: 1.10x slower                                                                                                 |
| sqlglot_v2_normalize       | 103 ms                                                                                                          | 114 ms: 1.10x slower                                                                                                  |
| async_tree_none_tg         | 301 ms                                                                                                          | 333 ms: 1.11x slower                                                                                                  |
| pickle_pure_python         | 301 us                                                                                                          | 335 us: 1.11x slower                                                                                                  |
| pprint_pformat             | 1.50 sec                                                                                                        | 1.67 sec: 1.11x slower                                                                                                |
| sqlglot_v2_optimize        | 50.6 ms                                                                                                         | 56.6 ms: 1.12x slower                                                                                                 |
| many_optionals             | 911 us                                                                                                          | 1.02 ms: 1.12x slower                                                                                                 |
| async_tree_memoization     | 376 ms                                                                                                          | 423 ms: 1.12x slower                                                                                                  |
| regex_effbot               | 2.65 ms                                                                                                         | 2.98 ms: 1.12x slower                                                                                                 |
| django_template            | 36.8 ms                                                                                                         | 41.5 ms: 1.13x slower                                                                                                 |
| sympy_expand               | 469 ms                                                                                                          | 529 ms: 1.13x slower                                                                                                  |
| logging_silent             | 94.6 ns                                                                                                         | 107 ns: 1.13x slower                                                                                                  |
| json_loads                 | 27.0 us                                                                                                         | 30.5 us: 1.13x slower                                                                                                 |
| sympy_str                  | 279 ms                                                                                                          | 316 ms: 1.13x slower                                                                                                  |
| xml_etree_generate         | 89.3 ms                                                                                                         | 101 ms: 1.13x slower                                                                                                  |
| sphinx                     | 984 ms                                                                                                          | 1.11 sec: 1.13x slower                                                                                                |
| deltablue                  | 3.32 ms                                                                                                         | 3.77 ms: 1.14x slower                                                                                                 |
| unpickle_pure_python       | 211 us                                                                                                          | 240 us: 1.14x slower                                                                                                  |
| mdp                        | 1.14 sec                                                                                                        | 1.30 sec: 1.14x slower                                                                                                |
| pyflate                    | 389 ms                                                                                                          | 443 ms: 1.14x slower                                                                                                  |
| sympy_integrate            | 19.1 ms                                                                                                         | 21.8 ms: 1.14x slower                                                                                                 |
| logging_simple             | 6.21 us                                                                                                         | 7.09 us: 1.14x slower                                                                                                 |
| sympy_sum                  | 157 ms                                                                                                          | 180 ms: 1.14x slower                                                                                                  |
| regex_compile              | 148 ms                                                                                                          | 169 ms: 1.14x slower                                                                                                  |
| scimark_sor                | 105 ms                                                                                                          | 121 ms: 1.15x slower                                                                                                  |
| 2to3                       | 257 ms                                                                                                          | 296 ms: 1.15x slower                                                                                                  |
| raytrace                   | 252 ms                                                                                                          | 291 ms: 1.16x slower                                                                                                  |
| scimark_sparse_mat_mult    | 4.20 ms                                                                                                         | 4.86 ms: 1.16x slower                                                                                                 |
| logging_format             | 6.91 us                                                                                                         | 7.99 us: 1.16x slower                                                                                                 |
| pylint                     | 113 ms                                                                                                          | 131 ms: 1.16x slower                                                                                                  |
| nqueens                    | 75.3 ms                                                                                                         | 87.2 ms: 1.16x slower                                                                                                 |
| subparsers                 | 8.99 ms                                                                                                         | 10.4 ms: 1.16x slower                                                                                                 |
| async_tree_none            | 295 ms                                                                                                          | 343 ms: 1.16x slower                                                                                                  |
| go                         | 103 ms                                                                                                          | 120 ms: 1.16x slower                                                                                                  |
| html5lib                   | 57.9 ms                                                                                                         | 67.4 ms: 1.16x slower                                                                                                 |
| async_tree_cpu_io_mixed    | 543 ms                                                                                                          | 632 ms: 1.16x slower                                                                                                  |
| comprehensions             | 15.8 us                                                                                                         | 18.4 us: 1.17x slower                                                                                                 |
| deepcopy_reduce            | 2.49 us                                                                                                         | 2.91 us: 1.17x slower                                                                                                 |
| deepcopy                   | 227 us                                                                                                          | 266 us: 1.17x slower                                                                                                  |
| spectral_norm              | 88.3 ms                                                                                                         | 103 ms: 1.17x slower                                                                                                  |
| coroutines                 | 22.9 ms                                                                                                         | 27.1 ms: 1.18x slower                                                                                                 |
| hexiom                     | 5.65 ms                                                                                                         | 6.69 ms: 1.18x slower                                                                                                 |
| float                      | 71.7 ms                                                                                                         | 85.2 ms: 1.19x slower                                                                                                 |
| thrift                     | 788 us                                                                                                          | 936 us: 1.19x slower                                                                                                  |
| sqlglot_v2_transpile       | 1.44 ms                                                                                                         | 1.73 ms: 1.20x slower                                                                                                 |
| xml_etree_process          | 63.0 ms                                                                                                         | 75.5 ms: 1.20x slower                                                                                                 |
| richards                   | 44.1 ms                                                                                                         | 53.1 ms: 1.20x slower                                                                                                 |
| richards_super             | 50.1 ms                                                                                                         | 60.7 ms: 1.21x slower                                                                                                 |
| async_generators           | 347 ms                                                                                                          | 421 ms: 1.22x slower                                                                                                  |
| sqlglot_v2_parse           | 1.15 ms                                                                                                         | 1.40 ms: 1.22x slower                                                                                                 |
| bench_thread_pool          | 1.34 ms                                                                                                         | 1.64 ms: 1.22x slower                                                                                                 |
| shortest_path              | 436 ms                                                                                                          | 532 ms: 1.22x slower                                                                                                  |
| deepcopy_memo              | 26.9 us                                                                                                         | 32.9 us: 1.22x slower                                                                                                 |
| docutils                   | 2.37 sec                                                                                                        | 2.90 sec: 1.22x slower                                                                                                |
| connected_components       | 397 ms                                                                                                          | 487 ms: 1.23x slower                                                                                                  |
| typing_runtime_protocols   | 119 us                                                                                                          | 146 us: 1.23x slower                                                                                                  |
| scimark_monte_carlo        | 62.2 ms                                                                                                         | 76.9 ms: 1.24x slower                                                                                                 |
| fannkuch                   | 372 ms                                                                                                          | 465 ms: 1.25x slower                                                                                                  |
| python_startup_no_site     | 7.71 ms                                                                                                         | 9.70 ms: 1.26x slower                                                                                                 |
| python_startup             | 12.9 ms                                                                                                         | 16.3 ms: 1.26x slower                                                                                                 |
| generators                 | 27.7 ms                                                                                                         | 35.1 ms: 1.27x slower                                                                                                 |
| meteor_contest             | 100 ms                                                                                                          | 128 ms: 1.27x slower                                                                                                  |
| crypto_pyaes               | 67.1 ms                                                                                                         | 87.1 ms: 1.30x slower                                                                                                 |
| nbody                      | 89.7 ms                                                                                                         | 117 ms: 1.30x slower                                                                                                  |
| mako                       | 11.8 ms                                                                                                         | 15.9 ms: 1.35x slower                                                                                                 |
| coverage                   | 85.7 ms                                                                                                         | 117 ms: 1.37x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.08x slower                                                                                                          |

Benchmark hidden because not significant (1): pathlib

- Geometric mean (including insignificant results): 1.107x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.18x