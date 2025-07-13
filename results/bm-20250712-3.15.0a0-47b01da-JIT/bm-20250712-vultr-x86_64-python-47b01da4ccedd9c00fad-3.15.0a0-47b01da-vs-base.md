# Results vs. base

- fork: python
- ref: 47b01da4ccedd9c00fad
- machine: linux-x86_64
- commit hash: 47b01da
- commit date: 2025-07-12
- overall geometric mean: 1.013x faster
- HPT reliability: 52.17%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250712-3.15.0a0-47b01da/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json | results/bm-20250712-3.15.0a0-47b01da-JIT/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 249 ms                                                                                                          | 254 ms: 1.02x slower                                                                                                |
| docutils       | 2.54 sec                                                                                                        | 2.60 sec: 1.02x slower                                                                                              |
| sphinx         | 972 ms                                                                                                          | 982 ms: 1.01x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.01x slower                                                                                                        |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250712-3.15.0a0-47b01da/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json | results/bm-20250712-3.15.0a0-47b01da-JIT/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| asyncio_tcp                | 497 ms                                                                                                          | 501 ms: 1.01x slower                                                                                                |
| async_tree_cpu_io_mixed    | 501 ms                                                                                                          | 505 ms: 1.01x slower                                                                                                |
| async_tree_cpu_io_mixed_tg | 502 ms                                                                                                          | 514 ms: 1.02x slower                                                                                                |
| async_generators           | 339 ms                                                                                                          | 355 ms: 1.05x slower                                                                                                |
| Geometric mean             | (ref)                                                                                                           | 1.01x slower                                                                                                        |

Benchmark hidden because not significant (9): asyncio_tcp_ssl, async_tree_none, async_tree_memoization, asyncio_websockets, async_tree_io, coroutines, async_tree_memoization_tg, async_tree_none_tg, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250712-3.15.0a0-47b01da/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json | results/bm-20250712-3.15.0a0-47b01da-JIT/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| float          | 71.4 ms                                                                                                         | 64.5 ms: 1.11x faster                                                                                               |
| nbody          | 89.4 ms                                                                                                         | 88.5 ms: 1.01x faster                                                                                               |
| pidigits       | 195 ms                                                                                                          | 210 ms: 1.08x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.01x faster                                                                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250712-3.15.0a0-47b01da/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json | results/bm-20250712-3.15.0a0-47b01da-JIT/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| regex_compile  | 123 ms                                                                                                          | 124 ms: 1.01x slower                                                                                                |
| regex_dna      | 176 ms                                                                                                          | 180 ms: 1.02x slower                                                                                                |
| regex_effbot   | 2.68 ms                                                                                                         | 2.76 ms: 1.03x slower                                                                                               |
| regex_v8       | 21.2 ms                                                                                                         | 22.3 ms: 1.05x slower                                                                                               |
| Geometric mean | (ref)                                                                                                           | 1.03x slower                                                                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250712-3.15.0a0-47b01da/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json | results/bm-20250712-3.15.0a0-47b01da-JIT/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| tomli_loads          | 1.92 sec                                                                                                        | 1.75 sec: 1.10x faster                                                                                              |
| unpickle_pure_python | 206 us                                                                                                          | 187 us: 1.10x faster                                                                                                |
| xml_etree_generate   | 83.1 ms                                                                                                         | 77.9 ms: 1.07x faster                                                                                               |
| xml_etree_process    | 57.3 ms                                                                                                         | 54.3 ms: 1.06x faster                                                                                               |
| xml_etree_parse      | 134 ms                                                                                                          | 130 ms: 1.03x faster                                                                                                |
| json_dumps           | 10.9 ms                                                                                                         | 10.7 ms: 1.02x faster                                                                                               |
| xml_etree_iterparse  | 93.1 ms                                                                                                         | 92.5 ms: 1.01x faster                                                                                               |
| pickle_pure_python   | 304 us                                                                                                          | 306 us: 1.01x slower                                                                                                |
| pickle               | 12.2 us                                                                                                         | 12.4 us: 1.01x slower                                                                                               |
| pickle_list          | 5.09 us                                                                                                         | 5.19 us: 1.02x slower                                                                                               |
| unpickle             | 13.8 us                                                                                                         | 14.2 us: 1.03x slower                                                                                               |
| pickle_dict          | 30.5 us                                                                                                         | 32.6 us: 1.07x slower                                                                                               |
| Geometric mean       | (ref)                                                                                                           | 1.02x faster                                                                                                        |

