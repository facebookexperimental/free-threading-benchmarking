# Results vs. 3.12.6

- fork: python
- ref: 10ee2d9d3bcde27c75f1
- machine: linux-x86_64
- commit hash: 10ee2d9
- commit date: 2025-01-30
- overall geometric mean: 1.089x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 4.00 sec                                               | 3.71 sec: 1.08x faster                                                 |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (2): 2to3, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.85 sec                                               | 888 ms: 2.08x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 452 ms: 2.06x faster                                                   |
| async_tree_io_tg           | 1.93 sec                                               | 958 ms: 2.02x faster                                                   |
| async_tree_none            | 741 ms                                                 | 380 ms: 1.95x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 361 ms: 1.95x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 526 ms: 1.86x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 679 ms: 1.59x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 727 ms: 1.51x faster                                                   |
| async_generators           | 589 ms                                                 | 546 ms: 1.08x faster                                                   |
| coroutines                 | 29.5 ms                                                | 31.0 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.58x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 101 ms: 1.22x faster                                                   |
| pidigits       | 250 ms                                                 | 239 ms: 1.04x faster                                                   |
| nbody          | 119 ms                                                 | 127 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                  | 1.06x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.46 ms: 1.15x faster                                                  |
| regex_compile  | 187 ms                                                 | 173 ms: 1.08x faster                                                   |
| Geometric mean | (ref)                                                  | 1.05x faster                                                           |

