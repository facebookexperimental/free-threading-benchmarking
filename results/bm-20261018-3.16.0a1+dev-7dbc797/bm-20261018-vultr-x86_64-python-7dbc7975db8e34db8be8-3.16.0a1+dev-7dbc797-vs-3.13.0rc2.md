# Results vs. 3.13.0rc2

- fork: python
- ref: 7dbc7975db8e34db8be8
- machine: linux-x86_64
- commit hash: 7dbc797
- commit date: 2026-10-18
- overall geometric mean: 1.042x faster
- HPT reliability: 99.77%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261018-vultr-x86_64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 256 ms: 1.01x faster                                                      |
| docutils       | 2.63 sec                                                               | 2.36 sec: 1.11x faster                                                    |
| html5lib       | 68.6 ms                                                                | 58.6 ms: 1.17x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.10x faster                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261018-vultr-x86_64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io              | 881 ms                                                                 | 658 ms: 1.34x faster                                                      |
| async_tree_memoization     | 459 ms                                                                 | 346 ms: 1.33x faster                                                      |
| async_tree_io_tg           | 901 ms                                                                 | 693 ms: 1.30x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 516 ms: 1.29x faster                                                      |
| async_tree_none            | 353 ms                                                                 | 276 ms: 1.28x faster                                                      |
| async_tree_memoization_tg  | 410 ms                                                                 | 344 ms: 1.19x faster                                                      |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 533 ms: 1.19x faster                                                      |
| async_tree_none_tg         | 333 ms                                                                 | 282 ms: 1.18x faster                                                      |
| async_generators           | 375 ms                                                                 | 351 ms: 1.07x faster                                                      |
| coroutines                 | 23.3 ms                                                                | 23.4 ms: 1.00x slower                                                     |
| asyncio_websockets         | 517 ms                                                                 | 544 ms: 1.05x slower                                                      |
| Geometric mean             | (ref)                                                                  | 1.19x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261018-vultr-x86_64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 184 ms: 1.18x faster                                                      |
| float          | 76.7 ms                                                                | 72.9 ms: 1.05x faster                                                     |
| nbody          | 85.3 ms                                                                | 93.2 ms: 1.09x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261018-vultr-x86_64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.55 ms: 1.26x faster                                                     |
| regex_v8       | 23.2 ms                                                                | 21.3 ms: 1.09x faster                                                     |
| regex_dna      | 189 ms                                                                 | 175 ms: 1.08x faster                                                      |
| regex_compile  | 131 ms                                                                 | 150 ms: 1.14x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261018-vultr-x86_64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json_dumps           | 10.6 ms                                                                | 9.08 ms: 1.17x faster                                                     |
| tomli_loads          | 2.01 sec                                                               | 1.82 sec: 1.10x faster                                                    |
| xml_etree_iterparse  | 94.4 ms                                                                | 92.2 ms: 1.02x faster                                                     |
| json_loads           | 27.3 us                                                                | 27.2 us: 1.01x faster                                                     |
| unpickle_pure_python | 208 us                                                                 | 210 us: 1.01x slower                                                      |
| xml_etree_generate   | 85.4 ms                                                                | 88.6 ms: 1.04x slower                                                     |
| pickle_pure_python   | 292 us                                                                 | 303 us: 1.04x slower                                                      |
| xml_etree_parse      | 136 ms                                                                 | 143 ms: 1.06x slower                                                      |
| xml_etree_process    | 59.2 ms                                                                | 62.7 ms: 1.06x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261018-vultr-x86_64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 7.52 ms: 1.01x slower                                                     |
| python_startup         | 11.0 ms                                                                | 12.6 ms: 1.15x slower                                                     |
| Geometric mean         | (ref)                                                                  | 1.08x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261018-vultr-x86_64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako            | 11.2 ms                                                                | 12.1 ms: 1.07x slower                                                     |
| django_template | 34.2 ms                                                                | 37.1 ms: 1.09x slower                                                     |
| Geometric mean  | (ref)                                                                  | 1.08x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261018-vultr-x86_64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pylint                     | 317 ms                                                                 | 113 ms: 2.81x faster                                                      |
| mdp                        | 2.34 sec                                                               | 1.15 sec: 2.04x faster                                                    |
| deepcopy                   | 357 us                                                                 | 230 us: 1.55x faster                                                      |
| deepcopy_memo              | 38.1 us                                                                | 27.3 us: 1.40x faster                                                     |
| go                         | 141 ms                                                                 | 103 ms: 1.37x faster                                                      |
| async_tree_io              | 881 ms                                                                 | 658 ms: 1.34x faster                                                      |
| async_tree_memoization     | 459 ms                                                                 | 346 ms: 1.33x faster                                                      |
| async_tree_io_tg           | 901 ms                                                                 | 693 ms: 1.30x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 516 ms: 1.29x faster                                                      |
| typing_runtime_protocols   | 156 us                                                                 | 121 us: 1.29x faster                                                      |
| async_tree_none            | 353 ms                                                                 | 276 ms: 1.28x faster                                                      |
| regex_effbot               | 3.21 ms                                                                | 2.55 ms: 1.26x faster                                                     |
| scimark_sor                | 134 ms                                                                 | 108 ms: 1.23x faster                                                      |
| spectral_norm              | 108 ms                                                                 | 87.4 ms: 1.23x faster                                                     |
| deepcopy_reduce            | 3.12 us                                                                | 2.56 us: 1.22x faster                                                     |
| async_tree_memoization_tg  | 410 ms                                                                 | 344 ms: 1.19x faster                                                      |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 533 ms: 1.19x faster                                                      |
| async_tree_none_tg         | 333 ms                                                                 | 282 ms: 1.18x faster                                                      |
| pidigits                   | 216 ms                                                                 | 184 ms: 1.18x faster                                                      |
| json_dumps                 | 10.6 ms                                                                | 9.08 ms: 1.17x faster                                                     |
| html5lib                   | 68.6 ms                                                                | 58.6 ms: 1.17x faster                                                     |
| pyflate                    | 449 ms                                                                 | 387 ms: 1.16x faster                                                      |
| scimark_fft                | 348 ms                                                                 | 311 ms: 1.12x faster                                                      |
| docutils                   | 2.63 sec                                                               | 2.36 sec: 1.11x faster                                                    |
| dulwich_log                | 74.5 ms                                                                | 67.2 ms: 1.11x faster                                                     |
| tomli_loads                | 2.01 sec                                                               | 1.82 sec: 1.10x faster                                                    |
| pathlib                    | 19.3 ms                                                                | 17.6 ms: 1.10x faster                                                     |
| regex_v8                   | 23.2 ms                                                                | 21.3 ms: 1.09x faster                                                     |
| regex_dna                  | 189 ms                                                                 | 175 ms: 1.08x faster                                                      |
| async_generators           | 375 ms                                                                 | 351 ms: 1.07x faster                                                      |
| bpe_tokeniser              | 4.46 sec                                                               | 4.23 sec: 1.05x faster                                                    |
| scimark_monte_carlo        | 65.8 ms                                                                | 62.5 ms: 1.05x faster                                                     |
| float                      | 76.7 ms                                                                | 72.9 ms: 1.05x faster                                                     |
| comprehensions             | 16.6 us                                                                | 15.8 us: 1.05x faster                                                     |
| hexiom                     | 5.95 ms                                                                | 5.67 ms: 1.05x faster                                                     |
| chaos                      | 56.3 ms                                                                | 54.0 ms: 1.04x faster                                                     |
| logging_format             | 6.92 us                                                                | 6.64 us: 1.04x faster                                                     |
| logging_silent             | 98.2 ns                                                                | 94.4 ns: 1.04x faster                                                     |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.57 ms: 1.04x faster                                                     |
| nqueens                    | 77.7 ms                                                                | 75.3 ms: 1.03x faster                                                     |
| logging_simple             | 6.14 us                                                                | 5.96 us: 1.03x faster                                                     |
| crypto_pyaes               | 68.2 ms                                                                | 66.6 ms: 1.02x faster                                                     |
| xml_etree_iterparse        | 94.4 ms                                                                | 92.2 ms: 1.02x faster                                                     |
| sympy_integrate            | 19.7 ms                                                                | 19.3 ms: 1.02x faster                                                     |
| meteor_contest             | 101 ms                                                                 | 99.3 ms: 1.02x faster                                                     |
| generators                 | 28.5 ms                                                                | 28.0 ms: 1.02x faster                                                     |
| pycparser                  | 1.12 sec                                                               | 1.10 sec: 1.02x faster                                                    |
| 2to3                       | 259 ms                                                                 | 256 ms: 1.01x faster                                                      |
| fannkuch                   | 376 ms                                                                 | 372 ms: 1.01x faster                                                      |
| json_loads                 | 27.3 us                                                                | 27.2 us: 1.01x faster                                                     |
| coroutines                 | 23.3 ms                                                                | 23.4 ms: 1.00x slower                                                     |
| richards                   | 44.4 ms                                                                | 44.7 ms: 1.01x slower                                                     |
| richards_super             | 50.4 ms                                                                | 50.9 ms: 1.01x slower                                                     |
| unpickle_pure_python       | 208 us                                                                 | 210 us: 1.01x slower                                                      |
| python_startup_no_site     | 7.41 ms                                                                | 7.52 ms: 1.01x slower                                                     |
| raytrace                   | 250 ms                                                                 | 254 ms: 1.02x slower                                                      |
| coverage                   | 82.5 ms                                                                | 84.2 ms: 1.02x slower                                                     |
| sympy_str                  | 274 ms                                                                 | 281 ms: 1.03x slower                                                      |
| sympy_sum                  | 154 ms                                                                 | 158 ms: 1.03x slower                                                      |
| pprint_pformat             | 1.46 sec                                                               | 1.49 sec: 1.03x slower                                                    |
| create_gc_cycles           | 1.33 ms                                                                | 1.37 ms: 1.03x slower                                                     |
| pprint_safe_repr           | 719 ms                                                                 | 738 ms: 1.03x slower                                                      |
| xml_etree_generate         | 85.4 ms                                                                | 88.6 ms: 1.04x slower                                                     |
| thrift                     | 772 us                                                                 | 800 us: 1.04x slower                                                      |
| pickle_pure_python         | 292 us                                                                 | 303 us: 1.04x slower                                                      |
| sympy_expand               | 454 ms                                                                 | 474 ms: 1.05x slower                                                      |
| deltablue                  | 3.10 ms                                                                | 3.25 ms: 1.05x slower                                                     |
| asyncio_websockets         | 517 ms                                                                 | 544 ms: 1.05x slower                                                      |
| scimark_lu                 | 112 ms                                                                 | 119 ms: 1.05x slower                                                      |
| xml_etree_parse            | 136 ms                                                                 | 143 ms: 1.06x slower                                                      |
| xml_etree_process          | 59.2 ms                                                                | 62.7 ms: 1.06x slower                                                     |
| mako                       | 11.2 ms                                                                | 12.1 ms: 1.07x slower                                                     |
| django_template            | 34.2 ms                                                                | 37.1 ms: 1.09x slower                                                     |
| nbody                      | 85.3 ms                                                                | 93.2 ms: 1.09x slower                                                     |
| regex_compile              | 131 ms                                                                 | 150 ms: 1.14x slower                                                      |
| gc_traversal               | 3.32 ms                                                                | 3.80 ms: 1.15x slower                                                     |
| python_startup             | 11.0 ms                                                                | 12.6 ms: 1.15x slower                                                     |
| bench_thread_pool          | 924 us                                                                 | 1.36 ms: 1.47x slower                                                     |
| telco                      | 7.77 ms                                                                | 162 ms: 20.83x slower                                                     |
| bench_mp_pool              | 11.0 ms                                                                | 258 ms: 23.45x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                              |

Benchmark hidden because not significant (2): json, sqlite_synth
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20261018-3.16.0a1+dev-7dbc797/bm-20261018-vultr-x86_64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.042x faster

# HPT report

- Reliability score: 99.77% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.14x