Benchmark hidden because not significant (2): unpickle_list, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250712-3.15.0a0-47b01da/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json | results/bm-20250712-3.15.0a0-47b01da-JIT/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| python_startup_no_site | 7.32 ms                                                                                                         | 7.35 ms: 1.00x slower                                                                                               |
| python_startup         | 12.6 ms                                                                                                         | 12.6 ms: 1.01x slower                                                                                               |
| Geometric mean         | (ref)                                                                                                           | 1.01x slower                                                                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250712-3.15.0a0-47b01da/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json | results/bm-20250712-3.15.0a0-47b01da-JIT/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| mako            | 11.6 ms                                                                                                         | 10.7 ms: 1.08x faster                                                                                               |
| genshi_text     | 20.7 ms                                                                                                         | 20.8 ms: 1.01x slower                                                                                               |
| django_template | 34.2 ms                                                                                                         | 34.5 ms: 1.01x slower                                                                                               |
| genshi_xml      | 48.4 ms                                                                                                         | 49.0 ms: 1.01x slower                                                                                               |
| Geometric mean  | (ref)                                                                                                           | 1.01x faster                                                                                                        |

All benchmarks:
===============

| Benchmark                  | results/bm-20250712-3.15.0a0-47b01da/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json | results/bm-20250712-3.15.0a0-47b01da-JIT/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| richards_super             | 46.8 ms                                                                                                         | 34.4 ms: 1.36x faster                                                                                               |
| richards                   | 41.1 ms                                                                                                         | 30.3 ms: 1.36x faster                                                                                               |
| scimark_fft                | 336 ms                                                                                                          | 286 ms: 1.18x faster                                                                                                |
| spectral_norm              | 99.3 ms                                                                                                         | 85.0 ms: 1.17x faster                                                                                               |
| float                      | 71.4 ms                                                                                                         | 64.5 ms: 1.11x faster                                                                                               |
| tomli_loads                | 1.92 sec                                                                                                        | 1.75 sec: 1.10x faster                                                                                              |
| unpickle_pure_python       | 206 us                                                                                                          | 187 us: 1.10x faster                                                                                                |
| mako                       | 11.6 ms                                                                                                         | 10.7 ms: 1.08x faster                                                                                               |
| deltablue                  | 3.08 ms                                                                                                         | 2.85 ms: 1.08x faster                                                                                               |
| fannkuch                   | 388 ms                                                                                                          | 363 ms: 1.07x faster                                                                                                |
| xml_etree_generate         | 83.1 ms                                                                                                         | 77.9 ms: 1.07x faster                                                                                               |
| scimark_monte_carlo        | 62.5 ms                                                                                                         | 58.7 ms: 1.06x faster                                                                                               |
| xml_etree_process          | 57.3 ms                                                                                                         | 54.3 ms: 1.06x faster                                                                                               |
| sqlite_synth               | 2.30 us                                                                                                         | 2.18 us: 1.05x faster                                                                                               |
| pyflate                    | 400 ms                                                                                                          | 381 ms: 1.05x faster                                                                                                |
| bpe_tokeniser              | 4.19 sec                                                                                                        | 4.00 sec: 1.05x faster                                                                                              |
| scimark_sparse_mat_mult    | 4.66 ms                                                                                                         | 4.47 ms: 1.04x faster                                                                                               |
| xml_etree_parse            | 134 ms                                                                                                          | 130 ms: 1.03x faster                                                                                                |
| gc_traversal               | 4.69 ms                                                                                                         | 4.59 ms: 1.02x faster                                                                                               |
| pprint_pformat             | 1.43 sec                                                                                                        | 1.40 sec: 1.02x faster                                                                                              |
| json_dumps                 | 10.9 ms                                                                                                         | 10.7 ms: 1.02x faster                                                                                               |
| generators                 | 28.0 ms                                                                                                         | 27.5 ms: 1.02x faster                                                                                               |
| pathlib                    | 19.6 ms                                                                                                         | 19.3 ms: 1.02x faster                                                                                               |
| connected_components       | 398 ms                                                                                                          | 394 ms: 1.01x faster                                                                                                |
| nbody                      | 89.4 ms                                                                                                         | 88.5 ms: 1.01x faster                                                                                               |
| telco                      | 159 ms                                                                                                          | 158 ms: 1.01x faster                                                                                                |
| nqueens                    | 78.5 ms                                                                                                         | 77.8 ms: 1.01x faster                                                                                               |
| xml_etree_iterparse        | 93.1 ms                                                                                                         | 92.5 ms: 1.01x faster                                                                                               |
| crypto_pyaes               | 68.0 ms                                                                                                         | 67.7 ms: 1.00x faster                                                                                               |
| scimark_sor                | 109 ms                                                                                                          | 108 ms: 1.00x faster                                                                                                |
| meteor_contest             | 98.5 ms                                                                                                         | 98.0 ms: 1.00x faster                                                                                               |
| bench_thread_pool          | 1.05 ms                                                                                                         | 1.05 ms: 1.00x slower                                                                                               |
| coverage                   | 80.8 ms                                                                                                         | 81.1 ms: 1.00x slower                                                                                               |
| python_startup_no_site     | 7.32 ms                                                                                                         | 7.35 ms: 1.00x slower                                                                                               |
| pickle_pure_python         | 304 us                                                                                                          | 306 us: 1.01x slower                                                                                                |
| genshi_text                | 20.7 ms                                                                                                         | 20.8 ms: 1.01x slower                                                                                               |
| python_startup             | 12.6 ms                                                                                                         | 12.6 ms: 1.01x slower                                                                                               |
| mdp                        | 1.15 sec                                                                                                        | 1.16 sec: 1.01x slower                                                                                              |
| django_template            | 34.2 ms                                                                                                         | 34.5 ms: 1.01x slower                                                                                               |
| asyncio_tcp                | 497 ms                                                                                                          | 501 ms: 1.01x slower                                                                                                |
| thrift                     | 752 us                                                                                                          | 758 us: 1.01x slower                                                                                                |
| async_tree_cpu_io_mixed    | 501 ms                                                                                                          | 505 ms: 1.01x slower                                                                                                |
| chaos                      | 56.2 ms                                                                                                         | 56.7 ms: 1.01x slower                                                                                               |
| sphinx                     | 972 ms                                                                                                          | 982 ms: 1.01x slower                                                                                                |
| regex_compile              | 123 ms                                                                                                          | 124 ms: 1.01x slower                                                                                                |
| sqlglot_v2_normalize       | 98.0 ms                                                                                                         | 99.2 ms: 1.01x slower                                                                                               |
| genshi_xml                 | 48.4 ms                                                                                                         | 49.0 ms: 1.01x slower                                                                                               |
| logging_simple             | 5.82 us                                                                                                         | 5.89 us: 1.01x slower                                                                                               |
| sympy_sum                  | 153 ms                                                                                                          | 155 ms: 1.01x slower                                                                                                |
| sqlglot_v2_transpile       | 1.51 ms                                                                                                         | 1.53 ms: 1.01x slower                                                                                               |
| sqlglot_v2_optimize        | 49.7 ms                                                                                                         | 50.4 ms: 1.01x slower                                                                                               |
| pickle                     | 12.2 us                                                                                                         | 12.4 us: 1.01x slower                                                                                               |
| logging_format             | 6.51 us                                                                                                         | 6.61 us: 1.01x slower                                                                                               |
| raytrace                   | 250 ms                                                                                                          | 254 ms: 1.02x slower                                                                                                |
| sympy_str                  | 269 ms                                                                                                          | 273 ms: 1.02x slower                                                                                                |
| dulwich_log                | 66.5 ms                                                                                                         | 67.7 ms: 1.02x slower                                                                                               |
| deepcopy_reduce            | 2.65 us                                                                                                         | 2.70 us: 1.02x slower                                                                                               |
| many_optionals             | 1.05 ms                                                                                                         | 1.07 ms: 1.02x slower                                                                                               |
| pickle_list                | 5.09 us                                                                                                         | 5.19 us: 1.02x slower                                                                                               |
| sympy_integrate            | 18.8 ms                                                                                                         | 19.2 ms: 1.02x slower                                                                                               |
| deepcopy                   | 250 us                                                                                                          | 255 us: 1.02x slower                                                                                                |
| 2to3                       | 249 ms                                                                                                          | 254 ms: 1.02x slower                                                                                                |
| docutils                   | 2.54 sec                                                                                                        | 2.60 sec: 1.02x slower                                                                                              |
| regex_dna                  | 176 ms                                                                                                          | 180 ms: 1.02x slower                                                                                                |
| async_tree_cpu_io_mixed_tg | 502 ms                                                                                                          | 514 ms: 1.02x slower                                                                                                |
| pycparser                  | 1.09 sec                                                                                                        | 1.12 sec: 1.03x slower                                                                                              |
| unpickle                   | 13.8 us                                                                                                         | 14.2 us: 1.03x slower                                                                                               |
| regex_effbot               | 2.68 ms                                                                                                         | 2.76 ms: 1.03x slower                                                                                               |
| deepcopy_memo              | 28.6 us                                                                                                         | 29.5 us: 1.03x slower                                                                                               |
| sympy_expand               | 458 ms                                                                                                          | 474 ms: 1.04x slower                                                                                                |
| hexiom                     | 5.59 ms                                                                                                         | 5.86 ms: 1.05x slower                                                                                               |
| async_generators           | 339 ms                                                                                                          | 355 ms: 1.05x slower                                                                                                |
| logging_silent             | 96.3 ns                                                                                                         | 101 ns: 1.05x slower                                                                                                |
| comprehensions             | 15.4 us                                                                                                         | 16.2 us: 1.05x slower                                                                                               |
| regex_v8                   | 21.2 ms                                                                                                         | 22.3 ms: 1.05x slower                                                                                               |
| go                         | 104 ms                                                                                                          | 110 ms: 1.06x slower                                                                                                |
| pickle_dict                | 30.5 us                                                                                                         | 32.6 us: 1.07x slower                                                                                               |
| pidigits                   | 195 ms                                                                                                          | 210 ms: 1.08x slower                                                                                                |
| unpack_sequence            | 42.1 ns                                                                                                         | 48.2 ns: 1.14x slower                                                                                               |
| Geometric mean             | (ref)                                                                                                           | 1.01x faster                                                                                                        |

Benchmark hidden because not significant (23): typing_runtime_protocols, k_core, html5lib, pprint_safe_repr, shortest_path, unpickle_list, json, asyncio_tcp_ssl, bench_mp_pool, async_tree_none, async_tree_memoization, json_loads, asyncio_websockets, async_tree_io, coroutines, sqlglot_v2_parse, subparsers, create_gc_cycles, async_tree_memoization_tg, async_tree_none_tg, async_tree_io_tg, scimark_lu, pylint

- Geometric mean (including insignificant results): 1.013x faster

# HPT report

- Reliability score: 52.17% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.02x