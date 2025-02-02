# Results vs. 3.13.0rc2

- fork: python
- ref: cf4c4ecc26c7e3b89f2e
- machine: linux-x86_64
- commit hash: cf4c4ec
- commit date: 2025-02-01
- overall geometric mean: 1.091x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 562 ms: 1.26x slower                                                   |
| html5lib       | 92.6 ms                                                      | 98.6 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                        | 1.11x slower                                                           |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 801 ms: 1.75x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 838 ms: 1.65x faster                                                   |
| async_tree_none            | 572 ms                                                       | 406 ms: 1.41x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 511 ms: 1.39x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 506 ms: 1.33x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 383 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 648 ms: 1.31x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 795 ms: 1.12x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 817 ms: 1.07x slower                                                   |
| coroutines                 | 30.9 ms                                                      | 34.3 ms: 1.11x slower                                                  |
| asyncio_tcp_ssl            | 2.77 sec                                                     | 3.50 sec: 1.26x slower                                                 |
| asyncio_tcp                | 948 ms                                                       | 1.21 sec: 1.28x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.17x faster                                                           |

Benchmark hidden because not significant (1): async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 108 ms: 1.08x faster                                                   |
| nbody          | 119 ms                                                       | 194 ms: 1.63x slower                                                   |
| Geometric mean | (ref)                                                        | 1.13x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.48 ms: 1.06x faster                                                  |
| regex_v8       | 32.8 ms                                                      | 36.0 ms: 1.10x slower                                                  |
| regex_dna      | 282 ms                                                       | 310 ms: 1.10x slower                                                   |
| regex_compile  | 182 ms                                                       | 211 ms: 1.16x slower                                                   |
| Geometric mean | (ref)                                                        | 1.07x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 150 ms: 1.18x faster                                                   |
| pickle_list          | 6.86 us                                                      | 7.27 us: 1.06x slower                                                  |
| pickle_pure_python   | 416 us                                                       | 464 us: 1.11x slower                                                   |
| tomli_loads          | 2.78 sec                                                     | 3.13 sec: 1.13x slower                                                 |
| pickle               | 15.1 us                                                      | 17.4 us: 1.15x slower                                                  |
| unpickle_list        | 6.68 us                                                      | 7.84 us: 1.17x slower                                                  |
| xml_etree_process    | 85.9 ms                                                      | 101 ms: 1.18x slower                                                   |
| json_dumps           | 14.1 ms                                                      | 16.8 ms: 1.19x slower                                                  |
| xml_etree_generate   | 122 ms                                                       | 147 ms: 1.20x slower                                                   |
| unpickle_pure_python | 290 us                                                       | 357 us: 1.23x slower                                                   |
| json_loads           | 34.3 us                                                      | 47.2 us: 1.38x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.11x slower                                                           |

