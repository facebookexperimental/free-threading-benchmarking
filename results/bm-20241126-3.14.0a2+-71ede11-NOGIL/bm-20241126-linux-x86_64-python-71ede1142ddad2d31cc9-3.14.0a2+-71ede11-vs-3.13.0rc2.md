# Results vs. 3.13.0rc2

- fork: python
- ref: 71ede1142ddad2d31cc9
- machine: linux-x86_64
- commit hash: 71ede11
- commit date: 2024-11-26
- overall geometric mean: 1.261x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.23x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 647 ms: 1.45x slower                                                   |
| docutils       | 4.01 sec                                                     | 4.75 sec: 1.19x slower                                                 |
| html5lib       | 92.6 ms                                                      | 136 ms: 1.47x slower                                                   |
| Geometric mean | (ref)                                                        | 1.36x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 1.13 sec: 1.24x faster                                                 |
| async_tree_io              | 1.39 sec                                                     | 1.15 sec: 1.21x faster                                                 |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 820 ms: 1.04x faster                                                   |
| coroutines                 | 30.9 ms                                                      | 38.7 ms: 1.25x slower                                                  |
| async_generators           | 567 ms                                                       | 711 ms: 1.25x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.01x faster                                                           |

Benchmark hidden because not significant (6): async_tree_memoization_tg, async_tree_memoization, async_tree_none, async_tree_cpu_io_mixed, async_tree_none_tg, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 237 ms: 1.06x faster                                                   |
| float          | 116 ms                                                       | 172 ms: 1.49x slower                                                   |
| nbody          | 119 ms                                                       | 217 ms: 1.83x slower                                                   |
| Geometric mean | (ref)                                                        | 1.37x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 32.8 ms                                                      | 34.4 ms: 1.05x slower                                                  |
| regex_compile  | 182 ms                                                       | 253 ms: 1.39x slower                                                   |
| Geometric mean | (ref)                                                        | 1.09x slower                                                           |

