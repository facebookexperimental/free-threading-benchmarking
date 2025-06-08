# Results vs. base

- fork: python
- ref: 8fdbbf8b18f1405abe67
- machine: linux-x86_64
- commit hash: 8fdbbf8
- commit date: 2025-06-07
- overall geometric mean: 1.048x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.05x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250607-3.15.0a0-8fdbbf8/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json | results/bm-20250607-3.15.0a0-8fdbbf8-CLANG/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 250 ms                                                                                                          | 242 ms: 1.03x faster                                                                                                  |
| docutils       | 2.54 sec                                                                                                        | 2.50 sec: 1.01x faster                                                                                                |
| html5lib       | 61.1 ms                                                                                                         | 59.9 ms: 1.02x faster                                                                                                 |
| sphinx         | 976 ms                                                                                                          | 961 ms: 1.02x faster                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.02x faster                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250607-3.15.0a0-8fdbbf8/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json | results/bm-20250607-3.15.0a0-8fdbbf8-CLANG/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_generators           | 340 ms                                                                                                          | 315 ms: 1.08x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 521 ms                                                                                                          | 484 ms: 1.08x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 514 ms                                                                                                          | 479 ms: 1.07x faster                                                                                                  |
| coroutines                 | 23.1 ms                                                                                                         | 21.6 ms: 1.07x faster                                                                                                 |
| async_tree_io_tg           | 623 ms                                                                                                          | 598 ms: 1.04x faster                                                                                                  |
| async_tree_none            | 270 ms                                                                                                          | 260 ms: 1.04x faster                                                                                                  |
| async_tree_none_tg         | 251 ms                                                                                                          | 244 ms: 1.03x faster                                                                                                  |
| async_tree_io              | 593 ms                                                                                                          | 577 ms: 1.03x faster                                                                                                  |
| async_tree_memoization     | 307 ms                                                                                                          | 300 ms: 1.02x faster                                                                                                  |
| async_tree_memoization_tg  | 306 ms                                                                                                          | 302 ms: 1.01x faster                                                                                                  |
| asyncio_tcp                | 500 ms                                                                                                          | 496 ms: 1.01x faster                                                                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                                                                                        | 1.51 sec: 1.01x faster                                                                                                |
| Geometric mean             | (ref)                                                                                                           | 1.04x faster                                                                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250607-3.15.0a0-8fdbbf8/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json | results/bm-20250607-3.15.0a0-8fdbbf8-CLANG/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| float          | 71.8 ms                                                                                                         | 66.1 ms: 1.09x faster                                                                                                 |
| nbody          | 87.5 ms                                                                                                         | 80.7 ms: 1.08x faster                                                                                                 |
| pidigits       | 197 ms                                                                                                          | 192 ms: 1.03x faster                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.06x faster                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250607-3.15.0a0-8fdbbf8/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json | results/bm-20250607-3.15.0a0-8fdbbf8-CLANG/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_compile  | 124 ms                                                                                                          | 117 ms: 1.05x faster                                                                                                  |
| regex_v8       | 23.0 ms                                                                                                         | 22.6 ms: 1.02x faster                                                                                                 |
| regex_effbot   | 2.88 ms                                                                                                         | 3.12 ms: 1.08x slower                                                                                                 |
| regex_dna      | 176 ms                                                                                                          | 195 ms: 1.11x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.03x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250607-3.15.0a0-8fdbbf8/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json | results/bm-20250607-3.15.0a0-8fdbbf8-CLANG/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| json_loads           | 29.1 us                                                                                                         | 25.1 us: 1.16x faster                                                                                                 |
| unpickle_list        | 5.00 us                                                                                                         | 4.39 us: 1.14x faster                                                                                                 |
| tomli_loads          | 1.95 sec                                                                                                        | 1.79 sec: 1.09x faster                                                                                                |
| unpickle_pure_python | 208 us                                                                                                          | 195 us: 1.07x faster                                                                                                  |
| pickle_pure_python   | 307 us                                                                                                          | 296 us: 1.04x faster                                                                                                  |
| unpickle             | 13.8 us                                                                                                         | 13.3 us: 1.04x faster                                                                                                 |
| pickle_list          | 5.14 us                                                                                                         | 4.96 us: 1.04x faster                                                                                                 |
| xml_etree_process    | 58.5 ms                                                                                                         | 56.6 ms: 1.03x faster                                                                                                 |
| xml_etree_generate   | 83.3 ms                                                                                                         | 80.8 ms: 1.03x faster                                                                                                 |
| pickle_dict          | 32.4 us                                                                                                         | 31.6 us: 1.03x faster                                                                                                 |
| json_dumps           | 10.9 ms                                                                                                         | 10.8 ms: 1.01x faster                                                                                                 |
| xml_etree_iterparse  | 92.4 ms                                                                                                         | 94.8 ms: 1.03x slower                                                                                                 |
| pickle               | 12.2 us                                                                                                         | 12.6 us: 1.03x slower                                                                                                 |
| xml_etree_parse      | 133 ms                                                                                                          | 146 ms: 1.10x slower                                                                                                  |
| Geometric mean       | (ref)                                                                                                           | 1.04x faster                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250607-3.15.0a0-8fdbbf8/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json | results/bm-20250607-3.15.0a0-8fdbbf8-CLANG/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.6 ms                                                                                                         | 12.6 ms: 1.00x faster                                                                                                 |
| python_startup_no_site | 7.33 ms                                                                                                         | 7.39 ms: 1.01x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.00x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250607-3.15.0a0-8fdbbf8/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json | results/bm-20250607-3.15.0a0-8fdbbf8-CLANG/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 34.8 ms                                                                                                         | 32.7 ms: 1.06x faster                                                                                                 |
| genshi_xml      | 48.4 ms                                                                                                         | 46.1 ms: 1.05x faster                                                                                                 |
| genshi_text     | 20.5 ms                                                                                                         | 19.8 ms: 1.04x faster                                                                                                 |
| mako            | 11.8 ms                                                                                                         | 11.5 ms: 1.03x faster                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.04x faster                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20250607-3.15.0a0-8fdbbf8/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json | results/bm-20250607-3.15.0a0-8fdbbf8-CLANG/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| scimark_fft                | 340 ms                                                                                                          | 268 ms: 1.27x faster                                                                                                  |
| scimark_sparse_mat_mult    | 4.83 ms                                                                                                         | 3.89 ms: 1.24x faster                                                                                                 |
| spectral_norm              | 101 ms                                                                                                          | 83.1 ms: 1.22x faster                                                                                                 |
| chaos                      | 57.0 ms                                                                                                         | 49.0 ms: 1.16x faster                                                                                                 |
| json_loads                 | 29.1 us                                                                                                         | 25.1 us: 1.16x faster                                                                                                 |
| unpickle_list              | 5.00 us                                                                                                         | 4.39 us: 1.14x faster                                                                                                 |
| scimark_monte_carlo        | 62.0 ms                                                                                                         | 54.4 ms: 1.14x faster                                                                                                 |
| deltablue                  | 3.23 ms                                                                                                         | 2.85 ms: 1.13x faster                                                                                                 |
| comprehensions             | 15.7 us                                                                                                         | 14.0 us: 1.12x faster                                                                                                 |
| richards                   | 41.1 ms                                                                                                         | 36.5 ms: 1.12x faster                                                                                                 |
| scimark_lu                 | 110 ms                                                                                                          | 97.8 ms: 1.12x faster                                                                                                 |
| deepcopy_reduce            | 2.67 us                                                                                                         | 2.39 us: 1.12x faster                                                                                                 |
| deepcopy_memo              | 28.9 us                                                                                                         | 25.9 us: 1.12x faster                                                                                                 |
| scimark_sor                | 111 ms                                                                                                          | 99.9 ms: 1.11x faster                                                                                                 |
| deepcopy                   | 252 us                                                                                                          | 228 us: 1.11x faster                                                                                                  |
| richards_super             | 46.3 ms                                                                                                         | 42.0 ms: 1.10x faster                                                                                                 |
| go                         | 105 ms                                                                                                          | 95.9 ms: 1.10x faster                                                                                                 |
| raytrace                   | 253 ms                                                                                                          | 231 ms: 1.10x faster                                                                                                  |
| typing_runtime_protocols   | 153 us                                                                                                          | 140 us: 1.09x faster                                                                                                  |
| tomli_loads                | 1.95 sec                                                                                                        | 1.79 sec: 1.09x faster                                                                                                |
| coverage                   | 82.8 ms                                                                                                         | 76.0 ms: 1.09x faster                                                                                                 |
| float                      | 71.8 ms                                                                                                         | 66.1 ms: 1.09x faster                                                                                                 |
| nbody                      | 87.5 ms                                                                                                         | 80.7 ms: 1.08x faster                                                                                                 |
| async_generators           | 340 ms                                                                                                          | 315 ms: 1.08x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 521 ms                                                                                                          | 484 ms: 1.08x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 514 ms                                                                                                          | 479 ms: 1.07x faster                                                                                                  |
| json                       | 5.26 ms                                                                                                         | 4.91 ms: 1.07x faster                                                                                                 |
| coroutines                 | 23.1 ms                                                                                                         | 21.6 ms: 1.07x faster                                                                                                 |
| mdp                        | 1.15 sec                                                                                                        | 1.08 sec: 1.07x faster                                                                                                |
| unpickle_pure_python       | 208 us                                                                                                          | 195 us: 1.07x faster                                                                                                  |
| django_template            | 34.8 ms                                                                                                         | 32.7 ms: 1.06x faster                                                                                                 |
| hexiom                     | 5.46 ms                                                                                                         | 5.15 ms: 1.06x faster                                                                                                 |
| pycparser                  | 1.13 sec                                                                                                        | 1.07 sec: 1.06x faster                                                                                                |
| logging_simple             | 6.53 us                                                                                                         | 6.18 us: 1.06x faster                                                                                                 |
| sqlglot_v2_parse           | 1.20 ms                                                                                                         | 1.14 ms: 1.05x faster                                                                                                 |
| regex_compile              | 124 ms                                                                                                          | 117 ms: 1.05x faster                                                                                                  |
| sympy_expand               | 450 ms                                                                                                          | 428 ms: 1.05x faster                                                                                                  |
| genshi_xml                 | 48.4 ms                                                                                                         | 46.1 ms: 1.05x faster                                                                                                 |
| bpe_tokeniser              | 4.16 sec                                                                                                        | 3.97 sec: 1.05x faster                                                                                                |
| telco                      | 7.24 ms                                                                                                         | 6.92 ms: 1.05x faster                                                                                                 |
| sqlglot_v2_transpile       | 1.49 ms                                                                                                         | 1.43 ms: 1.05x faster                                                                                                 |
| pyflate                    | 406 ms                                                                                                          | 388 ms: 1.05x faster                                                                                                  |
| sympy_integrate            | 18.8 ms                                                                                                         | 18.0 ms: 1.04x faster                                                                                                 |
| async_tree_io_tg           | 623 ms                                                                                                          | 598 ms: 1.04x faster                                                                                                  |
| sympy_str                  | 267 ms                                                                                                          | 257 ms: 1.04x faster                                                                                                  |
| pathlib                    | 19.5 ms                                                                                                         | 18.7 ms: 1.04x faster                                                                                                 |
| async_tree_none            | 270 ms                                                                                                          | 260 ms: 1.04x faster                                                                                                  |
| genshi_text                | 20.5 ms                                                                                                         | 19.8 ms: 1.04x faster                                                                                                 |
| pickle_pure_python         | 307 us                                                                                                          | 296 us: 1.04x faster                                                                                                  |
| sqlglot_v2_optimize        | 49.7 ms                                                                                                         | 47.9 ms: 1.04x faster                                                                                                 |
| unpickle                   | 13.8 us                                                                                                         | 13.3 us: 1.04x faster                                                                                                 |
| sympy_sum                  | 153 ms                                                                                                          | 148 ms: 1.04x faster                                                                                                  |
| pickle_list                | 5.14 us                                                                                                         | 4.96 us: 1.04x faster                                                                                                 |
| xml_etree_process          | 58.5 ms                                                                                                         | 56.6 ms: 1.03x faster                                                                                                 |
| 2to3                       | 250 ms                                                                                                          | 242 ms: 1.03x faster                                                                                                  |
| xml_etree_generate         | 83.3 ms                                                                                                         | 80.8 ms: 1.03x faster                                                                                                 |
| fannkuch                   | 378 ms                                                                                                          | 366 ms: 1.03x faster                                                                                                  |
| bench_thread_pool          | 1.04 ms                                                                                                         | 1.01 ms: 1.03x faster                                                                                                 |
| generators                 | 27.7 ms                                                                                                         | 26.9 ms: 1.03x faster                                                                                                 |
| async_tree_none_tg         | 251 ms                                                                                                          | 244 ms: 1.03x faster                                                                                                  |
| logging_format             | 7.32 us                                                                                                         | 7.12 us: 1.03x faster                                                                                                 |
| k_core                     | 2.03 sec                                                                                                        | 1.98 sec: 1.03x faster                                                                                                |
| async_tree_io              | 593 ms                                                                                                          | 577 ms: 1.03x faster                                                                                                  |
| thrift                     | 735 us                                                                                                          | 716 us: 1.03x faster                                                                                                  |
| logging_silent             | 470 ns                                                                                                          | 458 ns: 1.03x faster                                                                                                  |
| pidigits                   | 197 ms                                                                                                          | 192 ms: 1.03x faster                                                                                                  |
| mako                       | 11.8 ms                                                                                                         | 11.5 ms: 1.03x faster                                                                                                 |
| pickle_dict                | 32.4 us                                                                                                         | 31.6 us: 1.03x faster                                                                                                 |
| pprint_pformat             | 1.57 sec                                                                                                        | 1.53 sec: 1.02x faster                                                                                                |
| async_tree_memoization     | 307 ms                                                                                                          | 300 ms: 1.02x faster                                                                                                  |
| html5lib                   | 61.1 ms                                                                                                         | 59.9 ms: 1.02x faster                                                                                                 |
| regex_v8                   | 23.0 ms                                                                                                         | 22.6 ms: 1.02x faster                                                                                                 |
| nqueens                    | 75.8 ms                                                                                                         | 74.3 ms: 1.02x faster                                                                                                 |
| sqlite_synth               | 2.25 us                                                                                                         | 2.21 us: 1.02x faster                                                                                                 |
| pprint_safe_repr           | 763 ms                                                                                                          | 749 ms: 1.02x faster                                                                                                  |
| sqlglot_v2_normalize       | 98.5 ms                                                                                                         | 96.7 ms: 1.02x faster                                                                                                 |
| sphinx                     | 976 ms                                                                                                          | 961 ms: 1.02x faster                                                                                                  |
| bench_mp_pool              | 98.9 ms                                                                                                         | 97.3 ms: 1.02x faster                                                                                                 |
| crypto_pyaes               | 67.3 ms                                                                                                         | 66.3 ms: 1.01x faster                                                                                                 |
| docutils                   | 2.54 sec                                                                                                        | 2.50 sec: 1.01x faster                                                                                                |
| dulwich_log                | 66.4 ms                                                                                                         | 65.5 ms: 1.01x faster                                                                                                 |
| async_tree_memoization_tg  | 306 ms                                                                                                          | 302 ms: 1.01x faster                                                                                                  |
| json_dumps                 | 10.9 ms                                                                                                         | 10.8 ms: 1.01x faster                                                                                                 |
| many_optionals             | 1.04 ms                                                                                                         | 1.03 ms: 1.01x faster                                                                                                 |
| asyncio_tcp                | 500 ms                                                                                                          | 496 ms: 1.01x faster                                                                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                                                                                        | 1.51 sec: 1.01x faster                                                                                                |
| python_startup             | 12.6 ms                                                                                                         | 12.6 ms: 1.00x faster                                                                                                 |
| python_startup_no_site     | 7.33 ms                                                                                                         | 7.39 ms: 1.01x slower                                                                                                 |
| connected_components       | 400 ms                                                                                                          | 404 ms: 1.01x slower                                                                                                  |
| subparsers                 | 25.2 ms                                                                                                         | 25.6 ms: 1.02x slower                                                                                                 |
| xml_etree_iterparse        | 92.4 ms                                                                                                         | 94.8 ms: 1.03x slower                                                                                                 |
| pickle                     | 12.2 us                                                                                                         | 12.6 us: 1.03x slower                                                                                                 |
| meteor_contest             | 98.7 ms                                                                                                         | 102 ms: 1.03x slower                                                                                                  |
| create_gc_cycles           | 1.89 ms                                                                                                         | 2.00 ms: 1.06x slower                                                                                                 |
| regex_effbot               | 2.88 ms                                                                                                         | 3.12 ms: 1.08x slower                                                                                                 |
| xml_etree_parse            | 133 ms                                                                                                          | 146 ms: 1.10x slower                                                                                                  |
| regex_dna                  | 176 ms                                                                                                          | 195 ms: 1.11x slower                                                                                                  |
| unpack_sequence            | 41.8 ns                                                                                                         | 47.3 ns: 1.13x slower                                                                                                 |
| Geometric mean             | (ref)                                                                                                           | 1.05x faster                                                                                                          |

Benchmark hidden because not significant (4): pylint, asyncio_websockets, gc_traversal, shortest_path

- Geometric mean (including insignificant results): 1.048x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.05x