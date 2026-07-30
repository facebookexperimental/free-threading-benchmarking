# Results vs. base

- fork: python
- ref: 8b048eb35eb7f83dbff8
- machine: linux-x86_64
- commit hash: 8b048eb
- commit date: 2026-07-28
- overall geometric mean: 1.099x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260728-3.16.0a0-8b048eb/bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb.json | results/bm-20260728-3.16.0a0-8b048eb-NOGIL/bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 262 ms                                                                                                          | 298 ms: 1.14x slower                                                                                                  |
| docutils       | 2.39 sec                                                                                                        | 2.91 sec: 1.22x slower                                                                                                |
| html5lib       | 60.5 ms                                                                                                         | 67.2 ms: 1.11x slower                                                                                                 |
| sphinx         | 997 ms                                                                                                          | 1.12 sec: 1.12x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.15x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260728-3.16.0a0-8b048eb/bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb.json | results/bm-20260728-3.16.0a0-8b048eb-NOGIL/bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 763 ms                                                                                                          | 686 ms: 1.11x faster                                                                                                  |
| asyncio_websockets         | 544 ms                                                                                                          | 513 ms: 1.06x faster                                                                                                  |
| async_tree_io              | 721 ms                                                                                                          | 703 ms: 1.03x faster                                                                                                  |
| coroutines                 | 23.4 ms                                                                                                         | 24.5 ms: 1.05x slower                                                                                                 |
| async_tree_cpu_io_mixed_tg | 553 ms                                                                                                          | 580 ms: 1.05x slower                                                                                                  |
| async_tree_memoization_tg  | 365 ms                                                                                                          | 391 ms: 1.07x slower                                                                                                  |
| async_tree_none_tg         | 297 ms                                                                                                          | 322 ms: 1.09x slower                                                                                                  |
| async_generators           | 349 ms                                                                                                          | 381 ms: 1.09x slower                                                                                                  |
| async_tree_memoization     | 377 ms                                                                                                          | 423 ms: 1.12x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 538 ms                                                                                                          | 608 ms: 1.13x slower                                                                                                  |
| async_tree_none            | 291 ms                                                                                                          | 344 ms: 1.18x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.05x slower                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260728-3.16.0a0-8b048eb/bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb.json | results/bm-20260728-3.16.0a0-8b048eb-NOGIL/bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 187 ms                                                                                                          | 180 ms: 1.04x faster                                                                                                  |
| float          | 73.8 ms                                                                                                         | 83.1 ms: 1.13x slower                                                                                                 |
| nbody          | 92.3 ms                                                                                                         | 120 ms: 1.30x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.12x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260728-3.16.0a0-8b048eb/bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb.json | results/bm-20260728-3.16.0a0-8b048eb-NOGIL/bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 22.0 ms                                                                                                         | 20.6 ms: 1.07x faster                                                                                                 |
| regex_dna      | 192 ms                                                                                                          | 183 ms: 1.05x faster                                                                                                  |
| regex_effbot   | 2.83 ms                                                                                                         | 3.05 ms: 1.08x slower                                                                                                 |
| regex_compile  | 149 ms                                                                                                          | 169 ms: 1.14x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.02x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260728-3.16.0a0-8b048eb/bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb.json | results/bm-20260728-3.16.0a0-8b048eb-NOGIL/bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 143 ms                                                                                                          | 140 ms: 1.02x faster                                                                                                  |
| xml_etree_iterparse  | 91.7 ms                                                                                                         | 95.4 ms: 1.04x slower                                                                                                 |
| json_dumps           | 9.87 ms                                                                                                         | 10.6 ms: 1.07x slower                                                                                                 |
| tomli_loads          | 1.80 sec                                                                                                        | 1.97 sec: 1.10x slower                                                                                                |
| pickle_pure_python   | 304 us                                                                                                          | 336 us: 1.10x slower                                                                                                  |
| unpickle_pure_python | 214 us                                                                                                          | 238 us: 1.11x slower                                                                                                  |
| json_loads           | 27.5 us                                                                                                         | 30.6 us: 1.11x slower                                                                                                 |
| xml_etree_generate   | 88.1 ms                                                                                                         | 102 ms: 1.16x slower                                                                                                  |
| xml_etree_process    | 62.5 ms                                                                                                         | 75.7 ms: 1.21x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.10x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260728-3.16.0a0-8b048eb/bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb.json | results/bm-20260728-3.16.0a0-8b048eb-NOGIL/bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.6 ms                                                                                                         | 15.7 ms: 1.25x slower                                                                                                 |
| python_startup_no_site | 7.07 ms                                                                                                         | 9.22 ms: 1.30x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.28x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260728-3.16.0a0-8b048eb/bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb.json | results/bm-20260728-3.16.0a0-8b048eb-NOGIL/bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 36.2 ms                                                                                                         | 41.2 ms: 1.14x slower                                                                                                 |
| mako            | 12.0 ms                                                                                                         | 15.9 ms: 1.33x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.23x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20260728-3.16.0a0-8b048eb/bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb.json | results/bm-20260728-3.16.0a0-8b048eb-NOGIL/bm-20260728-vultr-x86_64-python-8b048eb35eb7f83dbff8-3.16.0a0-8b048eb.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 262 ms                                                                                                          | 13.3 ms: 19.74x faster                                                                                                |
| gc_traversal               | 4.03 ms                                                                                                         | 1.78 ms: 2.27x faster                                                                                                 |
| create_gc_cycles           | 1.69 ms                                                                                                         | 1.37 ms: 1.23x faster                                                                                                 |
| sqlite_synth               | 2.23 us                                                                                                         | 1.95 us: 1.14x faster                                                                                                 |
| async_tree_io_tg           | 763 ms                                                                                                          | 686 ms: 1.11x faster                                                                                                  |
| regex_v8                   | 22.0 ms                                                                                                         | 20.6 ms: 1.07x faster                                                                                                 |
| asyncio_websockets         | 544 ms                                                                                                          | 513 ms: 1.06x faster                                                                                                  |
| regex_dna                  | 192 ms                                                                                                          | 183 ms: 1.05x faster                                                                                                  |
| pidigits                   | 187 ms                                                                                                          | 180 ms: 1.04x faster                                                                                                  |
| async_tree_io              | 721 ms                                                                                                          | 703 ms: 1.03x faster                                                                                                  |
| xml_etree_parse            | 143 ms                                                                                                          | 140 ms: 1.02x faster                                                                                                  |
| pathlib                    | 17.9 ms                                                                                                         | 17.8 ms: 1.01x faster                                                                                                 |
| dulwich_log                | 67.9 ms                                                                                                         | 69.8 ms: 1.03x slower                                                                                                 |
| pycparser                  | 1.13 sec                                                                                                        | 1.17 sec: 1.04x slower                                                                                                |
| bpe_tokeniser              | 4.21 sec                                                                                                        | 4.37 sec: 1.04x slower                                                                                                |
| xml_etree_iterparse        | 91.7 ms                                                                                                         | 95.4 ms: 1.04x slower                                                                                                 |
| coroutines                 | 23.4 ms                                                                                                         | 24.5 ms: 1.05x slower                                                                                                 |
| async_tree_cpu_io_mixed_tg | 553 ms                                                                                                          | 580 ms: 1.05x slower                                                                                                  |
| async_tree_memoization_tg  | 365 ms                                                                                                          | 391 ms: 1.07x slower                                                                                                  |
| json_dumps                 | 9.87 ms                                                                                                         | 10.6 ms: 1.07x slower                                                                                                 |
| logging_silent             | 98.7 ns                                                                                                         | 106 ns: 1.08x slower                                                                                                  |
| regex_effbot               | 2.83 ms                                                                                                         | 3.05 ms: 1.08x slower                                                                                                 |
| async_tree_none_tg         | 297 ms                                                                                                          | 322 ms: 1.09x slower                                                                                                  |
| scimark_fft                | 307 ms                                                                                                          | 335 ms: 1.09x slower                                                                                                  |
| deltablue                  | 3.37 ms                                                                                                         | 3.68 ms: 1.09x slower                                                                                                 |
| async_generators           | 349 ms                                                                                                          | 381 ms: 1.09x slower                                                                                                  |
| k_core                     | 2.07 sec                                                                                                        | 2.27 sec: 1.09x slower                                                                                                |
| tomli_loads                | 1.80 sec                                                                                                        | 1.97 sec: 1.10x slower                                                                                                |
| scimark_lu                 | 118 ms                                                                                                          | 130 ms: 1.10x slower                                                                                                  |
| json                       | 4.87 ms                                                                                                         | 5.36 ms: 1.10x slower                                                                                                 |
| pickle_pure_python         | 304 us                                                                                                          | 336 us: 1.10x slower                                                                                                  |
| telco                      | 159 ms                                                                                                          | 175 ms: 1.11x slower                                                                                                  |
| bench_thread_pool          | 1.34 ms                                                                                                         | 1.49 ms: 1.11x slower                                                                                                 |
| sqlglot_v2_optimize        | 52.2 ms                                                                                                         | 58.0 ms: 1.11x slower                                                                                                 |
| html5lib                   | 60.5 ms                                                                                                         | 67.2 ms: 1.11x slower                                                                                                 |
| unpickle_pure_python       | 214 us                                                                                                          | 238 us: 1.11x slower                                                                                                  |
| json_loads                 | 27.5 us                                                                                                         | 30.6 us: 1.11x slower                                                                                                 |
| scimark_sparse_mat_mult    | 4.46 ms                                                                                                         | 4.97 ms: 1.11x slower                                                                                                 |
| sqlglot_v2_normalize       | 103 ms                                                                                                          | 115 ms: 1.12x slower                                                                                                  |
| chaos                      | 54.3 ms                                                                                                         | 60.6 ms: 1.12x slower                                                                                                 |
| scimark_sor                | 109 ms                                                                                                          | 122 ms: 1.12x slower                                                                                                  |
| sphinx                     | 997 ms                                                                                                          | 1.12 sec: 1.12x slower                                                                                                |
| many_optionals             | 905 us                                                                                                          | 1.01 ms: 1.12x slower                                                                                                 |
| async_tree_memoization     | 377 ms                                                                                                          | 423 ms: 1.12x slower                                                                                                  |
| float                      | 73.8 ms                                                                                                         | 83.1 ms: 1.13x slower                                                                                                 |
| async_tree_cpu_io_mixed    | 538 ms                                                                                                          | 608 ms: 1.13x slower                                                                                                  |
| go                         | 106 ms                                                                                                          | 119 ms: 1.13x slower                                                                                                  |
| spectral_norm              | 92.3 ms                                                                                                         | 105 ms: 1.14x slower                                                                                                  |
| sympy_expand               | 472 ms                                                                                                          | 537 ms: 1.14x slower                                                                                                  |
| 2to3                       | 262 ms                                                                                                          | 298 ms: 1.14x slower                                                                                                  |
| django_template            | 36.2 ms                                                                                                         | 41.2 ms: 1.14x slower                                                                                                 |
| regex_compile              | 149 ms                                                                                                          | 169 ms: 1.14x slower                                                                                                  |
| comprehensions             | 15.9 us                                                                                                         | 18.1 us: 1.14x slower                                                                                                 |
| pprint_safe_repr           | 721 ms                                                                                                          | 822 ms: 1.14x slower                                                                                                  |
| hexiom                     | 5.68 ms                                                                                                         | 6.48 ms: 1.14x slower                                                                                                 |
| pylint                     | 114 ms                                                                                                          | 130 ms: 1.14x slower                                                                                                  |
| raytrace                   | 254 ms                                                                                                          | 290 ms: 1.14x slower                                                                                                  |
| sympy_integrate            | 19.1 ms                                                                                                         | 21.8 ms: 1.14x slower                                                                                                 |
| mdp                        | 1.14 sec                                                                                                        | 1.30 sec: 1.15x slower                                                                                                |
| sympy_sum                  | 158 ms                                                                                                          | 181 ms: 1.15x slower                                                                                                  |
| generators                 | 29.3 ms                                                                                                         | 33.8 ms: 1.15x slower                                                                                                 |
| sympy_str                  | 278 ms                                                                                                          | 320 ms: 1.15x slower                                                                                                  |
| richards                   | 45.3 ms                                                                                                         | 52.3 ms: 1.16x slower                                                                                                 |
| xml_etree_generate         | 88.1 ms                                                                                                         | 102 ms: 1.16x slower                                                                                                  |
| deepcopy_reduce            | 2.58 us                                                                                                         | 2.99 us: 1.16x slower                                                                                                 |
| richards_super             | 51.2 ms                                                                                                         | 59.7 ms: 1.16x slower                                                                                                 |
| subparsers                 | 9.04 ms                                                                                                         | 10.5 ms: 1.17x slower                                                                                                 |
| pprint_pformat             | 1.47 sec                                                                                                        | 1.72 sec: 1.17x slower                                                                                                |
| pyflate                    | 400 ms                                                                                                          | 466 ms: 1.17x slower                                                                                                  |
| logging_simple             | 5.99 us                                                                                                         | 7.04 us: 1.17x slower                                                                                                 |
| deepcopy_memo              | 26.7 us                                                                                                         | 31.5 us: 1.18x slower                                                                                                 |
| async_tree_none            | 291 ms                                                                                                          | 344 ms: 1.18x slower                                                                                                  |
| deepcopy                   | 233 us                                                                                                          | 275 us: 1.18x slower                                                                                                  |
| nqueens                    | 74.3 ms                                                                                                         | 87.9 ms: 1.18x slower                                                                                                 |
| thrift                     | 781 us                                                                                                          | 925 us: 1.18x slower                                                                                                  |
| sqlglot_v2_transpile       | 1.46 ms                                                                                                         | 1.76 ms: 1.21x slower                                                                                                 |
| xml_etree_process          | 62.5 ms                                                                                                         | 75.7 ms: 1.21x slower                                                                                                 |
| logging_format             | 6.75 us                                                                                                         | 8.20 us: 1.22x slower                                                                                                 |
| sqlglot_v2_parse           | 1.16 ms                                                                                                         | 1.41 ms: 1.22x slower                                                                                                 |
| docutils                   | 2.39 sec                                                                                                        | 2.91 sec: 1.22x slower                                                                                                |
| typing_runtime_protocols   | 119 us                                                                                                          | 145 us: 1.22x slower                                                                                                  |
| shortest_path              | 435 ms                                                                                                          | 539 ms: 1.24x slower                                                                                                  |
| scimark_monte_carlo        | 62.5 ms                                                                                                         | 77.5 ms: 1.24x slower                                                                                                 |
| fannkuch                   | 376 ms                                                                                                          | 467 ms: 1.24x slower                                                                                                  |
| connected_components       | 395 ms                                                                                                          | 492 ms: 1.25x slower                                                                                                  |
| python_startup             | 12.6 ms                                                                                                         | 15.7 ms: 1.25x slower                                                                                                 |
| meteor_contest             | 102 ms                                                                                                          | 129 ms: 1.26x slower                                                                                                  |
| crypto_pyaes               | 68.2 ms                                                                                                         | 87.7 ms: 1.29x slower                                                                                                 |
| nbody                      | 92.3 ms                                                                                                         | 120 ms: 1.30x slower                                                                                                  |
| python_startup_no_site     | 7.07 ms                                                                                                         | 9.22 ms: 1.30x slower                                                                                                 |
| mako                       | 12.0 ms                                                                                                         | 15.9 ms: 1.33x slower                                                                                                 |
| coverage                   | 83.8 ms                                                                                                         | 116 ms: 1.38x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.07x slower                                                                                                          |

- Geometric mean (including insignificant results): 1.099x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.10x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.19x