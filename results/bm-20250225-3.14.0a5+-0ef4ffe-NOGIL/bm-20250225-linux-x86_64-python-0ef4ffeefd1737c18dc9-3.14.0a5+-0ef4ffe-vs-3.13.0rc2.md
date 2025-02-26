# Results vs. 3.13.0rc2

- fork: python
- ref: 0ef4ffeefd1737c18dc9
- machine: linux-x86_64
- commit hash: 0ef4ffe
- commit date: 2025-02-25
- overall geometric mean: 1.048x slower
- HPT reliability: 99.73%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 514 ms: 1.15x slower                                                   |
| docutils       | 4.01 sec                                                     | 4.22 sec: 1.05x slower                                                 |
| html5lib       | 92.6 ms                                                      | 98.2 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                        | 1.09x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 726 ms: 1.93x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 822 ms: 1.69x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 334 ms: 1.51x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 459 ms: 1.46x faster                                                   |
| async_tree_none            | 572 ms                                                       | 406 ms: 1.41x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 524 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 681 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 758 ms: 1.17x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 742 ms: 1.03x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.32x faster                                                           |

Benchmark hidden because not significant (2): async_generators, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 103 ms: 1.12x faster                                                   |
| nbody          | 119 ms                                                       | 174 ms: 1.46x slower                                                   |
| Geometric mean | (ref)                                                        | 1.09x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.50 ms: 1.05x faster                                                  |
| regex_compile  | 182 ms                                                       | 197 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                        | 1.00x faster                                                           |

Benchmark hidden because not significant (2): regex_v8, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 147 ms: 1.20x faster                                                   |
| unpickle_pure_python | 290 us                                                       | 315 us: 1.09x slower                                                   |
| tomli_loads          | 2.78 sec                                                     | 3.07 sec: 1.10x slower                                                 |
| pickle_pure_python   | 416 us                                                       | 464 us: 1.11x slower                                                   |
| json_dumps           | 14.1 ms                                                      | 17.8 ms: 1.26x slower                                                  |
| json_loads           | 34.3 us                                                      | 43.4 us: 1.27x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.07x slower                                                           |

