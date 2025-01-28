# Results vs. 3.13.0rc2

- fork: python
- ref: 1c3bb200da77f9df30af
- machine: linux-x86_64
- commit hash: 1c3bb20
- commit date: 2025-01-28
- overall geometric mean: 1.131x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 550 ms: 1.24x slower                                                   |
| html5lib       | 92.6 ms                                                      | 114 ms: 1.23x slower                                                   |
| Geometric mean | (ref)                                                        | 1.15x slower                                                           |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 859 ms: 1.63x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 897 ms: 1.55x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 351 ms: 1.44x faster                                                   |
| async_tree_none            | 572 ms                                                       | 448 ms: 1.28x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 563 ms: 1.26x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 542 ms: 1.24x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 697 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 794 ms: 1.12x faster                                                   |
| async_generators           | 567 ms                                                       | 618 ms: 1.09x slower                                                   |
| coroutines                 | 30.9 ms                                                      | 34.9 ms: 1.13x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.21x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 110 ms: 1.06x faster                                                   |
| nbody          | 119 ms                                                       | 183 ms: 1.54x slower                                                   |
| Geometric mean | (ref)                                                        | 1.12x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 282 ms                                                       | 293 ms: 1.04x slower                                                   |
| regex_v8       | 32.8 ms                                                      | 37.5 ms: 1.14x slower                                                  |
| regex_compile  | 182 ms                                                       | 225 ms: 1.24x slower                                                   |
| Geometric mean | (ref)                                                        | 1.10x slower                                                           |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 162 ms: 1.09x faster                                                   |
| tomli_loads          | 2.78 sec                                                     | 3.15 sec: 1.13x slower                                                 |
| xml_etree_generate   | 122 ms                                                       | 140 ms: 1.14x slower                                                   |
| pickle_pure_python   | 416 us                                                       | 505 us: 1.21x slower                                                   |
| xml_etree_process    | 85.9 ms                                                      | 107 ms: 1.25x slower                                                   |
| json_loads           | 34.3 us                                                      | 43.1 us: 1.26x slower                                                  |
| unpickle_pure_python | 290 us                                                       | 376 us: 1.29x slower                                                   |
| json_dumps           | 14.1 ms                                                      | 19.7 ms: 1.39x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.17x slower                                                           |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 21.7 ms: 1.42x slower                                                  |
| python_startup         | 22.4 ms                                                      | 31.9 ms: 1.42x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.42x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                      | 37.8 ms: 1.19x slower                                                  |
| genshi_xml      | 72.1 ms                                                      | 92.3 ms: 1.28x slower                                                  |
| django_template | 44.3 ms                                                      | 62.4 ms: 1.41x slower                                                  |
| mako            | 15.9 ms                                                      | 25.0 ms: 1.57x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.36x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 859 ms: 1.63x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 897 ms: 1.55x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 351 ms: 1.44x faster                                                   |
| async_tree_none            | 572 ms                                                       | 448 ms: 1.28x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 563 ms: 1.26x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 542 ms: 1.24x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 697 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 794 ms: 1.12x faster                                                   |
| xml_etree_iterparse        | 177 ms                                                       | 162 ms: 1.09x faster                                                   |
| sqlite_synth               | 3.99 us                                                      | 3.65 us: 1.09x faster                                                  |
| float                      | 116 ms                                                       | 110 ms: 1.06x faster                                                   |
| regex_dna                  | 282 ms                                                       | 293 ms: 1.04x slower                                                   |
| sympy_integrate            | 30.2 ms                                                      | 31.9 ms: 1.06x slower                                                  |
| pathlib                    | 29.9 ms                                                      | 31.9 ms: 1.07x slower                                                  |
| pycparser                  | 1.57 sec                                                     | 1.69 sec: 1.07x slower                                                 |
| spectral_norm              | 157 ms                                                       | 170 ms: 1.09x slower                                                   |
| async_generators           | 567 ms                                                       | 618 ms: 1.09x slower                                                   |
| telco                      | 12.2 ms                                                      | 13.3 ms: 1.09x slower                                                  |
| scimark_sor                | 179 ms                                                       | 197 ms: 1.10x slower                                                   |
| nqueens                    | 112 ms                                                       | 124 ms: 1.11x slower                                                   |
| mdp                        | 3.80 sec                                                     | 4.26 sec: 1.12x slower                                                 |
| coroutines                 | 30.9 ms                                                      | 34.9 ms: 1.13x slower                                                  |
| tomli_loads                | 2.78 sec                                                     | 3.15 sec: 1.13x slower                                                 |
| generators                 | 40.0 ms                                                      | 45.6 ms: 1.14x slower                                                  |
| xml_etree_generate         | 122 ms                                                       | 140 ms: 1.14x slower                                                   |
| regex_v8                   | 32.8 ms                                                      | 37.5 ms: 1.14x slower                                                  |
| deepcopy_memo              | 50.1 us                                                      | 57.6 us: 1.15x slower                                                  |
| sqlglot_optimize           | 74.7 ms                                                      | 86.8 ms: 1.16x slower                                                  |
| genshi_text                | 31.7 ms                                                      | 37.8 ms: 1.19x slower                                                  |
| pprint_pformat             | 1.94 sec                                                     | 2.35 sec: 1.21x slower                                                 |
| pickle_pure_python         | 416 us                                                       | 505 us: 1.21x slower                                                   |
| go                         | 191 ms                                                       | 232 ms: 1.22x slower                                                   |
| pprint_safe_repr           | 987 ms                                                       | 1.21 sec: 1.22x slower                                                 |
| scimark_fft                | 473 ms                                                       | 580 ms: 1.23x slower                                                   |
| html5lib                   | 92.6 ms                                                      | 114 ms: 1.23x slower                                                   |
| crypto_pyaes               | 100 ms                                                       | 123 ms: 1.23x slower                                                   |
| richards                   | 65.5 ms                                                      | 80.5 ms: 1.23x slower                                                  |
| fannkuch                   | 547 ms                                                       | 673 ms: 1.23x slower                                                   |
| scimark_lu                 | 146 ms                                                       | 181 ms: 1.23x slower                                                   |
| deepcopy_reduce            | 4.10 us                                                      | 5.06 us: 1.24x slower                                                  |
| 2to3                       | 445 ms                                                       | 550 ms: 1.24x slower                                                   |
| regex_compile              | 182 ms                                                       | 225 ms: 1.24x slower                                                   |
| xml_etree_process          | 85.9 ms                                                      | 107 ms: 1.25x slower                                                   |
| thrift                     | 1.10 ms                                                      | 1.37 ms: 1.25x slower                                                  |
| richards_super             | 73.2 ms                                                      | 91.4 ms: 1.25x slower                                                  |
| json_loads                 | 34.3 us                                                      | 43.1 us: 1.26x slower                                                  |
| dulwich_log                | 93.7 ms                                                      | 118 ms: 1.26x slower                                                   |
| pyflate                    | 664 ms                                                       | 840 ms: 1.27x slower                                                   |
| logging_silent             | 130 ns                                                       | 165 ns: 1.27x slower                                                   |
| bpe_tokeniser              | 6.28 sec                                                     | 7.96 sec: 1.27x slower                                                 |
| chaos                      | 83.6 ms                                                      | 106 ms: 1.27x slower                                                   |
| sympy_str                  | 379 ms                                                       | 483 ms: 1.27x slower                                                   |
| logging_format             | 9.24 us                                                      | 11.8 us: 1.28x slower                                                  |
| genshi_xml                 | 72.1 ms                                                      | 92.3 ms: 1.28x slower                                                  |
| sqlglot_transpile          | 2.20 ms                                                      | 2.83 ms: 1.29x slower                                                  |
| coverage                   | 107 ms                                                       | 139 ms: 1.29x slower                                                   |
| unpickle_pure_python       | 290 us                                                       | 376 us: 1.29x slower                                                   |
| scimark_monte_carlo        | 90.6 ms                                                      | 119 ms: 1.32x slower                                                   |
| create_gc_cycles           | 2.41 ms                                                      | 3.19 ms: 1.32x slower                                                  |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 8.94 ms: 1.32x slower                                                  |
| sympy_expand               | 601 ms                                                       | 798 ms: 1.33x slower                                                   |
| sqlglot_normalize          | 140 ms                                                       | 186 ms: 1.33x slower                                                   |
| bench_thread_pool          | 2.89 ms                                                      | 3.88 ms: 1.34x slower                                                  |
| json                       | 6.51 ms                                                      | 8.76 ms: 1.35x slower                                                  |
| meteor_contest             | 150 ms                                                       | 206 ms: 1.37x slower                                                   |
| typing_runtime_protocols   | 226 us                                                       | 310 us: 1.38x slower                                                   |
| logging_simple             | 8.56 us                                                      | 11.8 us: 1.38x slower                                                  |
| sqlglot_parse              | 1.76 ms                                                      | 2.44 ms: 1.39x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 19.7 ms: 1.39x slower                                                  |
| comprehensions             | 22.2 us                                                      | 31.2 us: 1.40x slower                                                  |
| django_template            | 44.3 ms                                                      | 62.4 ms: 1.41x slower                                                  |
| python_startup_no_site     | 15.3 ms                                                      | 21.7 ms: 1.42x slower                                                  |
| sympy_sum                  | 210 ms                                                       | 299 ms: 1.42x slower                                                   |
| python_startup             | 22.4 ms                                                      | 31.9 ms: 1.42x slower                                                  |
| raytrace                   | 344 ms                                                       | 493 ms: 1.43x slower                                                   |
| deltablue                  | 4.44 ms                                                      | 6.71 ms: 1.51x slower                                                  |
| hexiom                     | 8.11 ms                                                      | 12.4 ms: 1.53x slower                                                  |
| nbody                      | 119 ms                                                       | 183 ms: 1.54x slower                                                   |
| mako                       | 15.9 ms                                                      | 25.0 ms: 1.57x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 9.07 ms: 1.59x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 95.7 ms: 5.12x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.19x slower                                                           |

Benchmark hidden because not significant (7): pidigits, regex_effbot, docutils, asyncio_websockets, xml_etree_parse, pylint, deepcopy
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250128-3.14.0a4+-1c3bb20-NOGIL/bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.131x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.13x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.34x