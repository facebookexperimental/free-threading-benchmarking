# Results vs. base

- fork: python
- ref: 1f9d20bbd4fed601e7ca
- machine: linux-x86_64
- commit hash: 1f9d20b
- commit date: 2026-07-20
- overall geometric mean: 1.109x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260720-3.16.0a0-1f9d20b/bm-20260720-vultr-x86_64-python-1f9d20bbd4fed601e7ca-3.16.0a0-1f9d20b.json | results/bm-20260720-3.16.0a0-1f9d20b-NOGIL/bm-20260720-vultr-x86_64-python-1f9d20bbd4fed601e7ca-3.16.0a0-1f9d20b.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 257 ms                                                                                                          | 294 ms: 1.14x slower                                                                                                  |
| docutils       | 2.37 sec                                                                                                        | 2.96 sec: 1.24x slower                                                                                                |
| html5lib       | 58.8 ms                                                                                                         | 65.0 ms: 1.10x slower                                                                                                 |
| sphinx         | 979 ms                                                                                                          | 1.12 sec: 1.15x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.16x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260720-3.16.0a0-1f9d20b/bm-20260720-vultr-x86_64-python-1f9d20bbd4fed601e7ca-3.16.0a0-1f9d20b.json | results/bm-20260720-3.16.0a0-1f9d20b-NOGIL/bm-20260720-vultr-x86_64-python-1f9d20bbd4fed601e7ca-3.16.0a0-1f9d20b.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 754 ms                                                                                                          | 683 ms: 1.10x faster                                                                                                  |
| asyncio_websockets         | 544 ms                                                                                                          | 515 ms: 1.06x faster                                                                                                  |
| async_tree_io              | 714 ms                                                                                                          | 699 ms: 1.02x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 556 ms                                                                                                          | 578 ms: 1.04x slower                                                                                                  |
| coroutines                 | 23.4 ms                                                                                                         | 25.1 ms: 1.07x slower                                                                                                 |
| async_tree_memoization_tg  | 362 ms                                                                                                          | 394 ms: 1.09x slower                                                                                                  |
| async_tree_none_tg         | 295 ms                                                                                                          | 324 ms: 1.10x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 540 ms                                                                                                          | 597 ms: 1.11x slower                                                                                                  |
| async_tree_memoization     | 371 ms                                                                                                          | 418 ms: 1.13x slower                                                                                                  |
| async_generators           | 341 ms                                                                                                          | 385 ms: 1.13x slower                                                                                                  |
| async_tree_none            | 290 ms                                                                                                          | 339 ms: 1.17x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.06x slower                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260720-3.16.0a0-1f9d20b/bm-20260720-vultr-x86_64-python-1f9d20bbd4fed601e7ca-3.16.0a0-1f9d20b.json | results/bm-20260720-3.16.0a0-1f9d20b-NOGIL/bm-20260720-vultr-x86_64-python-1f9d20bbd4fed601e7ca-3.16.0a0-1f9d20b.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 187 ms                                                                                                          | 180 ms: 1.04x faster                                                                                                  |
| float          | 73.5 ms                                                                                                         | 86.4 ms: 1.18x slower                                                                                                 |
| nbody          | 93.0 ms                                                                                                         | 127 ms: 1.37x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.16x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260720-3.16.0a0-1f9d20b/bm-20260720-vultr-x86_64-python-1f9d20bbd4fed601e7ca-3.16.0a0-1f9d20b.json | results/bm-20260720-3.16.0a0-1f9d20b-NOGIL/bm-20260720-vultr-x86_64-python-1f9d20bbd4fed601e7ca-3.16.0a0-1f9d20b.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.5 ms                                                                                                         | 20.7 ms: 1.04x faster                                                                                                 |
| regex_dna      | 181 ms                                                                                                          | 182 ms: 1.01x slower                                                                                                  |
| regex_compile  | 147 ms                                                                                                          | 168 ms: 1.14x slower                                                                                                  |
| regex_effbot   | 2.63 ms                                                                                                         | 3.03 ms: 1.15x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                           | 1.06x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260720-3.16.0a0-1f9d20b/bm-20260720-vultr-x86_64-python-1f9d20bbd4fed601e7ca-3.16.0a0-1f9d20b.json | results/bm-20260720-3.16.0a0-1f9d20b-NOGIL/bm-20260720-vultr-x86_64-python-1f9d20bbd4fed601e7ca-3.16.0a0-1f9d20b.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 144 ms                                                                                                          | 140 ms: 1.03x faster                                                                                                  |
| tomli_loads          | 1.85 sec                                                                                                        | 1.94 sec: 1.05x slower                                                                                                |
| xml_etree_iterparse  | 89.4 ms                                                                                                         | 94.9 ms: 1.06x slower                                                                                                 |
| json_dumps           | 9.80 ms                                                                                                         | 10.6 ms: 1.08x slower                                                                                                 |
| json_loads           | 27.4 us                                                                                                         | 30.3 us: 1.11x slower                                                                                                 |
| pickle_pure_python   | 304 us                                                                                                          | 341 us: 1.12x slower                                                                                                  |
| unpickle_pure_python | 211 us                                                                                                          | 238 us: 1.13x slower                                                                                                  |
| xml_etree_generate   | 85.8 ms                                                                                                         | 101 ms: 1.17x slower                                                                                                  |
| xml_etree_process    | 60.1 ms                                                                                                         | 74.7 ms: 1.24x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.10x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260720-3.16.0a0-1f9d20b/bm-20260720-vultr-x86_64-python-1f9d20bbd4fed601e7ca-3.16.0a0-1f9d20b.json | results/bm-20260720-3.16.0a0-1f9d20b-NOGIL/bm-20260720-vultr-x86_64-python-1f9d20bbd4fed601e7ca-3.16.0a0-1f9d20b.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.4 ms                                                                                                         | 15.6 ms: 1.26x slower                                                                                                 |
| python_startup_no_site | 7.05 ms                                                                                                         | 9.29 ms: 1.32x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.29x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260720-3.16.0a0-1f9d20b/bm-20260720-vultr-x86_64-python-1f9d20bbd4fed601e7ca-3.16.0a0-1f9d20b.json | results/bm-20260720-3.16.0a0-1f9d20b-NOGIL/bm-20260720-vultr-x86_64-python-1f9d20bbd4fed601e7ca-3.16.0a0-1f9d20b.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 35.9 ms                                                                                                         | 40.7 ms: 1.13x slower                                                                                                 |
| mako            | 11.8 ms                                                                                                         | 16.1 ms: 1.36x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.24x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20260720-3.16.0a0-1f9d20b/bm-20260720-vultr-x86_64-python-1f9d20bbd4fed601e7ca-3.16.0a0-1f9d20b.json | results/bm-20260720-3.16.0a0-1f9d20b-NOGIL/bm-20260720-vultr-x86_64-python-1f9d20bbd4fed601e7ca-3.16.0a0-1f9d20b.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 256 ms                                                                                                          | 13.3 ms: 19.25x faster                                                                                                |
| gc_traversal               | 3.99 ms                                                                                                         | 1.77 ms: 2.25x faster                                                                                                 |
| create_gc_cycles           | 1.65 ms                                                                                                         | 1.37 ms: 1.20x faster                                                                                                 |
| sqlite_synth               | 2.22 us                                                                                                         | 1.97 us: 1.13x faster                                                                                                 |
| async_tree_io_tg           | 754 ms                                                                                                          | 683 ms: 1.10x faster                                                                                                  |
| asyncio_websockets         | 544 ms                                                                                                          | 515 ms: 1.06x faster                                                                                                  |
| regex_v8                   | 21.5 ms                                                                                                         | 20.7 ms: 1.04x faster                                                                                                 |
| pidigits                   | 187 ms                                                                                                          | 180 ms: 1.04x faster                                                                                                  |
| xml_etree_parse            | 144 ms                                                                                                          | 140 ms: 1.03x faster                                                                                                  |
| async_tree_io              | 714 ms                                                                                                          | 699 ms: 1.02x faster                                                                                                  |
| regex_dna                  | 181 ms                                                                                                          | 182 ms: 1.01x slower                                                                                                  |
| pathlib                    | 17.7 ms                                                                                                         | 17.9 ms: 1.01x slower                                                                                                 |
| bpe_tokeniser              | 4.21 sec                                                                                                        | 4.35 sec: 1.03x slower                                                                                                |
| async_tree_cpu_io_mixed_tg | 556 ms                                                                                                          | 578 ms: 1.04x slower                                                                                                  |
| tomli_loads                | 1.85 sec                                                                                                        | 1.94 sec: 1.05x slower                                                                                                |
| dulwich_log                | 67.5 ms                                                                                                         | 71.3 ms: 1.06x slower                                                                                                 |
| xml_etree_iterparse        | 89.4 ms                                                                                                         | 94.9 ms: 1.06x slower                                                                                                 |
| pycparser                  | 1.09 sec                                                                                                        | 1.17 sec: 1.07x slower                                                                                                |
| coroutines                 | 23.4 ms                                                                                                         | 25.1 ms: 1.07x slower                                                                                                 |
| json                       | 4.99 ms                                                                                                         | 5.37 ms: 1.08x slower                                                                                                 |
| json_dumps                 | 9.80 ms                                                                                                         | 10.6 ms: 1.08x slower                                                                                                 |
| k_core                     | 2.07 sec                                                                                                        | 2.24 sec: 1.08x slower                                                                                                |
| async_tree_memoization_tg  | 362 ms                                                                                                          | 394 ms: 1.09x slower                                                                                                  |
| logging_silent             | 94.7 ns                                                                                                         | 103 ns: 1.09x slower                                                                                                  |
| scimark_fft                | 319 ms                                                                                                          | 349 ms: 1.09x slower                                                                                                  |
| async_tree_none_tg         | 295 ms                                                                                                          | 324 ms: 1.10x slower                                                                                                  |
| telco                      | 158 ms                                                                                                          | 174 ms: 1.10x slower                                                                                                  |
| html5lib                   | 58.8 ms                                                                                                         | 65.0 ms: 1.10x slower                                                                                                 |
| many_optionals             | 912 us                                                                                                          | 1.01 ms: 1.11x slower                                                                                                 |
| async_tree_cpu_io_mixed    | 540 ms                                                                                                          | 597 ms: 1.11x slower                                                                                                  |
| json_loads                 | 27.4 us                                                                                                         | 30.3 us: 1.11x slower                                                                                                 |
| pprint_safe_repr           | 721 ms                                                                                                          | 799 ms: 1.11x slower                                                                                                  |
| bench_thread_pool          | 1.34 ms                                                                                                         | 1.49 ms: 1.11x slower                                                                                                 |
| scimark_sparse_mat_mult    | 4.66 ms                                                                                                         | 5.20 ms: 1.12x slower                                                                                                 |
| pickle_pure_python         | 304 us                                                                                                          | 341 us: 1.12x slower                                                                                                  |
| unpickle_pure_python       | 211 us                                                                                                          | 238 us: 1.13x slower                                                                                                  |
| sqlglot_v2_normalize       | 100 ms                                                                                                          | 113 ms: 1.13x slower                                                                                                  |
| async_tree_memoization     | 371 ms                                                                                                          | 418 ms: 1.13x slower                                                                                                  |
| async_generators           | 341 ms                                                                                                          | 385 ms: 1.13x slower                                                                                                  |
| pprint_pformat             | 1.46 sec                                                                                                        | 1.65 sec: 1.13x slower                                                                                                |
| django_template            | 35.9 ms                                                                                                         | 40.7 ms: 1.13x slower                                                                                                 |
| scimark_lu                 | 113 ms                                                                                                          | 128 ms: 1.14x slower                                                                                                  |
| sqlglot_v2_optimize        | 50.4 ms                                                                                                         | 57.4 ms: 1.14x slower                                                                                                 |
| sympy_expand               | 456 ms                                                                                                          | 521 ms: 1.14x slower                                                                                                  |
| sympy_str                  | 271 ms                                                                                                          | 310 ms: 1.14x slower                                                                                                  |
| regex_compile              | 147 ms                                                                                                          | 168 ms: 1.14x slower                                                                                                  |
| 2to3                       | 257 ms                                                                                                          | 294 ms: 1.14x slower                                                                                                  |
| comprehensions             | 15.7 us                                                                                                         | 18.0 us: 1.15x slower                                                                                                 |
| subparsers                 | 9.18 ms                                                                                                         | 10.5 ms: 1.15x slower                                                                                                 |
| sphinx                     | 979 ms                                                                                                          | 1.12 sec: 1.15x slower                                                                                                |
| pylint                     | 114 ms                                                                                                          | 130 ms: 1.15x slower                                                                                                  |
| mdp                        | 1.13 sec                                                                                                        | 1.30 sec: 1.15x slower                                                                                                |
| regex_effbot               | 2.63 ms                                                                                                         | 3.03 ms: 1.15x slower                                                                                                 |
| hexiom                     | 5.69 ms                                                                                                         | 6.55 ms: 1.15x slower                                                                                                 |
| scimark_sor                | 108 ms                                                                                                          | 124 ms: 1.15x slower                                                                                                  |
| deltablue                  | 3.22 ms                                                                                                         | 3.72 ms: 1.15x slower                                                                                                 |
| chaos                      | 53.8 ms                                                                                                         | 62.2 ms: 1.16x slower                                                                                                 |
| sympy_integrate            | 18.9 ms                                                                                                         | 21.9 ms: 1.16x slower                                                                                                 |
| deepcopy_reduce            | 2.52 us                                                                                                         | 2.92 us: 1.16x slower                                                                                                 |
| deepcopy                   | 232 us                                                                                                          | 270 us: 1.16x slower                                                                                                  |
| deepcopy_memo              | 26.6 us                                                                                                         | 30.9 us: 1.16x slower                                                                                                 |
| nqueens                    | 75.0 ms                                                                                                         | 87.5 ms: 1.17x slower                                                                                                 |
| sympy_sum                  | 154 ms                                                                                                          | 180 ms: 1.17x slower                                                                                                  |
| async_tree_none            | 290 ms                                                                                                          | 339 ms: 1.17x slower                                                                                                  |
| pyflate                    | 394 ms                                                                                                          | 462 ms: 1.17x slower                                                                                                  |
| xml_etree_generate         | 85.8 ms                                                                                                         | 101 ms: 1.17x slower                                                                                                  |
| float                      | 73.5 ms                                                                                                         | 86.4 ms: 1.18x slower                                                                                                 |
| go                         | 102 ms                                                                                                          | 120 ms: 1.18x slower                                                                                                  |
| spectral_norm              | 94.4 ms                                                                                                         | 112 ms: 1.18x slower                                                                                                  |
| logging_simple             | 5.86 us                                                                                                         | 6.96 us: 1.19x slower                                                                                                 |
| thrift                     | 764 us                                                                                                          | 910 us: 1.19x slower                                                                                                  |
| sqlglot_v2_transpile       | 1.45 ms                                                                                                         | 1.74 ms: 1.20x slower                                                                                                 |
| raytrace                   | 250 ms                                                                                                          | 300 ms: 1.20x slower                                                                                                  |
| logging_format             | 6.56 us                                                                                                         | 7.92 us: 1.21x slower                                                                                                 |
| typing_runtime_protocols   | 118 us                                                                                                          | 144 us: 1.22x slower                                                                                                  |
| shortest_path              | 435 ms                                                                                                          | 531 ms: 1.22x slower                                                                                                  |
| fannkuch                   | 375 ms                                                                                                          | 458 ms: 1.22x slower                                                                                                  |
| generators                 | 27.4 ms                                                                                                         | 33.5 ms: 1.22x slower                                                                                                 |
| meteor_contest             | 101 ms                                                                                                          | 124 ms: 1.23x slower                                                                                                  |
| sqlglot_v2_parse           | 1.14 ms                                                                                                         | 1.40 ms: 1.23x slower                                                                                                 |
| connected_components       | 394 ms                                                                                                          | 487 ms: 1.24x slower                                                                                                  |
| xml_etree_process          | 60.1 ms                                                                                                         | 74.7 ms: 1.24x slower                                                                                                 |
| docutils                   | 2.37 sec                                                                                                        | 2.96 sec: 1.24x slower                                                                                                |
| richards_super             | 48.0 ms                                                                                                         | 60.0 ms: 1.25x slower                                                                                                 |
| scimark_monte_carlo        | 63.2 ms                                                                                                         | 79.1 ms: 1.25x slower                                                                                                 |
| python_startup             | 12.4 ms                                                                                                         | 15.6 ms: 1.26x slower                                                                                                 |
| richards                   | 42.2 ms                                                                                                         | 53.9 ms: 1.28x slower                                                                                                 |
| crypto_pyaes               | 69.4 ms                                                                                                         | 89.9 ms: 1.30x slower                                                                                                 |
| python_startup_no_site     | 7.05 ms                                                                                                         | 9.29 ms: 1.32x slower                                                                                                 |
| mako                       | 11.8 ms                                                                                                         | 16.1 ms: 1.36x slower                                                                                                 |
| nbody                      | 93.0 ms                                                                                                         | 127 ms: 1.37x slower                                                                                                  |
| coverage                   | 82.5 ms                                                                                                         | 115 ms: 1.39x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.09x slower                                                                                                          |

- Geometric mean (including insignificant results): 1.109x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.12x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.18x