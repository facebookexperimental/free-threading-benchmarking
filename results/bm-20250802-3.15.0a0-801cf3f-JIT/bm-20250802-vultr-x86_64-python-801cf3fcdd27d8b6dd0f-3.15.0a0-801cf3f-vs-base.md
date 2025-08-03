# Results vs. base

- fork: python
- ref: 801cf3fcdd27d8b6dd0f
- machine: linux-x86_64
- commit hash: 801cf3f
- commit date: 2025-08-02
- overall geometric mean: 1.004x faster
- HPT reliability: 99.80%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250802-3.15.0a0-801cf3f/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json | results/bm-20250802-3.15.0a0-801cf3f-JIT/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 249 ms                                                                                                          | 255 ms: 1.03x slower                                                                                                |
| docutils       | 2.57 sec                                                                                                        | 2.62 sec: 1.02x slower                                                                                              |
| html5lib       | 60.5 ms                                                                                                         | 63.4 ms: 1.05x slower                                                                                               |
| sphinx         | 972 ms                                                                                                          | 994 ms: 1.02x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.03x slower                                                                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250802-3.15.0a0-801cf3f/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json | results/bm-20250802-3.15.0a0-801cf3f-JIT/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| asyncio_tcp_ssl            | 1.51 sec                                                                                                        | 1.52 sec: 1.00x slower                                                                                              |
| asyncio_tcp                | 498 ms                                                                                                          | 502 ms: 1.01x slower                                                                                                |
| coroutines                 | 23.6 ms                                                                                                         | 24.0 ms: 1.02x slower                                                                                               |
| async_tree_memoization     | 305 ms                                                                                                          | 312 ms: 1.02x slower                                                                                                |
| async_tree_none            | 266 ms                                                                                                          | 272 ms: 1.02x slower                                                                                                |
| async_tree_io              | 603 ms                                                                                                          | 618 ms: 1.03x slower                                                                                                |
| async_tree_io_tg           | 612 ms                                                                                                          | 638 ms: 1.04x slower                                                                                                |
| async_tree_cpu_io_mixed    | 497 ms                                                                                                          | 533 ms: 1.07x slower                                                                                                |
| async_generators           | 338 ms                                                                                                          | 363 ms: 1.07x slower                                                                                                |
| async_tree_cpu_io_mixed_tg | 497 ms                                                                                                          | 534 ms: 1.07x slower                                                                                                |
| Geometric mean             | (ref)                                                                                                           | 1.03x slower                                                                                                        |

Benchmark hidden because not significant (3): async_tree_none_tg, asyncio_websockets, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250802-3.15.0a0-801cf3f/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json | results/bm-20250802-3.15.0a0-801cf3f-JIT/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| float          | 72.5 ms                                                                                                         | 65.0 ms: 1.11x faster                                                                                               |
| nbody          | 89.3 ms                                                                                                         | 86.9 ms: 1.03x faster                                                                                               |
| pidigits       | 213 ms                                                                                                          | 230 ms: 1.08x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.02x faster                                                                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250802-3.15.0a0-801cf3f/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json | results/bm-20250802-3.15.0a0-801cf3f-JIT/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 22.4 ms                                                                                                         | 22.2 ms: 1.01x faster                                                                                               |
| regex_compile  | 123 ms                                                                                                          | 125 ms: 1.01x slower                                                                                                |
| regex_dna      | 180 ms                                                                                                          | 186 ms: 1.03x slower                                                                                                |
| regex_effbot   | 2.78 ms                                                                                                         | 2.88 ms: 1.04x slower                                                                                               |
| Geometric mean | (ref)                                                                                                           | 1.02x slower                                                                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250802-3.15.0a0-801cf3f/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json | results/bm-20250802-3.15.0a0-801cf3f-JIT/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| unpickle_pure_python | 208 us                                                                                                          | 189 us: 1.10x faster                                                                                                |
| tomli_loads          | 1.93 sec                                                                                                        | 1.77 sec: 1.09x faster                                                                                              |
| xml_etree_process    | 57.8 ms                                                                                                         | 54.1 ms: 1.07x faster                                                                                               |
| xml_etree_generate   | 83.2 ms                                                                                                         | 78.3 ms: 1.06x faster                                                                                               |
| json_dumps           | 10.7 ms                                                                                                         | 10.7 ms: 1.00x slower                                                                                               |
| unpickle             | 13.9 us                                                                                                         | 14.0 us: 1.01x slower                                                                                               |
| xml_etree_iterparse  | 92.2 ms                                                                                                         | 93.4 ms: 1.01x slower                                                                                               |
| xml_etree_parse      | 130 ms                                                                                                          | 132 ms: 1.01x slower                                                                                                |
| pickle               | 12.2 us                                                                                                         | 12.6 us: 1.03x slower                                                                                               |
| unpickle_list        | 4.94 us                                                                                                         | 5.11 us: 1.03x slower                                                                                               |
| pickle_list          | 5.06 us                                                                                                         | 5.27 us: 1.04x slower                                                                                               |
| pickle_dict          | 30.8 us                                                                                                         | 33.0 us: 1.07x slower                                                                                               |
| Geometric mean       | (ref)                                                                                                           | 1.01x faster                                                                                                        |