Benchmark hidden because not significant (2): regex_effbot, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 155 ms: 1.14x faster                                                   |
| json_loads           | 34.3 us                                                      | 37.4 us: 1.09x slower                                                  |
| xml_etree_generate   | 122 ms                                                       | 150 ms: 1.22x slower                                                   |
| json_dumps           | 14.1 ms                                                      | 18.8 ms: 1.33x slower                                                  |
| tomli_loads          | 2.78 sec                                                     | 3.91 sec: 1.41x slower                                                 |
| xml_etree_process    | 85.9 ms                                                      | 133 ms: 1.55x slower                                                   |
| unpickle_pure_python | 290 us                                                       | 479 us: 1.65x slower                                                   |
| pickle_pure_python   | 416 us                                                       | 756 us: 1.81x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.30x slower                                                           |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 23.8 ms: 1.55x slower                                                  |
| python_startup         | 22.4 ms                                                      | 37.0 ms: 1.65x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.60x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 102 ms: 1.42x slower                                                   |
| genshi_text     | 31.7 ms                                                      | 47.4 ms: 1.50x slower                                                  |
| django_template | 44.3 ms                                                      | 72.1 ms: 1.63x slower                                                  |
| mako            | 15.9 ms                                                      | 32.2 ms: 2.02x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.62x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 1.13 sec: 1.24x faster                                                 |
| async_tree_io              | 1.39 sec                                                     | 1.15 sec: 1.21x faster                                                 |
| xml_etree_iterparse        | 177 ms                                                       | 155 ms: 1.14x faster                                                   |
| deepcopy                   | 498 us                                                       | 447 us: 1.11x faster                                                   |
| pidigits                   | 251 ms                                                       | 237 ms: 1.06x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 820 ms: 1.04x faster                                                   |
| regex_v8                   | 32.8 ms                                                      | 34.4 ms: 1.05x slower                                                  |
| pathlib                    | 29.9 ms                                                      | 32.5 ms: 1.09x slower                                                  |
| json_loads                 | 34.3 us                                                      | 37.4 us: 1.09x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 6.47 ms: 1.13x slower                                                  |
| telco                      | 12.2 ms                                                      | 14.2 ms: 1.17x slower                                                  |
| scimark_fft                | 473 ms                                                       | 556 ms: 1.17x slower                                                   |
| docutils                   | 4.01 sec                                                     | 4.75 sec: 1.19x slower                                                 |
| pylint                     | 470 ms                                                       | 563 ms: 1.20x slower                                                   |
| spectral_norm              | 157 ms                                                       | 188 ms: 1.20x slower                                                   |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 8.19 ms: 1.21x slower                                                  |
| deepcopy_memo              | 50.1 us                                                      | 61.1 us: 1.22x slower                                                  |
| xml_etree_generate         | 122 ms                                                       | 150 ms: 1.22x slower                                                   |
| mdp                        | 3.80 sec                                                     | 4.69 sec: 1.24x slower                                                 |
| sqlglot_optimize           | 74.7 ms                                                      | 93.3 ms: 1.25x slower                                                  |
| coroutines                 | 30.9 ms                                                      | 38.7 ms: 1.25x slower                                                  |
| async_generators           | 567 ms                                                       | 711 ms: 1.25x slower                                                   |
| pycparser                  | 1.57 sec                                                     | 1.97 sec: 1.26x slower                                                 |
| json                       | 6.51 ms                                                      | 8.24 ms: 1.27x slower                                                  |
| deepcopy_reduce            | 4.10 us                                                      | 5.21 us: 1.27x slower                                                  |
| coverage                   | 107 ms                                                       | 140 ms: 1.31x slower                                                   |
| json_dumps                 | 14.1 ms                                                      | 18.8 ms: 1.33x slower                                                  |
| dulwich_log                | 93.7 ms                                                      | 128 ms: 1.36x slower                                                   |
| nqueens                    | 112 ms                                                       | 152 ms: 1.36x slower                                                   |
| meteor_contest             | 150 ms                                                       | 205 ms: 1.37x slower                                                   |
| crypto_pyaes               | 100 ms                                                       | 137 ms: 1.37x slower                                                   |
| regex_compile              | 182 ms                                                       | 253 ms: 1.39x slower                                                   |
| tomli_loads                | 2.78 sec                                                     | 3.91 sec: 1.41x slower                                                 |
| sqlglot_normalize          | 140 ms                                                       | 197 ms: 1.41x slower                                                   |
| bpe_tokeniser              | 6.28 sec                                                     | 8.88 sec: 1.41x slower                                                 |
| genshi_xml                 | 72.1 ms                                                      | 102 ms: 1.42x slower                                                   |
| sympy_integrate            | 30.2 ms                                                      | 42.8 ms: 1.42x slower                                                  |
| fannkuch                   | 547 ms                                                       | 775 ms: 1.42x slower                                                   |
| generators                 | 40.0 ms                                                      | 56.7 ms: 1.42x slower                                                  |
| pprint_safe_repr           | 987 ms                                                       | 1.40 sec: 1.42x slower                                                 |
| typing_runtime_protocols   | 226 us                                                       | 323 us: 1.43x slower                                                   |
| 2to3                       | 445 ms                                                       | 647 ms: 1.45x slower                                                   |
| thrift                     | 1.10 ms                                                      | 1.60 ms: 1.45x slower                                                  |
| html5lib                   | 92.6 ms                                                      | 136 ms: 1.47x slower                                                   |
| float                      | 116 ms                                                       | 172 ms: 1.49x slower                                                   |
| genshi_text                | 31.7 ms                                                      | 47.4 ms: 1.50x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 3.66 ms: 1.52x slower                                                  |
| pprint_pformat             | 1.94 sec                                                     | 2.96 sec: 1.52x slower                                                 |
| xml_etree_process          | 85.9 ms                                                      | 133 ms: 1.55x slower                                                   |
| python_startup_no_site     | 15.3 ms                                                      | 23.8 ms: 1.55x slower                                                  |
| pyflate                    | 664 ms                                                       | 1.04 sec: 1.57x slower                                                 |
| logging_format             | 9.24 us                                                      | 15.0 us: 1.62x slower                                                  |
| django_template            | 44.3 ms                                                      | 72.1 ms: 1.63x slower                                                  |
| richards_super             | 73.2 ms                                                      | 119 ms: 1.63x slower                                                   |
| scimark_monte_carlo        | 90.6 ms                                                      | 149 ms: 1.64x slower                                                   |
| unpickle_pure_python       | 290 us                                                       | 479 us: 1.65x slower                                                   |
| python_startup             | 22.4 ms                                                      | 37.0 ms: 1.65x slower                                                  |
| richards                   | 65.5 ms                                                      | 109 ms: 1.67x slower                                                   |
| scimark_sor                | 179 ms                                                       | 301 ms: 1.69x slower                                                   |
| bench_thread_pool          | 2.89 ms                                                      | 4.91 ms: 1.70x slower                                                  |
| sympy_str                  | 379 ms                                                       | 650 ms: 1.72x slower                                                   |
| scimark_lu                 | 146 ms                                                       | 254 ms: 1.74x slower                                                   |
| chaos                      | 83.6 ms                                                      | 147 ms: 1.76x slower                                                   |
| go                         | 191 ms                                                       | 342 ms: 1.79x slower                                                   |
| pickle_pure_python         | 416 us                                                       | 756 us: 1.81x slower                                                   |
| nbody                      | 119 ms                                                       | 217 ms: 1.83x slower                                                   |
| logging_simple             | 8.56 us                                                      | 15.7 us: 1.83x slower                                                  |
| hexiom                     | 8.11 ms                                                      | 15.0 ms: 1.84x slower                                                  |
| logging_silent             | 130 ns                                                       | 241 ns: 1.85x slower                                                   |
| comprehensions             | 22.2 us                                                      | 41.3 us: 1.86x slower                                                  |
| sqlglot_parse              | 1.76 ms                                                      | 3.40 ms: 1.94x slower                                                  |
| sympy_expand               | 601 ms                                                       | 1.17 sec: 1.95x slower                                                 |
| mako                       | 15.9 ms                                                      | 32.2 ms: 2.02x slower                                                  |
| sqlglot_transpile          | 2.20 ms                                                      | 4.52 ms: 2.06x slower                                                  |
| raytrace                   | 344 ms                                                       | 712 ms: 2.07x slower                                                   |
| sympy_sum                  | 210 ms                                                       | 470 ms: 2.24x slower                                                   |
| deltablue                  | 4.44 ms                                                      | 10.4 ms: 2.34x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 98.2 ms: 5.26x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.39x slower                                                           |

Benchmark hidden because not significant (10): async_tree_memoization_tg, regex_effbot, async_tree_memoization, async_tree_none, async_tree_cpu_io_mixed, async_tree_none_tg, asyncio_websockets, regex_dna, sqlite_synth, xml_etree_parse
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241126-3.14.0a2+-71ede11-NOGIL/bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.261x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.28x
- 95% likely to have a slowdown of 1.26x
- 99% likely to have a slowdown of 1.23x

# Memory
- memory change: 1.33x