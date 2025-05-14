# Results vs. base

- fork: python
- ref: 9ad0c7b0f14c5fcda6bf
- machine: linux-x86_64
- commit hash: 9ad0c7b
- commit date: 2025-05-13
- overall geometric mean: 1.086x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250513-3.15.0a0-9ad0c7b/bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json | results/bm-20250513-3.15.0a0-9ad0c7b-NOGIL/bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 338 ms                                                                                                          | 378 ms: 1.12x slower                                                                                                  |
| docutils       | 3.39 sec                                                                                                        | 3.68 sec: 1.09x slower                                                                                                |
| html5lib       | 76.2 ms                                                                                                         | 82.2 ms: 1.08x slower                                                                                                 |
| sphinx         | 1.28 sec                                                                                                        | 1.44 sec: 1.13x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.10x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250513-3.15.0a0-9ad0c7b/bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json | results/bm-20250513-3.15.0a0-9ad0c7b-NOGIL/bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 841 ms                                                                                                          | 662 ms: 1.27x faster                                                                                                  |
| async_tree_none_tg         | 331 ms                                                                                                          | 293 ms: 1.13x faster                                                                                                  |
| async_tree_io              | 801 ms                                                                                                          | 711 ms: 1.13x faster                                                                                                  |
| async_tree_memoization_tg  | 416 ms                                                                                                          | 387 ms: 1.07x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 620 ms                                                                                                          | 579 ms: 1.07x faster                                                                                                  |
| async_tree_none            | 347 ms                                                                                                          | 340 ms: 1.02x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 618 ms                                                                                                          | 630 ms: 1.02x slower                                                                                                  |
| asyncio_websockets         | 649 ms                                                                                                          | 674 ms: 1.04x slower                                                                                                  |
| async_generators           | 512 ms                                                                                                          | 535 ms: 1.05x slower                                                                                                  |
| async_tree_memoization     | 412 ms                                                                                                          | 434 ms: 1.05x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.04x faster                                                                                                          |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250513-3.15.0a0-9ad0c7b/bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json | results/bm-20250513-3.15.0a0-9ad0c7b-NOGIL/bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 232 ms                                                                                                          | 216 ms: 1.08x faster                                                                                                  |
| float          | 97.2 ms                                                                                                         | 91.6 ms: 1.06x faster                                                                                                 |
| nbody          | 123 ms                                                                                                          | 154 ms: 1.25x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.03x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250513-3.15.0a0-9ad0c7b/bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json | results/bm-20250513-3.15.0a0-9ad0c7b-NOGIL/bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 27.7 ms                                                                                                         | 27.0 ms: 1.03x faster                                                                                                 |
| regex_dna      | 237 ms                                                                                                          | 249 ms: 1.05x slower                                                                                                  |
| regex_effbot   | 3.74 ms                                                                                                         | 3.97 ms: 1.06x slower                                                                                                 |
| regex_compile  | 153 ms                                                                                                          | 179 ms: 1.17x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.06x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250513-3.15.0a0-9ad0c7b/bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json | results/bm-20250513-3.15.0a0-9ad0c7b-NOGIL/bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 125 ms                                                                                                          | 116 ms: 1.08x faster                                                                                                  |
| xml_etree_parse      | 175 ms                                                                                                          | 172 ms: 1.02x faster                                                                                                  |
| tomli_loads          | 2.50 sec                                                                                                        | 2.77 sec: 1.11x slower                                                                                                |
| json_loads           | 37.8 us                                                                                                         | 42.2 us: 1.12x slower                                                                                                 |
| pickle_pure_python   | 390 us                                                                                                          | 435 us: 1.12x slower                                                                                                  |
| unpickle_pure_python | 269 us                                                                                                          | 301 us: 1.12x slower                                                                                                  |
| json_dumps           | 13.8 ms                                                                                                         | 15.6 ms: 1.13x slower                                                                                                 |
| xml_etree_generate   | 110 ms                                                                                                          | 129 ms: 1.17x slower                                                                                                  |
| xml_etree_process    | 75.2 ms                                                                                                         | 90.7 ms: 1.21x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250513-3.15.0a0-9ad0c7b/bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json | results/bm-20250513-3.15.0a0-9ad0c7b-NOGIL/bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 17.6 ms                                                                                                         | 22.5 ms: 1.28x slower                                                                                                 |
| python_startup_no_site | 10.4 ms                                                                                                         | 13.9 ms: 1.33x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.31x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250513-3.15.0a0-9ad0c7b/bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json | results/bm-20250513-3.15.0a0-9ad0c7b-NOGIL/bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 43.2 ms                                                                                                         | 49.2 ms: 1.14x slower                                                                                                 |
| genshi_xml      | 62.0 ms                                                                                                         | 73.4 ms: 1.18x slower                                                                                                 |
| genshi_text     | 26.4 ms                                                                                                         | 33.8 ms: 1.28x slower                                                                                                 |
| mako            | 16.1 ms                                                                                                         | 20.6 ms: 1.29x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.22x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20250513-3.15.0a0-9ad0c7b/bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json | results/bm-20250513-3.15.0a0-9ad0c7b-NOGIL/bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 6.39 ms                                                                                                         | 2.91 ms: 2.19x faster                                                                                                 |
| create_gc_cycles           | 3.16 ms                                                                                                         | 2.21 ms: 1.43x faster                                                                                                 |
| async_tree_io_tg           | 841 ms                                                                                                          | 662 ms: 1.27x faster                                                                                                  |
| async_tree_none_tg         | 331 ms                                                                                                          | 293 ms: 1.13x faster                                                                                                  |
| async_tree_io              | 801 ms                                                                                                          | 711 ms: 1.13x faster                                                                                                  |
| xml_etree_iterparse        | 125 ms                                                                                                          | 116 ms: 1.08x faster                                                                                                  |
| sqlite_synth               | 3.22 us                                                                                                         | 2.99 us: 1.08x faster                                                                                                 |
| pidigits                   | 232 ms                                                                                                          | 216 ms: 1.08x faster                                                                                                  |
| async_tree_memoization_tg  | 416 ms                                                                                                          | 387 ms: 1.07x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 620 ms                                                                                                          | 579 ms: 1.07x faster                                                                                                  |
| float                      | 97.2 ms                                                                                                         | 91.6 ms: 1.06x faster                                                                                                 |
| bench_mp_pool              | 80.3 ms                                                                                                         | 76.4 ms: 1.05x faster                                                                                                 |
| regex_v8                   | 27.7 ms                                                                                                         | 27.0 ms: 1.03x faster                                                                                                 |
| xml_etree_parse            | 175 ms                                                                                                          | 172 ms: 1.02x faster                                                                                                  |
| async_tree_none            | 347 ms                                                                                                          | 340 ms: 1.02x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 618 ms                                                                                                          | 630 ms: 1.02x slower                                                                                                  |
| pathlib                    | 24.0 ms                                                                                                         | 24.6 ms: 1.02x slower                                                                                                 |
| json                       | 6.97 ms                                                                                                         | 7.22 ms: 1.04x slower                                                                                                 |
| asyncio_websockets         | 649 ms                                                                                                          | 674 ms: 1.04x slower                                                                                                  |
| deltablue                  | 4.30 ms                                                                                                         | 4.50 ms: 1.05x slower                                                                                                 |
| async_generators           | 512 ms                                                                                                          | 535 ms: 1.05x slower                                                                                                  |
| regex_dna                  | 237 ms                                                                                                          | 249 ms: 1.05x slower                                                                                                  |
| dulwich_log                | 74.3 ms                                                                                                         | 78.1 ms: 1.05x slower                                                                                                 |
| async_tree_memoization     | 412 ms                                                                                                          | 434 ms: 1.05x slower                                                                                                  |
| regex_effbot               | 3.74 ms                                                                                                         | 3.97 ms: 1.06x slower                                                                                                 |
| scimark_fft                | 456 ms                                                                                                          | 488 ms: 1.07x slower                                                                                                  |
| k_core                     | 3.48 sec                                                                                                        | 3.74 sec: 1.07x slower                                                                                                |
| spectral_norm              | 131 ms                                                                                                          | 141 ms: 1.07x slower                                                                                                  |
| scimark_sor                | 149 ms                                                                                                          | 160 ms: 1.08x slower                                                                                                  |
| generators                 | 39.7 ms                                                                                                         | 42.7 ms: 1.08x slower                                                                                                 |
| html5lib                   | 76.2 ms                                                                                                         | 82.2 ms: 1.08x slower                                                                                                 |
| bench_thread_pool          | 1.79 ms                                                                                                         | 1.93 ms: 1.08x slower                                                                                                 |
| docutils                   | 3.39 sec                                                                                                        | 3.68 sec: 1.09x slower                                                                                                |
| chaos                      | 74.2 ms                                                                                                         | 81.6 ms: 1.10x slower                                                                                                 |
| pprint_safe_repr           | 909 ms                                                                                                          | 1.00 sec: 1.10x slower                                                                                                |
| pylint                     | 365 ms                                                                                                          | 404 ms: 1.11x slower                                                                                                  |
| tomli_loads                | 2.50 sec                                                                                                        | 2.77 sec: 1.11x slower                                                                                                |
| json_loads                 | 37.8 us                                                                                                         | 42.2 us: 1.12x slower                                                                                                 |
| pickle_pure_python         | 390 us                                                                                                          | 435 us: 1.12x slower                                                                                                  |
| 2to3                       | 338 ms                                                                                                          | 378 ms: 1.12x slower                                                                                                  |
| sqlglot_v2_normalize       | 129 ms                                                                                                          | 145 ms: 1.12x slower                                                                                                  |
| unpickle_pure_python       | 269 us                                                                                                          | 301 us: 1.12x slower                                                                                                  |
| bpe_tokeniser              | 5.52 sec                                                                                                        | 6.20 sec: 1.12x slower                                                                                                |
| deepcopy_reduce            | 3.40 us                                                                                                         | 3.82 us: 1.13x slower                                                                                                 |
| pprint_pformat             | 1.85 sec                                                                                                        | 2.08 sec: 1.13x slower                                                                                                |
| subparsers                 | 30.3 ms                                                                                                         | 34.2 ms: 1.13x slower                                                                                                 |
| sphinx                     | 1.28 sec                                                                                                        | 1.44 sec: 1.13x slower                                                                                                |
| many_optionals             | 1.16 ms                                                                                                         | 1.31 ms: 1.13x slower                                                                                                 |
| telco                      | 9.45 ms                                                                                                         | 10.7 ms: 1.13x slower                                                                                                 |
| nqueens                    | 99.3 ms                                                                                                         | 112 ms: 1.13x slower                                                                                                  |
| json_dumps                 | 13.8 ms                                                                                                         | 15.6 ms: 1.13x slower                                                                                                 |
| go                         | 142 ms                                                                                                          | 161 ms: 1.13x slower                                                                                                  |
| thrift                     | 946 us                                                                                                          | 1.07 ms: 1.14x slower                                                                                                 |
| logging_silent             | 615 ns                                                                                                          | 701 ns: 1.14x slower                                                                                                  |
| django_template            | 43.2 ms                                                                                                         | 49.2 ms: 1.14x slower                                                                                                 |
| sqlglot_v2_optimize        | 64.9 ms                                                                                                         | 74.0 ms: 1.14x slower                                                                                                 |
| scimark_lu                 | 146 ms                                                                                                          | 167 ms: 1.14x slower                                                                                                  |
| logging_simple             | 8.20 us                                                                                                         | 9.38 us: 1.14x slower                                                                                                 |
| deepcopy                   | 326 us                                                                                                          | 373 us: 1.15x slower                                                                                                  |
| raytrace                   | 336 ms                                                                                                          | 387 ms: 1.15x slower                                                                                                  |
| hexiom                     | 7.59 ms                                                                                                         | 8.83 ms: 1.16x slower                                                                                                 |
| scimark_sparse_mat_mult    | 6.25 ms                                                                                                         | 7.28 ms: 1.16x slower                                                                                                 |
| regex_compile              | 153 ms                                                                                                          | 179 ms: 1.17x slower                                                                                                  |
| sympy_expand               | 550 ms                                                                                                          | 646 ms: 1.17x slower                                                                                                  |
| xml_etree_generate         | 110 ms                                                                                                          | 129 ms: 1.17x slower                                                                                                  |
| logging_format             | 8.97 us                                                                                                         | 10.5 us: 1.17x slower                                                                                                 |
| pyflate                    | 559 ms                                                                                                          | 658 ms: 1.18x slower                                                                                                  |
| comprehensions             | 21.4 us                                                                                                         | 25.2 us: 1.18x slower                                                                                                 |
| fannkuch                   | 512 ms                                                                                                          | 606 ms: 1.18x slower                                                                                                  |
| genshi_xml                 | 62.0 ms                                                                                                         | 73.4 ms: 1.18x slower                                                                                                 |
| sympy_sum                  | 183 ms                                                                                                          | 218 ms: 1.19x slower                                                                                                  |
| sympy_str                  | 325 ms                                                                                                          | 387 ms: 1.19x slower                                                                                                  |
| scimark_monte_carlo        | 83.9 ms                                                                                                         | 100 ms: 1.20x slower                                                                                                  |
| richards                   | 54.0 ms                                                                                                         | 64.9 ms: 1.20x slower                                                                                                 |
| shortest_path              | 747 ms                                                                                                          | 901 ms: 1.21x slower                                                                                                  |
| crypto_pyaes               | 92.3 ms                                                                                                         | 111 ms: 1.21x slower                                                                                                  |
| xml_etree_process          | 75.2 ms                                                                                                         | 90.7 ms: 1.21x slower                                                                                                 |
| richards_super             | 62.3 ms                                                                                                         | 75.4 ms: 1.21x slower                                                                                                 |
| sympy_integrate            | 23.4 ms                                                                                                         | 28.3 ms: 1.21x slower                                                                                                 |
| connected_components       | 675 ms                                                                                                          | 818 ms: 1.21x slower                                                                                                  |
| meteor_contest             | 129 ms                                                                                                          | 159 ms: 1.23x slower                                                                                                  |
| sqlglot_v2_transpile       | 1.92 ms                                                                                                         | 2.35 ms: 1.23x slower                                                                                                 |
| deepcopy_memo              | 37.4 us                                                                                                         | 46.0 us: 1.23x slower                                                                                                 |
| sqlglot_v2_parse           | 1.53 ms                                                                                                         | 1.88 ms: 1.23x slower                                                                                                 |
| mdp                        | 1.74 sec                                                                                                        | 2.16 sec: 1.24x slower                                                                                                |
| nbody                      | 123 ms                                                                                                          | 154 ms: 1.25x slower                                                                                                  |
| typing_runtime_protocols   | 197 us                                                                                                          | 248 us: 1.26x slower                                                                                                  |
| genshi_text                | 26.4 ms                                                                                                         | 33.8 ms: 1.28x slower                                                                                                 |
| python_startup             | 17.6 ms                                                                                                         | 22.5 ms: 1.28x slower                                                                                                 |
| mako                       | 16.1 ms                                                                                                         | 20.6 ms: 1.29x slower                                                                                                 |
| python_startup_no_site     | 10.4 ms                                                                                                         | 13.9 ms: 1.33x slower                                                                                                 |
| coverage                   | 105 ms                                                                                                          | 145 ms: 1.38x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmark hidden because not significant (2): coroutines, pycparser

- Geometric mean (including insignificant results): 1.086x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.22x