Benchmark hidden because not significant (2): json_loads, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250802-3.15.0a0-801cf3f/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json | results/bm-20250802-3.15.0a0-801cf3f-JIT/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.6 ms                                                                                                         | 12.6 ms: 1.01x slower                                                                                               |
| python_startup_no_site | 7.24 ms                                                                                                         | 7.29 ms: 1.01x slower                                                                                               |
| Geometric mean         | (ref)                                                                                                           | 1.01x slower                                                                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark      | results/bm-20250802-3.15.0a0-801cf3f/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json | results/bm-20250802-3.15.0a0-801cf3f-JIT/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| mako           | 11.8 ms                                                                                                         | 10.7 ms: 1.09x faster                                                                                               |
| genshi_text    | 20.3 ms                                                                                                         | 20.4 ms: 1.01x slower                                                                                               |
| genshi_xml     | 47.8 ms                                                                                                         | 49.6 ms: 1.04x slower                                                                                               |
| Geometric mean | (ref)                                                                                                           | 1.01x faster                                                                                                        |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | results/bm-20250802-3.15.0a0-801cf3f/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json | results/bm-20250802-3.15.0a0-801cf3f-JIT/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| richards                   | 41.5 ms                                                                                                         | 29.7 ms: 1.40x faster                                                                                               |
| richards_super             | 47.2 ms                                                                                                         | 34.3 ms: 1.38x faster                                                                                               |
| deltablue                  | 3.28 ms                                                                                                         | 2.83 ms: 1.16x faster                                                                                               |
| scimark_fft                | 324 ms                                                                                                          | 282 ms: 1.15x faster                                                                                                |
| float                      | 72.5 ms                                                                                                         | 65.0 ms: 1.11x faster                                                                                               |
| unpickle_pure_python       | 208 us                                                                                                          | 189 us: 1.10x faster                                                                                                |
| mako                       | 11.8 ms                                                                                                         | 10.7 ms: 1.09x faster                                                                                               |
| tomli_loads                | 1.93 sec                                                                                                        | 1.77 sec: 1.09x faster                                                                                              |
| spectral_norm              | 92.7 ms                                                                                                         | 84.9 ms: 1.09x faster                                                                                               |
| xml_etree_process          | 57.8 ms                                                                                                         | 54.1 ms: 1.07x faster                                                                                               |
| xml_etree_generate         | 83.2 ms                                                                                                         | 78.3 ms: 1.06x faster                                                                                               |
| bpe_tokeniser              | 4.16 sec                                                                                                        | 3.97 sec: 1.05x faster                                                                                              |
| fannkuch                   | 384 ms                                                                                                          | 367 ms: 1.05x faster                                                                                                |
| scimark_monte_carlo        | 61.6 ms                                                                                                         | 59.9 ms: 1.03x faster                                                                                               |
| nbody                      | 89.3 ms                                                                                                         | 86.9 ms: 1.03x faster                                                                                               |
| connected_components       | 399 ms                                                                                                          | 390 ms: 1.02x faster                                                                                                |
| pyflate                    | 395 ms                                                                                                          | 389 ms: 1.01x faster                                                                                                |
| sqlite_synth               | 2.26 us                                                                                                         | 2.23 us: 1.01x faster                                                                                               |
| telco                      | 158 ms                                                                                                          | 156 ms: 1.01x faster                                                                                                |
| regex_v8                   | 22.4 ms                                                                                                         | 22.2 ms: 1.01x faster                                                                                               |
| shortest_path              | 440 ms                                                                                                          | 436 ms: 1.01x faster                                                                                                |
| meteor_contest             | 98.8 ms                                                                                                         | 98.1 ms: 1.01x faster                                                                                               |
| json_dumps                 | 10.7 ms                                                                                                         | 10.7 ms: 1.00x slower                                                                                               |
| asyncio_tcp_ssl            | 1.51 sec                                                                                                        | 1.52 sec: 1.00x slower                                                                                              |
| coverage                   | 81.4 ms                                                                                                         | 81.8 ms: 1.01x slower                                                                                               |
| python_startup             | 12.6 ms                                                                                                         | 12.6 ms: 1.01x slower                                                                                               |
| sqlglot_v2_transpile       | 1.52 ms                                                                                                         | 1.53 ms: 1.01x slower                                                                                               |
| sqlglot_v2_parse           | 1.21 ms                                                                                                         | 1.22 ms: 1.01x slower                                                                                               |
| genshi_text                | 20.3 ms                                                                                                         | 20.4 ms: 1.01x slower                                                                                               |
| sqlglot_v2_normalize       | 98.9 ms                                                                                                         | 99.5 ms: 1.01x slower                                                                                               |
| python_startup_no_site     | 7.24 ms                                                                                                         | 7.29 ms: 1.01x slower                                                                                               |
| bench_thread_pool          | 1.05 ms                                                                                                         | 1.05 ms: 1.01x slower                                                                                               |
| unpickle                   | 13.9 us                                                                                                         | 14.0 us: 1.01x slower                                                                                               |
| sympy_expand               | 468 ms                                                                                                          | 473 ms: 1.01x slower                                                                                                |
| asyncio_tcp                | 498 ms                                                                                                          | 502 ms: 1.01x slower                                                                                                |
| pprint_pformat             | 1.40 sec                                                                                                        | 1.41 sec: 1.01x slower                                                                                              |
| deepcopy                   | 253 us                                                                                                          | 256 us: 1.01x slower                                                                                                |
| deepcopy_memo              | 29.0 us                                                                                                         | 29.3 us: 1.01x slower                                                                                               |
| regex_compile              | 123 ms                                                                                                          | 125 ms: 1.01x slower                                                                                                |
| scimark_sparse_mat_mult    | 4.58 ms                                                                                                         | 4.64 ms: 1.01x slower                                                                                               |
| sqlglot_v2_optimize        | 49.9 ms                                                                                                         | 50.5 ms: 1.01x slower                                                                                               |
| sympy_sum                  | 153 ms                                                                                                          | 156 ms: 1.01x slower                                                                                                |
| sympy_str                  | 272 ms                                                                                                          | 275 ms: 1.01x slower                                                                                                |
| xml_etree_iterparse        | 92.2 ms                                                                                                         | 93.4 ms: 1.01x slower                                                                                               |
| mdp                        | 1.15 sec                                                                                                        | 1.16 sec: 1.01x slower                                                                                              |
| xml_etree_parse            | 130 ms                                                                                                          | 132 ms: 1.01x slower                                                                                                |
| pprint_safe_repr           | 682 ms                                                                                                          | 692 ms: 1.02x slower                                                                                                |
| docutils                   | 2.57 sec                                                                                                        | 2.62 sec: 1.02x slower                                                                                              |
| coroutines                 | 23.6 ms                                                                                                         | 24.0 ms: 1.02x slower                                                                                               |
| nqueens                    | 77.2 ms                                                                                                         | 78.6 ms: 1.02x slower                                                                                               |
| raytrace                   | 251 ms                                                                                                          | 256 ms: 1.02x slower                                                                                                |
| typing_runtime_protocols   | 154 us                                                                                                          | 157 us: 1.02x slower                                                                                                |
| chaos                      | 55.7 ms                                                                                                         | 56.9 ms: 1.02x slower                                                                                               |
| scimark_lu                 | 107 ms                                                                                                          | 110 ms: 1.02x slower                                                                                                |
| async_tree_memoization     | 305 ms                                                                                                          | 312 ms: 1.02x slower                                                                                                |
| pathlib                    | 19.1 ms                                                                                                         | 19.5 ms: 1.02x slower                                                                                               |
| sphinx                     | 972 ms                                                                                                          | 994 ms: 1.02x slower                                                                                                |
| async_tree_none            | 266 ms                                                                                                          | 272 ms: 1.02x slower                                                                                                |
| dulwich_log                | 66.1 ms                                                                                                         | 67.7 ms: 1.02x slower                                                                                               |
| sympy_integrate            | 18.8 ms                                                                                                         | 19.3 ms: 1.03x slower                                                                                               |
| async_tree_io              | 603 ms                                                                                                          | 618 ms: 1.03x slower                                                                                                |
| 2to3                       | 249 ms                                                                                                          | 255 ms: 1.03x slower                                                                                                |
| many_optionals             | 1.21 ms                                                                                                         | 1.25 ms: 1.03x slower                                                                                               |
| pickle                     | 12.2 us                                                                                                         | 12.6 us: 1.03x slower                                                                                               |
| regex_dna                  | 180 ms                                                                                                          | 186 ms: 1.03x slower                                                                                                |
| hexiom                     | 5.69 ms                                                                                                         | 5.87 ms: 1.03x slower                                                                                               |
| logging_silent             | 96.6 ns                                                                                                         | 100.0 ns: 1.03x slower                                                                                              |
| unpickle_list              | 4.94 us                                                                                                         | 5.11 us: 1.03x slower                                                                                               |
| scimark_sor                | 107 ms                                                                                                          | 110 ms: 1.04x slower                                                                                                |
| regex_effbot               | 2.78 ms                                                                                                         | 2.88 ms: 1.04x slower                                                                                               |
| subparsers                 | 42.3 ms                                                                                                         | 43.8 ms: 1.04x slower                                                                                               |
| genshi_xml                 | 47.8 ms                                                                                                         | 49.6 ms: 1.04x slower                                                                                               |
| deepcopy_reduce            | 2.64 us                                                                                                         | 2.74 us: 1.04x slower                                                                                               |
| logging_format             | 6.58 us                                                                                                         | 6.85 us: 1.04x slower                                                                                               |
| async_tree_io_tg           | 612 ms                                                                                                          | 638 ms: 1.04x slower                                                                                                |
| pickle_list                | 5.06 us                                                                                                         | 5.27 us: 1.04x slower                                                                                               |
| generators                 | 27.9 ms                                                                                                         | 29.2 ms: 1.04x slower                                                                                               |
| comprehensions             | 15.6 us                                                                                                         | 16.3 us: 1.05x slower                                                                                               |
| html5lib                   | 60.5 ms                                                                                                         | 63.4 ms: 1.05x slower                                                                                               |
| logging_simple             | 5.81 us                                                                                                         | 6.11 us: 1.05x slower                                                                                               |
| pycparser                  | 1.09 sec                                                                                                        | 1.15 sec: 1.05x slower                                                                                              |
| go                         | 105 ms                                                                                                          | 111 ms: 1.06x slower                                                                                                |
| pickle_dict                | 30.8 us                                                                                                         | 33.0 us: 1.07x slower                                                                                               |
| async_tree_cpu_io_mixed    | 497 ms                                                                                                          | 533 ms: 1.07x slower                                                                                                |
| async_generators           | 338 ms                                                                                                          | 363 ms: 1.07x slower                                                                                                |
| async_tree_cpu_io_mixed_tg | 497 ms                                                                                                          | 534 ms: 1.07x slower                                                                                                |
| pidigits                   | 213 ms                                                                                                          | 230 ms: 1.08x slower                                                                                                |
| gc_traversal               | 4.36 ms                                                                                                         | 4.73 ms: 1.09x slower                                                                                               |
| unpack_sequence            | 39.9 ns                                                                                                         | 48.3 ns: 1.21x slower                                                                                               |
| Geometric mean             | (ref)                                                                                                           | 1.00x slower                                                                                                        |

Benchmark hidden because not significant (13): k_core, json, async_tree_none_tg, thrift, create_gc_cycles, crypto_pyaes, asyncio_websockets, django_template, json_loads, pickle_pure_python, bench_mp_pool, async_tree_memoization_tg, pylint

- Geometric mean (including insignificant results): 1.004x faster

# HPT report

- Reliability score: 99.80% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x