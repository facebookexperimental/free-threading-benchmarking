# Results vs. base

- fork: python
- ref: fe3a26f43fad1d6eed20
- machine: linux-x86_64
- commit hash: fe3a26f
- commit date: 2026-08-26
- overall geometric mean: 1.103x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260826-3.16.0a0-fe3a26f/bm-20260826-vultr-x86_64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f.json | results/bm-20260826-3.16.0a0-fe3a26f-NOGIL/bm-20260826-vultr-x86_64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                                                          | 297 ms: 1.15x slower                                                                                                  |
| docutils       | 2.34 sec                                                                                                        | 2.93 sec: 1.25x slower                                                                                                |
| html5lib       | 59.4 ms                                                                                                         | 67.0 ms: 1.13x slower                                                                                                 |
| sphinx         | 982 ms                                                                                                          | 1.11 sec: 1.13x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.16x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260826-3.16.0a0-fe3a26f/bm-20260826-vultr-x86_64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f.json | results/bm-20260826-3.16.0a0-fe3a26f-NOGIL/bm-20260826-vultr-x86_64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 765 ms                                                                                                          | 684 ms: 1.12x faster                                                                                                  |
| asyncio_websockets         | 544 ms                                                                                                          | 511 ms: 1.06x faster                                                                                                  |
| async_tree_io              | 723 ms                                                                                                          | 701 ms: 1.03x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 560 ms                                                                                                          | 581 ms: 1.04x slower                                                                                                  |
| coroutines                 | 23.1 ms                                                                                                         | 24.0 ms: 1.04x slower                                                                                                 |
| async_tree_memoization_tg  | 366 ms                                                                                                          | 395 ms: 1.08x slower                                                                                                  |
| async_tree_none_tg         | 301 ms                                                                                                          | 331 ms: 1.10x slower                                                                                                  |
| async_tree_memoization     | 374 ms                                                                                                          | 418 ms: 1.12x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 536 ms                                                                                                          | 599 ms: 1.12x slower                                                                                                  |
| async_tree_none            | 292 ms                                                                                                          | 340 ms: 1.16x slower                                                                                                  |
| async_generators           | 349 ms                                                                                                          | 418 ms: 1.19x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.06x slower                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260826-3.16.0a0-fe3a26f/bm-20260826-vultr-x86_64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f.json | results/bm-20260826-3.16.0a0-fe3a26f-NOGIL/bm-20260826-vultr-x86_64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 187 ms                                                                                                          | 181 ms: 1.03x faster                                                                                                  |
| float          | 72.8 ms                                                                                                         | 84.3 ms: 1.16x slower                                                                                                 |
| nbody          | 92.3 ms                                                                                                         | 123 ms: 1.33x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.14x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260826-3.16.0a0-fe3a26f/bm-20260826-vultr-x86_64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f.json | results/bm-20260826-3.16.0a0-fe3a26f-NOGIL/bm-20260826-vultr-x86_64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.5 ms                                                                                                         | 21.1 ms: 1.02x faster                                                                                                 |
| regex_dna      | 177 ms                                                                                                          | 184 ms: 1.04x slower                                                                                                  |
| regex_compile  | 147 ms                                                                                                          | 169 ms: 1.15x slower                                                                                                  |
| regex_effbot   | 2.55 ms                                                                                                         | 2.99 ms: 1.17x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                           | 1.08x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260826-3.16.0a0-fe3a26f/bm-20260826-vultr-x86_64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f.json | results/bm-20260826-3.16.0a0-fe3a26f-NOGIL/bm-20260826-vultr-x86_64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 90.8 ms                                                                                                         | 95.1 ms: 1.05x slower                                                                                                 |
| json_dumps           | 9.48 ms                                                                                                         | 10.0 ms: 1.06x slower                                                                                                 |
| tomli_loads          | 1.81 sec                                                                                                        | 1.95 sec: 1.07x slower                                                                                                |
| pickle_pure_python   | 304 us                                                                                                          | 333 us: 1.09x slower                                                                                                  |
| json_loads           | 27.1 us                                                                                                         | 30.6 us: 1.13x slower                                                                                                 |
| unpickle_pure_python | 210 us                                                                                                          | 240 us: 1.14x slower                                                                                                  |
| xml_etree_generate   | 88.1 ms                                                                                                         | 101 ms: 1.15x slower                                                                                                  |
| xml_etree_process    | 62.0 ms                                                                                                         | 75.2 ms: 1.21x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.10x slower                                                                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260826-3.16.0a0-fe3a26f/bm-20260826-vultr-x86_64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f.json | results/bm-20260826-3.16.0a0-fe3a26f-NOGIL/bm-20260826-vultr-x86_64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 13.0 ms                                                                                                         | 16.1 ms: 1.24x slower                                                                                                 |
| python_startup_no_site | 7.74 ms                                                                                                         | 9.94 ms: 1.28x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.26x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260826-3.16.0a0-fe3a26f/bm-20260826-vultr-x86_64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f.json | results/bm-20260826-3.16.0a0-fe3a26f-NOGIL/bm-20260826-vultr-x86_64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 36.8 ms                                                                                                         | 41.3 ms: 1.12x slower                                                                                                 |
| mako            | 11.9 ms                                                                                                         | 16.2 ms: 1.36x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.23x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20260826-3.16.0a0-fe3a26f/bm-20260826-vultr-x86_64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f.json | results/bm-20260826-3.16.0a0-fe3a26f-NOGIL/bm-20260826-vultr-x86_64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 250 ms                                                                                                          | 6.70 ms: 37.37x faster                                                                                                |
| gc_traversal               | 3.77 ms                                                                                                         | 1.78 ms: 2.12x faster                                                                                                 |
| create_gc_cycles           | 1.70 ms                                                                                                         | 1.37 ms: 1.24x faster                                                                                                 |
| sqlite_synth               | 2.27 us                                                                                                         | 1.94 us: 1.17x faster                                                                                                 |
| async_tree_io_tg           | 765 ms                                                                                                          | 684 ms: 1.12x faster                                                                                                  |
| asyncio_websockets         | 544 ms                                                                                                          | 511 ms: 1.06x faster                                                                                                  |
| pidigits                   | 187 ms                                                                                                          | 181 ms: 1.03x faster                                                                                                  |
| async_tree_io              | 723 ms                                                                                                          | 701 ms: 1.03x faster                                                                                                  |
| regex_v8                   | 21.5 ms                                                                                                         | 21.1 ms: 1.02x faster                                                                                                 |
| pathlib                    | 17.8 ms                                                                                                         | 18.1 ms: 1.01x slower                                                                                                 |
| bpe_tokeniser              | 4.24 sec                                                                                                        | 4.36 sec: 1.03x slower                                                                                                |
| regex_dna                  | 177 ms                                                                                                          | 184 ms: 1.04x slower                                                                                                  |
| async_tree_cpu_io_mixed_tg | 560 ms                                                                                                          | 581 ms: 1.04x slower                                                                                                  |
| pycparser                  | 1.12 sec                                                                                                        | 1.16 sec: 1.04x slower                                                                                                |
| coroutines                 | 23.1 ms                                                                                                         | 24.0 ms: 1.04x slower                                                                                                 |
| xml_etree_iterparse        | 90.8 ms                                                                                                         | 95.1 ms: 1.05x slower                                                                                                 |
| dulwich_log                | 68.3 ms                                                                                                         | 71.7 ms: 1.05x slower                                                                                                 |
| json_dumps                 | 9.48 ms                                                                                                         | 10.0 ms: 1.06x slower                                                                                                 |
| k_core                     | 2.11 sec                                                                                                        | 2.26 sec: 1.07x slower                                                                                                |
| tomli_loads                | 1.81 sec                                                                                                        | 1.95 sec: 1.07x slower                                                                                                |
| async_tree_memoization_tg  | 366 ms                                                                                                          | 395 ms: 1.08x slower                                                                                                  |
| pprint_safe_repr           | 734 ms                                                                                                          | 798 ms: 1.09x slower                                                                                                  |
| telco                      | 161 ms                                                                                                          | 175 ms: 1.09x slower                                                                                                  |
| pickle_pure_python         | 304 us                                                                                                          | 333 us: 1.09x slower                                                                                                  |
| json                       | 4.87 ms                                                                                                         | 5.34 ms: 1.10x slower                                                                                                 |
| many_optionals             | 915 us                                                                                                          | 1.01 ms: 1.10x slower                                                                                                 |
| scimark_fft                | 314 ms                                                                                                          | 346 ms: 1.10x slower                                                                                                  |
| async_tree_none_tg         | 301 ms                                                                                                          | 331 ms: 1.10x slower                                                                                                  |
| logging_silent             | 95.6 ns                                                                                                         | 106 ns: 1.11x slower                                                                                                  |
| scimark_lu                 | 117 ms                                                                                                          | 130 ms: 1.11x slower                                                                                                  |
| deltablue                  | 3.30 ms                                                                                                         | 3.66 ms: 1.11x slower                                                                                                 |
| bench_thread_pool          | 1.34 ms                                                                                                         | 1.49 ms: 1.11x slower                                                                                                 |
| pprint_pformat             | 1.50 sec                                                                                                        | 1.66 sec: 1.11x slower                                                                                                |
| sympy_expand               | 473 ms                                                                                                          | 528 ms: 1.12x slower                                                                                                  |
| sqlglot_v2_optimize        | 51.7 ms                                                                                                         | 57.7 ms: 1.12x slower                                                                                                 |
| async_tree_memoization     | 374 ms                                                                                                          | 418 ms: 1.12x slower                                                                                                  |
| sqlglot_v2_normalize       | 102 ms                                                                                                          | 114 ms: 1.12x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 536 ms                                                                                                          | 599 ms: 1.12x slower                                                                                                  |
| django_template            | 36.8 ms                                                                                                         | 41.3 ms: 1.12x slower                                                                                                 |
| deepcopy                   | 237 us                                                                                                          | 267 us: 1.12x slower                                                                                                  |
| html5lib                   | 59.4 ms                                                                                                         | 67.0 ms: 1.13x slower                                                                                                 |
| sphinx                     | 982 ms                                                                                                          | 1.11 sec: 1.13x slower                                                                                                |
| json_loads                 | 27.1 us                                                                                                         | 30.6 us: 1.13x slower                                                                                                 |
| scimark_sor                | 106 ms                                                                                                          | 120 ms: 1.13x slower                                                                                                  |
| sympy_integrate            | 19.1 ms                                                                                                         | 21.7 ms: 1.14x slower                                                                                                 |
| sympy_str                  | 278 ms                                                                                                          | 316 ms: 1.14x slower                                                                                                  |
| logging_simple             | 6.04 us                                                                                                         | 6.87 us: 1.14x slower                                                                                                 |
| logging_format             | 6.93 us                                                                                                         | 7.89 us: 1.14x slower                                                                                                 |
| spectral_norm              | 92.9 ms                                                                                                         | 106 ms: 1.14x slower                                                                                                  |
| chaos                      | 53.4 ms                                                                                                         | 60.8 ms: 1.14x slower                                                                                                 |
| subparsers                 | 9.05 ms                                                                                                         | 10.3 ms: 1.14x slower                                                                                                 |
| sympy_sum                  | 158 ms                                                                                                          | 180 ms: 1.14x slower                                                                                                  |
| mdp                        | 1.14 sec                                                                                                        | 1.30 sec: 1.14x slower                                                                                                |
| unpickle_pure_python       | 210 us                                                                                                          | 240 us: 1.14x slower                                                                                                  |
| deepcopy_reduce            | 2.56 us                                                                                                         | 2.93 us: 1.14x slower                                                                                                 |
| xml_etree_generate         | 88.1 ms                                                                                                         | 101 ms: 1.15x slower                                                                                                  |
| 2to3                       | 259 ms                                                                                                          | 297 ms: 1.15x slower                                                                                                  |
| regex_compile              | 147 ms                                                                                                          | 169 ms: 1.15x slower                                                                                                  |
| pylint                     | 114 ms                                                                                                          | 131 ms: 1.15x slower                                                                                                  |
| hexiom                     | 5.74 ms                                                                                                         | 6.63 ms: 1.16x slower                                                                                                 |
| float                      | 72.8 ms                                                                                                         | 84.3 ms: 1.16x slower                                                                                                 |
| raytrace                   | 251 ms                                                                                                          | 292 ms: 1.16x slower                                                                                                  |
| async_tree_none            | 292 ms                                                                                                          | 340 ms: 1.16x slower                                                                                                  |
| pyflate                    | 394 ms                                                                                                          | 459 ms: 1.17x slower                                                                                                  |
| go                         | 102 ms                                                                                                          | 119 ms: 1.17x slower                                                                                                  |
| regex_effbot               | 2.55 ms                                                                                                         | 2.99 ms: 1.17x slower                                                                                                 |
| typing_runtime_protocols   | 122 us                                                                                                          | 142 us: 1.17x slower                                                                                                  |
| comprehensions             | 15.5 us                                                                                                         | 18.2 us: 1.18x slower                                                                                                 |
| deepcopy_memo              | 26.7 us                                                                                                         | 31.5 us: 1.18x slower                                                                                                 |
| generators                 | 28.2 ms                                                                                                         | 33.5 ms: 1.19x slower                                                                                                 |
| thrift                     | 776 us                                                                                                          | 923 us: 1.19x slower                                                                                                  |
| richards_super             | 50.5 ms                                                                                                         | 60.2 ms: 1.19x slower                                                                                                 |
| scimark_sparse_mat_mult    | 4.65 ms                                                                                                         | 5.55 ms: 1.19x slower                                                                                                 |
| async_generators           | 349 ms                                                                                                          | 418 ms: 1.19x slower                                                                                                  |
| richards                   | 44.0 ms                                                                                                         | 52.6 ms: 1.20x slower                                                                                                 |
| sqlglot_v2_transpile       | 1.44 ms                                                                                                         | 1.73 ms: 1.20x slower                                                                                                 |
| nqueens                    | 73.5 ms                                                                                                         | 88.4 ms: 1.20x slower                                                                                                 |
| xml_etree_process          | 62.0 ms                                                                                                         | 75.2 ms: 1.21x slower                                                                                                 |
| sqlglot_v2_parse           | 1.15 ms                                                                                                         | 1.41 ms: 1.22x slower                                                                                                 |
| shortest_path              | 438 ms                                                                                                          | 535 ms: 1.22x slower                                                                                                  |
| meteor_contest             | 101 ms                                                                                                          | 124 ms: 1.23x slower                                                                                                  |
| scimark_monte_carlo        | 63.1 ms                                                                                                         | 77.5 ms: 1.23x slower                                                                                                 |
| python_startup             | 13.0 ms                                                                                                         | 16.1 ms: 1.24x slower                                                                                                 |
| connected_components       | 392 ms                                                                                                          | 490 ms: 1.25x slower                                                                                                  |
| docutils                   | 2.34 sec                                                                                                        | 2.93 sec: 1.25x slower                                                                                                |
| fannkuch                   | 368 ms                                                                                                          | 467 ms: 1.27x slower                                                                                                  |
| python_startup_no_site     | 7.74 ms                                                                                                         | 9.94 ms: 1.28x slower                                                                                                 |
| crypto_pyaes               | 67.5 ms                                                                                                         | 88.5 ms: 1.31x slower                                                                                                 |
| nbody                      | 92.3 ms                                                                                                         | 123 ms: 1.33x slower                                                                                                  |
| coverage                   | 85.7 ms                                                                                                         | 115 ms: 1.34x slower                                                                                                  |
| mako                       | 11.9 ms                                                                                                         | 16.2 ms: 1.36x slower                                                                                                 |
| Geometric mean             | (ref)                                                                                                           | 1.07x slower                                                                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

- Geometric mean (including insignificant results): 1.103x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.19x