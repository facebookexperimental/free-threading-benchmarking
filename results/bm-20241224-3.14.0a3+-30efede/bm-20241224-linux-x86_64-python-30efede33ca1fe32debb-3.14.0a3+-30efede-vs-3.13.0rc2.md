# Results vs. 3.13.0rc2

- fork: python
- ref: 30efede33ca1fe32debb
- machine: linux-x86_64
- commit hash: 30efede
- commit date: 2024-12-24
- overall geometric mean: 1.051x faster
- HPT reliability: 99.94%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 4.01 sec                                                     | 3.78 sec: 1.06x faster                                                 |
| Geometric mean | (ref)                                                        | 1.02x faster                                                           |

Benchmark hidden because not significant (2): 2to3, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 905 ms: 1.55x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 927 ms: 1.50x faster                                                   |
| async_tree_none            | 572 ms                                                       | 390 ms: 1.47x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 473 ms: 1.42x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 524 ms: 1.35x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 383 ms: 1.31x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 686 ms: 1.30x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 697 ms: 1.22x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.27x faster                                                           |

Benchmark hidden because not significant (3): asyncio_websockets, async_generators, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 119 ms                                                       | 129 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (2): pidigits, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.26 ms: 1.11x faster                                                  |
| regex_dna      | 282 ms                                                       | 267 ms: 1.06x faster                                                   |
| regex_v8       | 32.8 ms                                                      | 35.0 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|---------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse | 177 ms                                                       | 151 ms: 1.17x faster                                                   |
| xml_etree_parse     | 231 ms                                                       | 207 ms: 1.12x faster                                                   |
| tomli_loads         | 2.78 sec                                                     | 2.61 sec: 1.07x faster                                                 |
| xml_etree_generate  | 122 ms                                                       | 116 ms: 1.06x faster                                                   |
| json_loads          | 34.3 us                                                      | 35.9 us: 1.05x slower                                                  |
| pickle_pure_python  | 416 us                                                       | 441 us: 1.06x slower                                                   |
| json_dumps          | 14.1 ms                                                      | 16.0 ms: 1.13x slower                                                  |
| Geometric mean      | (ref)                                                        | 1.02x faster                                                           |

