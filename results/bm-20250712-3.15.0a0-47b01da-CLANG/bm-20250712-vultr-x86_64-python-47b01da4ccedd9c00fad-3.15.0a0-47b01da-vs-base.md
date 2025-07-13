# Results vs. base

- fork: python
- ref: 47b01da4ccedd9c00fad
- machine: linux-x86_64
- commit hash: 47b01da
- commit date: 2025-07-12
- overall geometric mean: 1.044x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250712-3.15.0a0-47b01da/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json | results/bm-20250712-3.15.0a0-47b01da-CLANG/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 249 ms                                                                                                          | 245 ms: 1.02x faster                                                                                                  |
| docutils       | 2.54 sec                                                                                                        | 2.50 sec: 1.02x faster                                                                                                |
| html5lib       | 61.7 ms                                                                                                         | 56.9 ms: 1.08x faster                                                                                                 |
| sphinx         | 972 ms                                                                                                          | 949 ms: 1.02x faster                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.04x faster                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250712-3.15.0a0-47b01da/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json | results/bm-20250712-3.15.0a0-47b01da-CLANG/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| coroutines                 | 23.7 ms                                                                                                         | 21.8 ms: 1.08x faster                                                                                                 |
| async_generators           | 339 ms                                                                                                          | 318 ms: 1.07x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 501 ms                                                                                                          | 473 ms: 1.06x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 502 ms                                                                                                          | 479 ms: 1.05x faster                                                                                                  |
| async_tree_memoization     | 316 ms                                                                                                          | 302 ms: 1.05x faster                                                                                                  |
| async_tree_none_tg         | 254 ms                                                                                                          | 243 ms: 1.05x faster                                                                                                  |
| async_tree_none            | 257 ms                                                                                                          | 246 ms: 1.05x faster                                                                                                  |
| async_tree_memoization_tg  | 313 ms                                                                                                          | 300 ms: 1.05x faster                                                                                                  |
| async_tree_io              | 600 ms                                                                                                          | 574 ms: 1.04x faster                                                                                                  |
| async_tree_io_tg           | 617 ms                                                                                                          | 599 ms: 1.03x faster                                                                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                                                                                        | 1.51 sec: 1.00x faster                                                                                                |
| asyncio_websockets         | 518 ms                                                                                                          | 516 ms: 1.00x faster                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.04x faster                                                                                                          |

