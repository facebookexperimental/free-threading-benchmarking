# Results vs. 3.13.0rc2

- fork: python
- ref: 7dbc7975db8e34db8be8
- machine: linux-x86_64
- commit hash: 7dbc797
- commit date: 2026-10-18
- overall geometric mean: 1.078x slower
- HPT reliability: 99.26%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261018-vultr-x86_64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 293 ms: 1.13x slower                                                      |
| docutils       | 2.63 sec                                                               | 2.87 sec: 1.09x slower                                                    |
| html5lib       | 68.6 ms                                                                | 67.2 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261018-vultr-x86_64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 707 ms: 1.28x faster                                                      |
| async_tree_io              | 881 ms                                                                 | 724 ms: 1.22x faster                                                      |
| async_tree_memoization     | 459 ms                                                                 | 428 ms: 1.07x faster                                                      |
| async_tree_none            | 353 ms                                                                 | 345 ms: 1.02x faster                                                      |
| asyncio_websockets         | 517 ms                                                                 | 508 ms: 1.02x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 701 ms: 1.05x slower                                                      |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 684 ms: 1.08x slower                                                      |
| coroutines                 | 23.3 ms                                                                | 25.6 ms: 1.10x slower                                                     |
| async_generators           | 375 ms                                                                 | 417 ms: 1.11x slower                                                      |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                              |

