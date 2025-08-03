# Results vs. base

- fork: python
- ref: 801cf3fcdd27d8b6dd0f
- machine: linux-x86_64
- commit hash: 801cf3f
- commit date: 2025-08-02
- overall geometric mean: 1.040x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250802-3.15.0a0-801cf3f/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json | results/bm-20250802-3.15.0a0-801cf3f-CLANG/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 249 ms                                                                                                          | 246 ms: 1.01x faster                                                                                                  |
| docutils       | 2.57 sec                                                                                                        | 2.51 sec: 1.02x faster                                                                                                |
| html5lib       | 60.5 ms                                                                                                         | 57.9 ms: 1.05x faster                                                                                                 |
| sphinx         | 972 ms                                                                                                          | 959 ms: 1.01x faster                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.02x faster                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250802-3.15.0a0-801cf3f/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json | results/bm-20250802-3.15.0a0-801cf3f-CLANG/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| coroutines                 | 23.6 ms                                                                                                         | 21.6 ms: 1.09x faster                                                                                                 |
| async_tree_cpu_io_mixed    | 497 ms                                                                                                          | 470 ms: 1.06x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 497 ms                                                                                                          | 471 ms: 1.06x faster                                                                                                  |
| async_generators           | 338 ms                                                                                                          | 322 ms: 1.05x faster                                                                                                  |
| async_tree_memoization     | 305 ms                                                                                                          | 296 ms: 1.03x faster                                                                                                  |
| async_tree_io              | 603 ms                                                                                                          | 587 ms: 1.03x faster                                                                                                  |
| async_tree_memoization_tg  | 311 ms                                                                                                          | 304 ms: 1.02x faster                                                                                                  |
| async_tree_none            | 266 ms                                                                                                          | 260 ms: 1.02x faster                                                                                                  |
| async_tree_none_tg         | 257 ms                                                                                                          | 252 ms: 1.02x faster                                                                                                  |
| asyncio_tcp                | 498 ms                                                                                                          | 492 ms: 1.01x faster                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.03x faster                                                                                                          |

