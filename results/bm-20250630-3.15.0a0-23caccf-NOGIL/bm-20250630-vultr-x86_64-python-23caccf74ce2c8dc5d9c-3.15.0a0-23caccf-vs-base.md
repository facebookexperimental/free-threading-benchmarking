# Results vs. base

- fork: python
- ref: 23caccf74ce2c8dc5d9c
- machine: linux-x86_64
- commit hash: 23caccf
- commit date: 2025-06-30
- overall geometric mean: 1.091x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250630-3.15.0a0-23caccf/bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf.json | results/bm-20250630-3.15.0a0-23caccf-NOGIL/bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 250 ms                                                                                                          | 284 ms: 1.14x slower                                                                                                  |
| docutils       | 2.53 sec                                                                                                        | 2.70 sec: 1.07x slower                                                                                                |
| html5lib       | 61.5 ms                                                                                                         | 65.0 ms: 1.06x slower                                                                                                 |
| sphinx         | 962 ms                                                                                                          | 1.03 sec: 1.07x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.08x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250630-3.15.0a0-23caccf/bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf.json | results/bm-20250630-3.15.0a0-23caccf-NOGIL/bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 627 ms                                                                                                          | 524 ms: 1.20x faster                                                                                                  |
| async_tree_none_tg         | 254 ms                                                                                                          | 227 ms: 1.12x faster                                                                                                  |
| async_tree_io              | 609 ms                                                                                                          | 555 ms: 1.10x faster                                                                                                  |
| async_tree_memoization_tg  | 310 ms                                                                                                          | 286 ms: 1.09x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 498 ms                                                                                                          | 475 ms: 1.05x faster                                                                                                  |
| async_tree_none            | 268 ms                                                                                                          | 259 ms: 1.04x faster                                                                                                  |
| asyncio_websockets         | 517 ms                                                                                                          | 513 ms: 1.01x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 497 ms                                                                                                          | 499 ms: 1.01x slower                                                                                                  |
| async_tree_memoization     | 307 ms                                                                                                          | 313 ms: 1.02x slower                                                                                                  |
| coroutines                 | 23.2 ms                                                                                                         | 24.6 ms: 1.06x slower                                                                                                 |
| async_generators           | 340 ms                                                                                                          | 374 ms: 1.10x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.03x faster                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250630-3.15.0a0-23caccf/bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf.json | results/bm-20250630-3.15.0a0-23caccf-NOGIL/bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 203 ms                                                                                                          | 194 ms: 1.04x faster                                                                                                  |
| float          | 72.7 ms                                                                                                         | 69.7 ms: 1.04x faster                                                                                                 |
| nbody          | 88.3 ms                                                                                                         | 125 ms: 1.41x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250630-3.15.0a0-23caccf/bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf.json | results/bm-20250630-3.15.0a0-23caccf-NOGIL/bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_dna      | 173 ms                                                                                                          | 163 ms: 1.06x faster                                                                                                  |
| regex_v8       | 21.1 ms                                                                                                         | 20.1 ms: 1.05x faster                                                                                                 |
| regex_effbot   | 2.60 ms                                                                                                         | 2.59 ms: 1.00x faster                                                                                                 |
| regex_compile  | 124 ms                                                                                                          | 144 ms: 1.16x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.01x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250630-3.15.0a0-23caccf/bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf.json | results/bm-20250630-3.15.0a0-23caccf-NOGIL/bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 93.3 ms                                                                                                         | 87.1 ms: 1.07x faster                                                                                                 |
| xml_etree_parse      | 134 ms                                                                                                          | 131 ms: 1.02x faster                                                                                                  |
| json_loads           | 28.9 us                                                                                                         | 31.9 us: 1.10x slower                                                                                                 |
| pickle_pure_python   | 306 us                                                                                                          | 338 us: 1.10x slower                                                                                                  |
| tomli_loads          | 1.92 sec                                                                                                        | 2.15 sec: 1.12x slower                                                                                                |
| json_dumps           | 10.7 ms                                                                                                         | 12.0 ms: 1.12x slower                                                                                                 |
| unpickle_pure_python | 207 us                                                                                                          | 234 us: 1.13x slower                                                                                                  |
| xml_etree_generate   | 83.6 ms                                                                                                         | 95.5 ms: 1.14x slower                                                                                                 |
| xml_etree_process    | 58.4 ms                                                                                                         | 69.1 ms: 1.18x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250630-3.15.0a0-23caccf/bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf.json | results/bm-20250630-3.15.0a0-23caccf-NOGIL/bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.6 ms                                                                                                         | 16.0 ms: 1.27x slower                                                                                                 |
| python_startup_no_site | 7.32 ms                                                                                                         | 9.55 ms: 1.30x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.29x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250630-3.15.0a0-23caccf/bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf.json | results/bm-20250630-3.15.0a0-23caccf-NOGIL/bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 34.5 ms                                                                                                         | 39.9 ms: 1.15x slower                                                                                                 |
| genshi_xml      | 48.2 ms                                                                                                         | 58.6 ms: 1.22x slower                                                                                                 |
| genshi_text     | 20.8 ms                                                                                                         | 26.7 ms: 1.29x slower                                                                                                 |
| mako            | 11.8 ms                                                                                                         | 15.8 ms: 1.34x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.25x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20250630-3.15.0a0-23caccf/bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf.json | results/bm-20250630-3.15.0a0-23caccf-NOGIL/bm-20250630-vultr-x86_64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.33 ms                                                                                                         | 1.87 ms: 2.31x faster                                                                                                 |
| create_gc_cycles           | 1.89 ms                                                                                                         | 1.44 ms: 1.31x faster                                                                                                 |
| async_tree_io_tg           | 627 ms                                                                                                          | 524 ms: 1.20x faster                                                                                                  |
| async_tree_none_tg         | 254 ms                                                                                                          | 227 ms: 1.12x faster                                                                                                  |
| async_tree_io              | 609 ms                                                                                                          | 555 ms: 1.10x faster                                                                                                  |
| sqlite_synth               | 2.25 us                                                                                                         | 2.06 us: 1.09x faster                                                                                                 |
| async_tree_memoization_tg  | 310 ms                                                                                                          | 286 ms: 1.09x faster                                                                                                  |
| xml_etree_iterparse        | 93.3 ms                                                                                                         | 87.1 ms: 1.07x faster                                                                                                 |
| regex_dna                  | 173 ms                                                                                                          | 163 ms: 1.06x faster                                                                                                  |
| regex_v8                   | 21.1 ms                                                                                                         | 20.1 ms: 1.05x faster                                                                                                 |
| async_tree_cpu_io_mixed_tg | 498 ms                                                                                                          | 475 ms: 1.05x faster                                                                                                  |
| pidigits                   | 203 ms                                                                                                          | 194 ms: 1.04x faster                                                                                                  |
| float                      | 72.7 ms                                                                                                         | 69.7 ms: 1.04x faster                                                                                                 |
| async_tree_none            | 268 ms                                                                                                          | 259 ms: 1.04x faster                                                                                                  |
| xml_etree_parse            | 134 ms                                                                                                          | 131 ms: 1.02x faster                                                                                                  |
| pathlib                    | 19.8 ms                                                                                                         | 19.5 ms: 1.02x faster                                                                                                 |
| asyncio_websockets         | 517 ms                                                                                                          | 513 ms: 1.01x faster                                                                                                  |
| regex_effbot               | 2.60 ms                                                                                                         | 2.59 ms: 1.00x faster                                                                                                 |
| async_tree_cpu_io_mixed    | 497 ms                                                                                                          | 499 ms: 1.01x slower                                                                                                  |
| async_tree_memoization     | 307 ms                                                                                                          | 313 ms: 1.02x slower                                                                                                  |
| logging_silent             | 97.7 ns                                                                                                         | 100 ns: 1.03x slower                                                                                                  |
| pycparser                  | 1.10 sec                                                                                                        | 1.14 sec: 1.04x slower                                                                                                |
| bpe_tokeniser              | 4.19 sec                                                                                                        | 4.40 sec: 1.05x slower                                                                                                |
| bench_mp_pool              | 99.0 ms                                                                                                         | 104 ms: 1.05x slower                                                                                                  |
| html5lib                   | 61.5 ms                                                                                                         | 65.0 ms: 1.06x slower                                                                                                 |
| json                       | 5.12 ms                                                                                                         | 5.41 ms: 1.06x slower                                                                                                 |
| coroutines                 | 23.2 ms                                                                                                         | 24.6 ms: 1.06x slower                                                                                                 |
| docutils                   | 2.53 sec                                                                                                        | 2.70 sec: 1.07x slower                                                                                                |
| sphinx                     | 962 ms                                                                                                          | 1.03 sec: 1.07x slower                                                                                                |
| dulwich_log                | 67.0 ms                                                                                                         | 72.6 ms: 1.08x slower                                                                                                 |
| many_optionals             | 1.04 ms                                                                                                         | 1.13 ms: 1.09x slower                                                                                                 |
| k_core                     | 2.04 sec                                                                                                        | 2.23 sec: 1.10x slower                                                                                                |
| async_generators           | 340 ms                                                                                                          | 374 ms: 1.10x slower                                                                                                  |
| deltablue                  | 3.26 ms                                                                                                         | 3.59 ms: 1.10x slower                                                                                                 |
| json_loads                 | 28.9 us                                                                                                         | 31.9 us: 1.10x slower                                                                                                 |
| pickle_pure_python         | 306 us                                                                                                          | 338 us: 1.10x slower                                                                                                  |
| scimark_fft                | 337 ms                                                                                                          | 373 ms: 1.11x slower                                                                                                  |
| pylint                     | 279 ms                                                                                                          | 310 ms: 1.11x slower                                                                                                  |
| generators                 | 27.8 ms                                                                                                         | 31.2 ms: 1.12x slower                                                                                                 |
| tomli_loads                | 1.92 sec                                                                                                        | 2.15 sec: 1.12x slower                                                                                                |
| pprint_safe_repr           | 691 ms                                                                                                          | 775 ms: 1.12x slower                                                                                                  |
| json_dumps                 | 10.7 ms                                                                                                         | 12.0 ms: 1.12x slower                                                                                                 |
| unpickle_pure_python       | 207 us                                                                                                          | 234 us: 1.13x slower                                                                                                  |
| sympy_expand               | 460 ms                                                                                                          | 520 ms: 1.13x slower                                                                                                  |
| scimark_sparse_mat_mult    | 4.89 ms                                                                                                         | 5.54 ms: 1.13x slower                                                                                                 |
| chaos                      | 56.0 ms                                                                                                         | 63.6 ms: 1.13x slower                                                                                                 |
| 2to3                       | 250 ms                                                                                                          | 284 ms: 1.14x slower                                                                                                  |
| scimark_sor                | 110 ms                                                                                                          | 125 ms: 1.14x slower                                                                                                  |
| subparsers                 | 25.1 ms                                                                                                         | 28.6 ms: 1.14x slower                                                                                                 |
| comprehensions             | 15.6 us                                                                                                         | 17.7 us: 1.14x slower                                                                                                 |
| pprint_pformat             | 1.41 sec                                                                                                        | 1.61 sec: 1.14x slower                                                                                                |
| xml_etree_generate         | 83.6 ms                                                                                                         | 95.5 ms: 1.14x slower                                                                                                 |
| nqueens                    | 77.6 ms                                                                                                         | 88.7 ms: 1.14x slower                                                                                                 |
| hexiom                     | 5.64 ms                                                                                                         | 6.47 ms: 1.15x slower                                                                                                 |
| logging_simple             | 5.97 us                                                                                                         | 6.87 us: 1.15x slower                                                                                                 |
| django_template            | 34.5 ms                                                                                                         | 39.9 ms: 1.15x slower                                                                                                 |
| sqlglot_v2_optimize        | 49.8 ms                                                                                                         | 57.6 ms: 1.16x slower                                                                                                 |
| deepcopy                   | 253 us                                                                                                          | 293 us: 1.16x slower                                                                                                  |
| sqlglot_v2_normalize       | 99.2 ms                                                                                                         | 115 ms: 1.16x slower                                                                                                  |
| regex_compile              | 124 ms                                                                                                          | 144 ms: 1.16x slower                                                                                                  |
| mdp                        | 1.14 sec                                                                                                        | 1.32 sec: 1.16x slower                                                                                                |
| deepcopy_reduce            | 2.65 us                                                                                                         | 3.08 us: 1.16x slower                                                                                                 |
| logging_format             | 6.69 us                                                                                                         | 7.77 us: 1.16x slower                                                                                                 |
| sympy_sum                  | 154 ms                                                                                                          | 179 ms: 1.16x slower                                                                                                  |
| sympy_str                  | 269 ms                                                                                                          | 313 ms: 1.16x slower                                                                                                  |
| go                         | 104 ms                                                                                                          | 121 ms: 1.16x slower                                                                                                  |
| spectral_norm              | 97.1 ms                                                                                                         | 113 ms: 1.16x slower                                                                                                  |
| scimark_lu                 | 112 ms                                                                                                          | 131 ms: 1.17x slower                                                                                                  |
| sympy_integrate            | 18.7 ms                                                                                                         | 21.9 ms: 1.17x slower                                                                                                 |
| telco                      | 7.39 ms                                                                                                         | 8.67 ms: 1.17x slower                                                                                                 |
| pyflate                    | 399 ms                                                                                                          | 469 ms: 1.18x slower                                                                                                  |
| xml_etree_process          | 58.4 ms                                                                                                         | 69.1 ms: 1.18x slower                                                                                                 |
| thrift                     | 740 us                                                                                                          | 878 us: 1.19x slower                                                                                                  |
| fannkuch                   | 389 ms                                                                                                          | 464 ms: 1.19x slower                                                                                                  |
| deepcopy_memo              | 29.1 us                                                                                                         | 34.7 us: 1.20x slower                                                                                                 |
| sqlglot_v2_transpile       | 1.49 ms                                                                                                         | 1.79 ms: 1.20x slower                                                                                                 |
| raytrace                   | 252 ms                                                                                                          | 304 ms: 1.21x slower                                                                                                  |
| genshi_xml                 | 48.2 ms                                                                                                         | 58.6 ms: 1.22x slower                                                                                                 |
| meteor_contest             | 99.5 ms                                                                                                         | 122 ms: 1.22x slower                                                                                                  |
| sqlglot_v2_parse           | 1.19 ms                                                                                                         | 1.46 ms: 1.22x slower                                                                                                 |
| shortest_path              | 440 ms                                                                                                          | 542 ms: 1.23x slower                                                                                                  |
| typing_runtime_protocols   | 154 us                                                                                                          | 191 us: 1.24x slower                                                                                                  |
| connected_components       | 396 ms                                                                                                          | 492 ms: 1.24x slower                                                                                                  |
| richards                   | 41.2 ms                                                                                                         | 52.0 ms: 1.26x slower                                                                                                 |
| python_startup             | 12.6 ms                                                                                                         | 16.0 ms: 1.27x slower                                                                                                 |
| richards_super             | 46.7 ms                                                                                                         | 59.6 ms: 1.27x slower                                                                                                 |
| scimark_monte_carlo        | 61.6 ms                                                                                                         | 78.7 ms: 1.28x slower                                                                                                 |
| genshi_text                | 20.8 ms                                                                                                         | 26.7 ms: 1.29x slower                                                                                                 |
| crypto_pyaes               | 66.8 ms                                                                                                         | 86.7 ms: 1.30x slower                                                                                                 |
| python_startup_no_site     | 7.32 ms                                                                                                         | 9.55 ms: 1.30x slower                                                                                                 |
| mako                       | 11.8 ms                                                                                                         | 15.8 ms: 1.34x slower                                                                                                 |
| coverage                   | 81.6 ms                                                                                                         | 112 ms: 1.38x slower                                                                                                  |
| nbody                      | 88.3 ms                                                                                                         | 125 ms: 1.41x slower                                                                                                  |
| bench_thread_pool          | 1.05 ms                                                                                                         | 3.15 ms: 3.01x slower                                                                                                 |
| Geometric mean             | (ref)                                                                                                           | 1.11x slower                                                                                                          |

- Geometric mean (including insignificant results): 1.091x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.20x