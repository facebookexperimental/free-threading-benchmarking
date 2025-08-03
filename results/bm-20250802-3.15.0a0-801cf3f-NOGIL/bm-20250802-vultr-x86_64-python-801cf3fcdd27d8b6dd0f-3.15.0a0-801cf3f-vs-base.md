# Results vs. base

- fork: python
- ref: 801cf3fcdd27d8b6dd0f
- machine: linux-x86_64
- commit hash: 801cf3f
- commit date: 2025-08-02
- overall geometric mean: 1.094x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250802-3.15.0a0-801cf3f/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json | results/bm-20250802-3.15.0a0-801cf3f-NOGIL/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 249 ms                                                                                                          | 285 ms: 1.15x slower                                                                                                  |
| docutils       | 2.57 sec                                                                                                        | 2.71 sec: 1.05x slower                                                                                                |
| html5lib       | 60.5 ms                                                                                                         | 67.3 ms: 1.11x slower                                                                                                 |
| sphinx         | 972 ms                                                                                                          | 1.05 sec: 1.08x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.10x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250802-3.15.0a0-801cf3f/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json | results/bm-20250802-3.15.0a0-801cf3f-NOGIL/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 612 ms                                                                                                          | 513 ms: 1.19x faster                                                                                                  |
| async_tree_none_tg         | 257 ms                                                                                                          | 227 ms: 1.13x faster                                                                                                  |
| async_tree_io              | 603 ms                                                                                                          | 541 ms: 1.11x faster                                                                                                  |
| async_tree_memoization_tg  | 311 ms                                                                                                          | 284 ms: 1.09x faster                                                                                                  |
| async_tree_none            | 266 ms                                                                                                          | 256 ms: 1.04x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 497 ms                                                                                                          | 486 ms: 1.02x faster                                                                                                  |
| asyncio_websockets         | 517 ms                                                                                                          | 513 ms: 1.01x faster                                                                                                  |
| async_tree_memoization     | 305 ms                                                                                                          | 309 ms: 1.01x slower                                                                                                  |
| coroutines                 | 23.6 ms                                                                                                         | 24.1 ms: 1.02x slower                                                                                                 |
| async_tree_cpu_io_mixed    | 497 ms                                                                                                          | 510 ms: 1.03x slower                                                                                                  |
| asyncio_tcp                | 498 ms                                                                                                          | 514 ms: 1.03x slower                                                                                                  |
| async_generators           | 338 ms                                                                                                          | 377 ms: 1.12x slower                                                                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                                                                                        | 1.80 sec: 1.19x slower                                                                                                |
| Geometric mean             | (ref)                                                                                                           | 1.01x faster                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250802-3.15.0a0-801cf3f/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json | results/bm-20250802-3.15.0a0-801cf3f-NOGIL/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| float          | 72.5 ms                                                                                                         | 68.7 ms: 1.06x faster                                                                                                 |
| pidigits       | 213 ms                                                                                                          | 202 ms: 1.05x faster                                                                                                  |
| nbody          | 89.3 ms                                                                                                         | 123 ms: 1.38x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.08x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250802-3.15.0a0-801cf3f/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json | results/bm-20250802-3.15.0a0-801cf3f-NOGIL/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 22.4 ms                                                                                                         | 20.8 ms: 1.08x faster                                                                                                 |
| regex_effbot   | 2.78 ms                                                                                                         | 2.63 ms: 1.06x faster                                                                                                 |
| regex_dna      | 180 ms                                                                                                          | 171 ms: 1.05x faster                                                                                                  |
| regex_compile  | 123 ms                                                                                                          | 144 ms: 1.17x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.01x faster                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250802-3.15.0a0-801cf3f/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json | results/bm-20250802-3.15.0a0-801cf3f-NOGIL/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 92.2 ms                                                                                                         | 87.1 ms: 1.06x faster                                                                                                 |
| pickle               | 12.2 us                                                                                                         | 12.4 us: 1.01x slower                                                                                                 |
| pickle_list          | 5.06 us                                                                                                         | 5.27 us: 1.04x slower                                                                                                 |
| pickle_dict          | 30.8 us                                                                                                         | 32.6 us: 1.06x slower                                                                                                 |
| json_dumps           | 10.7 ms                                                                                                         | 11.6 ms: 1.08x slower                                                                                                 |
| unpickle_list        | 4.94 us                                                                                                         | 5.36 us: 1.09x slower                                                                                                 |
| json_loads           | 28.9 us                                                                                                         | 31.8 us: 1.10x slower                                                                                                 |
| unpickle             | 13.9 us                                                                                                         | 15.5 us: 1.12x slower                                                                                                 |
| tomli_loads          | 1.93 sec                                                                                                        | 2.17 sec: 1.12x slower                                                                                                |
| unpickle_pure_python | 208 us                                                                                                          | 234 us: 1.13x slower                                                                                                  |
| pickle_pure_python   | 303 us                                                                                                          | 342 us: 1.13x slower                                                                                                  |
| xml_etree_generate   | 83.2 ms                                                                                                         | 95.7 ms: 1.15x slower                                                                                                 |
| xml_etree_process    | 57.8 ms                                                                                                         | 69.5 ms: 1.20x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.08x slower                                                                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250802-3.15.0a0-801cf3f/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json | results/bm-20250802-3.15.0a0-801cf3f-NOGIL/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.6 ms                                                                                                         | 15.7 ms: 1.25x slower                                                                                                 |
| python_startup_no_site | 7.24 ms                                                                                                         | 9.57 ms: 1.32x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.29x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250802-3.15.0a0-801cf3f/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json | results/bm-20250802-3.15.0a0-801cf3f-NOGIL/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 34.7 ms                                                                                                         | 40.8 ms: 1.18x slower                                                                                                 |
| genshi_xml      | 47.8 ms                                                                                                         | 57.5 ms: 1.20x slower                                                                                                 |
| genshi_text     | 20.3 ms                                                                                                         | 27.0 ms: 1.33x slower                                                                                                 |
| mako            | 11.8 ms                                                                                                         | 15.8 ms: 1.34x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.26x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20250802-3.15.0a0-801cf3f/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json | results/bm-20250802-3.15.0a0-801cf3f-NOGIL/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.36 ms                                                                                                         | 1.96 ms: 2.22x faster                                                                                                 |
| create_gc_cycles           | 1.96 ms                                                                                                         | 1.55 ms: 1.27x faster                                                                                                 |
| async_tree_io_tg           | 612 ms                                                                                                          | 513 ms: 1.19x faster                                                                                                  |
| async_tree_none_tg         | 257 ms                                                                                                          | 227 ms: 1.13x faster                                                                                                  |
| async_tree_io              | 603 ms                                                                                                          | 541 ms: 1.11x faster                                                                                                  |
| sqlite_synth               | 2.26 us                                                                                                         | 2.05 us: 1.10x faster                                                                                                 |
| async_tree_memoization_tg  | 311 ms                                                                                                          | 284 ms: 1.09x faster                                                                                                  |
| regex_v8                   | 22.4 ms                                                                                                         | 20.8 ms: 1.08x faster                                                                                                 |
| xml_etree_iterparse        | 92.2 ms                                                                                                         | 87.1 ms: 1.06x faster                                                                                                 |
| regex_effbot               | 2.78 ms                                                                                                         | 2.63 ms: 1.06x faster                                                                                                 |
| float                      | 72.5 ms                                                                                                         | 68.7 ms: 1.06x faster                                                                                                 |
| regex_dna                  | 180 ms                                                                                                          | 171 ms: 1.05x faster                                                                                                  |
| pidigits                   | 213 ms                                                                                                          | 202 ms: 1.05x faster                                                                                                  |
| async_tree_none            | 266 ms                                                                                                          | 256 ms: 1.04x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 497 ms                                                                                                          | 486 ms: 1.02x faster                                                                                                  |
| asyncio_websockets         | 517 ms                                                                                                          | 513 ms: 1.01x faster                                                                                                  |
| async_tree_memoization     | 305 ms                                                                                                          | 309 ms: 1.01x slower                                                                                                  |
| pickle                     | 12.2 us                                                                                                         | 12.4 us: 1.01x slower                                                                                                 |
| coroutines                 | 23.6 ms                                                                                                         | 24.1 ms: 1.02x slower                                                                                                 |
| async_tree_cpu_io_mixed    | 497 ms                                                                                                          | 510 ms: 1.03x slower                                                                                                  |
| asyncio_tcp                | 498 ms                                                                                                          | 514 ms: 1.03x slower                                                                                                  |
| json                       | 5.22 ms                                                                                                         | 5.43 ms: 1.04x slower                                                                                                 |
| pickle_list                | 5.06 us                                                                                                         | 5.27 us: 1.04x slower                                                                                                 |
| bpe_tokeniser              | 4.16 sec                                                                                                        | 4.38 sec: 1.05x slower                                                                                                |
| docutils                   | 2.57 sec                                                                                                        | 2.71 sec: 1.05x slower                                                                                                |
| pycparser                  | 1.09 sec                                                                                                        | 1.15 sec: 1.05x slower                                                                                                |
| bench_mp_pool              | 103 ms                                                                                                          | 108 ms: 1.05x slower                                                                                                  |
| pickle_dict                | 30.8 us                                                                                                         | 32.6 us: 1.06x slower                                                                                                 |
| sphinx                     | 972 ms                                                                                                          | 1.05 sec: 1.08x slower                                                                                                |
| deltablue                  | 3.28 ms                                                                                                         | 3.55 ms: 1.08x slower                                                                                                 |
| json_dumps                 | 10.7 ms                                                                                                         | 11.6 ms: 1.08x slower                                                                                                 |
| logging_silent             | 96.6 ns                                                                                                         | 105 ns: 1.08x slower                                                                                                  |
| unpickle_list              | 4.94 us                                                                                                         | 5.36 us: 1.09x slower                                                                                                 |
| dulwich_log                | 66.1 ms                                                                                                         | 72.2 ms: 1.09x slower                                                                                                 |
| json_loads                 | 28.9 us                                                                                                         | 31.8 us: 1.10x slower                                                                                                 |
| k_core                     | 2.03 sec                                                                                                        | 2.23 sec: 1.10x slower                                                                                                |
| pylint                     | 279 ms                                                                                                          | 308 ms: 1.10x slower                                                                                                  |
| telco                      | 158 ms                                                                                                          | 175 ms: 1.11x slower                                                                                                  |
| many_optionals             | 1.21 ms                                                                                                         | 1.34 ms: 1.11x slower                                                                                                 |
| html5lib                   | 60.5 ms                                                                                                         | 67.3 ms: 1.11x slower                                                                                                 |
| unpickle                   | 13.9 us                                                                                                         | 15.5 us: 1.12x slower                                                                                                 |
| async_generators           | 338 ms                                                                                                          | 377 ms: 1.12x slower                                                                                                  |
| tomli_loads                | 1.93 sec                                                                                                        | 2.17 sec: 1.12x slower                                                                                                |
| hexiom                     | 5.69 ms                                                                                                         | 6.39 ms: 1.12x slower                                                                                                 |
| comprehensions             | 15.6 us                                                                                                         | 17.6 us: 1.12x slower                                                                                                 |
| unpickle_pure_python       | 208 us                                                                                                          | 234 us: 1.13x slower                                                                                                  |
| pickle_pure_python         | 303 us                                                                                                          | 342 us: 1.13x slower                                                                                                  |
| sympy_expand               | 468 ms                                                                                                          | 528 ms: 1.13x slower                                                                                                  |
| chaos                      | 55.7 ms                                                                                                         | 63.6 ms: 1.14x slower                                                                                                 |
| nqueens                    | 77.2 ms                                                                                                         | 88.1 ms: 1.14x slower                                                                                                 |
| 2to3                       | 249 ms                                                                                                          | 285 ms: 1.15x slower                                                                                                  |
| thrift                     | 768 us                                                                                                          | 882 us: 1.15x slower                                                                                                  |
| mdp                        | 1.15 sec                                                                                                        | 1.32 sec: 1.15x slower                                                                                                |
| xml_etree_generate         | 83.2 ms                                                                                                         | 95.7 ms: 1.15x slower                                                                                                 |
| go                         | 105 ms                                                                                                          | 121 ms: 1.15x slower                                                                                                  |
| sympy_str                  | 272 ms                                                                                                          | 315 ms: 1.16x slower                                                                                                  |
| subparsers                 | 42.3 ms                                                                                                         | 49.0 ms: 1.16x slower                                                                                                 |
| pyflate                    | 395 ms                                                                                                          | 459 ms: 1.16x slower                                                                                                  |
| sqlglot_v2_optimize        | 49.9 ms                                                                                                         | 57.9 ms: 1.16x slower                                                                                                 |
| scimark_sor                | 107 ms                                                                                                          | 124 ms: 1.16x slower                                                                                                  |
| scimark_fft                | 324 ms                                                                                                          | 377 ms: 1.16x slower                                                                                                  |
| sqlglot_v2_normalize       | 98.9 ms                                                                                                         | 115 ms: 1.17x slower                                                                                                  |
| pprint_safe_repr           | 682 ms                                                                                                          | 796 ms: 1.17x slower                                                                                                  |
| regex_compile              | 123 ms                                                                                                          | 144 ms: 1.17x slower                                                                                                  |
| generators                 | 27.9 ms                                                                                                         | 32.6 ms: 1.17x slower                                                                                                 |
| sympy_sum                  | 153 ms                                                                                                          | 180 ms: 1.17x slower                                                                                                  |
| sympy_integrate            | 18.8 ms                                                                                                         | 22.1 ms: 1.17x slower                                                                                                 |
| django_template            | 34.7 ms                                                                                                         | 40.8 ms: 1.18x slower                                                                                                 |
| pprint_pformat             | 1.40 sec                                                                                                        | 1.64 sec: 1.18x slower                                                                                                |
| deepcopy_reduce            | 2.64 us                                                                                                         | 3.11 us: 1.18x slower                                                                                                 |
| deepcopy                   | 253 us                                                                                                          | 298 us: 1.18x slower                                                                                                  |
| fannkuch                   | 384 ms                                                                                                          | 458 ms: 1.19x slower                                                                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                                                                                        | 1.80 sec: 1.19x slower                                                                                                |
| logging_format             | 6.58 us                                                                                                         | 7.87 us: 1.20x slower                                                                                                 |
| meteor_contest             | 98.8 ms                                                                                                         | 118 ms: 1.20x slower                                                                                                  |
| xml_etree_process          | 57.8 ms                                                                                                         | 69.5 ms: 1.20x slower                                                                                                 |
| genshi_xml                 | 47.8 ms                                                                                                         | 57.5 ms: 1.20x slower                                                                                                 |
| logging_simple             | 5.81 us                                                                                                         | 7.00 us: 1.20x slower                                                                                                 |
| sqlglot_v2_transpile       | 1.52 ms                                                                                                         | 1.83 ms: 1.21x slower                                                                                                 |
| raytrace                   | 251 ms                                                                                                          | 303 ms: 1.21x slower                                                                                                  |
| sqlglot_v2_parse           | 1.21 ms                                                                                                         | 1.47 ms: 1.21x slower                                                                                                 |
| deepcopy_memo              | 29.0 us                                                                                                         | 35.2 us: 1.21x slower                                                                                                 |
| shortest_path              | 440 ms                                                                                                          | 536 ms: 1.22x slower                                                                                                  |
| scimark_lu                 | 107 ms                                                                                                          | 131 ms: 1.22x slower                                                                                                  |
| richards                   | 41.5 ms                                                                                                         | 50.9 ms: 1.23x slower                                                                                                 |
| typing_runtime_protocols   | 154 us                                                                                                          | 190 us: 1.23x slower                                                                                                  |
| scimark_sparse_mat_mult    | 4.58 ms                                                                                                         | 5.66 ms: 1.23x slower                                                                                                 |
| connected_components       | 399 ms                                                                                                          | 492 ms: 1.24x slower                                                                                                  |
| richards_super             | 47.2 ms                                                                                                         | 59.1 ms: 1.25x slower                                                                                                 |
| python_startup             | 12.6 ms                                                                                                         | 15.7 ms: 1.25x slower                                                                                                 |
| spectral_norm              | 92.7 ms                                                                                                         | 117 ms: 1.26x slower                                                                                                  |
| crypto_pyaes               | 68.1 ms                                                                                                         | 86.3 ms: 1.27x slower                                                                                                 |
| scimark_monte_carlo        | 61.6 ms                                                                                                         | 78.3 ms: 1.27x slower                                                                                                 |
| python_startup_no_site     | 7.24 ms                                                                                                         | 9.57 ms: 1.32x slower                                                                                                 |
| genshi_text                | 20.3 ms                                                                                                         | 27.0 ms: 1.33x slower                                                                                                 |
| mako                       | 11.8 ms                                                                                                         | 15.8 ms: 1.34x slower                                                                                                 |
| coverage                   | 81.4 ms                                                                                                         | 111 ms: 1.37x slower                                                                                                  |
| unpack_sequence            | 39.9 ns                                                                                                         | 55.1 ns: 1.38x slower                                                                                                 |
| nbody                      | 89.3 ms                                                                                                         | 123 ms: 1.38x slower                                                                                                  |
| bench_thread_pool          | 1.05 ms                                                                                                         | 3.15 ms: 3.02x slower                                                                                                 |
| Geometric mean             | (ref)                                                                                                           | 1.12x slower                                                                                                          |

Benchmark hidden because not significant (2): pathlib, xml_etree_parse

- Geometric mean (including insignificant results): 1.094x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.20x