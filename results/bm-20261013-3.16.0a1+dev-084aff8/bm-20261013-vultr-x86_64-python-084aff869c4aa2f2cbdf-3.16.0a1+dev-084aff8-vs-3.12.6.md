# Results vs. 3.12.6

- fork: python
- ref: 084aff869c4aa2f2cbdf
- machine: linux-x86_64
- commit hash: 084aff8
- commit date: 2026-10-13
- overall geometric mean: 1.082x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 255 ms: 1.03x faster                                                      |
| docutils       | 2.64 sec                                               | 2.33 sec: 1.13x faster                                                    |
| html5lib       | 63.6 ms                                                | 57.9 ms: 1.10x faster                                                     |
| Geometric mean | (ref)                                                  | 1.09x faster                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_none            | 464 ms                                                 | 276 ms: 1.68x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 657 ms: 1.65x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 341 ms: 1.64x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 348 ms: 1.59x faster                                                      |
| async_tree_io_tg           | 1.11 sec                                               | 696 ms: 1.59x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 281 ms: 1.59x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 514 ms: 1.39x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 529 ms: 1.36x faster                                                      |
| async_generators           | 384 ms                                                 | 350 ms: 1.10x faster                                                      |
| coroutines                 | 23.9 ms                                                | 23.6 ms: 1.02x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 543 ms: 1.05x slower                                                      |
| Geometric mean             | (ref)                                                  | 1.39x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.7 ms: 1.14x faster                                                     |
| nbody          | 89.3 ms                                                | 90.2 ms: 1.01x slower                                                     |
| pidigits       | 184 ms                                                 | 191 ms: 1.04x slower                                                      |
| Geometric mean | (ref)                                                  | 1.03x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.57 ms: 1.23x faster                                                     |
| regex_dna      | 168 ms                                                 | 166 ms: 1.01x faster                                                      |
| regex_v8       | 20.6 ms                                                | 21.0 ms: 1.02x slower                                                     |
| regex_compile  | 142 ms                                                 | 150 ms: 1.05x slower                                                      |
| Geometric mean | (ref)                                                  | 1.04x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.84 sec: 1.15x faster                                                    |
| json_dumps           | 10.4 ms                                                | 9.06 ms: 1.14x faster                                                     |
| xml_etree_iterparse  | 96.7 ms                                                | 91.5 ms: 1.06x faster                                                     |
| unpickle_pure_python | 221 us                                                 | 212 us: 1.04x faster                                                      |
| json_loads           | 26.5 us                                                | 26.9 us: 1.02x slower                                                     |
| xml_etree_parse      | 139 ms                                                 | 143 ms: 1.03x slower                                                      |
| xml_etree_generate   | 85.2 ms                                                | 88.6 ms: 1.04x slower                                                     |
| xml_etree_process    | 59.0 ms                                                | 62.8 ms: 1.07x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                              |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.51 ms: 1.05x slower                                                     |
| python_startup         | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                     |
| Geometric mean         | (ref)                                                  | 1.15x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 36.8 ms: 1.06x slower                                                     |
| mako            | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                     |
| Geometric mean  | (ref)                                                  | 1.07x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 113 ms: 2.82x faster                                                      |
| mdp                        | 2.42 sec                                               | 1.15 sec: 2.11x faster                                                    |
| async_tree_none            | 464 ms                                                 | 276 ms: 1.68x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 657 ms: 1.65x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 341 ms: 1.64x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 348 ms: 1.59x faster                                                      |
| async_tree_io_tg           | 1.11 sec                                               | 696 ms: 1.59x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 281 ms: 1.59x faster                                                      |
| deepcopy                   | 352 us                                                 | 232 us: 1.52x faster                                                      |
| deepcopy_memo              | 40.3 us                                                | 27.6 us: 1.46x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 514 ms: 1.39x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 529 ms: 1.36x faster                                                      |
| typing_runtime_protocols   | 163 us                                                 | 120 us: 1.36x faster                                                      |
| go                         | 139 ms                                                 | 104 ms: 1.34x faster                                                      |
| comprehensions             | 19.8 us                                                | 15.9 us: 1.25x faster                                                     |
| regex_effbot               | 3.17 ms                                                | 2.57 ms: 1.23x faster                                                     |
| spectral_norm              | 110 ms                                                 | 90.1 ms: 1.22x faster                                                     |
| pathlib                    | 21.5 ms                                                | 17.6 ms: 1.22x faster                                                     |
| deepcopy_reduce            | 3.08 us                                                | 2.57 us: 1.20x faster                                                     |
| scimark_sor                | 130 ms                                                 | 109 ms: 1.19x faster                                                      |
| dulwich_log                | 78.9 ms                                                | 66.7 ms: 1.18x faster                                                     |
| raytrace                   | 299 ms                                                 | 254 ms: 1.18x faster                                                      |
| chaos                      | 62.8 ms                                                | 53.9 ms: 1.17x faster                                                     |
| crypto_pyaes               | 76.6 ms                                                | 66.3 ms: 1.16x faster                                                     |
| pyflate                    | 448 ms                                                 | 390 ms: 1.15x faster                                                      |
| tomli_loads                | 2.11 sec                                               | 1.84 sec: 1.15x faster                                                    |
| float                      | 80.8 ms                                                | 70.7 ms: 1.14x faster                                                     |
| json_dumps                 | 10.4 ms                                                | 9.06 ms: 1.14x faster                                                     |
| scimark_fft                | 342 ms                                                 | 300 ms: 1.14x faster                                                      |
| generators                 | 32.2 ms                                                | 28.4 ms: 1.14x faster                                                     |
| docutils                   | 2.64 sec                                               | 2.33 sec: 1.13x faster                                                    |
| logging_silent             | 109 ns                                                 | 96.6 ns: 1.13x faster                                                     |
| bpe_tokeniser              | 4.74 sec                                               | 4.23 sec: 1.12x faster                                                    |
| html5lib                   | 63.6 ms                                                | 57.9 ms: 1.10x faster                                                     |
| scimark_monte_carlo        | 68.4 ms                                                | 62.3 ms: 1.10x faster                                                     |
| async_generators           | 384 ms                                                 | 350 ms: 1.10x faster                                                      |
| hexiom                     | 6.17 ms                                                | 5.67 ms: 1.09x faster                                                     |
| sympy_integrate            | 20.5 ms                                                | 19.0 ms: 1.08x faster                                                     |
| logging_simple             | 6.63 us                                                | 6.16 us: 1.08x faster                                                     |
| logging_format             | 7.35 us                                                | 6.89 us: 1.07x faster                                                     |
| nqueens                    | 80.1 ms                                                | 75.4 ms: 1.06x faster                                                     |
| sympy_sum                  | 166 ms                                                 | 157 ms: 1.06x faster                                                      |
| xml_etree_iterparse        | 96.7 ms                                                | 91.5 ms: 1.06x faster                                                     |
| pycparser                  | 1.17 sec                                               | 1.11 sec: 1.05x faster                                                    |
| sympy_str                  | 292 ms                                                 | 279 ms: 1.04x faster                                                      |
| deltablue                  | 3.45 ms                                                | 3.30 ms: 1.04x faster                                                     |
| unpickle_pure_python       | 221 us                                                 | 212 us: 1.04x faster                                                      |
| richards                   | 45.9 ms                                                | 44.3 ms: 1.04x faster                                                     |
| 2to3                       | 264 ms                                                 | 255 ms: 1.03x faster                                                      |
| pprint_pformat             | 1.52 sec                                               | 1.48 sec: 1.02x faster                                                    |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.29 ms: 1.02x faster                                                     |
| richards_super             | 51.9 ms                                                | 50.9 ms: 1.02x faster                                                     |
| pprint_safe_repr           | 743 ms                                                 | 730 ms: 1.02x faster                                                      |
| coroutines                 | 23.9 ms                                                | 23.6 ms: 1.02x faster                                                     |
| json                       | 5.02 ms                                                | 4.96 ms: 1.01x faster                                                     |
| regex_dna                  | 168 ms                                                 | 166 ms: 1.01x faster                                                      |
| sqlite_synth               | 2.20 us                                                | 2.19 us: 1.01x faster                                                     |
| gc_traversal               | 3.46 ms                                                | 3.49 ms: 1.01x slower                                                     |
| fannkuch                   | 372 ms                                                 | 376 ms: 1.01x slower                                                      |
| nbody                      | 89.3 ms                                                | 90.2 ms: 1.01x slower                                                     |
| sympy_expand               | 468 ms                                                 | 472 ms: 1.01x slower                                                      |
| json_loads                 | 26.5 us                                                | 26.9 us: 1.02x slower                                                     |
| thrift                     | 791 us                                                 | 806 us: 1.02x slower                                                      |
| regex_v8                   | 20.6 ms                                                | 21.0 ms: 1.02x slower                                                     |
| scimark_lu                 | 114 ms                                                 | 117 ms: 1.03x slower                                                      |
| xml_etree_parse            | 139 ms                                                 | 143 ms: 1.03x slower                                                      |
| pidigits                   | 184 ms                                                 | 191 ms: 1.04x slower                                                      |
| xml_etree_generate         | 85.2 ms                                                | 88.6 ms: 1.04x slower                                                     |
| python_startup_no_site     | 7.16 ms                                                | 7.51 ms: 1.05x slower                                                     |
| regex_compile              | 142 ms                                                 | 150 ms: 1.05x slower                                                      |
| asyncio_websockets         | 517 ms                                                 | 543 ms: 1.05x slower                                                      |
| django_template            | 34.7 ms                                                | 36.8 ms: 1.06x slower                                                     |
| xml_etree_process          | 59.0 ms                                                | 62.8 ms: 1.07x slower                                                     |
| mako                       | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                     |
| coverage                   | 71.4 ms                                                | 83.1 ms: 1.16x slower                                                     |
| create_gc_cycles           | 1.09 ms                                                | 1.36 ms: 1.24x slower                                                     |
| python_startup             | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                     |
| bench_thread_pool          | 941 us                                                 | 1.34 ms: 1.42x slower                                                     |
| telco                      | 6.53 ms                                                | 162 ms: 24.75x slower                                                     |
| bench_mp_pool              | 10.8 ms                                                | 340 ms: 31.45x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                              |

Benchmark hidden because not significant (2): pickle_pure_python, meteor_contest
Ignored benchmarks (23) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20261013-3.16.0a1+dev-084aff8/bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.082x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.15x