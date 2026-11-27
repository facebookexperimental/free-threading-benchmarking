# Results vs. 3.12.6

- fork: python
- ref: cc0e59f17d0fcd8ed9f3
- machine: linux-x86_64
- commit hash: cc0e59f
- commit date: 2026-11-25
- overall geometric mean: 1.022x slower
- HPT reliability: 66.13%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261125-vultr-x86_64-python-cc0e59f17d0fcd8ed9f3-3.16.0a2+dev-cc0e59f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 289 ms: 1.10x slower                                                      |
| docutils       | 2.64 sec                                               | 2.81 sec: 1.06x slower                                                    |
| html5lib       | 63.6 ms                                                | 66.9 ms: 1.05x slower                                                     |
| Geometric mean | (ref)                                                  | 1.07x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261125-vultr-x86_64-python-cc0e59f17d0fcd8ed9f3-3.16.0a2+dev-cc0e59f |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 699 ms: 1.59x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 728 ms: 1.49x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 395 ms: 1.42x faster                                                      |
| async_tree_none            | 464 ms                                                 | 340 ms: 1.37x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 411 ms: 1.35x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 333 ms: 1.34x faster                                                      |
| async_generators           | 384 ms                                                 | 293 ms: 1.31x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 576 ms: 1.25x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 586 ms: 1.22x faster                                                      |
| asyncio_websockets         | 517 ms                                                 | 502 ms: 1.03x faster                                                      |
| coroutines                 | 23.9 ms                                                | 26.2 ms: 1.09x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.28x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261125-vultr-x86_64-python-cc0e59f17d0fcd8ed9f3-3.16.0a2+dev-cc0e59f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 177 ms: 1.04x faster                                                      |
| float          | 80.8 ms                                                | 83.4 ms: 1.03x slower                                                     |
| nbody          | 89.3 ms                                                | 116 ms: 1.30x slower                                                      |
| Geometric mean | (ref)                                                  | 1.09x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261125-vultr-x86_64-python-cc0e59f17d0fcd8ed9f3-3.16.0a2+dev-cc0e59f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.86 ms: 1.11x faster                                                     |
| regex_v8       | 20.6 ms                                                | 20.8 ms: 1.01x slower                                                     |
| regex_dna      | 168 ms                                                 | 171 ms: 1.02x slower                                                      |
| regex_compile  | 142 ms                                                 | 168 ms: 1.18x slower                                                      |
| Geometric mean | (ref)                                                  | 1.02x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261125-vultr-x86_64-python-cc0e59f17d0fcd8ed9f3-3.16.0a2+dev-cc0e59f |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.93 sec: 1.09x faster                                                    |
| json_dumps           | 10.4 ms                                                | 9.91 ms: 1.04x faster                                                     |
| xml_etree_iterparse  | 96.7 ms                                                | 94.9 ms: 1.02x faster                                                     |
| xml_etree_parse      | 139 ms                                                 | 142 ms: 1.02x slower                                                      |
| unpickle_pure_python | 221 us                                                 | 238 us: 1.08x slower                                                      |
| pickle_pure_python   | 308 us                                                 | 343 us: 1.12x slower                                                      |
| xml_etree_generate   | 85.2 ms                                                | 95.6 ms: 1.12x slower                                                     |
| json_loads           | 26.5 us                                                | 30.7 us: 1.16x slower                                                     |
| xml_etree_process    | 59.0 ms                                                | 72.8 ms: 1.23x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.06x slower                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261125-vultr-x86_64-python-cc0e59f17d0fcd8ed9f3-3.16.0a2+dev-cc0e59f |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 8.93 ms: 1.25x slower                                                     |
| python_startup         | 9.93 ms                                                | 13.5 ms: 1.36x slower                                                     |
| Geometric mean         | (ref)                                                  | 1.30x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261125-vultr-x86_64-python-cc0e59f17d0fcd8ed9f3-3.16.0a2+dev-cc0e59f |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 40.4 ms: 1.16x slower                                                     |
| mako            | 11.0 ms                                                | 15.7 ms: 1.43x slower                                                     |
| Geometric mean  | (ref)                                                  | 1.29x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261125-vultr-x86_64-python-cc0e59f17d0fcd8ed9f3-3.16.0a2+dev-cc0e59f |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 115 ms: 2.77x faster                                                      |
| gc_traversal               | 3.46 ms                                                | 1.83 ms: 1.89x faster                                                     |
| mdp                        | 2.42 sec                                               | 1.30 sec: 1.86x faster                                                    |
| bench_mp_pool              | 10.8 ms                                                | 6.60 ms: 1.64x faster                                                     |
| async_tree_io_tg           | 1.11 sec                                               | 699 ms: 1.59x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 728 ms: 1.49x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 395 ms: 1.42x faster                                                      |
| async_tree_none            | 464 ms                                                 | 340 ms: 1.37x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 411 ms: 1.35x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 333 ms: 1.34x faster                                                      |
| deepcopy                   | 352 us                                                 | 268 us: 1.31x faster                                                      |
| async_generators           | 384 ms                                                 | 293 ms: 1.31x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 576 ms: 1.25x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 586 ms: 1.22x faster                                                      |
| deepcopy_memo              | 40.3 us                                                | 33.4 us: 1.21x faster                                                     |
| typing_runtime_protocols   | 163 us                                                 | 137 us: 1.19x faster                                                      |
| pathlib                    | 21.5 ms                                                | 18.1 ms: 1.19x faster                                                     |
| go                         | 139 ms                                                 | 119 ms: 1.17x faster                                                      |
| bpe_tokeniser              | 4.74 sec                                               | 4.26 sec: 1.11x faster                                                    |
| sqlite_synth               | 2.20 us                                                | 1.99 us: 1.11x faster                                                     |
| regex_effbot               | 3.17 ms                                                | 2.86 ms: 1.11x faster                                                     |
| dulwich_log                | 78.9 ms                                                | 71.9 ms: 1.10x faster                                                     |
| comprehensions             | 19.8 us                                                | 18.1 us: 1.10x faster                                                     |
| tomli_loads                | 2.11 sec                                               | 1.93 sec: 1.09x faster                                                    |
| scimark_sor                | 130 ms                                                 | 119 ms: 1.09x faster                                                      |
| spectral_norm              | 110 ms                                                 | 102 ms: 1.08x faster                                                      |
| deepcopy_reduce            | 3.08 us                                                | 2.94 us: 1.05x faster                                                     |
| json_dumps                 | 10.4 ms                                                | 9.91 ms: 1.04x faster                                                     |
| pidigits                   | 184 ms                                                 | 177 ms: 1.04x faster                                                      |
| scimark_fft                | 342 ms                                                 | 330 ms: 1.03x faster                                                      |
| chaos                      | 62.8 ms                                                | 60.8 ms: 1.03x faster                                                     |
| logging_silent             | 109 ns                                                 | 106 ns: 1.03x faster                                                      |
| asyncio_websockets         | 517 ms                                                 | 502 ms: 1.03x faster                                                      |
| xml_etree_iterparse        | 96.7 ms                                                | 94.9 ms: 1.02x faster                                                     |
| raytrace                   | 299 ms                                                 | 294 ms: 1.02x faster                                                      |
| pyflate                    | 448 ms                                                 | 444 ms: 1.01x faster                                                      |
| regex_v8                   | 20.6 ms                                                | 20.8 ms: 1.01x slower                                                     |
| generators                 | 32.2 ms                                                | 32.6 ms: 1.01x slower                                                     |
| xml_etree_parse            | 139 ms                                                 | 142 ms: 1.02x slower                                                      |
| regex_dna                  | 168 ms                                                 | 171 ms: 1.02x slower                                                      |
| pycparser                  | 1.17 sec                                               | 1.20 sec: 1.02x slower                                                    |
| float                      | 80.8 ms                                                | 83.4 ms: 1.03x slower                                                     |
| html5lib                   | 63.6 ms                                                | 66.9 ms: 1.05x slower                                                     |
| deltablue                  | 3.45 ms                                                | 3.63 ms: 1.05x slower                                                     |
| scimark_lu                 | 114 ms                                                 | 120 ms: 1.05x slower                                                      |
| hexiom                     | 6.17 ms                                                | 6.53 ms: 1.06x slower                                                     |
| docutils                   | 2.64 sec                                               | 2.81 sec: 1.06x slower                                                    |
| logging_simple             | 6.63 us                                                | 7.06 us: 1.06x slower                                                     |
| sympy_integrate            | 20.5 ms                                                | 22.0 ms: 1.07x slower                                                     |
| unpickle_pure_python       | 221 us                                                 | 238 us: 1.08x slower                                                      |
| json                       | 5.02 ms                                                | 5.43 ms: 1.08x slower                                                     |
| sympy_sum                  | 166 ms                                                 | 181 ms: 1.09x slower                                                      |
| sympy_str                  | 292 ms                                                 | 318 ms: 1.09x slower                                                      |
| nqueens                    | 80.1 ms                                                | 87.4 ms: 1.09x slower                                                     |
| coroutines                 | 23.9 ms                                                | 26.2 ms: 1.09x slower                                                     |
| pprint_safe_repr           | 743 ms                                                 | 814 ms: 1.10x slower                                                      |
| 2to3                       | 264 ms                                                 | 289 ms: 1.10x slower                                                      |
| logging_format             | 7.35 us                                                | 8.13 us: 1.11x slower                                                     |
| pprint_pformat             | 1.52 sec                                               | 1.68 sec: 1.11x slower                                                    |
| pickle_pure_python         | 308 us                                                 | 343 us: 1.12x slower                                                      |
| xml_etree_generate         | 85.2 ms                                                | 95.6 ms: 1.12x slower                                                     |
| scimark_monte_carlo        | 68.4 ms                                                | 76.8 ms: 1.12x slower                                                     |
| sympy_expand               | 468 ms                                                 | 531 ms: 1.14x slower                                                      |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.00 ms: 1.14x slower                                                     |
| richards                   | 45.9 ms                                                | 52.4 ms: 1.14x slower                                                     |
| crypto_pyaes               | 76.6 ms                                                | 88.2 ms: 1.15x slower                                                     |
| richards_super             | 51.9 ms                                                | 59.7 ms: 1.15x slower                                                     |
| json_loads                 | 26.5 us                                                | 30.7 us: 1.16x slower                                                     |
| django_template            | 34.7 ms                                                | 40.4 ms: 1.16x slower                                                     |
| thrift                     | 791 us                                                 | 927 us: 1.17x slower                                                      |
| regex_compile              | 142 ms                                                 | 168 ms: 1.18x slower                                                      |
| meteor_contest             | 104 ms                                                 | 125 ms: 1.21x slower                                                      |
| xml_etree_process          | 59.0 ms                                                | 72.8 ms: 1.23x slower                                                     |
| create_gc_cycles           | 1.09 ms                                                | 1.35 ms: 1.24x slower                                                     |
| fannkuch                   | 372 ms                                                 | 464 ms: 1.25x slower                                                      |
| python_startup_no_site     | 7.16 ms                                                | 8.93 ms: 1.25x slower                                                     |
| nbody                      | 89.3 ms                                                | 116 ms: 1.30x slower                                                      |
| python_startup             | 9.93 ms                                                | 13.5 ms: 1.36x slower                                                     |
| mako                       | 11.0 ms                                                | 15.7 ms: 1.43x slower                                                     |
| bench_thread_pool          | 941 us                                                 | 1.40 ms: 1.49x slower                                                     |
| coverage                   | 71.4 ms                                                | 118 ms: 1.66x slower                                                      |
| telco                      | 6.53 ms                                                | 173 ms: 26.46x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.02x slower                                                              |
Ignored benchmarks (23) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20261125-3.16.0a2+dev-cc0e59f-NOGIL/bm-20261125-vultr-x86_64-python-cc0e59f17d0fcd8ed9f3-3.16.0a2+dev-cc0e59f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.022x slower

# HPT report

- Reliability score: 66.13% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.31x