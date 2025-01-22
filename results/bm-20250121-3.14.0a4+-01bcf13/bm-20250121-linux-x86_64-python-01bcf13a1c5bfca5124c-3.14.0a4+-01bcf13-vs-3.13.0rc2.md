# Results vs. 3.13.0rc2

- fork: python
- ref: 01bcf13a1c5bfca5124c
- machine: linux-x86_64
- commit hash: 01bcf13
- commit date: 2025-01-21
- overall geometric mean: 1.005x faster
- HPT reliability: 95.10%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 510 ms: 1.15x slower                                                   |
| docutils       | 4.01 sec                                                     | 3.61 sec: 1.11x faster                                                 |
| Geometric mean | (ref)                                                        | 1.00x slower                                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 886 ms: 1.58x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 892 ms: 1.56x faster                                                   |
| async_tree_none            | 572 ms                                                       | 400 ms: 1.43x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 504 ms: 1.41x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 380 ms: 1.33x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 545 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 696 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 745 ms: 1.19x faster                                                   |
| async_generators           | 567 ms                                                       | 543 ms: 1.04x faster                                                   |
| coroutines                 | 30.9 ms                                                      | 33.3 ms: 1.08x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.25x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 275 ms: 1.10x slower                                                   |
| nbody          | 119 ms                                                       | 141 ms: 1.19x slower                                                   |
| Geometric mean | (ref)                                                        | 1.09x slower                                                           |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.39 ms: 1.08x faster                                                  |
| regex_v8       | 32.8 ms                                                      | 36.1 ms: 1.10x slower                                                  |
| Geometric mean | (ref)                                                        | 1.02x slower                                                           |

Benchmark hidden because not significant (2): regex_dna, regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 231 ms                                                       | 209 ms: 1.10x faster                                                   |
| tomli_loads          | 2.78 sec                                                     | 2.68 sec: 1.04x faster                                                 |
| unpickle_pure_python | 290 us                                                       | 304 us: 1.05x slower                                                   |
| xml_etree_generate   | 122 ms                                                       | 136 ms: 1.11x slower                                                   |
| pickle_pure_python   | 416 us                                                       | 469 us: 1.12x slower                                                   |
| json_loads           | 34.3 us                                                      | 42.4 us: 1.24x slower                                                  |
| json_dumps           | 14.1 ms                                                      | 19.9 ms: 1.41x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.07x slower                                                           |

