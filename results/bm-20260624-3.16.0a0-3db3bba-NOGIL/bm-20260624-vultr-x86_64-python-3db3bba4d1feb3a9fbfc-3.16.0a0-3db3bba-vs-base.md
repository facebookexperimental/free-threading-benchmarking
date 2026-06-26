# Results vs. base

- fork: python
- ref: 3db3bba4d1feb3a9fbfc
- machine: linux-x86_64
- commit hash: 3db3bba
- commit date: 2026-06-24
- overall geometric mean: 1.102x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260624-3.16.0a0-3db3bba/bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba.json | results/bm-20260624-3.16.0a0-3db3bba-NOGIL/bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 253 ms                                                                                                          | 293 ms: 1.16x slower                                                                                                  |
| docutils       | 2.38 sec                                                                                                        | 2.97 sec: 1.25x slower                                                                                                |
| html5lib       | 59.0 ms                                                                                                         | 65.3 ms: 1.11x slower                                                                                                 |
| sphinx         | 983 ms                                                                                                          | 1.11 sec: 1.13x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.16x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260624-3.16.0a0-3db3bba/bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba.json | results/bm-20260624-3.16.0a0-3db3bba-NOGIL/bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 767 ms                                                                                                          | 674 ms: 1.14x faster                                                                                                  |
| asyncio_websockets         | 545 ms                                                                                                          | 513 ms: 1.06x faster                                                                                                  |
| async_tree_io              | 720 ms                                                                                                          | 698 ms: 1.03x faster                                                                                                  |
| coroutines                 | 23.8 ms                                                                                                         | 24.4 ms: 1.03x slower                                                                                                 |
| async_tree_cpu_io_mixed_tg | 558 ms                                                                                                          | 577 ms: 1.03x slower                                                                                                  |
| async_tree_memoization_tg  | 368 ms                                                                                                          | 390 ms: 1.06x slower                                                                                                  |
| async_tree_none_tg         | 301 ms                                                                                                          | 322 ms: 1.07x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 546 ms                                                                                                          | 595 ms: 1.09x slower                                                                                                  |
| async_tree_memoization     | 376 ms                                                                                                          | 414 ms: 1.10x slower                                                                                                  |
| async_generators           | 338 ms                                                                                                          | 387 ms: 1.14x slower                                                                                                  |
| async_tree_none            | 289 ms                                                                                                          | 337 ms: 1.17x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.04x slower                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260624-3.16.0a0-3db3bba/bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba.json | results/bm-20260624-3.16.0a0-3db3bba-NOGIL/bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 184 ms                                                                                                          | 187 ms: 1.02x slower                                                                                                  |
| float          | 74.1 ms                                                                                                         | 85.0 ms: 1.15x slower                                                                                                 |
| nbody          | 91.8 ms                                                                                                         | 126 ms: 1.38x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.17x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260624-3.16.0a0-3db3bba/bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba.json | results/bm-20260624-3.16.0a0-3db3bba-NOGIL/bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_dna      | 177 ms                                                                                                          | 162 ms: 1.10x faster                                                                                                  |
| regex_v8       | 22.2 ms                                                                                                         | 20.4 ms: 1.09x faster                                                                                                 |
| regex_effbot   | 2.83 ms                                                                                                         | 2.78 ms: 1.02x faster                                                                                                 |
| regex_compile  | 120 ms                                                                                                          | 138 ms: 1.15x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.01x faster                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260624-3.16.0a0-3db3bba/bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba.json | results/bm-20260624-3.16.0a0-3db3bba-NOGIL/bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 143 ms                                                                                                          | 142 ms: 1.01x faster                                                                                                  |
| xml_etree_iterparse  | 90.0 ms                                                                                                         | 94.9 ms: 1.05x slower                                                                                                 |
| tomli_loads          | 1.85 sec                                                                                                        | 1.96 sec: 1.06x slower                                                                                                |
| json_dumps           | 9.79 ms                                                                                                         | 10.5 ms: 1.08x slower                                                                                                 |
| pickle_pure_python   | 307 us                                                                                                          | 336 us: 1.09x slower                                                                                                  |
| json_loads           | 27.3 us                                                                                                         | 30.2 us: 1.11x slower                                                                                                 |
| unpickle_pure_python | 209 us                                                                                                          | 236 us: 1.13x slower                                                                                                  |
| xml_etree_generate   | 85.6 ms                                                                                                         | 102 ms: 1.19x slower                                                                                                  |
| xml_etree_process    | 60.4 ms                                                                                                         | 74.8 ms: 1.24x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.10x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260624-3.16.0a0-3db3bba/bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba.json | results/bm-20260624-3.16.0a0-3db3bba-NOGIL/bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.3 ms                                                                                                         | 15.5 ms: 1.25x slower                                                                                                 |
| python_startup_no_site | 6.94 ms                                                                                                         | 9.21 ms: 1.33x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.29x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260624-3.16.0a0-3db3bba/bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba.json | results/bm-20260624-3.16.0a0-3db3bba-NOGIL/bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 35.7 ms                                                                                                         | 40.1 ms: 1.13x slower                                                                                                 |
| mako            | 12.1 ms                                                                                                         | 16.2 ms: 1.34x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.23x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20260624-3.16.0a0-3db3bba/bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba.json | results/bm-20260624-3.16.0a0-3db3bba-NOGIL/bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 227 ms                                                                                                          | 6.79 ms: 33.48x faster                                                                                                |
| gc_traversal               | 3.72 ms                                                                                                         | 1.78 ms: 2.09x faster                                                                                                 |
| create_gc_cycles           | 1.68 ms                                                                                                         | 1.34 ms: 1.25x faster                                                                                                 |
| async_tree_io_tg           | 767 ms                                                                                                          | 674 ms: 1.14x faster                                                                                                  |
| sqlite_synth               | 2.20 us                                                                                                         | 1.96 us: 1.12x faster                                                                                                 |
| regex_dna                  | 177 ms                                                                                                          | 162 ms: 1.10x faster                                                                                                  |
| regex_v8                   | 22.2 ms                                                                                                         | 20.4 ms: 1.09x faster                                                                                                 |
| asyncio_websockets         | 545 ms                                                                                                          | 513 ms: 1.06x faster                                                                                                  |
| async_tree_io              | 720 ms                                                                                                          | 698 ms: 1.03x faster                                                                                                  |
| regex_effbot               | 2.83 ms                                                                                                         | 2.78 ms: 1.02x faster                                                                                                 |
| xml_etree_parse            | 143 ms                                                                                                          | 142 ms: 1.01x faster                                                                                                  |
| pycparser                  | 1.11 sec                                                                                                        | 1.13 sec: 1.02x slower                                                                                                |
| pidigits                   | 184 ms                                                                                                          | 187 ms: 1.02x slower                                                                                                  |
| coroutines                 | 23.8 ms                                                                                                         | 24.4 ms: 1.03x slower                                                                                                 |
| async_tree_cpu_io_mixed_tg | 558 ms                                                                                                          | 577 ms: 1.03x slower                                                                                                  |
| bpe_tokeniser              | 4.20 sec                                                                                                        | 4.37 sec: 1.04x slower                                                                                                |
| json                       | 5.08 ms                                                                                                         | 5.29 ms: 1.04x slower                                                                                                 |
| xml_etree_iterparse        | 90.0 ms                                                                                                         | 94.9 ms: 1.05x slower                                                                                                 |
| tomli_loads                | 1.85 sec                                                                                                        | 1.96 sec: 1.06x slower                                                                                                |
| async_tree_memoization_tg  | 368 ms                                                                                                          | 390 ms: 1.06x slower                                                                                                  |
| dulwich_log                | 67.4 ms                                                                                                         | 72.0 ms: 1.07x slower                                                                                                 |
| async_tree_none_tg         | 301 ms                                                                                                          | 322 ms: 1.07x slower                                                                                                  |
| json_dumps                 | 9.79 ms                                                                                                         | 10.5 ms: 1.08x slower                                                                                                 |
| logging_silent             | 96.0 ns                                                                                                         | 103 ns: 1.08x slower                                                                                                  |
| scimark_fft                | 321 ms                                                                                                          | 349 ms: 1.09x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 546 ms                                                                                                          | 595 ms: 1.09x slower                                                                                                  |
| many_optionals             | 914 us                                                                                                          | 995 us: 1.09x slower                                                                                                  |
| pickle_pure_python         | 307 us                                                                                                          | 336 us: 1.09x slower                                                                                                  |
| async_tree_memoization     | 376 ms                                                                                                          | 414 ms: 1.10x slower                                                                                                  |
| json_loads                 | 27.3 us                                                                                                         | 30.2 us: 1.11x slower                                                                                                 |
| html5lib                   | 59.0 ms                                                                                                         | 65.3 ms: 1.11x slower                                                                                                 |
| bench_thread_pool          | 1.33 ms                                                                                                         | 1.48 ms: 1.11x slower                                                                                                 |
| pprint_safe_repr           | 723 ms                                                                                                          | 804 ms: 1.11x slower                                                                                                  |
| telco                      | 158 ms                                                                                                          | 176 ms: 1.12x slower                                                                                                  |
| comprehensions             | 15.6 us                                                                                                         | 17.5 us: 1.12x slower                                                                                                 |
| k_core                     | 2.02 sec                                                                                                        | 2.26 sec: 1.12x slower                                                                                                |
| django_template            | 35.7 ms                                                                                                         | 40.1 ms: 1.13x slower                                                                                                 |
| sqlglot_v2_optimize        | 50.6 ms                                                                                                         | 57.0 ms: 1.13x slower                                                                                                 |
| deltablue                  | 3.25 ms                                                                                                         | 3.66 ms: 1.13x slower                                                                                                 |
| deepcopy_reduce            | 2.53 us                                                                                                         | 2.86 us: 1.13x slower                                                                                                 |
| unpickle_pure_python       | 209 us                                                                                                          | 236 us: 1.13x slower                                                                                                  |
| sphinx                     | 983 ms                                                                                                          | 1.11 sec: 1.13x slower                                                                                                |
| logging_simple             | 6.07 us                                                                                                         | 6.88 us: 1.13x slower                                                                                                 |
| scimark_lu                 | 113 ms                                                                                                          | 128 ms: 1.13x slower                                                                                                  |
| subparsers                 | 9.25 ms                                                                                                         | 10.5 ms: 1.14x slower                                                                                                 |
| pprint_pformat             | 1.47 sec                                                                                                        | 1.67 sec: 1.14x slower                                                                                                |
| logging_format             | 6.90 us                                                                                                         | 7.87 us: 1.14x slower                                                                                                 |
| scimark_sor                | 107 ms                                                                                                          | 122 ms: 1.14x slower                                                                                                  |
| sqlglot_v2_normalize       | 99.7 ms                                                                                                         | 114 ms: 1.14x slower                                                                                                  |
| pyflate                    | 402 ms                                                                                                          | 459 ms: 1.14x slower                                                                                                  |
| deepcopy                   | 229 us                                                                                                          | 261 us: 1.14x slower                                                                                                  |
| async_generators           | 338 ms                                                                                                          | 387 ms: 1.14x slower                                                                                                  |
| float                      | 74.1 ms                                                                                                         | 85.0 ms: 1.15x slower                                                                                                 |
| sympy_sum                  | 156 ms                                                                                                          | 179 ms: 1.15x slower                                                                                                  |
| sympy_integrate            | 19.0 ms                                                                                                         | 21.9 ms: 1.15x slower                                                                                                 |
| sympy_str                  | 273 ms                                                                                                          | 313 ms: 1.15x slower                                                                                                  |
| regex_compile              | 120 ms                                                                                                          | 138 ms: 1.15x slower                                                                                                  |
| sympy_expand               | 456 ms                                                                                                          | 525 ms: 1.15x slower                                                                                                  |
| mdp                        | 1.13 sec                                                                                                        | 1.30 sec: 1.15x slower                                                                                                |
| chaos                      | 54.1 ms                                                                                                         | 62.5 ms: 1.16x slower                                                                                                 |
| 2to3                       | 253 ms                                                                                                          | 293 ms: 1.16x slower                                                                                                  |
| deepcopy_memo              | 26.4 us                                                                                                         | 30.6 us: 1.16x slower                                                                                                 |
| hexiom                     | 5.61 ms                                                                                                         | 6.53 ms: 1.16x slower                                                                                                 |
| scimark_sparse_mat_mult    | 4.74 ms                                                                                                         | 5.51 ms: 1.16x slower                                                                                                 |
| async_tree_none            | 289 ms                                                                                                          | 337 ms: 1.17x slower                                                                                                  |
| go                         | 102 ms                                                                                                          | 120 ms: 1.17x slower                                                                                                  |
| pylint                     | 114 ms                                                                                                          | 134 ms: 1.18x slower                                                                                                  |
| nqueens                    | 74.3 ms                                                                                                         | 87.3 ms: 1.18x slower                                                                                                 |
| spectral_norm              | 93.9 ms                                                                                                         | 111 ms: 1.18x slower                                                                                                  |
| sqlglot_v2_transpile       | 1.44 ms                                                                                                         | 1.71 ms: 1.19x slower                                                                                                 |
| xml_etree_generate         | 85.6 ms                                                                                                         | 102 ms: 1.19x slower                                                                                                  |
| generators                 | 27.9 ms                                                                                                         | 33.2 ms: 1.19x slower                                                                                                 |
| thrift                     | 770 us                                                                                                          | 918 us: 1.19x slower                                                                                                  |
| raytrace                   | 250 ms                                                                                                          | 301 ms: 1.21x slower                                                                                                  |
| shortest_path              | 439 ms                                                                                                          | 536 ms: 1.22x slower                                                                                                  |
| fannkuch                   | 378 ms                                                                                                          | 463 ms: 1.23x slower                                                                                                  |
| typing_runtime_protocols   | 117 us                                                                                                          | 144 us: 1.23x slower                                                                                                  |
| sqlglot_v2_parse           | 1.13 ms                                                                                                         | 1.39 ms: 1.23x slower                                                                                                 |
| xml_etree_process          | 60.4 ms                                                                                                         | 74.8 ms: 1.24x slower                                                                                                 |
| richards_super             | 48.0 ms                                                                                                         | 59.6 ms: 1.24x slower                                                                                                 |
| richards                   | 42.0 ms                                                                                                         | 52.2 ms: 1.24x slower                                                                                                 |
| connected_components       | 395 ms                                                                                                          | 490 ms: 1.24x slower                                                                                                  |
| docutils                   | 2.38 sec                                                                                                        | 2.97 sec: 1.25x slower                                                                                                |
| python_startup             | 12.3 ms                                                                                                         | 15.5 ms: 1.25x slower                                                                                                 |
| scimark_monte_carlo        | 62.8 ms                                                                                                         | 79.3 ms: 1.26x slower                                                                                                 |
| crypto_pyaes               | 69.2 ms                                                                                                         | 89.0 ms: 1.29x slower                                                                                                 |
| meteor_contest             | 99.1 ms                                                                                                         | 128 ms: 1.29x slower                                                                                                  |
| python_startup_no_site     | 6.94 ms                                                                                                         | 9.21 ms: 1.33x slower                                                                                                 |
| mako                       | 12.1 ms                                                                                                         | 16.2 ms: 1.34x slower                                                                                                 |
| coverage                   | 83.9 ms                                                                                                         | 113 ms: 1.35x slower                                                                                                  |
| nbody                      | 91.8 ms                                                                                                         | 126 ms: 1.38x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.07x slower                                                                                                          |

Benchmark hidden because not significant (1): pathlib

- Geometric mean (including insignificant results): 1.102x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.12x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.17x