# Results vs. base

- fork: python
- ref: 4ddf505d9982dc8afead
- machine: linux-x86_64
- commit hash: 4ddf505
- commit date: 2025-06-20
- overall geometric mean: 1.087x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250620-3.15.0a0-4ddf505/bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505.json | results/bm-20250620-3.15.0a0-4ddf505-NOGIL/bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 249 ms                                                                                                          | 282 ms: 1.13x slower                                                                                                  |
| docutils       | 2.53 sec                                                                                                        | 2.67 sec: 1.05x slower                                                                                                |
| html5lib       | 60.8 ms                                                                                                         | 66.1 ms: 1.09x slower                                                                                                 |
| sphinx         | 975 ms                                                                                                          | 1.06 sec: 1.09x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250620-3.15.0a0-4ddf505/bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505.json | results/bm-20250620-3.15.0a0-4ddf505-NOGIL/bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 622 ms                                                                                                          | 522 ms: 1.19x faster                                                                                                  |
| async_tree_none_tg         | 250 ms                                                                                                          | 224 ms: 1.12x faster                                                                                                  |
| async_tree_io              | 609 ms                                                                                                          | 550 ms: 1.11x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 509 ms                                                                                                          | 463 ms: 1.10x faster                                                                                                  |
| async_tree_memoization_tg  | 307 ms                                                                                                          | 284 ms: 1.08x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 511 ms                                                                                                          | 488 ms: 1.05x faster                                                                                                  |
| async_tree_none            | 268 ms                                                                                                          | 257 ms: 1.04x faster                                                                                                  |
| coroutines                 | 22.9 ms                                                                                                         | 23.1 ms: 1.01x slower                                                                                                 |
| async_tree_memoization     | 308 ms                                                                                                          | 312 ms: 1.01x slower                                                                                                  |
| async_generators           | 332 ms                                                                                                          | 364 ms: 1.10x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.05x faster                                                                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250620-3.15.0a0-4ddf505/bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505.json | results/bm-20250620-3.15.0a0-4ddf505-NOGIL/bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 196 ms                                                                                                          | 182 ms: 1.08x faster                                                                                                  |
| float          | 71.6 ms                                                                                                         | 68.8 ms: 1.04x faster                                                                                                 |
| nbody          | 88.5 ms                                                                                                         | 121 ms: 1.36x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.07x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250620-3.15.0a0-4ddf505/bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505.json | results/bm-20250620-3.15.0a0-4ddf505-NOGIL/bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 22.7 ms                                                                                                         | 20.8 ms: 1.09x faster                                                                                                 |
| regex_effbot   | 2.88 ms                                                                                                         | 2.66 ms: 1.08x faster                                                                                                 |
| regex_dna      | 175 ms                                                                                                          | 168 ms: 1.04x faster                                                                                                  |
| regex_compile  | 124 ms                                                                                                          | 143 ms: 1.15x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.02x faster                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250620-3.15.0a0-4ddf505/bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505.json | results/bm-20250620-3.15.0a0-4ddf505-NOGIL/bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 92.1 ms                                                                                                         | 86.8 ms: 1.06x faster                                                                                                 |
| xml_etree_parse      | 133 ms                                                                                                          | 129 ms: 1.03x faster                                                                                                  |
| json_loads           | 28.6 us                                                                                                         | 31.0 us: 1.08x slower                                                                                                 |
| pickle_pure_python   | 309 us                                                                                                          | 337 us: 1.09x slower                                                                                                  |
| unpickle_pure_python | 208 us                                                                                                          | 229 us: 1.10x slower                                                                                                  |
| json_dumps           | 10.7 ms                                                                                                         | 11.8 ms: 1.10x slower                                                                                                 |
| tomli_loads          | 1.90 sec                                                                                                        | 2.15 sec: 1.14x slower                                                                                                |
| xml_etree_generate   | 83.0 ms                                                                                                         | 94.6 ms: 1.14x slower                                                                                                 |
| xml_etree_process    | 58.2 ms                                                                                                         | 68.6 ms: 1.18x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.08x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250620-3.15.0a0-4ddf505/bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505.json | results/bm-20250620-3.15.0a0-4ddf505-NOGIL/bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.6 ms                                                                                                         | 16.1 ms: 1.27x slower                                                                                                 |
| python_startup_no_site | 7.33 ms                                                                                                         | 9.61 ms: 1.31x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.29x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250620-3.15.0a0-4ddf505/bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505.json | results/bm-20250620-3.15.0a0-4ddf505-NOGIL/bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 34.5 ms                                                                                                         | 39.4 ms: 1.14x slower                                                                                                 |
| genshi_xml      | 48.2 ms                                                                                                         | 58.2 ms: 1.21x slower                                                                                                 |
| genshi_text     | 21.1 ms                                                                                                         | 26.5 ms: 1.26x slower                                                                                                 |
| mako            | 11.7 ms                                                                                                         | 15.9 ms: 1.36x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.24x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20250620-3.15.0a0-4ddf505/bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505.json | results/bm-20250620-3.15.0a0-4ddf505-NOGIL/bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.38 ms                                                                                                         | 1.93 ms: 2.27x faster                                                                                                 |
| create_gc_cycles           | 1.91 ms                                                                                                         | 1.50 ms: 1.28x faster                                                                                                 |
| async_tree_io_tg           | 622 ms                                                                                                          | 522 ms: 1.19x faster                                                                                                  |
| sqlite_synth               | 2.27 us                                                                                                         | 2.02 us: 1.13x faster                                                                                                 |
| async_tree_none_tg         | 250 ms                                                                                                          | 224 ms: 1.12x faster                                                                                                  |
| async_tree_io              | 609 ms                                                                                                          | 550 ms: 1.11x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 509 ms                                                                                                          | 463 ms: 1.10x faster                                                                                                  |
| regex_v8                   | 22.7 ms                                                                                                         | 20.8 ms: 1.09x faster                                                                                                 |
| regex_effbot               | 2.88 ms                                                                                                         | 2.66 ms: 1.08x faster                                                                                                 |
| async_tree_memoization_tg  | 307 ms                                                                                                          | 284 ms: 1.08x faster                                                                                                  |
| pidigits                   | 196 ms                                                                                                          | 182 ms: 1.08x faster                                                                                                  |
| xml_etree_iterparse        | 92.1 ms                                                                                                         | 86.8 ms: 1.06x faster                                                                                                 |
| async_tree_cpu_io_mixed    | 511 ms                                                                                                          | 488 ms: 1.05x faster                                                                                                  |
| regex_dna                  | 175 ms                                                                                                          | 168 ms: 1.04x faster                                                                                                  |
| async_tree_none            | 268 ms                                                                                                          | 257 ms: 1.04x faster                                                                                                  |
| float                      | 71.6 ms                                                                                                         | 68.8 ms: 1.04x faster                                                                                                 |
| xml_etree_parse            | 133 ms                                                                                                          | 129 ms: 1.03x faster                                                                                                  |
| coroutines                 | 22.9 ms                                                                                                         | 23.1 ms: 1.01x slower                                                                                                 |
| pathlib                    | 19.2 ms                                                                                                         | 19.5 ms: 1.01x slower                                                                                                 |
| async_tree_memoization     | 308 ms                                                                                                          | 312 ms: 1.01x slower                                                                                                  |
| json                       | 5.15 ms                                                                                                         | 5.25 ms: 1.02x slower                                                                                                 |
| bench_mp_pool              | 99.4 ms                                                                                                         | 103 ms: 1.04x slower                                                                                                  |
| bpe_tokeniser              | 4.15 sec                                                                                                        | 4.34 sec: 1.04x slower                                                                                                |
| docutils                   | 2.53 sec                                                                                                        | 2.67 sec: 1.05x slower                                                                                                |
| dulwich_log                | 66.9 ms                                                                                                         | 71.1 ms: 1.06x slower                                                                                                 |
| many_optionals             | 1.05 ms                                                                                                         | 1.13 ms: 1.08x slower                                                                                                 |
| scimark_fft                | 330 ms                                                                                                          | 356 ms: 1.08x slower                                                                                                  |
| json_loads                 | 28.6 us                                                                                                         | 31.0 us: 1.08x slower                                                                                                 |
| html5lib                   | 60.8 ms                                                                                                         | 66.1 ms: 1.09x slower                                                                                                 |
| pickle_pure_python         | 309 us                                                                                                          | 337 us: 1.09x slower                                                                                                  |
| sphinx                     | 975 ms                                                                                                          | 1.06 sec: 1.09x slower                                                                                                |
| async_generators           | 332 ms                                                                                                          | 364 ms: 1.10x slower                                                                                                  |
| pylint                     | 278 ms                                                                                                          | 306 ms: 1.10x slower                                                                                                  |
| unpickle_pure_python       | 208 us                                                                                                          | 229 us: 1.10x slower                                                                                                  |
| json_dumps                 | 10.7 ms                                                                                                         | 11.8 ms: 1.10x slower                                                                                                 |
| k_core                     | 2.03 sec                                                                                                        | 2.24 sec: 1.11x slower                                                                                                |
| chaos                      | 55.4 ms                                                                                                         | 61.8 ms: 1.12x slower                                                                                                 |
| subparsers                 | 25.1 ms                                                                                                         | 28.2 ms: 1.12x slower                                                                                                 |
| hexiom                     | 5.65 ms                                                                                                         | 6.33 ms: 1.12x slower                                                                                                 |
| spectral_norm              | 96.4 ms                                                                                                         | 108 ms: 1.12x slower                                                                                                  |
| deltablue                  | 3.20 ms                                                                                                         | 3.60 ms: 1.13x slower                                                                                                 |
| logging_silent             | 464 ns                                                                                                          | 523 ns: 1.13x slower                                                                                                  |
| comprehensions             | 15.6 us                                                                                                         | 17.6 us: 1.13x slower                                                                                                 |
| 2to3                       | 249 ms                                                                                                          | 282 ms: 1.13x slower                                                                                                  |
| deepcopy_reduce            | 2.64 us                                                                                                         | 2.99 us: 1.13x slower                                                                                                 |
| deepcopy                   | 252 us                                                                                                          | 286 us: 1.13x slower                                                                                                  |
| tomli_loads                | 1.90 sec                                                                                                        | 2.15 sec: 1.14x slower                                                                                                |
| pprint_safe_repr           | 764 ms                                                                                                          | 868 ms: 1.14x slower                                                                                                  |
| scimark_sor                | 107 ms                                                                                                          | 122 ms: 1.14x slower                                                                                                  |
| nqueens                    | 75.4 ms                                                                                                         | 85.8 ms: 1.14x slower                                                                                                 |
| scimark_sparse_mat_mult    | 4.70 ms                                                                                                         | 5.36 ms: 1.14x slower                                                                                                 |
| django_template            | 34.5 ms                                                                                                         | 39.4 ms: 1.14x slower                                                                                                 |
| xml_etree_generate         | 83.0 ms                                                                                                         | 94.6 ms: 1.14x slower                                                                                                 |
| pprint_pformat             | 1.56 sec                                                                                                        | 1.79 sec: 1.15x slower                                                                                                |
| generators                 | 27.6 ms                                                                                                         | 31.7 ms: 1.15x slower                                                                                                 |
| mdp                        | 1.14 sec                                                                                                        | 1.31 sec: 1.15x slower                                                                                                |
| regex_compile              | 124 ms                                                                                                          | 143 ms: 1.15x slower                                                                                                  |
| sqlglot_v2_optimize        | 49.4 ms                                                                                                         | 56.8 ms: 1.15x slower                                                                                                 |
| sqlglot_v2_normalize       | 98.3 ms                                                                                                         | 113 ms: 1.15x slower                                                                                                  |
| scimark_lu                 | 109 ms                                                                                                          | 127 ms: 1.16x slower                                                                                                  |
| logging_simple             | 6.48 us                                                                                                         | 7.60 us: 1.17x slower                                                                                                 |
| sympy_expand               | 445 ms                                                                                                          | 522 ms: 1.17x slower                                                                                                  |
| sympy_sum                  | 153 ms                                                                                                          | 179 ms: 1.17x slower                                                                                                  |
| sympy_integrate            | 18.6 ms                                                                                                         | 21.9 ms: 1.18x slower                                                                                                 |
| sympy_str                  | 267 ms                                                                                                          | 314 ms: 1.18x slower                                                                                                  |
| xml_etree_process          | 58.2 ms                                                                                                         | 68.6 ms: 1.18x slower                                                                                                 |
| go                         | 103 ms                                                                                                          | 121 ms: 1.18x slower                                                                                                  |
| telco                      | 7.19 ms                                                                                                         | 8.49 ms: 1.18x slower                                                                                                 |
| logging_format             | 7.27 us                                                                                                         | 8.62 us: 1.19x slower                                                                                                 |
| raytrace                   | 250 ms                                                                                                          | 297 ms: 1.19x slower                                                                                                  |
| thrift                     | 736 us                                                                                                          | 876 us: 1.19x slower                                                                                                  |
| deepcopy_memo              | 28.8 us                                                                                                         | 34.4 us: 1.19x slower                                                                                                 |
| sqlglot_v2_transpile       | 1.49 ms                                                                                                         | 1.79 ms: 1.20x slower                                                                                                 |
| genshi_xml                 | 48.2 ms                                                                                                         | 58.2 ms: 1.21x slower                                                                                                 |
| meteor_contest             | 100 ms                                                                                                          | 121 ms: 1.21x slower                                                                                                  |
| sqlglot_v2_parse           | 1.20 ms                                                                                                         | 1.46 ms: 1.22x slower                                                                                                 |
| typing_runtime_protocols   | 154 us                                                                                                          | 188 us: 1.22x slower                                                                                                  |
| pyflate                    | 391 ms                                                                                                          | 477 ms: 1.22x slower                                                                                                  |
| shortest_path              | 440 ms                                                                                                          | 541 ms: 1.23x slower                                                                                                  |
| connected_components       | 399 ms                                                                                                          | 494 ms: 1.24x slower                                                                                                  |
| fannkuch                   | 374 ms                                                                                                          | 463 ms: 1.24x slower                                                                                                  |
| genshi_text                | 21.1 ms                                                                                                         | 26.5 ms: 1.26x slower                                                                                                 |
| scimark_monte_carlo        | 60.2 ms                                                                                                         | 75.9 ms: 1.26x slower                                                                                                 |
| crypto_pyaes               | 67.2 ms                                                                                                         | 85.1 ms: 1.27x slower                                                                                                 |
| python_startup             | 12.6 ms                                                                                                         | 16.1 ms: 1.27x slower                                                                                                 |
| richards                   | 40.8 ms                                                                                                         | 52.4 ms: 1.28x slower                                                                                                 |
| richards_super             | 46.5 ms                                                                                                         | 60.4 ms: 1.30x slower                                                                                                 |
| python_startup_no_site     | 7.33 ms                                                                                                         | 9.61 ms: 1.31x slower                                                                                                 |
| coverage                   | 81.6 ms                                                                                                         | 110 ms: 1.35x slower                                                                                                  |
| mako                       | 11.7 ms                                                                                                         | 15.9 ms: 1.36x slower                                                                                                 |
| nbody                      | 88.5 ms                                                                                                         | 121 ms: 1.36x slower                                                                                                  |
| bench_thread_pool          | 1.04 ms                                                                                                         | 3.11 ms: 2.99x slower                                                                                                 |
| Geometric mean             | (ref)                                                                                                           | 1.11x slower                                                                                                          |

Benchmark hidden because not significant (2): asyncio_websockets, pycparser

- Geometric mean (including insignificant results): 1.087x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.22x