Benchmark hidden because not significant (2): regex_dna, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 241 ms                                                 | 204 ms: 1.18x faster                                                   |
| tomli_loads          | 2.88 sec                                               | 2.52 sec: 1.14x faster                                                 |
| xml_etree_generate   | 127 ms                                                 | 117 ms: 1.09x faster                                                   |
| xml_etree_iterparse  | 169 ms                                                 | 157 ms: 1.08x faster                                                   |
| unpickle_pure_python | 300 us                                                 | 322 us: 1.07x slower                                                   |
| json_dumps           | 14.3 ms                                                | 16.8 ms: 1.17x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (3): pickle_pure_python, json_loads, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 15.9 ms: 1.11x faster                                                  |
| python_startup         | 23.7 ms                                                | 26.6 ms: 1.12x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.01x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 15.7 ms                                                | 16.7 ms: 1.06x slower                                                  |
| django_template | 44.9 ms                                                | 49.2 ms: 1.09x slower                                                  |
| genshi_xml      | 67.6 ms                                                | 76.1 ms: 1.13x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.07x slower                                                           |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.85 sec                                               | 888 ms: 2.08x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 452 ms: 2.06x faster                                                   |
| async_tree_io_tg           | 1.93 sec                                               | 958 ms: 2.02x faster                                                   |
| async_tree_none            | 741 ms                                                 | 380 ms: 1.95x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 361 ms: 1.95x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 526 ms: 1.86x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 679 ms: 1.59x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 727 ms: 1.51x faster                                                   |
| spectral_norm              | 156 ms                                                 | 119 ms: 1.30x faster                                                   |
| deepcopy                   | 468 us                                                 | 371 us: 1.26x faster                                                   |
| deepcopy_memo              | 52.4 us                                                | 42.8 us: 1.23x faster                                                  |
| float                      | 123 ms                                                 | 101 ms: 1.22x faster                                                   |
| pyflate                    | 727 ms                                                 | 602 ms: 1.21x faster                                                   |
| bench_thread_pool          | 3.48 ms                                                | 2.88 ms: 1.21x faster                                                  |
| comprehensions             | 27.1 us                                                | 22.6 us: 1.20x faster                                                  |
| crypto_pyaes               | 107 ms                                                 | 89.7 ms: 1.20x faster                                                  |
| xml_etree_parse            | 241 ms                                                 | 204 ms: 1.18x faster                                                   |
| bpe_tokeniser              | 6.59 sec                                               | 5.64 sec: 1.17x faster                                                 |
| sqlalchemy_declarative     | 218 ms                                                 | 187 ms: 1.16x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.46 ms: 1.15x faster                                                  |
| go                         | 172 ms                                                 | 151 ms: 1.14x faster                                                   |
| tomli_loads                | 2.88 sec                                               | 2.52 sec: 1.14x faster                                                 |
| pycparser                  | 1.79 sec                                               | 1.57 sec: 1.14x faster                                                 |
| mdp                        | 3.97 sec                                               | 3.49 sec: 1.14x faster                                                 |
| pylint                     | 465 ms                                                 | 409 ms: 1.14x faster                                                   |
| scimark_fft                | 500 ms                                                 | 442 ms: 1.13x faster                                                   |
| raytrace                   | 408 ms                                                 | 362 ms: 1.13x faster                                                   |
| python_startup_no_site     | 17.6 ms                                                | 15.9 ms: 1.11x faster                                                  |
| sqlalchemy_imperative      | 24.7 ms                                                | 22.5 ms: 1.10x faster                                                  |
| deepcopy_reduce            | 4.04 us                                                | 3.70 us: 1.09x faster                                                  |
| xml_etree_generate         | 127 ms                                                 | 117 ms: 1.09x faster                                                   |
| pathlib                    | 31.6 ms                                                | 29.2 ms: 1.08x faster                                                  |
| regex_compile              | 187 ms                                                 | 173 ms: 1.08x faster                                                   |
| async_generators           | 589 ms                                                 | 546 ms: 1.08x faster                                                   |
| xml_etree_iterparse        | 169 ms                                                 | 157 ms: 1.08x faster                                                   |
| docutils                   | 4.00 sec                                               | 3.71 sec: 1.08x faster                                                 |
| nqueens                    | 117 ms                                                 | 109 ms: 1.07x faster                                                   |
| logging_simple             | 9.45 us                                                | 8.83 us: 1.07x faster                                                  |
| generators                 | 41.1 ms                                                | 38.5 ms: 1.07x faster                                                  |
| chaos                      | 84.9 ms                                                | 80.2 ms: 1.06x faster                                                  |
| sqlglot_parse              | 1.79 ms                                                | 1.70 ms: 1.05x faster                                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 92.0 ms: 1.05x faster                                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 6.41 ms: 1.05x faster                                                  |
| pidigits                   | 250 ms                                                 | 239 ms: 1.04x faster                                                   |
| scimark_sor                | 167 ms                                                 | 160 ms: 1.04x faster                                                   |
| pprint_pformat             | 1.98 sec                                               | 1.91 sec: 1.04x faster                                                 |
| richards_super             | 72.8 ms                                                | 75.9 ms: 1.04x slower                                                  |
| coroutines                 | 29.5 ms                                                | 31.0 ms: 1.05x slower                                                  |
| telco                      | 9.59 ms                                                | 10.1 ms: 1.05x slower                                                  |
| logging_silent             | 139 ns                                                 | 147 ns: 1.06x slower                                                   |
| meteor_contest             | 146 ms                                                 | 155 ms: 1.06x slower                                                   |
| deltablue                  | 4.27 ms                                                | 4.51 ms: 1.06x slower                                                  |
| mako                       | 15.7 ms                                                | 16.7 ms: 1.06x slower                                                  |
| nbody                      | 119 ms                                                 | 127 ms: 1.07x slower                                                   |
| unpickle_pure_python       | 300 us                                                 | 322 us: 1.07x slower                                                   |
| json                       | 6.85 ms                                                | 7.38 ms: 1.08x slower                                                  |
| django_template            | 44.9 ms                                                | 49.2 ms: 1.09x slower                                                  |
| python_startup             | 23.7 ms                                                | 26.6 ms: 1.12x slower                                                  |
| genshi_xml                 | 67.6 ms                                                | 76.1 ms: 1.13x slower                                                  |
| logging_format             | 9.59 us                                                | 11.1 us: 1.16x slower                                                  |
| json_dumps                 | 14.3 ms                                                | 16.8 ms: 1.17x slower                                                  |
| coverage                   | 95.4 ms                                                | 119 ms: 1.25x slower                                                   |
| gc_traversal               | 5.86 ms                                                | 7.56 ms: 1.29x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 3.75 ms: 1.93x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 100.0 ms: 4.83x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                           |

Benchmark hidden because not significant (25): sympy_integrate, scimark_lu, html5lib, sqlite_synth, pprint_safe_repr, sqlglot_optimize, typing_runtime_protocols, sqlglot_normalize, sqlglot_transpile, asyncio_websockets, regex_dna, sympy_sum, pickle_pure_python, json_loads, thrift, dulwich_log, genshi_text, xml_etree_process, sympy_str, fannkuch, hexiom, sympy_expand, 2to3, richards, regex_v8
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250130-3.14.0a4+-10ee2d9/bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.089x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.13x