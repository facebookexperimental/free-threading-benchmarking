# Results vs. base

- fork: python
- ref: 47b01da4ccedd9c00fad
- machine: linux-x86_64
- commit hash: 47b01da
- commit date: 2025-07-12
- overall geometric mean: 1.096x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250712-3.15.0a0-47b01da/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json | results/bm-20250712-3.15.0a0-47b01da-NOGIL/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 249 ms                                                                                                          | 285 ms: 1.15x slower                                                                                                  |
| docutils       | 2.54 sec                                                                                                        | 2.70 sec: 1.06x slower                                                                                                |
| html5lib       | 61.7 ms                                                                                                         | 66.1 ms: 1.07x slower                                                                                                 |
| sphinx         | 972 ms                                                                                                          | 1.05 sec: 1.08x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250712-3.15.0a0-47b01da/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json | results/bm-20250712-3.15.0a0-47b01da-NOGIL/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 617 ms                                                                                                          | 536 ms: 1.15x faster                                                                                                  |
| async_tree_none_tg         | 254 ms                                                                                                          | 233 ms: 1.09x faster                                                                                                  |
| async_tree_memoization_tg  | 313 ms                                                                                                          | 294 ms: 1.07x faster                                                                                                  |
| async_tree_io              | 600 ms                                                                                                          | 564 ms: 1.06x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 502 ms                                                                                                          | 488 ms: 1.03x faster                                                                                                  |
| asyncio_websockets         | 518 ms                                                                                                          | 512 ms: 1.01x faster                                                                                                  |
| async_tree_memoization     | 316 ms                                                                                                          | 322 ms: 1.02x slower                                                                                                  |
| async_tree_none            | 257 ms                                                                                                          | 264 ms: 1.03x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 501 ms                                                                                                          | 515 ms: 1.03x slower                                                                                                  |
| asyncio_tcp                | 497 ms                                                                                                          | 518 ms: 1.04x slower                                                                                                  |
| coroutines                 | 23.7 ms                                                                                                         | 24.7 ms: 1.04x slower                                                                                                 |
| async_generators           | 339 ms                                                                                                          | 371 ms: 1.09x slower                                                                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                                                                                        | 1.81 sec: 1.20x slower                                                                                                |
| Geometric mean             | (ref)                                                                                                           | 1.00x slower                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250712-3.15.0a0-47b01da/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json | results/bm-20250712-3.15.0a0-47b01da-NOGIL/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| float          | 71.4 ms                                                                                                         | 69.9 ms: 1.02x faster                                                                                                 |
| pidigits       | 195 ms                                                                                                          | 195 ms: 1.00x slower                                                                                                  |
| nbody          | 89.4 ms                                                                                                         | 122 ms: 1.37x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.10x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250712-3.15.0a0-47b01da/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json | results/bm-20250712-3.15.0a0-47b01da-NOGIL/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.2 ms                                                                                                         | 20.7 ms: 1.02x faster                                                                                                 |
| regex_dna      | 176 ms                                                                                                          | 174 ms: 1.01x faster                                                                                                  |
| regex_compile  | 123 ms                                                                                                          | 144 ms: 1.17x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.03x slower                                                                                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250712-3.15.0a0-47b01da/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json | results/bm-20250712-3.15.0a0-47b01da-NOGIL/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 93.1 ms                                                                                                         | 87.4 ms: 1.07x faster                                                                                                 |
| xml_etree_parse      | 134 ms                                                                                                          | 130 ms: 1.03x faster                                                                                                  |
| pickle               | 12.2 us                                                                                                         | 12.4 us: 1.01x slower                                                                                                 |
| pickle_list          | 5.09 us                                                                                                         | 5.22 us: 1.03x slower                                                                                                 |
| pickle_dict          | 30.5 us                                                                                                         | 32.8 us: 1.08x slower                                                                                                 |
| unpickle_list        | 4.96 us                                                                                                         | 5.33 us: 1.08x slower                                                                                                 |
| json_loads           | 28.2 us                                                                                                         | 31.3 us: 1.11x slower                                                                                                 |
| pickle_pure_python   | 304 us                                                                                                          | 339 us: 1.12x slower                                                                                                  |
| json_dumps           | 10.9 ms                                                                                                         | 12.2 ms: 1.12x slower                                                                                                 |
| unpickle_pure_python | 206 us                                                                                                          | 231 us: 1.12x slower                                                                                                  |
| tomli_loads          | 1.92 sec                                                                                                        | 2.16 sec: 1.12x slower                                                                                                |
| unpickle             | 13.8 us                                                                                                         | 15.7 us: 1.14x slower                                                                                                 |
| xml_etree_generate   | 83.1 ms                                                                                                         | 96.1 ms: 1.16x slower                                                                                                 |
| xml_etree_process    | 57.3 ms                                                                                                         | 69.4 ms: 1.21x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.08x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250712-3.15.0a0-47b01da/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json | results/bm-20250712-3.15.0a0-47b01da-NOGIL/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.6 ms                                                                                                         | 16.0 ms: 1.28x slower                                                                                                 |
| python_startup_no_site | 7.32 ms                                                                                                         | 9.57 ms: 1.31x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.29x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250712-3.15.0a0-47b01da/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json | results/bm-20250712-3.15.0a0-47b01da-NOGIL/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                                                         | 40.2 ms: 1.18x slower                                                                                                 |
| genshi_xml      | 48.4 ms                                                                                                         | 57.8 ms: 1.19x slower                                                                                                 |
| genshi_text     | 20.7 ms                                                                                                         | 26.9 ms: 1.30x slower                                                                                                 |
| mako            | 11.6 ms                                                                                                         | 15.5 ms: 1.34x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.25x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20250712-3.15.0a0-47b01da/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json | results/bm-20250712-3.15.0a0-47b01da-NOGIL/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.69 ms                                                                                                         | 1.88 ms: 2.49x faster                                                                                                 |
| create_gc_cycles           | 1.96 ms                                                                                                         | 1.46 ms: 1.34x faster                                                                                                 |
| async_tree_io_tg           | 617 ms                                                                                                          | 536 ms: 1.15x faster                                                                                                  |
| sqlite_synth               | 2.30 us                                                                                                         | 2.04 us: 1.12x faster                                                                                                 |
| async_tree_none_tg         | 254 ms                                                                                                          | 233 ms: 1.09x faster                                                                                                  |
| async_tree_memoization_tg  | 313 ms                                                                                                          | 294 ms: 1.07x faster                                                                                                  |
| xml_etree_iterparse        | 93.1 ms                                                                                                         | 87.4 ms: 1.07x faster                                                                                                 |
| async_tree_io              | 600 ms                                                                                                          | 564 ms: 1.06x faster                                                                                                  |
| xml_etree_parse            | 134 ms                                                                                                          | 130 ms: 1.03x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 502 ms                                                                                                          | 488 ms: 1.03x faster                                                                                                  |
| regex_v8                   | 21.2 ms                                                                                                         | 20.7 ms: 1.02x faster                                                                                                 |
| float                      | 71.4 ms                                                                                                         | 69.9 ms: 1.02x faster                                                                                                 |
| asyncio_websockets         | 518 ms                                                                                                          | 512 ms: 1.01x faster                                                                                                  |
| regex_dna                  | 176 ms                                                                                                          | 174 ms: 1.01x faster                                                                                                  |
| pidigits                   | 195 ms                                                                                                          | 195 ms: 1.00x slower                                                                                                  |
| pickle                     | 12.2 us                                                                                                         | 12.4 us: 1.01x slower                                                                                                 |
| async_tree_memoization     | 316 ms                                                                                                          | 322 ms: 1.02x slower                                                                                                  |
| async_tree_none            | 257 ms                                                                                                          | 264 ms: 1.03x slower                                                                                                  |
| pickle_list                | 5.09 us                                                                                                         | 5.22 us: 1.03x slower                                                                                                 |
| async_tree_cpu_io_mixed    | 501 ms                                                                                                          | 515 ms: 1.03x slower                                                                                                  |
| asyncio_tcp                | 497 ms                                                                                                          | 518 ms: 1.04x slower                                                                                                  |
| coroutines                 | 23.7 ms                                                                                                         | 24.7 ms: 1.04x slower                                                                                                 |
| pycparser                  | 1.09 sec                                                                                                        | 1.14 sec: 1.05x slower                                                                                                |
| bpe_tokeniser              | 4.19 sec                                                                                                        | 4.39 sec: 1.05x slower                                                                                                |
| json                       | 5.09 ms                                                                                                         | 5.35 ms: 1.05x slower                                                                                                 |
| bench_mp_pool              | 103 ms                                                                                                          | 109 ms: 1.06x slower                                                                                                  |
| docutils                   | 2.54 sec                                                                                                        | 2.70 sec: 1.06x slower                                                                                                |
| html5lib                   | 61.7 ms                                                                                                         | 66.1 ms: 1.07x slower                                                                                                 |
| sphinx                     | 972 ms                                                                                                          | 1.05 sec: 1.08x slower                                                                                                |
| pickle_dict                | 30.5 us                                                                                                         | 32.8 us: 1.08x slower                                                                                                 |
| unpickle_list              | 4.96 us                                                                                                         | 5.33 us: 1.08x slower                                                                                                 |
| dulwich_log                | 66.5 ms                                                                                                         | 71.8 ms: 1.08x slower                                                                                                 |
| logging_silent             | 96.3 ns                                                                                                         | 105 ns: 1.09x slower                                                                                                  |
| async_generators           | 339 ms                                                                                                          | 371 ms: 1.09x slower                                                                                                  |
| k_core                     | 2.03 sec                                                                                                        | 2.24 sec: 1.10x slower                                                                                                |
| telco                      | 159 ms                                                                                                          | 177 ms: 1.11x slower                                                                                                  |
| pylint                     | 279 ms                                                                                                          | 309 ms: 1.11x slower                                                                                                  |
| many_optionals             | 1.05 ms                                                                                                         | 1.16 ms: 1.11x slower                                                                                                 |
| scimark_fft                | 336 ms                                                                                                          | 373 ms: 1.11x slower                                                                                                  |
| json_loads                 | 28.2 us                                                                                                         | 31.3 us: 1.11x slower                                                                                                 |
| pprint_safe_repr           | 703 ms                                                                                                          | 783 ms: 1.11x slower                                                                                                  |
| subparsers                 | 25.4 ms                                                                                                         | 28.3 ms: 1.11x slower                                                                                                 |
| pickle_pure_python         | 304 us                                                                                                          | 339 us: 1.12x slower                                                                                                  |
| chaos                      | 56.2 ms                                                                                                         | 62.8 ms: 1.12x slower                                                                                                 |
| json_dumps                 | 10.9 ms                                                                                                         | 12.2 ms: 1.12x slower                                                                                                 |
| unpickle_pure_python       | 206 us                                                                                                          | 231 us: 1.12x slower                                                                                                  |
| tomli_loads                | 1.92 sec                                                                                                        | 2.16 sec: 1.12x slower                                                                                                |
| nqueens                    | 78.5 ms                                                                                                         | 88.9 ms: 1.13x slower                                                                                                 |
| deepcopy_reduce            | 2.65 us                                                                                                         | 3.01 us: 1.14x slower                                                                                                 |
| unpickle                   | 13.8 us                                                                                                         | 15.7 us: 1.14x slower                                                                                                 |
| pprint_pformat             | 1.43 sec                                                                                                        | 1.63 sec: 1.14x slower                                                                                                |
| spectral_norm              | 99.3 ms                                                                                                         | 113 ms: 1.14x slower                                                                                                  |
| 2to3                       | 249 ms                                                                                                          | 285 ms: 1.15x slower                                                                                                  |
| comprehensions             | 15.4 us                                                                                                         | 17.8 us: 1.15x slower                                                                                                 |
| generators                 | 28.0 ms                                                                                                         | 32.2 ms: 1.15x slower                                                                                                 |
| sympy_expand               | 458 ms                                                                                                          | 528 ms: 1.15x slower                                                                                                  |
| mdp                        | 1.15 sec                                                                                                        | 1.33 sec: 1.15x slower                                                                                                |
| xml_etree_generate         | 83.1 ms                                                                                                         | 96.1 ms: 1.16x slower                                                                                                 |
| scimark_sor                | 109 ms                                                                                                          | 125 ms: 1.16x slower                                                                                                  |
| hexiom                     | 5.59 ms                                                                                                         | 6.51 ms: 1.16x slower                                                                                                 |
| pyflate                    | 400 ms                                                                                                          | 467 ms: 1.17x slower                                                                                                  |
| go                         | 104 ms                                                                                                          | 121 ms: 1.17x slower                                                                                                  |
| sqlglot_v2_optimize        | 49.7 ms                                                                                                         | 58.1 ms: 1.17x slower                                                                                                 |
| fannkuch                   | 388 ms                                                                                                          | 454 ms: 1.17x slower                                                                                                  |
| sympy_str                  | 269 ms                                                                                                          | 314 ms: 1.17x slower                                                                                                  |
| regex_compile              | 123 ms                                                                                                          | 144 ms: 1.17x slower                                                                                                  |
| django_template            | 34.2 ms                                                                                                         | 40.2 ms: 1.18x slower                                                                                                 |
| sqlglot_v2_normalize       | 98.0 ms                                                                                                         | 115 ms: 1.18x slower                                                                                                  |
| sympy_integrate            | 18.8 ms                                                                                                         | 22.1 ms: 1.18x slower                                                                                                 |
| thrift                     | 752 us                                                                                                          | 885 us: 1.18x slower                                                                                                  |
| sympy_sum                  | 153 ms                                                                                                          | 181 ms: 1.18x slower                                                                                                  |
| deepcopy                   | 250 us                                                                                                          | 294 us: 1.18x slower                                                                                                  |
| scimark_lu                 | 110 ms                                                                                                          | 130 ms: 1.18x slower                                                                                                  |
| deltablue                  | 3.08 ms                                                                                                         | 3.65 ms: 1.19x slower                                                                                                 |
| genshi_xml                 | 48.4 ms                                                                                                         | 57.8 ms: 1.19x slower                                                                                                 |
| scimark_sparse_mat_mult    | 4.66 ms                                                                                                         | 5.57 ms: 1.20x slower                                                                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                                                                                        | 1.81 sec: 1.20x slower                                                                                                |
| raytrace                   | 250 ms                                                                                                          | 302 ms: 1.20x slower                                                                                                  |
| meteor_contest             | 98.5 ms                                                                                                         | 119 ms: 1.20x slower                                                                                                  |
| logging_simple             | 5.82 us                                                                                                         | 7.02 us: 1.21x slower                                                                                                 |
| xml_etree_process          | 57.3 ms                                                                                                         | 69.4 ms: 1.21x slower                                                                                                 |
| deepcopy_memo              | 28.6 us                                                                                                         | 34.7 us: 1.21x slower                                                                                                 |
| shortest_path              | 438 ms                                                                                                          | 535 ms: 1.22x slower                                                                                                  |
| sqlglot_v2_transpile       | 1.51 ms                                                                                                         | 1.85 ms: 1.22x slower                                                                                                 |
| sqlglot_v2_parse           | 1.21 ms                                                                                                         | 1.48 ms: 1.22x slower                                                                                                 |
| connected_components       | 398 ms                                                                                                          | 490 ms: 1.23x slower                                                                                                  |
| typing_runtime_protocols   | 155 us                                                                                                          | 191 us: 1.23x slower                                                                                                  |
| logging_format             | 6.51 us                                                                                                         | 8.07 us: 1.24x slower                                                                                                 |
| scimark_monte_carlo        | 62.5 ms                                                                                                         | 77.9 ms: 1.25x slower                                                                                                 |
| richards                   | 41.1 ms                                                                                                         | 51.4 ms: 1.25x slower                                                                                                 |
| richards_super             | 46.8 ms                                                                                                         | 59.0 ms: 1.26x slower                                                                                                 |
| crypto_pyaes               | 68.0 ms                                                                                                         | 86.7 ms: 1.28x slower                                                                                                 |
| python_startup             | 12.6 ms                                                                                                         | 16.0 ms: 1.28x slower                                                                                                 |
| genshi_text                | 20.7 ms                                                                                                         | 26.9 ms: 1.30x slower                                                                                                 |
| python_startup_no_site     | 7.32 ms                                                                                                         | 9.57 ms: 1.31x slower                                                                                                 |
| unpack_sequence            | 42.1 ns                                                                                                         | 55.5 ns: 1.32x slower                                                                                                 |
| mako                       | 11.6 ms                                                                                                         | 15.5 ms: 1.34x slower                                                                                                 |
| nbody                      | 89.4 ms                                                                                                         | 122 ms: 1.37x slower                                                                                                  |
| coverage                   | 80.8 ms                                                                                                         | 111 ms: 1.37x slower                                                                                                  |
| bench_thread_pool          | 1.05 ms                                                                                                         | 3.16 ms: 3.01x slower                                                                                                 |
| Geometric mean             | (ref)                                                                                                           | 1.12x slower                                                                                                          |

Benchmark hidden because not significant (2): regex_effbot, pathlib

- Geometric mean (including insignificant results): 1.096x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.20x