Benchmark hidden because not significant (3): async_tree_io_tg, asyncio_tcp_ssl, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250802-3.15.0a0-801cf3f/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json | results/bm-20250802-3.15.0a0-801cf3f-CLANG/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| nbody          | 89.3 ms                                                                                                         | 78.6 ms: 1.14x faster                                                                                                 |
| pidigits       | 213 ms                                                                                                          | 194 ms: 1.10x faster                                                                                                  |
| float          | 72.5 ms                                                                                                         | 66.4 ms: 1.09x faster                                                                                                 |
| Geometric mean | (ref)                                                                                                           | 1.11x faster                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250802-3.15.0a0-801cf3f/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json | results/bm-20250802-3.15.0a0-801cf3f-CLANG/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 22.4 ms                                                                                                         | 21.5 ms: 1.04x faster                                                                                                 |
| regex_compile  | 123 ms                                                                                                          | 119 ms: 1.03x faster                                                                                                  |
| regex_dna      | 180 ms                                                                                                          | 188 ms: 1.04x slower                                                                                                  |
| regex_effbot   | 2.78 ms                                                                                                         | 3.11 ms: 1.12x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                           | 1.02x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250802-3.15.0a0-801cf3f/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json | results/bm-20250802-3.15.0a0-801cf3f-CLANG/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| unpickle_list        | 4.94 us                                                                                                         | 4.33 us: 1.14x faster                                                                                                 |
| json_loads           | 28.9 us                                                                                                         | 25.5 us: 1.13x faster                                                                                                 |
| tomli_loads          | 1.93 sec                                                                                                        | 1.79 sec: 1.08x faster                                                                                                |
| xml_etree_generate   | 83.2 ms                                                                                                         | 79.9 ms: 1.04x faster                                                                                                 |
| xml_etree_process    | 57.8 ms                                                                                                         | 55.6 ms: 1.04x faster                                                                                                 |
| unpickle_pure_python | 208 us                                                                                                          | 200 us: 1.04x faster                                                                                                  |
| pickle_pure_python   | 303 us                                                                                                          | 296 us: 1.02x faster                                                                                                  |
| pickle_list          | 5.06 us                                                                                                         | 5.02 us: 1.01x faster                                                                                                 |
| json_dumps           | 10.7 ms                                                                                                         | 10.8 ms: 1.00x slower                                                                                                 |
| xml_etree_iterparse  | 92.2 ms                                                                                                         | 94.8 ms: 1.03x slower                                                                                                 |
| pickle_dict          | 30.8 us                                                                                                         | 32.3 us: 1.05x slower                                                                                                 |
| unpickle             | 13.9 us                                                                                                         | 14.7 us: 1.06x slower                                                                                                 |
| pickle               | 12.2 us                                                                                                         | 13.0 us: 1.06x slower                                                                                                 |
| xml_etree_parse      | 130 ms                                                                                                          | 145 ms: 1.12x slower                                                                                                  |
| Geometric mean       | (ref)                                                                                                           | 1.01x faster                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250802-3.15.0a0-801cf3f/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json | results/bm-20250802-3.15.0a0-801cf3f-CLANG/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.6 ms                                                                                                         | 12.7 ms: 1.01x slower                                                                                                 |
| python_startup_no_site | 7.24 ms                                                                                                         | 7.35 ms: 1.01x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.01x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250802-3.15.0a0-801cf3f/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json | results/bm-20250802-3.15.0a0-801cf3f-CLANG/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 34.7 ms                                                                                                         | 32.6 ms: 1.06x faster                                                                                                 |
| genshi_text     | 20.3 ms                                                                                                         | 19.4 ms: 1.05x faster                                                                                                 |
| mako            | 11.8 ms                                                                                                         | 11.4 ms: 1.04x faster                                                                                                 |
| genshi_xml      | 47.8 ms                                                                                                         | 46.5 ms: 1.03x faster                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.04x faster                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20250802-3.15.0a0-801cf3f/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json | results/bm-20250802-3.15.0a0-801cf3f-CLANG/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| logging_silent             | 96.6 ns                                                                                                         | 82.2 ns: 1.17x faster                                                                                                 |
| spectral_norm              | 92.7 ms                                                                                                         | 80.5 ms: 1.15x faster                                                                                                 |
| scimark_sparse_mat_mult    | 4.58 ms                                                                                                         | 3.98 ms: 1.15x faster                                                                                                 |
| scimark_fft                | 324 ms                                                                                                          | 283 ms: 1.15x faster                                                                                                  |
| unpickle_list              | 4.94 us                                                                                                         | 4.33 us: 1.14x faster                                                                                                 |
| nbody                      | 89.3 ms                                                                                                         | 78.6 ms: 1.14x faster                                                                                                 |
| json_loads                 | 28.9 us                                                                                                         | 25.5 us: 1.13x faster                                                                                                 |
| chaos                      | 55.7 ms                                                                                                         | 49.4 ms: 1.13x faster                                                                                                 |
| deepcopy                   | 253 us                                                                                                          | 226 us: 1.12x faster                                                                                                  |
| deltablue                  | 3.28 ms                                                                                                         | 2.97 ms: 1.10x faster                                                                                                 |
| pidigits                   | 213 ms                                                                                                          | 194 ms: 1.10x faster                                                                                                  |
| scimark_monte_carlo        | 61.6 ms                                                                                                         | 56.1 ms: 1.10x faster                                                                                                 |
| deepcopy_memo              | 29.0 us                                                                                                         | 26.5 us: 1.09x faster                                                                                                 |
| coverage                   | 81.4 ms                                                                                                         | 74.5 ms: 1.09x faster                                                                                                 |
| coroutines                 | 23.6 ms                                                                                                         | 21.6 ms: 1.09x faster                                                                                                 |
| richards                   | 41.5 ms                                                                                                         | 38.0 ms: 1.09x faster                                                                                                 |
| float                      | 72.5 ms                                                                                                         | 66.4 ms: 1.09x faster                                                                                                 |
| deepcopy_reduce            | 2.64 us                                                                                                         | 2.42 us: 1.09x faster                                                                                                 |
| tomli_loads                | 1.93 sec                                                                                                        | 1.79 sec: 1.08x faster                                                                                                |
| raytrace                   | 251 ms                                                                                                          | 233 ms: 1.08x faster                                                                                                  |
| sympy_expand               | 468 ms                                                                                                          | 435 ms: 1.08x faster                                                                                                  |
| richards_super             | 47.2 ms                                                                                                         | 43.9 ms: 1.08x faster                                                                                                 |
| scimark_lu                 | 107 ms                                                                                                          | 100 ms: 1.07x faster                                                                                                  |
| typing_runtime_protocols   | 154 us                                                                                                          | 144 us: 1.07x faster                                                                                                  |
| hexiom                     | 5.69 ms                                                                                                         | 5.31 ms: 1.07x faster                                                                                                 |
| comprehensions             | 15.6 us                                                                                                         | 14.6 us: 1.07x faster                                                                                                 |
| sqlglot_v2_transpile       | 1.52 ms                                                                                                         | 1.42 ms: 1.07x faster                                                                                                 |
| nqueens                    | 77.2 ms                                                                                                         | 72.4 ms: 1.07x faster                                                                                                 |
| scimark_sor                | 107 ms                                                                                                          | 100 ms: 1.06x faster                                                                                                  |
| django_template            | 34.7 ms                                                                                                         | 32.6 ms: 1.06x faster                                                                                                 |
| sqlglot_v2_parse           | 1.21 ms                                                                                                         | 1.14 ms: 1.06x faster                                                                                                 |
| thrift                     | 768 us                                                                                                          | 725 us: 1.06x faster                                                                                                  |
| fannkuch                   | 384 ms                                                                                                          | 362 ms: 1.06x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 497 ms                                                                                                          | 470 ms: 1.06x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 497 ms                                                                                                          | 471 ms: 1.06x faster                                                                                                  |
| json                       | 5.22 ms                                                                                                         | 4.96 ms: 1.05x faster                                                                                                 |
| async_generators           | 338 ms                                                                                                          | 322 ms: 1.05x faster                                                                                                  |
| genshi_text                | 20.3 ms                                                                                                         | 19.4 ms: 1.05x faster                                                                                                 |
| sympy_integrate            | 18.8 ms                                                                                                         | 17.9 ms: 1.05x faster                                                                                                 |
| html5lib                   | 60.5 ms                                                                                                         | 57.9 ms: 1.05x faster                                                                                                 |
| sympy_str                  | 272 ms                                                                                                          | 260 ms: 1.04x faster                                                                                                  |
| go                         | 105 ms                                                                                                          | 100 ms: 1.04x faster                                                                                                  |
| sqlglot_v2_optimize        | 49.9 ms                                                                                                         | 47.8 ms: 1.04x faster                                                                                                 |
| pathlib                    | 19.1 ms                                                                                                         | 18.3 ms: 1.04x faster                                                                                                 |
| xml_etree_generate         | 83.2 ms                                                                                                         | 79.9 ms: 1.04x faster                                                                                                 |
| sympy_sum                  | 153 ms                                                                                                          | 147 ms: 1.04x faster                                                                                                  |
| regex_v8                   | 22.4 ms                                                                                                         | 21.5 ms: 1.04x faster                                                                                                 |
| mdp                        | 1.15 sec                                                                                                        | 1.10 sec: 1.04x faster                                                                                                |
| xml_etree_process          | 57.8 ms                                                                                                         | 55.6 ms: 1.04x faster                                                                                                 |
| unpickle_pure_python       | 208 us                                                                                                          | 200 us: 1.04x faster                                                                                                  |
| bench_thread_pool          | 1.05 ms                                                                                                         | 1.01 ms: 1.04x faster                                                                                                 |
| sqlglot_v2_normalize       | 98.9 ms                                                                                                         | 95.4 ms: 1.04x faster                                                                                                 |
| mako                       | 11.8 ms                                                                                                         | 11.4 ms: 1.04x faster                                                                                                 |
| generators                 | 27.9 ms                                                                                                         | 27.0 ms: 1.03x faster                                                                                                 |
| regex_compile              | 123 ms                                                                                                          | 119 ms: 1.03x faster                                                                                                  |
| pylint                     | 279 ms                                                                                                          | 271 ms: 1.03x faster                                                                                                  |
| bpe_tokeniser              | 4.16 sec                                                                                                        | 4.04 sec: 1.03x faster                                                                                                |
| crypto_pyaes               | 68.1 ms                                                                                                         | 66.2 ms: 1.03x faster                                                                                                 |
| async_tree_memoization     | 305 ms                                                                                                          | 296 ms: 1.03x faster                                                                                                  |
| async_tree_io              | 603 ms                                                                                                          | 587 ms: 1.03x faster                                                                                                  |
| genshi_xml                 | 47.8 ms                                                                                                         | 46.5 ms: 1.03x faster                                                                                                 |
| sqlite_synth               | 2.26 us                                                                                                         | 2.20 us: 1.03x faster                                                                                                 |
| pickle_pure_python         | 303 us                                                                                                          | 296 us: 1.02x faster                                                                                                  |
| docutils                   | 2.57 sec                                                                                                        | 2.51 sec: 1.02x faster                                                                                                |
| telco                      | 158 ms                                                                                                          | 155 ms: 1.02x faster                                                                                                  |
| async_tree_memoization_tg  | 311 ms                                                                                                          | 304 ms: 1.02x faster                                                                                                  |
| async_tree_none            | 266 ms                                                                                                          | 260 ms: 1.02x faster                                                                                                  |
| async_tree_none_tg         | 257 ms                                                                                                          | 252 ms: 1.02x faster                                                                                                  |
| pycparser                  | 1.09 sec                                                                                                        | 1.08 sec: 1.02x faster                                                                                                |
| k_core                     | 2.03 sec                                                                                                        | 2.00 sec: 1.01x faster                                                                                                |
| sphinx                     | 972 ms                                                                                                          | 959 ms: 1.01x faster                                                                                                  |
| 2to3                       | 249 ms                                                                                                          | 246 ms: 1.01x faster                                                                                                  |
| asyncio_tcp                | 498 ms                                                                                                          | 492 ms: 1.01x faster                                                                                                  |
| many_optionals             | 1.21 ms                                                                                                         | 1.20 ms: 1.01x faster                                                                                                 |
| logging_format             | 6.58 us                                                                                                         | 6.52 us: 1.01x faster                                                                                                 |
| pickle_list                | 5.06 us                                                                                                         | 5.02 us: 1.01x faster                                                                                                 |
| pyflate                    | 395 ms                                                                                                          | 394 ms: 1.00x faster                                                                                                  |
| json_dumps                 | 10.7 ms                                                                                                         | 10.8 ms: 1.00x slower                                                                                                 |
| dulwich_log                | 66.1 ms                                                                                                         | 66.5 ms: 1.01x slower                                                                                                 |
| python_startup             | 12.6 ms                                                                                                         | 12.7 ms: 1.01x slower                                                                                                 |
| pprint_pformat             | 1.40 sec                                                                                                        | 1.41 sec: 1.01x slower                                                                                                |
| python_startup_no_site     | 7.24 ms                                                                                                         | 7.35 ms: 1.01x slower                                                                                                 |
| subparsers                 | 42.3 ms                                                                                                         | 43.0 ms: 1.02x slower                                                                                                 |
| pprint_safe_repr           | 682 ms                                                                                                          | 700 ms: 1.03x slower                                                                                                  |
| xml_etree_iterparse        | 92.2 ms                                                                                                         | 94.8 ms: 1.03x slower                                                                                                 |
| meteor_contest             | 98.8 ms                                                                                                         | 102 ms: 1.03x slower                                                                                                  |
| gc_traversal               | 4.36 ms                                                                                                         | 4.51 ms: 1.03x slower                                                                                                 |
| create_gc_cycles           | 1.96 ms                                                                                                         | 2.04 ms: 1.04x slower                                                                                                 |
| regex_dna                  | 180 ms                                                                                                          | 188 ms: 1.04x slower                                                                                                  |
| pickle_dict                | 30.8 us                                                                                                         | 32.3 us: 1.05x slower                                                                                                 |
| unpickle                   | 13.9 us                                                                                                         | 14.7 us: 1.06x slower                                                                                                 |
| pickle                     | 12.2 us                                                                                                         | 13.0 us: 1.06x slower                                                                                                 |
| xml_etree_parse            | 130 ms                                                                                                          | 145 ms: 1.12x slower                                                                                                  |
| regex_effbot               | 2.78 ms                                                                                                         | 3.11 ms: 1.12x slower                                                                                                 |
| unpack_sequence            | 39.9 ns                                                                                                         | 47.0 ns: 1.18x slower                                                                                                 |
| Geometric mean             | (ref)                                                                                                           | 1.04x faster                                                                                                          |

Benchmark hidden because not significant (7): async_tree_io_tg, logging_simple, asyncio_tcp_ssl, asyncio_websockets, shortest_path, connected_components, bench_mp_pool

- Geometric mean (including insignificant results): 1.040x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.03x