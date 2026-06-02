# Results vs. base

- fork: python
- ref: f4bda4d6cb13d4c57fba
- machine: linux-x86_64
- commit hash: f4bda4d
- commit date: 2026-05-31
- overall geometric mean: 1.091x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260531-3.16.0a0-f4bda4d/bm-20260531-vultr-x86_64-python-f4bda4d6cb13d4c57fba-3.16.0a0-f4bda4d.json | results/bm-20260531-3.16.0a0-f4bda4d-NOGIL/bm-20260531-vultr-x86_64-python-f4bda4d6cb13d4c57fba-3.16.0a0-f4bda4d.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| docutils       | 2.41 sec                                                                                                        | 2.97 sec: 1.24x slower                                                                                                |
| html5lib       | 61.3 ms                                                                                                         | 69.6 ms: 1.14x slower                                                                                                 |
| sphinx         | 988 ms                                                                                                          | 1.12 sec: 1.13x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.17x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260531-3.16.0a0-f4bda4d/bm-20260531-vultr-x86_64-python-f4bda4d6cb13d4c57fba-3.16.0a0-f4bda4d.json | results/bm-20260531-3.16.0a0-f4bda4d-NOGIL/bm-20260531-vultr-x86_64-python-f4bda4d6cb13d4c57fba-3.16.0a0-f4bda4d.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 756 ms                                                                                                          | 682 ms: 1.11x faster                                                                                                  |
| asyncio_websockets         | 545 ms                                                                                                          | 509 ms: 1.07x faster                                                                                                  |
| async_tree_io              | 718 ms                                                                                                          | 702 ms: 1.02x faster                                                                                                  |
| coroutines                 | 24.4 ms                                                                                                         | 24.6 ms: 1.01x slower                                                                                                 |
| async_tree_cpu_io_mixed_tg | 556 ms                                                                                                          | 574 ms: 1.03x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 546 ms                                                                                                          | 587 ms: 1.08x slower                                                                                                  |
| async_tree_memoization_tg  | 364 ms                                                                                                          | 395 ms: 1.09x slower                                                                                                  |
| async_tree_none_tg         | 300 ms                                                                                                          | 325 ms: 1.09x slower                                                                                                  |
| async_tree_memoization     | 374 ms                                                                                                          | 417 ms: 1.11x slower                                                                                                  |
| async_generators           | 342 ms                                                                                                          | 384 ms: 1.12x slower                                                                                                  |
| async_tree_none            | 291 ms                                                                                                          | 338 ms: 1.16x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.04x slower                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260531-3.16.0a0-f4bda4d/bm-20260531-vultr-x86_64-python-f4bda4d6cb13d4c57fba-3.16.0a0-f4bda4d.json | results/bm-20260531-3.16.0a0-f4bda4d-NOGIL/bm-20260531-vultr-x86_64-python-f4bda4d6cb13d4c57fba-3.16.0a0-f4bda4d.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 184 ms                                                                                                          | 185 ms: 1.01x slower                                                                                                  |
| float          | 75.4 ms                                                                                                         | 87.4 ms: 1.16x slower                                                                                                 |
| nbody          | 93.5 ms                                                                                                         | 124 ms: 1.33x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.16x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260531-3.16.0a0-f4bda4d/bm-20260531-vultr-x86_64-python-f4bda4d6cb13d4c57fba-3.16.0a0-f4bda4d.json | results/bm-20260531-3.16.0a0-f4bda4d-NOGIL/bm-20260531-vultr-x86_64-python-f4bda4d6cb13d4c57fba-3.16.0a0-f4bda4d.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 22.0 ms                                                                                                         | 21.4 ms: 1.03x faster                                                                                                 |
| regex_dna      | 186 ms                                                                                                          | 187 ms: 1.01x slower                                                                                                  |
| regex_effbot   | 2.99 ms                                                                                                         | 3.19 ms: 1.07x slower                                                                                                 |
| regex_compile  | 125 ms                                                                                                          | 143 ms: 1.14x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.04x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260531-3.16.0a0-f4bda4d/bm-20260531-vultr-x86_64-python-f4bda4d6cb13d4c57fba-3.16.0a0-f4bda4d.json | results/bm-20260531-3.16.0a0-f4bda4d-NOGIL/bm-20260531-vultr-x86_64-python-f4bda4d6cb13d4c57fba-3.16.0a0-f4bda4d.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 144 ms                                                                                                          | 140 ms: 1.03x faster                                                                                                  |
| xml_etree_iterparse  | 89.3 ms                                                                                                         | 94.6 ms: 1.06x slower                                                                                                 |
| tomli_loads          | 1.84 sec                                                                                                        | 1.96 sec: 1.06x slower                                                                                                |
| pickle_pure_python   | 316 us                                                                                                          | 337 us: 1.07x slower                                                                                                  |
| json_loads           | 28.1 us                                                                                                         | 31.0 us: 1.10x slower                                                                                                 |
| json_dumps           | 9.70 ms                                                                                                         | 10.7 ms: 1.10x slower                                                                                                 |
| unpickle_pure_python | 215 us                                                                                                          | 243 us: 1.13x slower                                                                                                  |
| xml_etree_generate   | 86.8 ms                                                                                                         | 102 ms: 1.17x slower                                                                                                  |
| xml_etree_process    | 62.2 ms                                                                                                         | 75.4 ms: 1.21x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260531-3.16.0a0-f4bda4d/bm-20260531-vultr-x86_64-python-f4bda4d6cb13d4c57fba-3.16.0a0-f4bda4d.json | results/bm-20260531-3.16.0a0-f4bda4d-NOGIL/bm-20260531-vultr-x86_64-python-f4bda4d6cb13d4c57fba-3.16.0a0-f4bda4d.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 35.5 ms                                                                                                         | 39.8 ms: 1.12x slower                                                                                                 |
| mako            | 12.1 ms                                                                                                         | 15.8 ms: 1.31x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.21x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20260531-3.16.0a0-f4bda4d/bm-20260531-vultr-x86_64-python-f4bda4d6cb13d4c57fba-3.16.0a0-f4bda4d.json | results/bm-20260531-3.16.0a0-f4bda4d-NOGIL/bm-20260531-vultr-x86_64-python-f4bda4d6cb13d4c57fba-3.16.0a0-f4bda4d.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 270 ms                                                                                                          | 6.99 ms: 38.66x faster                                                                                                |
| gc_traversal               | 3.88 ms                                                                                                         | 1.92 ms: 2.02x faster                                                                                                 |
| create_gc_cycles           | 1.80 ms                                                                                                         | 1.51 ms: 1.19x faster                                                                                                 |
| sqlite_synth               | 2.22 us                                                                                                         | 1.97 us: 1.13x faster                                                                                                 |
| async_tree_io_tg           | 756 ms                                                                                                          | 682 ms: 1.11x faster                                                                                                  |
| asyncio_websockets         | 545 ms                                                                                                          | 509 ms: 1.07x faster                                                                                                  |
| pycparser                  | 1.19 sec                                                                                                        | 1.13 sec: 1.05x faster                                                                                                |
| xml_etree_parse            | 144 ms                                                                                                          | 140 ms: 1.03x faster                                                                                                  |
| regex_v8                   | 22.0 ms                                                                                                         | 21.4 ms: 1.03x faster                                                                                                 |
| async_tree_io              | 718 ms                                                                                                          | 702 ms: 1.02x faster                                                                                                  |
| regex_dna                  | 186 ms                                                                                                          | 187 ms: 1.01x slower                                                                                                  |
| coroutines                 | 24.4 ms                                                                                                         | 24.6 ms: 1.01x slower                                                                                                 |
| pidigits                   | 184 ms                                                                                                          | 185 ms: 1.01x slower                                                                                                  |
| pathlib                    | 17.7 ms                                                                                                         | 18.0 ms: 1.01x slower                                                                                                 |
| logging_silent             | 102 ns                                                                                                          | 104 ns: 1.02x slower                                                                                                  |
| json                       | 5.21 ms                                                                                                         | 5.35 ms: 1.03x slower                                                                                                 |
| async_tree_cpu_io_mixed_tg | 556 ms                                                                                                          | 574 ms: 1.03x slower                                                                                                  |
| bpe_tokeniser              | 4.22 sec                                                                                                        | 4.39 sec: 1.04x slower                                                                                                |
| dulwich_log                | 67.8 ms                                                                                                         | 71.0 ms: 1.05x slower                                                                                                 |
| scimark_fft                | 329 ms                                                                                                          | 345 ms: 1.05x slower                                                                                                  |
| scimark_sor                | 114 ms                                                                                                          | 120 ms: 1.06x slower                                                                                                  |
| xml_etree_iterparse        | 89.3 ms                                                                                                         | 94.6 ms: 1.06x slower                                                                                                 |
| telco                      | 165 ms                                                                                                          | 176 ms: 1.06x slower                                                                                                  |
| tomli_loads                | 1.84 sec                                                                                                        | 1.96 sec: 1.06x slower                                                                                                |
| regex_effbot               | 2.99 ms                                                                                                         | 3.19 ms: 1.07x slower                                                                                                 |
| pickle_pure_python         | 316 us                                                                                                          | 337 us: 1.07x slower                                                                                                  |
| deltablue                  | 3.46 ms                                                                                                         | 3.71 ms: 1.07x slower                                                                                                 |
| async_tree_cpu_io_mixed    | 546 ms                                                                                                          | 587 ms: 1.08x slower                                                                                                  |
| many_optionals             | 923 us                                                                                                          | 996 us: 1.08x slower                                                                                                  |
| async_tree_memoization_tg  | 364 ms                                                                                                          | 395 ms: 1.09x slower                                                                                                  |
| async_tree_none_tg         | 300 ms                                                                                                          | 325 ms: 1.09x slower                                                                                                  |
| pprint_safe_repr           | 732 ms                                                                                                          | 800 ms: 1.09x slower                                                                                                  |
| comprehensions             | 15.9 us                                                                                                         | 17.4 us: 1.09x slower                                                                                                 |
| k_core                     | 2.08 sec                                                                                                        | 2.28 sec: 1.10x slower                                                                                                |
| bench_thread_pool          | 1.34 ms                                                                                                         | 1.47 ms: 1.10x slower                                                                                                 |
| json_loads                 | 28.1 us                                                                                                         | 31.0 us: 1.10x slower                                                                                                 |
| json_dumps                 | 9.70 ms                                                                                                         | 10.7 ms: 1.10x slower                                                                                                 |
| pprint_pformat             | 1.49 sec                                                                                                        | 1.65 sec: 1.11x slower                                                                                                |
| logging_format             | 6.92 us                                                                                                         | 7.69 us: 1.11x slower                                                                                                 |
| subparsers                 | 9.54 ms                                                                                                         | 10.6 ms: 1.11x slower                                                                                                 |
| async_tree_memoization     | 374 ms                                                                                                          | 417 ms: 1.11x slower                                                                                                  |
| chaos                      | 55.8 ms                                                                                                         | 62.4 ms: 1.12x slower                                                                                                 |
| scimark_sparse_mat_mult    | 4.79 ms                                                                                                         | 5.36 ms: 1.12x slower                                                                                                 |
| logging_simple             | 6.04 us                                                                                                         | 6.76 us: 1.12x slower                                                                                                 |
| spectral_norm              | 98.2 ms                                                                                                         | 110 ms: 1.12x slower                                                                                                  |
| django_template            | 35.5 ms                                                                                                         | 39.8 ms: 1.12x slower                                                                                                 |
| async_generators           | 342 ms                                                                                                          | 384 ms: 1.12x slower                                                                                                  |
| sympy_expand               | 460 ms                                                                                                          | 518 ms: 1.13x slower                                                                                                  |
| go                         | 108 ms                                                                                                          | 122 ms: 1.13x slower                                                                                                  |
| deepcopy_reduce            | 2.56 us                                                                                                         | 2.89 us: 1.13x slower                                                                                                 |
| thrift                     | 796 us                                                                                                          | 898 us: 1.13x slower                                                                                                  |
| unpickle_pure_python       | 215 us                                                                                                          | 243 us: 1.13x slower                                                                                                  |
| scimark_lu                 | 114 ms                                                                                                          | 129 ms: 1.13x slower                                                                                                  |
| pyflate                    | 409 ms                                                                                                          | 463 ms: 1.13x slower                                                                                                  |
| sympy_str                  | 273 ms                                                                                                          | 310 ms: 1.13x slower                                                                                                  |
| sphinx                     | 988 ms                                                                                                          | 1.12 sec: 1.13x slower                                                                                                |
| sqlglot_v2_optimize        | 51.1 ms                                                                                                         | 58.0 ms: 1.13x slower                                                                                                 |
| html5lib                   | 61.3 ms                                                                                                         | 69.6 ms: 1.14x slower                                                                                                 |
| sympy_integrate            | 19.1 ms                                                                                                         | 21.8 ms: 1.14x slower                                                                                                 |
| deepcopy                   | 237 us                                                                                                          | 270 us: 1.14x slower                                                                                                  |
| sqlglot_v2_normalize       | 101 ms                                                                                                          | 115 ms: 1.14x slower                                                                                                  |
| regex_compile              | 125 ms                                                                                                          | 143 ms: 1.14x slower                                                                                                  |
| hexiom                     | 5.78 ms                                                                                                         | 6.61 ms: 1.14x slower                                                                                                 |
| sympy_sum                  | 155 ms                                                                                                          | 178 ms: 1.15x slower                                                                                                  |
| pylint                     | 115 ms                                                                                                          | 133 ms: 1.15x slower                                                                                                  |
| deepcopy_memo              | 26.8 us                                                                                                         | 31.0 us: 1.16x slower                                                                                                 |
| float                      | 75.4 ms                                                                                                         | 87.4 ms: 1.16x slower                                                                                                 |
| async_tree_none            | 291 ms                                                                                                          | 338 ms: 1.16x slower                                                                                                  |
| raytrace                   | 260 ms                                                                                                          | 302 ms: 1.16x slower                                                                                                  |
| mdp                        | 1.14 sec                                                                                                        | 1.33 sec: 1.16x slower                                                                                                |
| generators                 | 29.1 ms                                                                                                         | 34.1 ms: 1.17x slower                                                                                                 |
| xml_etree_generate         | 86.8 ms                                                                                                         | 102 ms: 1.17x slower                                                                                                  |
| sqlglot_v2_transpile       | 1.47 ms                                                                                                         | 1.74 ms: 1.18x slower                                                                                                 |
| nqueens                    | 73.9 ms                                                                                                         | 87.9 ms: 1.19x slower                                                                                                 |
| scimark_monte_carlo        | 65.9 ms                                                                                                         | 78.9 ms: 1.20x slower                                                                                                 |
| richards                   | 43.9 ms                                                                                                         | 52.7 ms: 1.20x slower                                                                                                 |
| fannkuch                   | 383 ms                                                                                                          | 462 ms: 1.20x slower                                                                                                  |
| sqlglot_v2_parse           | 1.17 ms                                                                                                         | 1.41 ms: 1.20x slower                                                                                                 |
| shortest_path              | 443 ms                                                                                                          | 534 ms: 1.21x slower                                                                                                  |
| xml_etree_process          | 62.2 ms                                                                                                         | 75.4 ms: 1.21x slower                                                                                                 |
| richards_super             | 50.4 ms                                                                                                         | 61.1 ms: 1.21x slower                                                                                                 |
| connected_components       | 400 ms                                                                                                          | 493 ms: 1.23x slower                                                                                                  |
| docutils                   | 2.41 sec                                                                                                        | 2.97 sec: 1.24x slower                                                                                                |
| typing_runtime_protocols   | 117 us                                                                                                          | 145 us: 1.24x slower                                                                                                  |
| crypto_pyaes               | 70.5 ms                                                                                                         | 90.1 ms: 1.28x slower                                                                                                 |
| meteor_contest             | 100 ms                                                                                                          | 128 ms: 1.28x slower                                                                                                  |
| mako                       | 12.1 ms                                                                                                         | 15.8 ms: 1.31x slower                                                                                                 |
| nbody                      | 93.5 ms                                                                                                         | 124 ms: 1.33x slower                                                                                                  |
| coverage                   | 83.9 ms                                                                                                         | 115 ms: 1.37x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.05x slower                                                                                                          |

- Geometric mean (including insignificant results): 1.091x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.18x