Benchmark hidden because not significant (3): xml_etree_parse, xml_etree_generate, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 21.3 ms: 1.39x slower                                                  |
| python_startup         | 22.4 ms                                                      | 33.2 ms: 1.48x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.44x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 84.1 ms: 1.17x slower                                                  |
| genshi_text     | 31.7 ms                                                      | 37.2 ms: 1.18x slower                                                  |
| django_template | 44.3 ms                                                      | 55.1 ms: 1.24x slower                                                  |
| mako            | 15.9 ms                                                      | 23.2 ms: 1.46x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.26x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 726 ms: 1.93x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 822 ms: 1.69x faster                                                   |
| gc_traversal               | 5.70 ms                                                      | 3.72 ms: 1.53x faster                                                  |
| async_tree_none_tg         | 504 ms                                                       | 334 ms: 1.51x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 459 ms: 1.46x faster                                                   |
| async_tree_none            | 572 ms                                                       | 406 ms: 1.41x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 524 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 681 ms: 1.25x faster                                                   |
| deepcopy                   | 498 us                                                       | 404 us: 1.23x faster                                                   |
| xml_etree_iterparse        | 177 ms                                                       | 147 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 758 ms: 1.17x faster                                                   |
| sqlite_synth               | 3.99 us                                                      | 3.44 us: 1.16x faster                                                  |
| float                      | 116 ms                                                       | 103 ms: 1.12x faster                                                   |
| spectral_norm              | 157 ms                                                       | 147 ms: 1.06x faster                                                   |
| go                         | 191 ms                                                       | 181 ms: 1.05x faster                                                   |
| regex_effbot               | 4.74 ms                                                      | 4.50 ms: 1.05x faster                                                  |
| asyncio_websockets         | 766 ms                                                       | 742 ms: 1.03x faster                                                   |
| pycparser                  | 1.57 sec                                                     | 1.52 sec: 1.03x faster                                                 |
| deepcopy_reduce            | 4.10 us                                                      | 4.25 us: 1.04x slower                                                  |
| docutils                   | 4.01 sec                                                     | 4.22 sec: 1.05x slower                                                 |
| html5lib                   | 92.6 ms                                                      | 98.2 ms: 1.06x slower                                                  |
| logging_silent             | 130 ns                                                       | 138 ns: 1.06x slower                                                   |
| deepcopy_memo              | 50.1 us                                                      | 53.5 us: 1.07x slower                                                  |
| sqlglot_optimize           | 74.7 ms                                                      | 80.3 ms: 1.08x slower                                                  |
| logging_simple             | 8.56 us                                                      | 9.25 us: 1.08x slower                                                  |
| regex_compile              | 182 ms                                                       | 197 ms: 1.08x slower                                                   |
| mdp                        | 3.80 sec                                                     | 4.11 sec: 1.08x slower                                                 |
| thrift                     | 1.10 ms                                                      | 1.19 ms: 1.08x slower                                                  |
| sqlglot_normalize          | 140 ms                                                       | 152 ms: 1.09x slower                                                   |
| unpickle_pure_python       | 290 us                                                       | 315 us: 1.09x slower                                                   |
| pathlib                    | 29.9 ms                                                      | 32.5 ms: 1.09x slower                                                  |
| richards                   | 65.5 ms                                                      | 71.2 ms: 1.09x slower                                                  |
| tomli_loads                | 2.78 sec                                                     | 3.07 sec: 1.10x slower                                                 |
| logging_format             | 9.24 us                                                      | 10.2 us: 1.11x slower                                                  |
| pickle_pure_python         | 416 us                                                       | 464 us: 1.11x slower                                                   |
| sympy_integrate            | 30.2 ms                                                      | 33.8 ms: 1.12x slower                                                  |
| chaos                      | 83.6 ms                                                      | 94.1 ms: 1.13x slower                                                  |
| scimark_fft                | 473 ms                                                       | 533 ms: 1.13x slower                                                   |
| sympy_str                  | 379 ms                                                       | 430 ms: 1.13x slower                                                   |
| dulwich_log                | 93.7 ms                                                      | 106 ms: 1.14x slower                                                   |
| richards_super             | 73.2 ms                                                      | 83.4 ms: 1.14x slower                                                  |
| json                       | 6.51 ms                                                      | 7.46 ms: 1.15x slower                                                  |
| meteor_contest             | 150 ms                                                       | 173 ms: 1.15x slower                                                   |
| pyflate                    | 664 ms                                                       | 765 ms: 1.15x slower                                                   |
| 2to3                       | 445 ms                                                       | 514 ms: 1.15x slower                                                   |
| pprint_safe_repr           | 987 ms                                                       | 1.15 sec: 1.16x slower                                                 |
| sqlglot_transpile          | 2.20 ms                                                      | 2.55 ms: 1.16x slower                                                  |
| sympy_sum                  | 210 ms                                                       | 245 ms: 1.16x slower                                                   |
| genshi_xml                 | 72.1 ms                                                      | 84.1 ms: 1.17x slower                                                  |
| generators                 | 40.0 ms                                                      | 47.0 ms: 1.18x slower                                                  |
| genshi_text                | 31.7 ms                                                      | 37.2 ms: 1.18x slower                                                  |
| pprint_pformat             | 1.94 sec                                                     | 2.29 sec: 1.18x slower                                                 |
| sympy_expand               | 601 ms                                                       | 711 ms: 1.18x slower                                                   |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 8.05 ms: 1.19x slower                                                  |
| scimark_monte_carlo        | 90.6 ms                                                      | 108 ms: 1.19x slower                                                   |
| crypto_pyaes               | 100 ms                                                       | 120 ms: 1.20x slower                                                   |
| bpe_tokeniser              | 6.28 sec                                                     | 7.55 sec: 1.20x slower                                                 |
| scimark_lu                 | 146 ms                                                       | 177 ms: 1.21x slower                                                   |
| comprehensions             | 22.2 us                                                      | 26.9 us: 1.21x slower                                                  |
| deltablue                  | 4.44 ms                                                      | 5.40 ms: 1.22x slower                                                  |
| nqueens                    | 112 ms                                                       | 137 ms: 1.23x slower                                                   |
| django_template            | 44.3 ms                                                      | 55.1 ms: 1.24x slower                                                  |
| fannkuch                   | 547 ms                                                       | 684 ms: 1.25x slower                                                   |
| json_dumps                 | 14.1 ms                                                      | 17.8 ms: 1.26x slower                                                  |
| sqlglot_parse              | 1.76 ms                                                      | 2.22 ms: 1.27x slower                                                  |
| json_loads                 | 34.3 us                                                      | 43.4 us: 1.27x slower                                                  |
| typing_runtime_protocols   | 226 us                                                       | 289 us: 1.28x slower                                                   |
| raytrace                   | 344 ms                                                       | 443 ms: 1.29x slower                                                   |
| hexiom                     | 8.11 ms                                                      | 10.5 ms: 1.29x slower                                                  |
| coverage                   | 107 ms                                                       | 146 ms: 1.36x slower                                                   |
| python_startup_no_site     | 15.3 ms                                                      | 21.3 ms: 1.39x slower                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 4.06 ms: 1.41x slower                                                  |
| mako                       | 15.9 ms                                                      | 23.2 ms: 1.46x slower                                                  |
| nbody                      | 119 ms                                                       | 174 ms: 1.46x slower                                                   |
| python_startup             | 22.4 ms                                                      | 33.2 ms: 1.48x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 87.6 ms: 4.69x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.08x slower                                                           |

Benchmark hidden because not significant (12): xml_etree_parse, pylint, regex_v8, async_generators, scimark_sor, regex_dna, pidigits, coroutines, telco, xml_etree_generate, create_gc_cycles, xml_etree_process
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250225-3.14.0a5+-0ef4ffe-NOGIL/bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.048x slower

# HPT report

- Reliability score: 99.73% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.35x