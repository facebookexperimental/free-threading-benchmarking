# Results vs. base

- fork: python
- ref: 832bc0b0ea20c2fade5d
- machine: linux-x86_64
- commit hash: 832bc0b
- commit date: 2026-07-12
- overall geometric mean: 1.109x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260712-3.16.0a0-832bc0b/bm-20260712-vultr-x86_64-python-832bc0b0ea20c2fade5d-3.16.0a0-832bc0b.json | results/bm-20260712-3.16.0a0-832bc0b-NOGIL/bm-20260712-vultr-x86_64-python-832bc0b0ea20c2fade5d-3.16.0a0-832bc0b.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 257 ms                                                                                                          | 296 ms: 1.15x slower                                                                                                  |
| docutils       | 2.40 sec                                                                                                        | 3.00 sec: 1.25x slower                                                                                                |
| html5lib       | 58.0 ms                                                                                                         | 66.8 ms: 1.15x slower                                                                                                 |
| sphinx         | 982 ms                                                                                                          | 1.12 sec: 1.14x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.17x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260712-3.16.0a0-832bc0b/bm-20260712-vultr-x86_64-python-832bc0b0ea20c2fade5d-3.16.0a0-832bc0b.json | results/bm-20260712-3.16.0a0-832bc0b-NOGIL/bm-20260712-vultr-x86_64-python-832bc0b0ea20c2fade5d-3.16.0a0-832bc0b.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 754 ms                                                                                                          | 681 ms: 1.11x faster                                                                                                  |
| asyncio_websockets         | 543 ms                                                                                                          | 513 ms: 1.06x faster                                                                                                  |
| async_tree_io              | 715 ms                                                                                                          | 706 ms: 1.01x faster                                                                                                  |
| coroutines                 | 23.7 ms                                                                                                         | 25.0 ms: 1.05x slower                                                                                                 |
| async_tree_none_tg         | 295 ms                                                                                                          | 325 ms: 1.10x slower                                                                                                  |
| async_tree_memoization_tg  | 360 ms                                                                                                          | 396 ms: 1.10x slower                                                                                                  |
| async_tree_memoization     | 373 ms                                                                                                          | 419 ms: 1.12x slower                                                                                                  |
| async_generators           | 341 ms                                                                                                          | 392 ms: 1.15x slower                                                                                                  |
| async_tree_none            | 290 ms                                                                                                          | 340 ms: 1.17x slower                                                                                                  |
| async_tree_cpu_io_mixed_tg | 558 ms                                                                                                          | 676 ms: 1.21x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 541 ms                                                                                                          | 698 ms: 1.29x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260712-3.16.0a0-832bc0b/bm-20260712-vultr-x86_64-python-832bc0b0ea20c2fade5d-3.16.0a0-832bc0b.json | results/bm-20260712-3.16.0a0-832bc0b-NOGIL/bm-20260712-vultr-x86_64-python-832bc0b0ea20c2fade5d-3.16.0a0-832bc0b.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| float          | 75.9 ms                                                                                                         | 84.6 ms: 1.11x slower                                                                                                 |
| pidigits       | 199 ms                                                                                                          | 225 ms: 1.13x slower                                                                                                  |
| nbody          | 96.9 ms                                                                                                         | 127 ms: 1.31x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.18x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260712-3.16.0a0-832bc0b/bm-20260712-vultr-x86_64-python-832bc0b0ea20c2fade5d-3.16.0a0-832bc0b.json | results/bm-20260712-3.16.0a0-832bc0b-NOGIL/bm-20260712-vultr-x86_64-python-832bc0b0ea20c2fade5d-3.16.0a0-832bc0b.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.3 ms                                                                                                         | 20.3 ms: 1.05x faster                                                                                                 |
| regex_dna      | 178 ms                                                                                                          | 179 ms: 1.01x slower                                                                                                  |
| regex_effbot   | 2.60 ms                                                                                                         | 2.88 ms: 1.11x slower                                                                                                 |
| regex_compile  | 148 ms                                                                                                          | 168 ms: 1.13x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.05x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260712-3.16.0a0-832bc0b/bm-20260712-vultr-x86_64-python-832bc0b0ea20c2fade5d-3.16.0a0-832bc0b.json | results/bm-20260712-3.16.0a0-832bc0b-NOGIL/bm-20260712-vultr-x86_64-python-832bc0b0ea20c2fade5d-3.16.0a0-832bc0b.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 144 ms                                                                                                          | 141 ms: 1.02x faster                                                                                                  |
| xml_etree_iterparse  | 89.6 ms                                                                                                         | 95.2 ms: 1.06x slower                                                                                                 |
| tomli_loads          | 1.83 sec                                                                                                        | 1.98 sec: 1.08x slower                                                                                                |
| json_dumps           | 9.72 ms                                                                                                         | 10.6 ms: 1.09x slower                                                                                                 |
| json_loads           | 27.4 us                                                                                                         | 29.9 us: 1.09x slower                                                                                                 |
| pickle_pure_python   | 312 us                                                                                                          | 341 us: 1.10x slower                                                                                                  |
| unpickle_pure_python | 212 us                                                                                                          | 239 us: 1.13x slower                                                                                                  |
| xml_etree_generate   | 86.4 ms                                                                                                         | 101 ms: 1.16x slower                                                                                                  |
| xml_etree_process    | 60.8 ms                                                                                                         | 74.2 ms: 1.22x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.10x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260712-3.16.0a0-832bc0b/bm-20260712-vultr-x86_64-python-832bc0b0ea20c2fade5d-3.16.0a0-832bc0b.json | results/bm-20260712-3.16.0a0-832bc0b-NOGIL/bm-20260712-vultr-x86_64-python-832bc0b0ea20c2fade5d-3.16.0a0-832bc0b.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.4 ms                                                                                                         | 15.5 ms: 1.26x slower                                                                                                 |
| python_startup_no_site | 7.02 ms                                                                                                         | 9.23 ms: 1.32x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.29x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260712-3.16.0a0-832bc0b/bm-20260712-vultr-x86_64-python-832bc0b0ea20c2fade5d-3.16.0a0-832bc0b.json | results/bm-20260712-3.16.0a0-832bc0b-NOGIL/bm-20260712-vultr-x86_64-python-832bc0b0ea20c2fade5d-3.16.0a0-832bc0b.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 35.4 ms                                                                                                         | 39.7 ms: 1.12x slower                                                                                                 |
| mako            | 12.0 ms                                                                                                         | 15.9 ms: 1.32x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.22x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20260712-3.16.0a0-832bc0b/bm-20260712-vultr-x86_64-python-832bc0b0ea20c2fade5d-3.16.0a0-832bc0b.json | results/bm-20260712-3.16.0a0-832bc0b-NOGIL/bm-20260712-vultr-x86_64-python-832bc0b0ea20c2fade5d-3.16.0a0-832bc0b.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 233 ms                                                                                                          | 6.92 ms: 33.63x faster                                                                                                |
| gc_traversal               | 4.03 ms                                                                                                         | 1.76 ms: 2.29x faster                                                                                                 |
| create_gc_cycles           | 1.68 ms                                                                                                         | 1.36 ms: 1.24x faster                                                                                                 |
| sqlite_synth               | 2.22 us                                                                                                         | 1.96 us: 1.13x faster                                                                                                 |
| async_tree_io_tg           | 754 ms                                                                                                          | 681 ms: 1.11x faster                                                                                                  |
| asyncio_websockets         | 543 ms                                                                                                          | 513 ms: 1.06x faster                                                                                                  |
| regex_v8                   | 21.3 ms                                                                                                         | 20.3 ms: 1.05x faster                                                                                                 |
| xml_etree_parse            | 144 ms                                                                                                          | 141 ms: 1.02x faster                                                                                                  |
| async_tree_io              | 715 ms                                                                                                          | 706 ms: 1.01x faster                                                                                                  |
| pathlib                    | 17.9 ms                                                                                                         | 17.8 ms: 1.01x faster                                                                                                 |
| regex_dna                  | 178 ms                                                                                                          | 179 ms: 1.01x slower                                                                                                  |
| pycparser                  | 1.12 sec                                                                                                        | 1.13 sec: 1.01x slower                                                                                                |
| bpe_tokeniser              | 4.20 sec                                                                                                        | 4.37 sec: 1.04x slower                                                                                                |
| dulwich_log                | 68.2 ms                                                                                                         | 71.5 ms: 1.05x slower                                                                                                 |
| coroutines                 | 23.7 ms                                                                                                         | 25.0 ms: 1.05x slower                                                                                                 |
| json                       | 5.04 ms                                                                                                         | 5.31 ms: 1.05x slower                                                                                                 |
| xml_etree_iterparse        | 89.6 ms                                                                                                         | 95.2 ms: 1.06x slower                                                                                                 |
| tomli_loads                | 1.83 sec                                                                                                        | 1.98 sec: 1.08x slower                                                                                                |
| k_core                     | 2.09 sec                                                                                                        | 2.26 sec: 1.08x slower                                                                                                |
| many_optionals             | 912 us                                                                                                          | 990 us: 1.09x slower                                                                                                  |
| json_dumps                 | 9.72 ms                                                                                                         | 10.6 ms: 1.09x slower                                                                                                 |
| scimark_fft                | 323 ms                                                                                                          | 351 ms: 1.09x slower                                                                                                  |
| json_loads                 | 27.4 us                                                                                                         | 29.9 us: 1.09x slower                                                                                                 |
| pickle_pure_python         | 312 us                                                                                                          | 341 us: 1.10x slower                                                                                                  |
| bench_thread_pool          | 1.34 ms                                                                                                         | 1.47 ms: 1.10x slower                                                                                                 |
| async_tree_none_tg         | 295 ms                                                                                                          | 325 ms: 1.10x slower                                                                                                  |
| async_tree_memoization_tg  | 360 ms                                                                                                          | 396 ms: 1.10x slower                                                                                                  |
| telco                      | 157 ms                                                                                                          | 173 ms: 1.10x slower                                                                                                  |
| regex_effbot               | 2.60 ms                                                                                                         | 2.88 ms: 1.11x slower                                                                                                 |
| float                      | 75.9 ms                                                                                                         | 84.6 ms: 1.11x slower                                                                                                 |
| django_template            | 35.4 ms                                                                                                         | 39.7 ms: 1.12x slower                                                                                                 |
| async_tree_memoization     | 373 ms                                                                                                          | 419 ms: 1.12x slower                                                                                                  |
| comprehensions             | 16.0 us                                                                                                         | 18.0 us: 1.12x slower                                                                                                 |
| unpickle_pure_python       | 212 us                                                                                                          | 239 us: 1.13x slower                                                                                                  |
| logging_silent             | 97.7 ns                                                                                                         | 110 ns: 1.13x slower                                                                                                  |
| scimark_lu                 | 113 ms                                                                                                          | 128 ms: 1.13x slower                                                                                                  |
| sympy_str                  | 275 ms                                                                                                          | 312 ms: 1.13x slower                                                                                                  |
| sqlglot_v2_normalize       | 101 ms                                                                                                          | 114 ms: 1.13x slower                                                                                                  |
| logging_simple             | 6.03 us                                                                                                         | 6.84 us: 1.13x slower                                                                                                 |
| regex_compile              | 148 ms                                                                                                          | 168 ms: 1.13x slower                                                                                                  |
| sympy_expand               | 462 ms                                                                                                          | 524 ms: 1.13x slower                                                                                                  |
| pidigits                   | 199 ms                                                                                                          | 225 ms: 1.13x slower                                                                                                  |
| sphinx                     | 982 ms                                                                                                          | 1.12 sec: 1.14x slower                                                                                                |
| deepcopy_reduce            | 2.56 us                                                                                                         | 2.92 us: 1.14x slower                                                                                                 |
| deltablue                  | 3.26 ms                                                                                                         | 3.71 ms: 1.14x slower                                                                                                 |
| pprint_safe_repr           | 714 ms                                                                                                          | 815 ms: 1.14x slower                                                                                                  |
| sqlglot_v2_optimize        | 50.4 ms                                                                                                         | 57.5 ms: 1.14x slower                                                                                                 |
| sympy_integrate            | 19.1 ms                                                                                                         | 21.8 ms: 1.14x slower                                                                                                 |
| scimark_sor                | 108 ms                                                                                                          | 123 ms: 1.14x slower                                                                                                  |
| sympy_sum                  | 158 ms                                                                                                          | 180 ms: 1.14x slower                                                                                                  |
| chaos                      | 54.6 ms                                                                                                         | 62.5 ms: 1.14x slower                                                                                                 |
| thrift                     | 798 us                                                                                                          | 913 us: 1.15x slower                                                                                                  |
| logging_format             | 6.75 us                                                                                                         | 7.74 us: 1.15x slower                                                                                                 |
| pylint                     | 114 ms                                                                                                          | 131 ms: 1.15x slower                                                                                                  |
| 2to3                       | 257 ms                                                                                                          | 296 ms: 1.15x slower                                                                                                  |
| async_generators           | 341 ms                                                                                                          | 392 ms: 1.15x slower                                                                                                  |
| mdp                        | 1.14 sec                                                                                                        | 1.31 sec: 1.15x slower                                                                                                |
| html5lib                   | 58.0 ms                                                                                                         | 66.8 ms: 1.15x slower                                                                                                 |
| pyflate                    | 400 ms                                                                                                          | 461 ms: 1.15x slower                                                                                                  |
| subparsers                 | 9.19 ms                                                                                                         | 10.6 ms: 1.15x slower                                                                                                 |
| hexiom                     | 5.69 ms                                                                                                         | 6.60 ms: 1.16x slower                                                                                                 |
| spectral_norm              | 95.4 ms                                                                                                         | 111 ms: 1.16x slower                                                                                                  |
| pprint_pformat             | 1.45 sec                                                                                                        | 1.69 sec: 1.16x slower                                                                                                |
| xml_etree_generate         | 86.4 ms                                                                                                         | 101 ms: 1.16x slower                                                                                                  |
| deepcopy                   | 235 us                                                                                                          | 274 us: 1.17x slower                                                                                                  |
| async_tree_none            | 290 ms                                                                                                          | 340 ms: 1.17x slower                                                                                                  |
| go                         | 102 ms                                                                                                          | 120 ms: 1.18x slower                                                                                                  |
| scimark_sparse_mat_mult    | 4.64 ms                                                                                                         | 5.48 ms: 1.18x slower                                                                                                 |
| nqueens                    | 74.3 ms                                                                                                         | 87.8 ms: 1.18x slower                                                                                                 |
| sqlglot_v2_transpile       | 1.47 ms                                                                                                         | 1.75 ms: 1.18x slower                                                                                                 |
| deepcopy_memo              | 26.6 us                                                                                                         | 31.7 us: 1.19x slower                                                                                                 |
| raytrace                   | 254 ms                                                                                                          | 304 ms: 1.20x slower                                                                                                  |
| async_tree_cpu_io_mixed_tg | 558 ms                                                                                                          | 676 ms: 1.21x slower                                                                                                  |
| typing_runtime_protocols   | 117 us                                                                                                          | 142 us: 1.22x slower                                                                                                  |
| generators                 | 27.1 ms                                                                                                         | 33.1 ms: 1.22x slower                                                                                                 |
| xml_etree_process          | 60.8 ms                                                                                                         | 74.2 ms: 1.22x slower                                                                                                 |
| fannkuch                   | 381 ms                                                                                                          | 465 ms: 1.22x slower                                                                                                  |
| scimark_monte_carlo        | 64.4 ms                                                                                                         | 78.8 ms: 1.22x slower                                                                                                 |
| richards_super             | 48.7 ms                                                                                                         | 59.9 ms: 1.23x slower                                                                                                 |
| sqlglot_v2_parse           | 1.14 ms                                                                                                         | 1.41 ms: 1.24x slower                                                                                                 |
| shortest_path              | 437 ms                                                                                                          | 540 ms: 1.24x slower                                                                                                  |
| docutils                   | 2.40 sec                                                                                                        | 3.00 sec: 1.25x slower                                                                                                |
| richards                   | 42.9 ms                                                                                                         | 53.9 ms: 1.26x slower                                                                                                 |
| python_startup             | 12.4 ms                                                                                                         | 15.5 ms: 1.26x slower                                                                                                 |
| meteor_contest             | 103 ms                                                                                                          | 129 ms: 1.26x slower                                                                                                  |
| connected_components       | 393 ms                                                                                                          | 495 ms: 1.26x slower                                                                                                  |
| crypto_pyaes               | 69.8 ms                                                                                                         | 89.3 ms: 1.28x slower                                                                                                 |
| async_tree_cpu_io_mixed    | 541 ms                                                                                                          | 698 ms: 1.29x slower                                                                                                  |
| nbody                      | 96.9 ms                                                                                                         | 127 ms: 1.31x slower                                                                                                  |
| python_startup_no_site     | 7.02 ms                                                                                                         | 9.23 ms: 1.32x slower                                                                                                 |
| mako                       | 12.0 ms                                                                                                         | 15.9 ms: 1.32x slower                                                                                                 |
| coverage                   | 82.8 ms                                                                                                         | 114 ms: 1.38x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.08x slower                                                                                                          |

- Geometric mean (including insignificant results): 1.109x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.13x
- 95% likely to have a slowdown of 1.13x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 1.18x