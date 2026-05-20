# Results vs. base

- fork: python
- ref: de9c32fc34fe2e000de1
- machine: linux-x86_64
- commit hash: de9c32f
- commit date: 2026-05-20
- overall geometric mean: 1.100x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260520-3.16.0a0-de9c32f/bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f.json | results/bm-20260520-3.16.0a0-de9c32f-NOGIL/bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| docutils       | 2.40 sec                                                                                                        | 2.98 sec: 1.24x slower                                                                                                |
| html5lib       | 61.0 ms                                                                                                         | 69.9 ms: 1.15x slower                                                                                                 |
| sphinx         | 1000 ms                                                                                                         | 1.13 sec: 1.13x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.17x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260520-3.16.0a0-de9c32f/bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f.json | results/bm-20260520-3.16.0a0-de9c32f-NOGIL/bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 765 ms                                                                                                          | 694 ms: 1.10x faster                                                                                                  |
| asyncio_websockets         | 544 ms                                                                                                          | 509 ms: 1.07x faster                                                                                                  |
| async_tree_io              | 724 ms                                                                                                          | 713 ms: 1.02x faster                                                                                                  |
| coroutines                 | 24.5 ms                                                                                                         | 24.9 ms: 1.02x slower                                                                                                 |
| async_tree_cpu_io_mixed_tg | 559 ms                                                                                                          | 581 ms: 1.04x slower                                                                                                  |
| async_tree_memoization_tg  | 368 ms                                                                                                          | 398 ms: 1.08x slower                                                                                                  |
| async_tree_none_tg         | 301 ms                                                                                                          | 329 ms: 1.09x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 545 ms                                                                                                          | 599 ms: 1.10x slower                                                                                                  |
| async_generators           | 345 ms                                                                                                          | 386 ms: 1.12x slower                                                                                                  |
| async_tree_memoization     | 378 ms                                                                                                          | 426 ms: 1.13x slower                                                                                                  |
| async_tree_none            | 294 ms                                                                                                          | 344 ms: 1.17x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.05x slower                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260520-3.16.0a0-de9c32f/bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f.json | results/bm-20260520-3.16.0a0-de9c32f-NOGIL/bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 192 ms                                                                                                          | 185 ms: 1.03x faster                                                                                                  |
| float          | 75.6 ms                                                                                                         | 88.5 ms: 1.17x slower                                                                                                 |
| nbody          | 90.5 ms                                                                                                         | 129 ms: 1.43x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.17x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260520-3.16.0a0-de9c32f/bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f.json | results/bm-20260520-3.16.0a0-de9c32f-NOGIL/bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.9 ms                                                                                                         | 21.6 ms: 1.01x faster                                                                                                 |
| regex_dna      | 180 ms                                                                                                          | 186 ms: 1.03x slower                                                                                                  |
| regex_effbot   | 2.91 ms                                                                                                         | 3.11 ms: 1.07x slower                                                                                                 |
| regex_compile  | 126 ms                                                                                                          | 144 ms: 1.14x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.06x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260520-3.16.0a0-de9c32f/bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f.json | results/bm-20260520-3.16.0a0-de9c32f-NOGIL/bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 142 ms                                                                                                          | 140 ms: 1.02x faster                                                                                                  |
| xml_etree_iterparse  | 89.6 ms                                                                                                         | 95.0 ms: 1.06x slower                                                                                                 |
| tomli_loads          | 1.83 sec                                                                                                        | 1.98 sec: 1.08x slower                                                                                                |
| json_dumps           | 9.88 ms                                                                                                         | 10.7 ms: 1.09x slower                                                                                                 |
| pickle_pure_python   | 317 us                                                                                                          | 347 us: 1.09x slower                                                                                                  |
| unpickle_pure_python | 216 us                                                                                                          | 244 us: 1.13x slower                                                                                                  |
| json_loads           | 27.7 us                                                                                                         | 31.5 us: 1.14x slower                                                                                                 |
| xml_etree_generate   | 86.9 ms                                                                                                         | 102 ms: 1.18x slower                                                                                                  |
| xml_etree_process    | 61.4 ms                                                                                                         | 76.0 ms: 1.24x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.11x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260520-3.16.0a0-de9c32f/bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f.json | results/bm-20260520-3.16.0a0-de9c32f-NOGIL/bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 35.5 ms                                                                                                         | 41.0 ms: 1.15x slower                                                                                                 |
| mako            | 12.3 ms                                                                                                         | 16.3 ms: 1.33x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.24x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20260520-3.16.0a0-de9c32f/bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f.json | results/bm-20260520-3.16.0a0-de9c32f-NOGIL/bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 243 ms                                                                                                          | 6.98 ms: 34.77x faster                                                                                                |
| gc_traversal               | 4.15 ms                                                                                                         | 1.93 ms: 2.15x faster                                                                                                 |
| create_gc_cycles           | 1.82 ms                                                                                                         | 1.47 ms: 1.24x faster                                                                                                 |
| sqlite_synth               | 2.22 us                                                                                                         | 1.96 us: 1.13x faster                                                                                                 |
| async_tree_io_tg           | 765 ms                                                                                                          | 694 ms: 1.10x faster                                                                                                  |
| asyncio_websockets         | 544 ms                                                                                                          | 509 ms: 1.07x faster                                                                                                  |
| pidigits                   | 192 ms                                                                                                          | 185 ms: 1.03x faster                                                                                                  |
| xml_etree_parse            | 142 ms                                                                                                          | 140 ms: 1.02x faster                                                                                                  |
| async_tree_io              | 724 ms                                                                                                          | 713 ms: 1.02x faster                                                                                                  |
| regex_v8                   | 21.9 ms                                                                                                         | 21.6 ms: 1.01x faster                                                                                                 |
| dulwich_log                | 69.7 ms                                                                                                         | 70.1 ms: 1.01x slower                                                                                                 |
| coroutines                 | 24.5 ms                                                                                                         | 24.9 ms: 1.02x slower                                                                                                 |
| pathlib                    | 17.6 ms                                                                                                         | 18.1 ms: 1.03x slower                                                                                                 |
| regex_dna                  | 180 ms                                                                                                          | 186 ms: 1.03x slower                                                                                                  |
| pycparser                  | 1.11 sec                                                                                                        | 1.15 sec: 1.03x slower                                                                                                |
| async_tree_cpu_io_mixed_tg | 559 ms                                                                                                          | 581 ms: 1.04x slower                                                                                                  |
| json                       | 5.15 ms                                                                                                         | 5.39 ms: 1.05x slower                                                                                                 |
| bpe_tokeniser              | 4.20 sec                                                                                                        | 4.40 sec: 1.05x slower                                                                                                |
| xml_etree_iterparse        | 89.6 ms                                                                                                         | 95.0 ms: 1.06x slower                                                                                                 |
| regex_effbot               | 2.91 ms                                                                                                         | 3.11 ms: 1.07x slower                                                                                                 |
| logging_silent             | 98.6 ns                                                                                                         | 106 ns: 1.07x slower                                                                                                  |
| deltablue                  | 3.45 ms                                                                                                         | 3.73 ms: 1.08x slower                                                                                                 |
| tomli_loads                | 1.83 sec                                                                                                        | 1.98 sec: 1.08x slower                                                                                                |
| async_tree_memoization_tg  | 368 ms                                                                                                          | 398 ms: 1.08x slower                                                                                                  |
| k_core                     | 2.09 sec                                                                                                        | 2.27 sec: 1.08x slower                                                                                                |
| json_dumps                 | 9.88 ms                                                                                                         | 10.7 ms: 1.09x slower                                                                                                 |
| async_tree_none_tg         | 301 ms                                                                                                          | 329 ms: 1.09x slower                                                                                                  |
| pickle_pure_python         | 317 us                                                                                                          | 347 us: 1.09x slower                                                                                                  |
| scimark_fft                | 319 ms                                                                                                          | 350 ms: 1.09x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 545 ms                                                                                                          | 599 ms: 1.10x slower                                                                                                  |
| bench_thread_pool          | 1.35 ms                                                                                                         | 1.48 ms: 1.10x slower                                                                                                 |
| comprehensions             | 16.1 us                                                                                                         | 17.7 us: 1.10x slower                                                                                                 |
| telco                      | 161 ms                                                                                                          | 177 ms: 1.10x slower                                                                                                  |
| many_optionals             | 923 us                                                                                                          | 1.02 ms: 1.11x slower                                                                                                 |
| pprint_safe_repr           | 739 ms                                                                                                          | 819 ms: 1.11x slower                                                                                                  |
| scimark_sor                | 109 ms                                                                                                          | 122 ms: 1.11x slower                                                                                                  |
| hexiom                     | 5.84 ms                                                                                                         | 6.53 ms: 1.12x slower                                                                                                 |
| async_generators           | 345 ms                                                                                                          | 386 ms: 1.12x slower                                                                                                  |
| sphinx                     | 1000 ms                                                                                                         | 1.13 sec: 1.13x slower                                                                                                |
| async_tree_memoization     | 378 ms                                                                                                          | 426 ms: 1.13x slower                                                                                                  |
| scimark_lu                 | 115 ms                                                                                                          | 130 ms: 1.13x slower                                                                                                  |
| unpickle_pure_python       | 216 us                                                                                                          | 244 us: 1.13x slower                                                                                                  |
| pprint_pformat             | 1.50 sec                                                                                                        | 1.70 sec: 1.13x slower                                                                                                |
| sympy_expand               | 472 ms                                                                                                          | 535 ms: 1.13x slower                                                                                                  |
| json_loads                 | 27.7 us                                                                                                         | 31.5 us: 1.14x slower                                                                                                 |
| deepcopy                   | 239 us                                                                                                          | 272 us: 1.14x slower                                                                                                  |
| pyflate                    | 409 ms                                                                                                          | 467 ms: 1.14x slower                                                                                                  |
| chaos                      | 55.7 ms                                                                                                         | 63.6 ms: 1.14x slower                                                                                                 |
| spectral_norm              | 96.2 ms                                                                                                         | 110 ms: 1.14x slower                                                                                                  |
| regex_compile              | 126 ms                                                                                                          | 144 ms: 1.14x slower                                                                                                  |
| html5lib                   | 61.0 ms                                                                                                         | 69.9 ms: 1.15x slower                                                                                                 |
| go                         | 108 ms                                                                                                          | 124 ms: 1.15x slower                                                                                                  |
| deepcopy_reduce            | 2.59 us                                                                                                         | 2.97 us: 1.15x slower                                                                                                 |
| sqlglot_v2_optimize        | 51.2 ms                                                                                                         | 58.8 ms: 1.15x slower                                                                                                 |
| subparsers                 | 9.44 ms                                                                                                         | 10.9 ms: 1.15x slower                                                                                                 |
| thrift                     | 801 us                                                                                                          | 923 us: 1.15x slower                                                                                                  |
| sympy_str                  | 276 ms                                                                                                          | 318 ms: 1.15x slower                                                                                                  |
| sympy_integrate            | 19.2 ms                                                                                                         | 22.1 ms: 1.15x slower                                                                                                 |
| scimark_sparse_mat_mult    | 4.73 ms                                                                                                         | 5.46 ms: 1.15x slower                                                                                                 |
| django_template            | 35.5 ms                                                                                                         | 41.0 ms: 1.15x slower                                                                                                 |
| pylint                     | 115 ms                                                                                                          | 133 ms: 1.16x slower                                                                                                  |
| sympy_sum                  | 156 ms                                                                                                          | 181 ms: 1.16x slower                                                                                                  |
| deepcopy_memo              | 27.5 us                                                                                                         | 31.9 us: 1.16x slower                                                                                                 |
| sqlglot_v2_normalize       | 101 ms                                                                                                          | 117 ms: 1.16x slower                                                                                                  |
| mdp                        | 1.14 sec                                                                                                        | 1.33 sec: 1.16x slower                                                                                                |
| logging_simple             | 5.96 us                                                                                                         | 6.95 us: 1.17x slower                                                                                                 |
| generators                 | 29.2 ms                                                                                                         | 34.1 ms: 1.17x slower                                                                                                 |
| float                      | 75.6 ms                                                                                                         | 88.5 ms: 1.17x slower                                                                                                 |
| async_tree_none            | 294 ms                                                                                                          | 344 ms: 1.17x slower                                                                                                  |
| logging_format             | 6.69 us                                                                                                         | 7.83 us: 1.17x slower                                                                                                 |
| nqueens                    | 75.4 ms                                                                                                         | 88.3 ms: 1.17x slower                                                                                                 |
| raytrace                   | 261 ms                                                                                                          | 307 ms: 1.18x slower                                                                                                  |
| xml_etree_generate         | 86.9 ms                                                                                                         | 102 ms: 1.18x slower                                                                                                  |
| sqlglot_v2_transpile       | 1.47 ms                                                                                                         | 1.75 ms: 1.19x slower                                                                                                 |
| sqlglot_v2_parse           | 1.17 ms                                                                                                         | 1.41 ms: 1.21x slower                                                                                                 |
| richards_super             | 50.0 ms                                                                                                         | 60.5 ms: 1.21x slower                                                                                                 |
| richards                   | 43.8 ms                                                                                                         | 53.1 ms: 1.21x slower                                                                                                 |
| shortest_path              | 441 ms                                                                                                          | 535 ms: 1.21x slower                                                                                                  |
| typing_runtime_protocols   | 118 us                                                                                                          | 145 us: 1.23x slower                                                                                                  |
| scimark_monte_carlo        | 65.0 ms                                                                                                         | 80.3 ms: 1.24x slower                                                                                                 |
| xml_etree_process          | 61.4 ms                                                                                                         | 76.0 ms: 1.24x slower                                                                                                 |
| docutils                   | 2.40 sec                                                                                                        | 2.98 sec: 1.24x slower                                                                                                |
| connected_components       | 396 ms                                                                                                          | 490 ms: 1.24x slower                                                                                                  |
| fannkuch                   | 379 ms                                                                                                          | 470 ms: 1.24x slower                                                                                                  |
| crypto_pyaes               | 71.1 ms                                                                                                         | 89.5 ms: 1.26x slower                                                                                                 |
| meteor_contest             | 98.7 ms                                                                                                         | 129 ms: 1.31x slower                                                                                                  |
| mako                       | 12.3 ms                                                                                                         | 16.3 ms: 1.33x slower                                                                                                 |
| coverage                   | 84.6 ms                                                                                                         | 116 ms: 1.37x slower                                                                                                  |
| nbody                      | 90.5 ms                                                                                                         | 129 ms: 1.43x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.07x slower                                                                                                          |

- Geometric mean (including insignificant results): 1.100x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.18x