Benchmark hidden because not significant (3): pickle_dict, xml_etree_parse, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 19.6 ms: 1.28x slower                                                  |
| python_startup         | 22.4 ms                                                      | 31.6 ms: 1.41x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.34x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                      | 38.3 ms: 1.21x slower                                                  |
| genshi_xml      | 72.1 ms                                                      | 87.5 ms: 1.21x slower                                                  |
| django_template | 44.3 ms                                                      | 56.1 ms: 1.27x slower                                                  |
| mako            | 15.9 ms                                                      | 23.5 ms: 1.48x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.29x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 801 ms: 1.75x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 838 ms: 1.65x faster                                                   |
| gc_traversal               | 5.70 ms                                                      | 3.76 ms: 1.52x faster                                                  |
| async_tree_none            | 572 ms                                                       | 406 ms: 1.41x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 511 ms: 1.39x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 506 ms: 1.33x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 383 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 648 ms: 1.31x faster                                                   |
| deepcopy                   | 498 us                                                       | 403 us: 1.24x faster                                                   |
| xml_etree_iterparse        | 177 ms                                                       | 150 ms: 1.18x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 795 ms: 1.12x faster                                                   |
| float                      | 116 ms                                                       | 108 ms: 1.08x faster                                                   |
| regex_effbot               | 4.74 ms                                                      | 4.48 ms: 1.06x faster                                                  |
| pycparser                  | 1.57 sec                                                     | 1.66 sec: 1.05x slower                                                 |
| pickle_list                | 6.86 us                                                      | 7.27 us: 1.06x slower                                                  |
| html5lib                   | 92.6 ms                                                      | 98.6 ms: 1.06x slower                                                  |
| asyncio_websockets         | 766 ms                                                       | 817 ms: 1.07x slower                                                   |
| deepcopy_reduce            | 4.10 us                                                      | 4.38 us: 1.07x slower                                                  |
| logging_simple             | 8.56 us                                                      | 9.29 us: 1.09x slower                                                  |
| dulwich_log                | 93.7 ms                                                      | 102 ms: 1.09x slower                                                   |
| pathlib                    | 29.9 ms                                                      | 32.6 ms: 1.09x slower                                                  |
| pprint_safe_repr           | 987 ms                                                       | 1.08 sec: 1.10x slower                                                 |
| regex_v8                   | 32.8 ms                                                      | 36.0 ms: 1.10x slower                                                  |
| generators                 | 40.0 ms                                                      | 44.0 ms: 1.10x slower                                                  |
| regex_dna                  | 282 ms                                                       | 310 ms: 1.10x slower                                                   |
| mdp                        | 3.80 sec                                                     | 4.21 sec: 1.11x slower                                                 |
| coroutines                 | 30.9 ms                                                      | 34.3 ms: 1.11x slower                                                  |
| scimark_sor                | 179 ms                                                       | 198 ms: 1.11x slower                                                   |
| pickle_pure_python         | 416 us                                                       | 464 us: 1.11x slower                                                   |
| tomli_loads                | 2.78 sec                                                     | 3.13 sec: 1.13x slower                                                 |
| pyflate                    | 664 ms                                                       | 750 ms: 1.13x slower                                                   |
| scimark_fft                | 473 ms                                                       | 536 ms: 1.13x slower                                                   |
| pickle                     | 15.1 us                                                      | 17.4 us: 1.15x slower                                                  |
| regex_compile              | 182 ms                                                       | 211 ms: 1.16x slower                                                   |
| deepcopy_memo              | 50.1 us                                                      | 58.3 us: 1.16x slower                                                  |
| richards                   | 65.5 ms                                                      | 76.4 ms: 1.17x slower                                                  |
| sympy_sum                  | 210 ms                                                       | 246 ms: 1.17x slower                                                   |
| unpickle_list              | 6.68 us                                                      | 7.84 us: 1.17x slower                                                  |
| xml_etree_process          | 85.9 ms                                                      | 101 ms: 1.18x slower                                                   |
| richards_super             | 73.2 ms                                                      | 86.8 ms: 1.19x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 16.8 ms: 1.19x slower                                                  |
| pprint_pformat             | 1.94 sec                                                     | 2.32 sec: 1.19x slower                                                 |
| sympy_integrate            | 30.2 ms                                                      | 36.2 ms: 1.20x slower                                                  |
| xml_etree_generate         | 122 ms                                                       | 147 ms: 1.20x slower                                                   |
| bpe_tokeniser              | 6.28 sec                                                     | 7.57 sec: 1.20x slower                                                 |
| fannkuch                   | 547 ms                                                       | 660 ms: 1.21x slower                                                   |
| genshi_text                | 31.7 ms                                                      | 38.3 ms: 1.21x slower                                                  |
| scimark_monte_carlo        | 90.6 ms                                                      | 110 ms: 1.21x slower                                                   |
| genshi_xml                 | 72.1 ms                                                      | 87.5 ms: 1.21x slower                                                  |
| logging_silent             | 130 ns                                                       | 158 ns: 1.22x slower                                                   |
| meteor_contest             | 150 ms                                                       | 183 ms: 1.22x slower                                                   |
| nqueens                    | 112 ms                                                       | 136 ms: 1.22x slower                                                   |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 8.26 ms: 1.22x slower                                                  |
| scimark_lu                 | 146 ms                                                       | 180 ms: 1.23x slower                                                   |
| json                       | 6.51 ms                                                      | 8.00 ms: 1.23x slower                                                  |
| unpickle_pure_python       | 290 us                                                       | 357 us: 1.23x slower                                                   |
| sympy_expand               | 601 ms                                                       | 741 ms: 1.23x slower                                                   |
| typing_runtime_protocols   | 226 us                                                       | 280 us: 1.24x slower                                                   |
| sqlglot_normalize          | 140 ms                                                       | 173 ms: 1.24x slower                                                   |
| create_gc_cycles           | 2.41 ms                                                      | 3.04 ms: 1.26x slower                                                  |
| 2to3                       | 445 ms                                                       | 562 ms: 1.26x slower                                                   |
| asyncio_tcp_ssl            | 2.77 sec                                                     | 3.50 sec: 1.26x slower                                                 |
| django_template            | 44.3 ms                                                      | 56.1 ms: 1.27x slower                                                  |
| crypto_pyaes               | 100 ms                                                       | 128 ms: 1.27x slower                                                   |
| sympy_str                  | 379 ms                                                       | 483 ms: 1.27x slower                                                   |
| asyncio_tcp                | 948 ms                                                       | 1.21 sec: 1.28x slower                                                 |
| python_startup_no_site     | 15.3 ms                                                      | 19.6 ms: 1.28x slower                                                  |
| comprehensions             | 22.2 us                                                      | 28.6 us: 1.29x slower                                                  |
| chaos                      | 83.6 ms                                                      | 108 ms: 1.29x slower                                                   |
| sqlglot_optimize           | 74.7 ms                                                      | 97.0 ms: 1.30x slower                                                  |
| sqlglot_transpile          | 2.20 ms                                                      | 2.90 ms: 1.32x slower                                                  |
| thrift                     | 1.10 ms                                                      | 1.45 ms: 1.32x slower                                                  |
| coverage                   | 107 ms                                                       | 143 ms: 1.33x slower                                                   |
| hexiom                     | 8.11 ms                                                      | 10.8 ms: 1.33x slower                                                  |
| logging_format             | 9.24 us                                                      | 12.6 us: 1.36x slower                                                  |
| json_loads                 | 34.3 us                                                      | 47.2 us: 1.38x slower                                                  |
| raytrace                   | 344 ms                                                       | 480 ms: 1.39x slower                                                   |
| python_startup             | 22.4 ms                                                      | 31.6 ms: 1.41x slower                                                  |
| sqlglot_parse              | 1.76 ms                                                      | 2.55 ms: 1.45x slower                                                  |
| mako                       | 15.9 ms                                                      | 23.5 ms: 1.48x slower                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 4.49 ms: 1.56x slower                                                  |
| deltablue                  | 4.44 ms                                                      | 7.02 ms: 1.58x slower                                                  |
| nbody                      | 119 ms                                                       | 194 ms: 1.63x slower                                                   |
| bench_mp_pool              | 18.7 ms                                                      | 85.5 ms: 4.57x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.13x slower                                                           |

Benchmark hidden because not significant (12): pidigits, pickle_dict, go, unpack_sequence, telco, async_generators, xml_etree_parse, spectral_norm, docutils, sqlite_synth, unpickle, pylint
Ignored benchmarks (6) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, tornado_http
Ignored benchmarks (8) of results/bm-20250201-3.14.0a4+-cf4c4ec-NOGIL/bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.091x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.34x