Benchmark hidden because not significant (2): async_tree_memoization_tg, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261018-vultr-x86_64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 218 ms: 1.01x slower                                                      |
| float          | 76.7 ms                                                                | 83.5 ms: 1.09x slower                                                     |
| nbody          | 85.3 ms                                                                | 115 ms: 1.35x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.14x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261018-vultr-x86_64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.81 ms: 1.14x faster                                                     |
| regex_v8       | 23.2 ms                                                                | 21.0 ms: 1.11x faster                                                     |
| regex_dna      | 189 ms                                                                 | 174 ms: 1.09x faster                                                      |
| regex_compile  | 131 ms                                                                 | 170 ms: 1.29x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261018-vultr-x86_64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json_dumps           | 10.6 ms                                                                | 10.0 ms: 1.06x faster                                                     |
| tomli_loads          | 2.01 sec                                                               | 1.95 sec: 1.03x faster                                                    |
| xml_etree_iterparse  | 94.4 ms                                                                | 96.4 ms: 1.02x slower                                                     |
| xml_etree_parse      | 136 ms                                                                 | 142 ms: 1.04x slower                                                      |
| json_loads           | 27.3 us                                                                | 30.5 us: 1.12x slower                                                     |
| pickle_pure_python   | 292 us                                                                 | 334 us: 1.15x slower                                                      |
| unpickle_pure_python | 208 us                                                                 | 239 us: 1.15x slower                                                      |
| xml_etree_generate   | 85.4 ms                                                                | 101 ms: 1.18x slower                                                      |
| xml_etree_process    | 59.2 ms                                                                | 75.4 ms: 1.27x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.09x slower                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261018-vultr-x86_64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.57 ms: 1.29x slower                                                     |
| python_startup         | 11.0 ms                                                                | 16.2 ms: 1.46x slower                                                     |
| Geometric mean         | (ref)                                                                  | 1.38x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261018-vultr-x86_64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 41.8 ms: 1.22x slower                                                     |
| mako            | 11.2 ms                                                                | 15.8 ms: 1.41x slower                                                     |
| Geometric mean  | (ref)                                                                  | 1.31x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261018-vultr-x86_64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pylint                     | 317 ms                                                                 | 130 ms: 2.44x faster                                                      |
| gc_traversal               | 3.32 ms                                                                | 1.78 ms: 1.86x faster                                                     |
| mdp                        | 2.34 sec                                                               | 1.30 sec: 1.80x faster                                                    |
| bench_mp_pool              | 11.0 ms                                                                | 6.72 ms: 1.64x faster                                                     |
| deepcopy                   | 357 us                                                                 | 271 us: 1.32x faster                                                      |
| async_tree_io_tg           | 901 ms                                                                 | 707 ms: 1.28x faster                                                      |
| async_tree_io              | 881 ms                                                                 | 724 ms: 1.22x faster                                                      |
| sqlite_synth               | 2.25 us                                                                | 1.92 us: 1.17x faster                                                     |
| go                         | 141 ms                                                                 | 121 ms: 1.17x faster                                                      |
| deepcopy_memo              | 38.1 us                                                                | 33.0 us: 1.15x faster                                                     |
| regex_effbot               | 3.21 ms                                                                | 2.81 ms: 1.14x faster                                                     |
| scimark_sor                | 134 ms                                                                 | 120 ms: 1.11x faster                                                      |
| regex_v8                   | 23.2 ms                                                                | 21.0 ms: 1.11x faster                                                     |
| regex_dna                  | 189 ms                                                                 | 174 ms: 1.09x faster                                                      |
| typing_runtime_protocols   | 156 us                                                                 | 143 us: 1.09x faster                                                      |
| async_tree_memoization     | 459 ms                                                                 | 428 ms: 1.07x faster                                                      |
| pathlib                    | 19.3 ms                                                                | 18.1 ms: 1.07x faster                                                     |
| deepcopy_reduce            | 3.12 us                                                                | 2.93 us: 1.06x faster                                                     |
| json_dumps                 | 10.6 ms                                                                | 10.0 ms: 1.06x faster                                                     |
| scimark_fft                | 348 ms                                                                 | 332 ms: 1.05x faster                                                      |
| dulwich_log                | 74.5 ms                                                                | 71.2 ms: 1.05x faster                                                     |
| tomli_loads                | 2.01 sec                                                               | 1.95 sec: 1.03x faster                                                    |
| spectral_norm              | 108 ms                                                                 | 104 ms: 1.03x faster                                                      |
| pyflate                    | 449 ms                                                                 | 438 ms: 1.02x faster                                                      |
| async_tree_none            | 353 ms                                                                 | 345 ms: 1.02x faster                                                      |
| html5lib                   | 68.6 ms                                                                | 67.2 ms: 1.02x faster                                                     |
| asyncio_websockets         | 517 ms                                                                 | 508 ms: 1.02x faster                                                      |
| bpe_tokeniser              | 4.46 sec                                                               | 4.39 sec: 1.02x faster                                                    |
| pidigits                   | 216 ms                                                                 | 218 ms: 1.01x slower                                                      |
| xml_etree_iterparse        | 94.4 ms                                                                | 96.4 ms: 1.02x slower                                                     |
| create_gc_cycles           | 1.33 ms                                                                | 1.36 ms: 1.02x slower                                                     |
| xml_etree_parse            | 136 ms                                                                 | 142 ms: 1.04x slower                                                      |
| pycparser                  | 1.12 sec                                                               | 1.17 sec: 1.05x slower                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 701 ms: 1.05x slower                                                      |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.01 ms: 1.06x slower                                                     |
| chaos                      | 56.3 ms                                                                | 60.4 ms: 1.07x slower                                                     |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 684 ms: 1.08x slower                                                      |
| json                       | 4.98 ms                                                                | 5.38 ms: 1.08x slower                                                     |
| float                      | 76.7 ms                                                                | 83.5 ms: 1.09x slower                                                     |
| logging_silent             | 98.2 ns                                                                | 107 ns: 1.09x slower                                                      |
| docutils                   | 2.63 sec                                                               | 2.87 sec: 1.09x slower                                                    |
| comprehensions             | 16.6 us                                                                | 18.1 us: 1.09x slower                                                     |
| coroutines                 | 23.3 ms                                                                | 25.6 ms: 1.10x slower                                                     |
| hexiom                     | 5.95 ms                                                                | 6.60 ms: 1.11x slower                                                     |
| async_generators           | 375 ms                                                                 | 417 ms: 1.11x slower                                                      |
| json_loads                 | 27.3 us                                                                | 30.5 us: 1.12x slower                                                     |
| sympy_integrate            | 19.7 ms                                                                | 22.1 ms: 1.12x slower                                                     |
| 2to3                       | 259 ms                                                                 | 293 ms: 1.13x slower                                                      |
| nqueens                    | 77.7 ms                                                                | 88.2 ms: 1.13x slower                                                     |
| pprint_safe_repr           | 719 ms                                                                 | 819 ms: 1.14x slower                                                      |
| pickle_pure_python         | 292 us                                                                 | 334 us: 1.15x slower                                                      |
| unpickle_pure_python       | 208 us                                                                 | 239 us: 1.15x slower                                                      |
| logging_format             | 6.92 us                                                                | 7.95 us: 1.15x slower                                                     |
| scimark_lu                 | 112 ms                                                                 | 131 ms: 1.16x slower                                                      |
| scimark_monte_carlo        | 65.8 ms                                                                | 76.6 ms: 1.16x slower                                                     |
| logging_simple             | 6.14 us                                                                | 7.15 us: 1.16x slower                                                     |
| pprint_pformat             | 1.46 sec                                                               | 1.70 sec: 1.17x slower                                                    |
| sympy_str                  | 274 ms                                                                 | 321 ms: 1.17x slower                                                      |
| raytrace                   | 250 ms                                                                 | 293 ms: 1.17x slower                                                      |
| generators                 | 28.5 ms                                                                | 33.7 ms: 1.18x slower                                                     |
| xml_etree_generate         | 85.4 ms                                                                | 101 ms: 1.18x slower                                                      |
| richards                   | 44.4 ms                                                                | 52.7 ms: 1.19x slower                                                     |
| sympy_sum                  | 154 ms                                                                 | 183 ms: 1.19x slower                                                      |
| sympy_expand               | 454 ms                                                                 | 540 ms: 1.19x slower                                                      |
| richards_super             | 50.4 ms                                                                | 60.2 ms: 1.19x slower                                                     |
| deltablue                  | 3.10 ms                                                                | 3.70 ms: 1.20x slower                                                     |
| django_template            | 34.2 ms                                                                | 41.8 ms: 1.22x slower                                                     |
| meteor_contest             | 101 ms                                                                 | 124 ms: 1.22x slower                                                      |
| thrift                     | 772 us                                                                 | 947 us: 1.23x slower                                                      |
| fannkuch                   | 376 ms                                                                 | 462 ms: 1.23x slower                                                      |
| xml_etree_process          | 59.2 ms                                                                | 75.4 ms: 1.27x slower                                                     |
| crypto_pyaes               | 68.2 ms                                                                | 87.2 ms: 1.28x slower                                                     |
| python_startup_no_site     | 7.41 ms                                                                | 9.57 ms: 1.29x slower                                                     |
| regex_compile              | 131 ms                                                                 | 170 ms: 1.29x slower                                                      |
| nbody                      | 85.3 ms                                                                | 115 ms: 1.35x slower                                                      |
| coverage                   | 82.5 ms                                                                | 116 ms: 1.41x slower                                                      |
| mako                       | 11.2 ms                                                                | 15.8 ms: 1.41x slower                                                     |
| python_startup             | 11.0 ms                                                                | 16.2 ms: 1.46x slower                                                     |
| bench_thread_pool          | 924 us                                                                 | 1.64 ms: 1.77x slower                                                     |
| telco                      | 7.77 ms                                                                | 179 ms: 23.02x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.08x slower                                                              |

Benchmark hidden because not significant (2): async_tree_memoization_tg, async_tree_none_tg
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20261018-3.16.0a1+dev-7dbc797-NOGIL/bm-20261018-vultr-x86_64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.078x slower

# HPT report

- Reliability score: 99.26% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.34x