Benchmark hidden because not significant (2): xml_etree_iterparse, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 18.0 ms: 1.18x slower                                                  |
| python_startup         | 22.4 ms                                                      | 30.8 ms: 1.38x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.27x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 77.9 ms: 1.08x slower                                                  |
| mako            | 15.9 ms                                                      | 18.1 ms: 1.13x slower                                                  |
| django_template | 44.3 ms                                                      | 51.0 ms: 1.15x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.08x slower                                                           |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 886 ms: 1.58x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 892 ms: 1.56x faster                                                   |
| async_tree_none            | 572 ms                                                       | 400 ms: 1.43x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 504 ms: 1.41x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 380 ms: 1.33x faster                                                   |
| deepcopy                   | 498 us                                                       | 394 us: 1.26x faster                                                   |
| deepcopy_memo              | 50.1 us                                                      | 40.3 us: 1.24x faster                                                  |
| async_tree_memoization_tg  | 670 ms                                                       | 545 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 696 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 745 ms: 1.19x faster                                                   |
| deepcopy_reduce            | 4.10 us                                                      | 3.46 us: 1.18x faster                                                  |
| scimark_sor                | 179 ms                                                       | 157 ms: 1.14x faster                                                   |
| pylint                     | 470 ms                                                       | 414 ms: 1.14x faster                                                   |
| go                         | 191 ms                                                       | 171 ms: 1.12x faster                                                   |
| docutils                   | 4.01 sec                                                     | 3.61 sec: 1.11x faster                                                 |
| xml_etree_parse            | 231 ms                                                       | 209 ms: 1.10x faster                                                   |
| comprehensions             | 22.2 us                                                      | 20.3 us: 1.10x faster                                                  |
| typing_runtime_protocols   | 226 us                                                       | 208 us: 1.08x faster                                                   |
| regex_effbot               | 4.74 ms                                                      | 4.39 ms: 1.08x faster                                                  |
| mdp                        | 3.80 sec                                                     | 3.55 sec: 1.07x faster                                                 |
| spectral_norm              | 157 ms                                                       | 147 ms: 1.07x faster                                                   |
| chaos                      | 83.6 ms                                                      | 78.6 ms: 1.06x faster                                                  |
| sympy_sum                  | 210 ms                                                       | 198 ms: 1.06x faster                                                   |
| bpe_tokeniser              | 6.28 sec                                                     | 5.96 sec: 1.06x faster                                                 |
| scimark_fft                | 473 ms                                                       | 453 ms: 1.05x faster                                                   |
| async_generators           | 567 ms                                                       | 543 ms: 1.04x faster                                                   |
| thrift                     | 1.10 ms                                                      | 1.06 ms: 1.04x faster                                                  |
| tomli_loads                | 2.78 sec                                                     | 2.68 sec: 1.04x faster                                                 |
| sympy_expand               | 601 ms                                                       | 580 ms: 1.04x faster                                                   |
| unpickle_pure_python       | 290 us                                                       | 304 us: 1.05x slower                                                   |
| pathlib                    | 29.9 ms                                                      | 31.4 ms: 1.05x slower                                                  |
| sqlglot_optimize           | 74.7 ms                                                      | 78.6 ms: 1.05x slower                                                  |
| deltablue                  | 4.44 ms                                                      | 4.68 ms: 1.06x slower                                                  |
| generators                 | 40.0 ms                                                      | 42.7 ms: 1.07x slower                                                  |
| coroutines                 | 30.9 ms                                                      | 33.3 ms: 1.08x slower                                                  |
| logging_silent             | 130 ns                                                       | 141 ns: 1.08x slower                                                   |
| genshi_xml                 | 72.1 ms                                                      | 77.9 ms: 1.08x slower                                                  |
| fannkuch                   | 547 ms                                                       | 592 ms: 1.08x slower                                                   |
| pycparser                  | 1.57 sec                                                     | 1.70 sec: 1.08x slower                                                 |
| sqlglot_transpile          | 2.20 ms                                                      | 2.38 ms: 1.08x slower                                                  |
| pidigits                   | 251 ms                                                       | 275 ms: 1.10x slower                                                   |
| crypto_pyaes               | 100 ms                                                       | 110 ms: 1.10x slower                                                   |
| regex_v8                   | 32.8 ms                                                      | 36.1 ms: 1.10x slower                                                  |
| json                       | 6.51 ms                                                      | 7.18 ms: 1.10x slower                                                  |
| xml_etree_generate         | 122 ms                                                       | 136 ms: 1.11x slower                                                   |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 7.52 ms: 1.11x slower                                                  |
| logging_simple             | 8.56 us                                                      | 9.54 us: 1.11x slower                                                  |
| coverage                   | 107 ms                                                       | 120 ms: 1.12x slower                                                   |
| pickle_pure_python         | 416 us                                                       | 469 us: 1.12x slower                                                   |
| sqlglot_normalize          | 140 ms                                                       | 158 ms: 1.13x slower                                                   |
| mako                       | 15.9 ms                                                      | 18.1 ms: 1.13x slower                                                  |
| hexiom                     | 8.11 ms                                                      | 9.28 ms: 1.14x slower                                                  |
| 2to3                       | 445 ms                                                       | 510 ms: 1.15x slower                                                   |
| django_template            | 44.3 ms                                                      | 51.0 ms: 1.15x slower                                                  |
| dulwich_log                | 93.7 ms                                                      | 110 ms: 1.17x slower                                                   |
| python_startup_no_site     | 15.3 ms                                                      | 18.0 ms: 1.18x slower                                                  |
| nbody                      | 119 ms                                                       | 141 ms: 1.19x slower                                                   |
| logging_format             | 9.24 us                                                      | 11.2 us: 1.21x slower                                                  |
| json_loads                 | 34.3 us                                                      | 42.4 us: 1.24x slower                                                  |
| python_startup             | 22.4 ms                                                      | 30.8 ms: 1.38x slower                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 4.01 ms: 1.39x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 19.9 ms: 1.41x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 8.79 ms: 1.54x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 4.11 ms: 1.70x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 98.9 ms: 5.29x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.03x slower                                                           |

Benchmark hidden because not significant (23): xml_etree_iterparse, genshi_text, pprint_safe_repr, scimark_monte_carlo, html5lib, telco, meteor_contest, regex_dna, float, richards, xml_etree_process, asyncio_websockets, sympy_str, pprint_pformat, nqueens, raytrace, sqlite_synth, pyflate, richards_super, scimark_lu, sqlglot_parse, regex_compile, sympy_integrate
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250121-3.14.0a4+-01bcf13/bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.005x faster

# HPT report

- Reliability score: 95.10% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.13x