Benchmark hidden because not significant (1): asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250712-3.15.0a0-47b01da/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json | results/bm-20250712-3.15.0a0-47b01da-CLANG/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| nbody          | 89.4 ms                                                                                                         | 80.4 ms: 1.11x faster                                                                                                 |
| float          | 71.4 ms                                                                                                         | 67.0 ms: 1.07x faster                                                                                                 |
| pidigits       | 195 ms                                                                                                          | 193 ms: 1.01x faster                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.06x faster                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250712-3.15.0a0-47b01da/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json | results/bm-20250712-3.15.0a0-47b01da-CLANG/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_compile  | 123 ms                                                                                                          | 118 ms: 1.04x faster                                                                                                  |
| regex_v8       | 21.2 ms                                                                                                         | 21.8 ms: 1.03x slower                                                                                                 |
| regex_dna      | 176 ms                                                                                                          | 187 ms: 1.07x slower                                                                                                  |
| regex_effbot   | 2.68 ms                                                                                                         | 3.06 ms: 1.14x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                           | 1.05x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250712-3.15.0a0-47b01da/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json | results/bm-20250712-3.15.0a0-47b01da-CLANG/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| json_loads           | 28.2 us                                                                                                         | 25.0 us: 1.13x faster                                                                                                 |
| unpickle_list        | 4.96 us                                                                                                         | 4.51 us: 1.10x faster                                                                                                 |
| tomli_loads          | 1.92 sec                                                                                                        | 1.79 sec: 1.08x faster                                                                                                |
| unpickle_pure_python | 206 us                                                                                                          | 197 us: 1.04x faster                                                                                                  |
| xml_etree_generate   | 83.1 ms                                                                                                         | 79.8 ms: 1.04x faster                                                                                                 |
| xml_etree_process    | 57.3 ms                                                                                                         | 55.0 ms: 1.04x faster                                                                                                 |
| pickle_list          | 5.09 us                                                                                                         | 4.90 us: 1.04x faster                                                                                                 |
| pickle_pure_python   | 304 us                                                                                                          | 295 us: 1.03x faster                                                                                                  |
| json_dumps           | 10.9 ms                                                                                                         | 10.8 ms: 1.01x faster                                                                                                 |
| pickle_dict          | 30.5 us                                                                                                         | 30.9 us: 1.01x slower                                                                                                 |
| xml_etree_iterparse  | 93.1 ms                                                                                                         | 96.6 ms: 1.04x slower                                                                                                 |
| pickle               | 12.2 us                                                                                                         | 12.9 us: 1.06x slower                                                                                                 |
| unpickle             | 13.8 us                                                                                                         | 14.7 us: 1.06x slower                                                                                                 |
| xml_etree_parse      | 134 ms                                                                                                          | 149 ms: 1.11x slower                                                                                                  |
| Geometric mean       | (ref)                                                                                                           | 1.02x faster                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250712-3.15.0a0-47b01da/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json | results/bm-20250712-3.15.0a0-47b01da-CLANG/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.6 ms                                                                                                         | 12.5 ms: 1.01x faster                                                                                                 |
| python_startup_no_site | 7.32 ms                                                                                                         | 7.36 ms: 1.01x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.00x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250712-3.15.0a0-47b01da/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json | results/bm-20250712-3.15.0a0-47b01da-CLANG/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| genshi_text     | 20.7 ms                                                                                                         | 19.1 ms: 1.08x faster                                                                                                 |
| django_template | 34.2 ms                                                                                                         | 32.7 ms: 1.05x faster                                                                                                 |
| genshi_xml      | 48.4 ms                                                                                                         | 46.6 ms: 1.04x faster                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.04x faster                                                                                                          |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | results/bm-20250712-3.15.0a0-47b01da/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json | results/bm-20250712-3.15.0a0-47b01da-CLANG/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| spectral_norm              | 99.3 ms                                                                                                         | 80.2 ms: 1.24x faster                                                                                                 |
| logging_silent             | 96.3 ns                                                                                                         | 79.0 ns: 1.22x faster                                                                                                 |
| scimark_sparse_mat_mult    | 4.66 ms                                                                                                         | 3.90 ms: 1.19x faster                                                                                                 |
| scimark_fft                | 336 ms                                                                                                          | 287 ms: 1.17x faster                                                                                                  |
| chaos                      | 56.2 ms                                                                                                         | 48.9 ms: 1.15x faster                                                                                                 |
| scimark_monte_carlo        | 62.5 ms                                                                                                         | 54.6 ms: 1.14x faster                                                                                                 |
| json_loads                 | 28.2 us                                                                                                         | 25.0 us: 1.13x faster                                                                                                 |
| scimark_lu                 | 110 ms                                                                                                          | 98.6 ms: 1.11x faster                                                                                                 |
| nbody                      | 89.4 ms                                                                                                         | 80.4 ms: 1.11x faster                                                                                                 |
| deepcopy                   | 250 us                                                                                                          | 227 us: 1.10x faster                                                                                                  |
| richards                   | 41.1 ms                                                                                                         | 37.3 ms: 1.10x faster                                                                                                 |
| unpickle_list              | 4.96 us                                                                                                         | 4.51 us: 1.10x faster                                                                                                 |
| deepcopy_reduce            | 2.65 us                                                                                                         | 2.42 us: 1.09x faster                                                                                                 |
| comprehensions             | 15.4 us                                                                                                         | 14.1 us: 1.09x faster                                                                                                 |
| raytrace                   | 250 ms                                                                                                          | 231 ms: 1.09x faster                                                                                                  |
| html5lib                   | 61.7 ms                                                                                                         | 56.9 ms: 1.08x faster                                                                                                 |
| coroutines                 | 23.7 ms                                                                                                         | 21.8 ms: 1.08x faster                                                                                                 |
| genshi_text                | 20.7 ms                                                                                                         | 19.1 ms: 1.08x faster                                                                                                 |
| deltablue                  | 3.08 ms                                                                                                         | 2.84 ms: 1.08x faster                                                                                                 |
| deepcopy_memo              | 28.6 us                                                                                                         | 26.5 us: 1.08x faster                                                                                                 |
| richards_super             | 46.8 ms                                                                                                         | 43.4 ms: 1.08x faster                                                                                                 |
| typing_runtime_protocols   | 155 us                                                                                                          | 144 us: 1.08x faster                                                                                                  |
| nqueens                    | 78.5 ms                                                                                                         | 72.9 ms: 1.08x faster                                                                                                 |
| scimark_sor                | 109 ms                                                                                                          | 101 ms: 1.08x faster                                                                                                  |
| tomli_loads                | 1.92 sec                                                                                                        | 1.79 sec: 1.08x faster                                                                                                |
| gc_traversal               | 4.69 ms                                                                                                         | 4.38 ms: 1.07x faster                                                                                                 |
| async_generators           | 339 ms                                                                                                          | 318 ms: 1.07x faster                                                                                                  |
| thrift                     | 752 us                                                                                                          | 705 us: 1.07x faster                                                                                                  |
| sqlglot_v2_parse           | 1.21 ms                                                                                                         | 1.14 ms: 1.07x faster                                                                                                 |
| float                      | 71.4 ms                                                                                                         | 67.0 ms: 1.07x faster                                                                                                 |
| go                         | 104 ms                                                                                                          | 97.7 ms: 1.06x faster                                                                                                 |
| mdp                        | 1.15 sec                                                                                                        | 1.08 sec: 1.06x faster                                                                                                |
| coverage                   | 80.8 ms                                                                                                         | 76.1 ms: 1.06x faster                                                                                                 |
| json                       | 5.09 ms                                                                                                         | 4.80 ms: 1.06x faster                                                                                                 |
| async_tree_cpu_io_mixed    | 501 ms                                                                                                          | 473 ms: 1.06x faster                                                                                                  |
| hexiom                     | 5.59 ms                                                                                                         | 5.28 ms: 1.06x faster                                                                                                 |
| sqlglot_v2_transpile       | 1.51 ms                                                                                                         | 1.43 ms: 1.06x faster                                                                                                 |
| sympy_expand               | 458 ms                                                                                                          | 433 ms: 1.06x faster                                                                                                  |
| sympy_sum                  | 153 ms                                                                                                          | 146 ms: 1.05x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 502 ms                                                                                                          | 479 ms: 1.05x faster                                                                                                  |
| async_tree_memoization     | 316 ms                                                                                                          | 302 ms: 1.05x faster                                                                                                  |
| fannkuch                   | 388 ms                                                                                                          | 371 ms: 1.05x faster                                                                                                  |
| django_template            | 34.2 ms                                                                                                         | 32.7 ms: 1.05x faster                                                                                                 |
| sympy_integrate            | 18.8 ms                                                                                                         | 17.9 ms: 1.05x faster                                                                                                 |
| async_tree_none_tg         | 254 ms                                                                                                          | 243 ms: 1.05x faster                                                                                                  |
| async_tree_none            | 257 ms                                                                                                          | 246 ms: 1.05x faster                                                                                                  |
| sqlite_synth               | 2.30 us                                                                                                         | 2.19 us: 1.05x faster                                                                                                 |
| async_tree_memoization_tg  | 313 ms                                                                                                          | 300 ms: 1.05x faster                                                                                                  |
| pathlib                    | 19.6 ms                                                                                                         | 18.8 ms: 1.05x faster                                                                                                 |
| bench_thread_pool          | 1.05 ms                                                                                                         | 1.00 ms: 1.05x faster                                                                                                 |
| bpe_tokeniser              | 4.19 sec                                                                                                        | 4.01 sec: 1.05x faster                                                                                                |
| unpickle_pure_python       | 206 us                                                                                                          | 197 us: 1.04x faster                                                                                                  |
| async_tree_io              | 600 ms                                                                                                          | 574 ms: 1.04x faster                                                                                                  |
| xml_etree_generate         | 83.1 ms                                                                                                         | 79.8 ms: 1.04x faster                                                                                                 |
| xml_etree_process          | 57.3 ms                                                                                                         | 55.0 ms: 1.04x faster                                                                                                 |
| regex_compile              | 123 ms                                                                                                          | 118 ms: 1.04x faster                                                                                                  |
| sympy_str                  | 269 ms                                                                                                          | 258 ms: 1.04x faster                                                                                                  |
| pickle_list                | 5.09 us                                                                                                         | 4.90 us: 1.04x faster                                                                                                 |
| sqlglot_v2_optimize        | 49.7 ms                                                                                                         | 47.9 ms: 1.04x faster                                                                                                 |
| genshi_xml                 | 48.4 ms                                                                                                         | 46.6 ms: 1.04x faster                                                                                                 |
| pylint                     | 279 ms                                                                                                          | 269 ms: 1.03x faster                                                                                                  |
| telco                      | 159 ms                                                                                                          | 155 ms: 1.03x faster                                                                                                  |
| pickle_pure_python         | 304 us                                                                                                          | 295 us: 1.03x faster                                                                                                  |
| async_tree_io_tg           | 617 ms                                                                                                          | 599 ms: 1.03x faster                                                                                                  |
| pyflate                    | 400 ms                                                                                                          | 389 ms: 1.03x faster                                                                                                  |
| pprint_pformat             | 1.43 sec                                                                                                        | 1.39 sec: 1.03x faster                                                                                                |
| sphinx                     | 972 ms                                                                                                          | 949 ms: 1.02x faster                                                                                                  |
| many_optionals             | 1.05 ms                                                                                                         | 1.02 ms: 1.02x faster                                                                                                 |
| k_core                     | 2.03 sec                                                                                                        | 1.98 sec: 1.02x faster                                                                                                |
| pprint_safe_repr           | 703 ms                                                                                                          | 689 ms: 1.02x faster                                                                                                  |
| sqlglot_v2_normalize       | 98.0 ms                                                                                                         | 96.3 ms: 1.02x faster                                                                                                 |
| docutils                   | 2.54 sec                                                                                                        | 2.50 sec: 1.02x faster                                                                                                |
| bench_mp_pool              | 103 ms                                                                                                          | 101 ms: 1.02x faster                                                                                                  |
| generators                 | 28.0 ms                                                                                                         | 27.5 ms: 1.02x faster                                                                                                 |
| 2to3                       | 249 ms                                                                                                          | 245 ms: 1.02x faster                                                                                                  |
| crypto_pyaes               | 68.0 ms                                                                                                         | 66.9 ms: 1.02x faster                                                                                                 |
| json_dumps                 | 10.9 ms                                                                                                         | 10.8 ms: 1.01x faster                                                                                                 |
| subparsers                 | 25.4 ms                                                                                                         | 25.2 ms: 1.01x faster                                                                                                 |
| pidigits                   | 195 ms                                                                                                          | 193 ms: 1.01x faster                                                                                                  |
| logging_simple             | 5.82 us                                                                                                         | 5.78 us: 1.01x faster                                                                                                 |
| python_startup             | 12.6 ms                                                                                                         | 12.5 ms: 1.01x faster                                                                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                                                                                        | 1.51 sec: 1.00x faster                                                                                                |
| dulwich_log                | 66.5 ms                                                                                                         | 66.3 ms: 1.00x faster                                                                                                 |
| asyncio_websockets         | 518 ms                                                                                                          | 516 ms: 1.00x faster                                                                                                  |
| python_startup_no_site     | 7.32 ms                                                                                                         | 7.36 ms: 1.01x slower                                                                                                 |
| meteor_contest             | 98.5 ms                                                                                                         | 99.5 ms: 1.01x slower                                                                                                 |
| shortest_path              | 438 ms                                                                                                          | 443 ms: 1.01x slower                                                                                                  |
| pickle_dict                | 30.5 us                                                                                                         | 30.9 us: 1.01x slower                                                                                                 |
| connected_components       | 398 ms                                                                                                          | 405 ms: 1.02x slower                                                                                                  |
| regex_v8                   | 21.2 ms                                                                                                         | 21.8 ms: 1.03x slower                                                                                                 |
| create_gc_cycles           | 1.96 ms                                                                                                         | 2.03 ms: 1.04x slower                                                                                                 |
| xml_etree_iterparse        | 93.1 ms                                                                                                         | 96.6 ms: 1.04x slower                                                                                                 |
| pycparser                  | 1.09 sec                                                                                                        | 1.14 sec: 1.04x slower                                                                                                |
| pickle                     | 12.2 us                                                                                                         | 12.9 us: 1.06x slower                                                                                                 |
| unpickle                   | 13.8 us                                                                                                         | 14.7 us: 1.06x slower                                                                                                 |
| regex_dna                  | 176 ms                                                                                                          | 187 ms: 1.07x slower                                                                                                  |
| unpack_sequence            | 42.1 ns                                                                                                         | 46.8 ns: 1.11x slower                                                                                                 |
| xml_etree_parse            | 134 ms                                                                                                          | 149 ms: 1.11x slower                                                                                                  |
| regex_effbot               | 2.68 ms                                                                                                         | 3.06 ms: 1.14x slower                                                                                                 |
| Geometric mean             | (ref)                                                                                                           | 1.04x faster                                                                                                          |

Benchmark hidden because not significant (3): mako, asyncio_tcp, logging_format

- Geometric mean (including insignificant results): 1.044x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.02x