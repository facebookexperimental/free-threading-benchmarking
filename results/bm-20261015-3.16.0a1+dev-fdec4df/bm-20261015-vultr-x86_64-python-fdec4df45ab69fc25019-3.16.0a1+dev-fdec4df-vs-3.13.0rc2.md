# Results vs. 3.13.0rc2

- fork: python
- ref: fdec4df45ab69fc25019
- machine: linux-x86_64
- commit hash: fdec4df
- commit date: 2026-10-15
- overall geometric mean: 1.041x faster
- HPT reliability: 99.62%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261015-vultr-x86_64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 257 ms: 1.01x faster                                                      |
| docutils       | 2.63 sec                                                               | 2.30 sec: 1.15x faster                                                    |
| html5lib       | 68.6 ms                                                                | 58.7 ms: 1.17x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.11x faster                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261015-vultr-x86_64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io              | 881 ms                                                                 | 660 ms: 1.33x faster                                                      |
| async_tree_memoization     | 459 ms                                                                 | 348 ms: 1.32x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 514 ms: 1.30x faster                                                      |
| async_tree_io_tg           | 901 ms                                                                 | 698 ms: 1.29x faster                                                      |
| async_tree_none            | 353 ms                                                                 | 274 ms: 1.29x faster                                                      |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 531 ms: 1.19x faster                                                      |
| async_tree_memoization_tg  | 410 ms                                                                 | 344 ms: 1.19x faster                                                      |
| async_tree_none_tg         | 333 ms                                                                 | 282 ms: 1.18x faster                                                      |
| async_generators           | 375 ms                                                                 | 347 ms: 1.08x faster                                                      |
| coroutines                 | 23.3 ms                                                                | 23.8 ms: 1.02x slower                                                     |
| asyncio_websockets         | 517 ms                                                                 | 544 ms: 1.05x slower                                                      |
| Geometric mean             | (ref)                                                                  | 1.18x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261015-vultr-x86_64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 190 ms: 1.14x faster                                                      |
| float          | 76.7 ms                                                                | 73.0 ms: 1.05x faster                                                     |
| nbody          | 85.3 ms                                                                | 96.9 ms: 1.14x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261015-vultr-x86_64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.63 ms: 1.22x faster                                                     |
| regex_v8       | 23.2 ms                                                                | 20.9 ms: 1.11x faster                                                     |
| regex_dna      | 189 ms                                                                 | 177 ms: 1.06x faster                                                      |
| regex_compile  | 131 ms                                                                 | 148 ms: 1.13x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261015-vultr-x86_64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json_dumps           | 10.6 ms                                                                | 9.08 ms: 1.17x faster                                                     |
| tomli_loads          | 2.01 sec                                                               | 1.84 sec: 1.09x faster                                                    |
| xml_etree_iterparse  | 94.4 ms                                                                | 90.6 ms: 1.04x faster                                                     |
| json_loads           | 27.3 us                                                                | 27.1 us: 1.01x faster                                                     |
| unpickle_pure_python | 208 us                                                                 | 214 us: 1.03x slower                                                      |
| xml_etree_parse      | 136 ms                                                                 | 142 ms: 1.04x slower                                                      |
| xml_etree_generate   | 85.4 ms                                                                | 89.7 ms: 1.05x slower                                                     |
| pickle_pure_python   | 292 us                                                                 | 310 us: 1.06x slower                                                      |
| xml_etree_process    | 59.2 ms                                                                | 63.4 ms: 1.07x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261015-vultr-x86_64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 7.49 ms: 1.01x slower                                                     |
| python_startup         | 11.0 ms                                                                | 12.6 ms: 1.14x slower                                                     |
| Geometric mean         | (ref)                                                                  | 1.07x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261015-vultr-x86_64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 36.4 ms: 1.06x slower                                                     |
| mako            | 11.2 ms                                                                | 12.0 ms: 1.07x slower                                                     |
| Geometric mean  | (ref)                                                                  | 1.07x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261015-vultr-x86_64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pylint                     | 317 ms                                                                 | 113 ms: 2.82x faster                                                      |
| mdp                        | 2.34 sec                                                               | 1.13 sec: 2.08x faster                                                    |
| deepcopy                   | 357 us                                                                 | 235 us: 1.52x faster                                                      |
| deepcopy_memo              | 38.1 us                                                                | 27.9 us: 1.36x faster                                                     |
| async_tree_io              | 881 ms                                                                 | 660 ms: 1.33x faster                                                      |
| go                         | 141 ms                                                                 | 106 ms: 1.33x faster                                                      |
| async_tree_memoization     | 459 ms                                                                 | 348 ms: 1.32x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 514 ms: 1.30x faster                                                      |
| typing_runtime_protocols   | 156 us                                                                 | 120 us: 1.29x faster                                                      |
| async_tree_io_tg           | 901 ms                                                                 | 698 ms: 1.29x faster                                                      |
| async_tree_none            | 353 ms                                                                 | 274 ms: 1.29x faster                                                      |
| scimark_sor                | 134 ms                                                                 | 109 ms: 1.22x faster                                                      |
| regex_effbot               | 3.21 ms                                                                | 2.63 ms: 1.22x faster                                                     |
| deepcopy_reduce            | 3.12 us                                                                | 2.57 us: 1.22x faster                                                     |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 531 ms: 1.19x faster                                                      |
| async_tree_memoization_tg  | 410 ms                                                                 | 344 ms: 1.19x faster                                                      |
| async_tree_none_tg         | 333 ms                                                                 | 282 ms: 1.18x faster                                                      |
| spectral_norm              | 108 ms                                                                 | 91.6 ms: 1.17x faster                                                     |
| json_dumps                 | 10.6 ms                                                                | 9.08 ms: 1.17x faster                                                     |
| html5lib                   | 68.6 ms                                                                | 58.7 ms: 1.17x faster                                                     |
| scimark_fft                | 348 ms                                                                 | 304 ms: 1.15x faster                                                      |
| pyflate                    | 449 ms                                                                 | 392 ms: 1.15x faster                                                      |
| docutils                   | 2.63 sec                                                               | 2.30 sec: 1.15x faster                                                    |
| pidigits                   | 216 ms                                                                 | 190 ms: 1.14x faster                                                      |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.26 ms: 1.12x faster                                                     |
| regex_v8                   | 23.2 ms                                                                | 20.9 ms: 1.11x faster                                                     |
| dulwich_log                | 74.5 ms                                                                | 67.5 ms: 1.10x faster                                                     |
| tomli_loads                | 2.01 sec                                                               | 1.84 sec: 1.09x faster                                                    |
| pathlib                    | 19.3 ms                                                                | 17.7 ms: 1.09x faster                                                     |
| async_generators           | 375 ms                                                                 | 347 ms: 1.08x faster                                                      |
| regex_dna                  | 189 ms                                                                 | 177 ms: 1.06x faster                                                      |
| bpe_tokeniser              | 4.46 sec                                                               | 4.19 sec: 1.06x faster                                                    |
| scimark_monte_carlo        | 65.8 ms                                                                | 62.4 ms: 1.05x faster                                                     |
| hexiom                     | 5.95 ms                                                                | 5.65 ms: 1.05x faster                                                     |
| float                      | 76.7 ms                                                                | 73.0 ms: 1.05x faster                                                     |
| nqueens                    | 77.7 ms                                                                | 74.2 ms: 1.05x faster                                                     |
| xml_etree_iterparse        | 94.4 ms                                                                | 90.6 ms: 1.04x faster                                                     |
| comprehensions             | 16.6 us                                                                | 15.9 us: 1.04x faster                                                     |
| crypto_pyaes               | 68.2 ms                                                                | 65.6 ms: 1.04x faster                                                     |
| sympy_integrate            | 19.7 ms                                                                | 19.1 ms: 1.03x faster                                                     |
| chaos                      | 56.3 ms                                                                | 54.5 ms: 1.03x faster                                                     |
| logging_format             | 6.92 us                                                                | 6.71 us: 1.03x faster                                                     |
| generators                 | 28.5 ms                                                                | 27.9 ms: 1.02x faster                                                     |
| logging_simple             | 6.14 us                                                                | 6.03 us: 1.02x faster                                                     |
| logging_silent             | 98.2 ns                                                                | 96.6 ns: 1.02x faster                                                     |
| 2to3                       | 259 ms                                                                 | 257 ms: 1.01x faster                                                      |
| json_loads                 | 27.3 us                                                                | 27.1 us: 1.01x faster                                                     |
| fannkuch                   | 376 ms                                                                 | 373 ms: 1.01x faster                                                      |
| pycparser                  | 1.12 sec                                                               | 1.11 sec: 1.01x faster                                                    |
| create_gc_cycles           | 1.33 ms                                                                | 1.34 ms: 1.01x slower                                                     |
| coverage                   | 82.5 ms                                                                | 83.3 ms: 1.01x slower                                                     |
| meteor_contest             | 101 ms                                                                 | 102 ms: 1.01x slower                                                      |
| python_startup_no_site     | 7.41 ms                                                                | 7.49 ms: 1.01x slower                                                     |
| richards                   | 44.4 ms                                                                | 44.9 ms: 1.01x slower                                                     |
| richards_super             | 50.4 ms                                                                | 51.1 ms: 1.01x slower                                                     |
| json                       | 4.98 ms                                                                | 5.07 ms: 1.02x slower                                                     |
| sympy_sum                  | 154 ms                                                                 | 157 ms: 1.02x slower                                                      |
| coroutines                 | 23.3 ms                                                                | 23.8 ms: 1.02x slower                                                     |
| sympy_str                  | 274 ms                                                                 | 281 ms: 1.02x slower                                                      |
| unpickle_pure_python       | 208 us                                                                 | 214 us: 1.03x slower                                                      |
| gc_traversal               | 3.32 ms                                                                | 3.42 ms: 1.03x slower                                                     |
| pprint_safe_repr           | 719 ms                                                                 | 743 ms: 1.03x slower                                                      |
| xml_etree_parse            | 136 ms                                                                 | 142 ms: 1.04x slower                                                      |
| raytrace                   | 250 ms                                                                 | 260 ms: 1.04x slower                                                      |
| pprint_pformat             | 1.46 sec                                                               | 1.52 sec: 1.04x slower                                                    |
| sympy_expand               | 454 ms                                                                 | 474 ms: 1.04x slower                                                      |
| thrift                     | 772 us                                                                 | 806 us: 1.04x slower                                                      |
| xml_etree_generate         | 85.4 ms                                                                | 89.7 ms: 1.05x slower                                                     |
| scimark_lu                 | 112 ms                                                                 | 118 ms: 1.05x slower                                                      |
| asyncio_websockets         | 517 ms                                                                 | 544 ms: 1.05x slower                                                      |
| pickle_pure_python         | 292 us                                                                 | 310 us: 1.06x slower                                                      |
| django_template            | 34.2 ms                                                                | 36.4 ms: 1.06x slower                                                     |
| mako                       | 11.2 ms                                                                | 12.0 ms: 1.07x slower                                                     |
| xml_etree_process          | 59.2 ms                                                                | 63.4 ms: 1.07x slower                                                     |
| deltablue                  | 3.10 ms                                                                | 3.38 ms: 1.09x slower                                                     |
| regex_compile              | 131 ms                                                                 | 148 ms: 1.13x slower                                                      |
| nbody                      | 85.3 ms                                                                | 96.9 ms: 1.14x slower                                                     |
| python_startup             | 11.0 ms                                                                | 12.6 ms: 1.14x slower                                                     |
| bench_thread_pool          | 924 us                                                                 | 1.35 ms: 1.46x slower                                                     |
| telco                      | 7.77 ms                                                                | 165 ms: 21.20x slower                                                     |
| bench_mp_pool              | 11.0 ms                                                                | 285 ms: 25.87x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                              |

Benchmark hidden because not significant (1): sqlite_synth
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20261015-3.16.0a1+dev-fdec4df/bm-20261015-vultr-x86_64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.041x faster

# HPT report

- Reliability score: 99.62% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.14x