Benchmark hidden because not significant (2): xml_etree_process, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 14.8 ms: 1.03x faster                                                  |
| python_startup         | 22.4 ms                                                      | 26.0 ms: 1.16x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.06x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 68.9 ms: 1.05x faster                                                  |
| mako            | 15.9 ms                                                      | 16.9 ms: 1.06x slower                                                  |
| django_template | 44.3 ms                                                      | 48.1 ms: 1.09x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                           |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 905 ms: 1.55x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 927 ms: 1.50x faster                                                   |
| async_tree_none            | 572 ms                                                       | 390 ms: 1.47x faster                                                   |
| deepcopy                   | 498 us                                                       | 343 us: 1.45x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 473 ms: 1.42x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 524 ms: 1.35x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 383 ms: 1.31x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 686 ms: 1.30x faster                                                   |
| deepcopy_memo              | 50.1 us                                                      | 39.5 us: 1.27x faster                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 697 ms: 1.22x faster                                                   |
| telco                      | 12.2 ms                                                      | 10.3 ms: 1.18x faster                                                  |
| pylint                     | 470 ms                                                       | 401 ms: 1.17x faster                                                   |
| xml_etree_iterparse        | 177 ms                                                       | 151 ms: 1.17x faster                                                   |
| scimark_sor                | 179 ms                                                       | 153 ms: 1.17x faster                                                   |
| richards_super             | 73.2 ms                                                      | 63.9 ms: 1.15x faster                                                  |
| go                         | 191 ms                                                       | 168 ms: 1.14x faster                                                   |
| logging_simple             | 8.56 us                                                      | 7.60 us: 1.13x faster                                                  |
| xml_etree_parse            | 231 ms                                                       | 207 ms: 1.12x faster                                                   |
| regex_effbot               | 4.74 ms                                                      | 4.26 ms: 1.11x faster                                                  |
| richards                   | 65.5 ms                                                      | 59.0 ms: 1.11x faster                                                  |
| deepcopy_reduce            | 4.10 us                                                      | 3.70 us: 1.11x faster                                                  |
| spectral_norm              | 157 ms                                                       | 144 ms: 1.09x faster                                                   |
| thrift                     | 1.10 ms                                                      | 1.01 ms: 1.08x faster                                                  |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 6.27 ms: 1.08x faster                                                  |
| sqlglot_normalize          | 140 ms                                                       | 130 ms: 1.07x faster                                                   |
| sympy_integrate            | 30.2 ms                                                      | 28.4 ms: 1.07x faster                                                  |
| tomli_loads                | 2.78 sec                                                     | 2.61 sec: 1.07x faster                                                 |
| crypto_pyaes               | 100 ms                                                       | 94.0 ms: 1.07x faster                                                  |
| fannkuch                   | 547 ms                                                       | 514 ms: 1.06x faster                                                   |
| docutils                   | 4.01 sec                                                     | 3.78 sec: 1.06x faster                                                 |
| xml_etree_generate         | 122 ms                                                       | 116 ms: 1.06x faster                                                   |
| regex_dna                  | 282 ms                                                       | 267 ms: 1.06x faster                                                   |
| sqlite_synth               | 3.99 us                                                      | 3.78 us: 1.06x faster                                                  |
| pprint_safe_repr           | 987 ms                                                       | 936 ms: 1.05x faster                                                   |
| logging_format             | 9.24 us                                                      | 8.76 us: 1.05x faster                                                  |
| scimark_fft                | 473 ms                                                       | 449 ms: 1.05x faster                                                   |
| pathlib                    | 29.9 ms                                                      | 28.5 ms: 1.05x faster                                                  |
| genshi_xml                 | 72.1 ms                                                      | 68.9 ms: 1.05x faster                                                  |
| bpe_tokeniser              | 6.28 sec                                                     | 6.01 sec: 1.05x faster                                                 |
| sqlglot_parse              | 1.76 ms                                                      | 1.68 ms: 1.04x faster                                                  |
| mdp                        | 3.80 sec                                                     | 3.64 sec: 1.04x faster                                                 |
| sympy_sum                  | 210 ms                                                       | 203 ms: 1.04x faster                                                   |
| python_startup_no_site     | 15.3 ms                                                      | 14.8 ms: 1.03x faster                                                  |
| pyflate                    | 664 ms                                                       | 684 ms: 1.03x slower                                                   |
| dulwich_log                | 93.7 ms                                                      | 98.0 ms: 1.05x slower                                                  |
| json_loads                 | 34.3 us                                                      | 35.9 us: 1.05x slower                                                  |
| sqlglot_optimize           | 74.7 ms                                                      | 79.0 ms: 1.06x slower                                                  |
| mako                       | 15.9 ms                                                      | 16.9 ms: 1.06x slower                                                  |
| pickle_pure_python         | 416 us                                                       | 441 us: 1.06x slower                                                   |
| regex_v8                   | 32.8 ms                                                      | 35.0 ms: 1.07x slower                                                  |
| logging_silent             | 130 ns                                                       | 139 ns: 1.07x slower                                                   |
| bench_thread_pool          | 2.89 ms                                                      | 3.13 ms: 1.08x slower                                                  |
| nbody                      | 119 ms                                                       | 129 ms: 1.08x slower                                                   |
| django_template            | 44.3 ms                                                      | 48.1 ms: 1.09x slower                                                  |
| hexiom                     | 8.11 ms                                                      | 8.87 ms: 1.09x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 16.0 ms: 1.13x slower                                                  |
| python_startup             | 22.4 ms                                                      | 26.0 ms: 1.16x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 3.90 ms: 1.62x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 9.27 ms: 1.63x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 94.0 ms: 5.03x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.03x faster                                                           |

Benchmark hidden because not significant (28): pidigits, regex_compile, sqlglot_transpile, typing_runtime_protocols, nqueens, scimark_monte_carlo, genshi_text, asyncio_websockets, html5lib, async_generators, pprint_pformat, generators, xml_etree_process, coroutines, meteor_contest, float, sympy_str, raytrace, comprehensions, unpickle_pure_python, 2to3, scimark_lu, json, sympy_expand, deltablue, chaos, pycparser, coverage
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241224-3.14.0a3+-30efede/bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.051x faster

# HPT report

- Reliability score: 99.94% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.13x