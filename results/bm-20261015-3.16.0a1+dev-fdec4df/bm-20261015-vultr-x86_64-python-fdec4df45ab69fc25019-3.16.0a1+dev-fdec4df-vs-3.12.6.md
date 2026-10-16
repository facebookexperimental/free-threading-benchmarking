# Results vs. 3.12.6

- fork: python
- ref: fdec4df45ab69fc25019
- machine: linux-x86_64
- commit hash: fdec4df
- commit date: 2026-10-15
- overall geometric mean: 1.078x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261015-vultr-x86_64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 257 ms: 1.03x faster                                                      |
| docutils       | 2.64 sec                                               | 2.30 sec: 1.15x faster                                                    |
| html5lib       | 63.6 ms                                                | 58.7 ms: 1.08x faster                                                     |
| Geometric mean | (ref)                                                  | 1.09x faster                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261015-vultr-x86_64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_none            | 464 ms                                                 | 274 ms: 1.70x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 660 ms: 1.64x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 344 ms: 1.63x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 348 ms: 1.60x faster                                                      |
| async_tree_io_tg           | 1.11 sec                                               | 698 ms: 1.59x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 282 ms: 1.58x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 514 ms: 1.39x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 531 ms: 1.36x faster                                                      |
| async_generators           | 384 ms                                                 | 347 ms: 1.11x faster                                                      |
| coroutines                 | 23.9 ms                                                | 23.8 ms: 1.01x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                      |
| Geometric mean             | (ref)                                                  | 1.39x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261015-vultr-x86_64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 73.0 ms: 1.11x faster                                                     |
| pidigits       | 184 ms                                                 | 190 ms: 1.03x slower                                                      |
| nbody          | 89.3 ms                                                | 96.9 ms: 1.08x slower                                                     |
| Geometric mean | (ref)                                                  | 1.00x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261015-vultr-x86_64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.63 ms: 1.20x faster                                                     |
| regex_v8       | 20.6 ms                                                | 20.9 ms: 1.01x slower                                                     |
| regex_compile  | 142 ms                                                 | 148 ms: 1.04x slower                                                      |
| regex_dna      | 168 ms                                                 | 177 ms: 1.06x slower                                                      |
| Geometric mean | (ref)                                                  | 1.02x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261015-vultr-x86_64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.84 sec: 1.15x faster                                                    |
| json_dumps           | 10.4 ms                                                | 9.08 ms: 1.14x faster                                                     |
| xml_etree_iterparse  | 96.7 ms                                                | 90.6 ms: 1.07x faster                                                     |
| unpickle_pure_python | 221 us                                                 | 214 us: 1.03x faster                                                      |
| pickle_pure_python   | 308 us                                                 | 310 us: 1.01x slower                                                      |
| json_loads           | 26.5 us                                                | 27.1 us: 1.02x slower                                                     |
| xml_etree_parse      | 139 ms                                                 | 142 ms: 1.02x slower                                                      |
| xml_etree_generate   | 85.2 ms                                                | 89.7 ms: 1.05x slower                                                     |
| xml_etree_process    | 59.0 ms                                                | 63.4 ms: 1.07x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261015-vultr-x86_64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.49 ms: 1.05x slower                                                     |
| python_startup         | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                     |
| Geometric mean         | (ref)                                                  | 1.15x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261015-vultr-x86_64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 36.4 ms: 1.05x slower                                                     |
| mako            | 11.0 ms                                                | 12.0 ms: 1.09x slower                                                     |
| Geometric mean  | (ref)                                                  | 1.07x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261015-vultr-x86_64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 113 ms: 2.83x faster                                                      |
| mdp                        | 2.42 sec                                               | 1.13 sec: 2.14x faster                                                    |
| async_tree_none            | 464 ms                                                 | 274 ms: 1.70x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 660 ms: 1.64x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 344 ms: 1.63x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 348 ms: 1.60x faster                                                      |
| async_tree_io_tg           | 1.11 sec                                               | 698 ms: 1.59x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 282 ms: 1.58x faster                                                      |
| deepcopy                   | 352 us                                                 | 235 us: 1.50x faster                                                      |
| deepcopy_memo              | 40.3 us                                                | 27.9 us: 1.44x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 514 ms: 1.39x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 531 ms: 1.36x faster                                                      |
| typing_runtime_protocols   | 163 us                                                 | 120 us: 1.36x faster                                                      |
| go                         | 139 ms                                                 | 106 ms: 1.32x faster                                                      |
| comprehensions             | 19.8 us                                                | 15.9 us: 1.25x faster                                                     |
| pathlib                    | 21.5 ms                                                | 17.7 ms: 1.22x faster                                                     |
| spectral_norm              | 110 ms                                                 | 91.6 ms: 1.20x faster                                                     |
| regex_effbot               | 3.17 ms                                                | 2.63 ms: 1.20x faster                                                     |
| deepcopy_reduce            | 3.08 us                                                | 2.57 us: 1.20x faster                                                     |
| scimark_sor                | 130 ms                                                 | 109 ms: 1.19x faster                                                      |
| dulwich_log                | 78.9 ms                                                | 67.5 ms: 1.17x faster                                                     |
| crypto_pyaes               | 76.6 ms                                                | 65.6 ms: 1.17x faster                                                     |
| generators                 | 32.2 ms                                                | 27.9 ms: 1.16x faster                                                     |
| chaos                      | 62.8 ms                                                | 54.5 ms: 1.15x faster                                                     |
| docutils                   | 2.64 sec                                               | 2.30 sec: 1.15x faster                                                    |
| raytrace                   | 299 ms                                                 | 260 ms: 1.15x faster                                                      |
| tomli_loads                | 2.11 sec                                               | 1.84 sec: 1.15x faster                                                    |
| pyflate                    | 448 ms                                                 | 392 ms: 1.14x faster                                                      |
| json_dumps                 | 10.4 ms                                                | 9.08 ms: 1.14x faster                                                     |
| bpe_tokeniser              | 4.74 sec                                               | 4.19 sec: 1.13x faster                                                    |
| logging_silent             | 109 ns                                                 | 96.6 ns: 1.13x faster                                                     |
| scimark_fft                | 342 ms                                                 | 304 ms: 1.12x faster                                                      |
| async_generators           | 384 ms                                                 | 347 ms: 1.11x faster                                                      |
| float                      | 80.8 ms                                                | 73.0 ms: 1.11x faster                                                     |
| logging_simple             | 6.63 us                                                | 6.03 us: 1.10x faster                                                     |
| scimark_monte_carlo        | 68.4 ms                                                | 62.4 ms: 1.10x faster                                                     |
| logging_format             | 7.35 us                                                | 6.71 us: 1.09x faster                                                     |
| hexiom                     | 6.17 ms                                                | 5.65 ms: 1.09x faster                                                     |
| html5lib                   | 63.6 ms                                                | 58.7 ms: 1.08x faster                                                     |
| nqueens                    | 80.1 ms                                                | 74.2 ms: 1.08x faster                                                     |
| sympy_integrate            | 20.5 ms                                                | 19.1 ms: 1.08x faster                                                     |
| xml_etree_iterparse        | 96.7 ms                                                | 90.6 ms: 1.07x faster                                                     |
| sympy_sum                  | 166 ms                                                 | 157 ms: 1.06x faster                                                      |
| pycparser                  | 1.17 sec                                               | 1.11 sec: 1.05x faster                                                    |
| sympy_str                  | 292 ms                                                 | 281 ms: 1.04x faster                                                      |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.26 ms: 1.03x faster                                                     |
| unpickle_pure_python       | 221 us                                                 | 214 us: 1.03x faster                                                      |
| 2to3                       | 264 ms                                                 | 257 ms: 1.03x faster                                                      |
| richards                   | 45.9 ms                                                | 44.9 ms: 1.02x faster                                                     |
| deltablue                  | 3.45 ms                                                | 3.38 ms: 1.02x faster                                                     |
| richards_super             | 51.9 ms                                                | 51.1 ms: 1.01x faster                                                     |
| gc_traversal               | 3.46 ms                                                | 3.42 ms: 1.01x faster                                                     |
| meteor_contest             | 104 ms                                                 | 102 ms: 1.01x faster                                                      |
| coroutines                 | 23.9 ms                                                | 23.8 ms: 1.01x faster                                                     |
| pickle_pure_python         | 308 us                                                 | 310 us: 1.01x slower                                                      |
| sympy_expand               | 468 ms                                                 | 474 ms: 1.01x slower                                                      |
| sqlite_synth               | 2.20 us                                                | 2.23 us: 1.01x slower                                                     |
| regex_v8                   | 20.6 ms                                                | 20.9 ms: 1.01x slower                                                     |
| thrift                     | 791 us                                                 | 806 us: 1.02x slower                                                      |
| json_loads                 | 26.5 us                                                | 27.1 us: 1.02x slower                                                     |
| xml_etree_parse            | 139 ms                                                 | 142 ms: 1.02x slower                                                      |
| pidigits                   | 184 ms                                                 | 190 ms: 1.03x slower                                                      |
| scimark_lu                 | 114 ms                                                 | 118 ms: 1.04x slower                                                      |
| regex_compile              | 142 ms                                                 | 148 ms: 1.04x slower                                                      |
| python_startup_no_site     | 7.16 ms                                                | 7.49 ms: 1.05x slower                                                     |
| django_template            | 34.7 ms                                                | 36.4 ms: 1.05x slower                                                     |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                      |
| xml_etree_generate         | 85.2 ms                                                | 89.7 ms: 1.05x slower                                                     |
| regex_dna                  | 168 ms                                                 | 177 ms: 1.06x slower                                                      |
| xml_etree_process          | 59.0 ms                                                | 63.4 ms: 1.07x slower                                                     |
| nbody                      | 89.3 ms                                                | 96.9 ms: 1.08x slower                                                     |
| mako                       | 11.0 ms                                                | 12.0 ms: 1.09x slower                                                     |
| coverage                   | 71.4 ms                                                | 83.3 ms: 1.17x slower                                                     |
| create_gc_cycles           | 1.09 ms                                                | 1.34 ms: 1.23x slower                                                     |
| python_startup             | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                     |
| bench_thread_pool          | 941 us                                                 | 1.35 ms: 1.43x slower                                                     |
| telco                      | 6.53 ms                                                | 165 ms: 25.25x slower                                                     |
| bench_mp_pool              | 10.8 ms                                                | 285 ms: 26.35x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                              |

Benchmark hidden because not significant (4): pprint_pformat, pprint_safe_repr, fannkuch, json
Ignored benchmarks (23) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20261015-3.16.0a1+dev-fdec4df/bm-20261015-vultr-x86_64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.078x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.15x