# Results vs. 3.12.6

- fork: python
- ref: f0dcb29d3affbbe1ec25
- machine: linux-x86_64
- commit hash: f0dcb29
- commit date: 2025-04-07
- overall geometric mean: 1.076x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 310 ms: 1.18x slower                                                   |
| docutils       | 2.64 sec                                               | 2.91 sec: 1.10x slower                                                 |
| html5lib       | 63.6 ms                                                | 75.8 ms: 1.19x slower                                                  |
| Geometric mean | (ref)                                                  | 1.16x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 567 ms: 1.96x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 246 ms: 1.82x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 597 ms: 1.81x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 312 ms: 1.79x faster                                                   |
| async_tree_none            | 464 ms                                                 | 280 ms: 1.66x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 339 ms: 1.64x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 498 ms: 1.45x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 525 ms: 1.36x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 516 ms: 1.00x faster                                                   |
| async_generators           | 384 ms                                                 | 387 ms: 1.01x slower                                                   |
| coroutines                 | 23.9 ms                                                | 27.0 ms: 1.13x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.44x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 77.6 ms: 1.04x faster                                                  |
| pidigits       | 184 ms                                                 | 191 ms: 1.04x slower                                                   |
| nbody          | 89.3 ms                                                | 140 ms: 1.57x slower                                                   |
| Geometric mean | (ref)                                                  | 1.16x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.96 ms: 1.07x faster                                                  |
| regex_v8       | 20.6 ms                                                | 21.7 ms: 1.05x slower                                                  |
| regex_dna      | 168 ms                                                 | 180 ms: 1.07x slower                                                   |
| regex_compile  | 142 ms                                                 | 169 ms: 1.19x slower                                                   |
| Geometric mean | (ref)                                                  | 1.06x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.06x faster                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 93.1 ms: 1.04x faster                                                  |
| json_loads           | 26.5 us                                                | 30.3 us: 1.14x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 101 ms: 1.19x slower                                                   |
| tomli_loads          | 2.11 sec                                               | 2.51 sec: 1.19x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 270 us: 1.23x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 381 us: 1.24x slower                                                   |
| xml_etree_process    | 59.0 ms                                                | 74.2 ms: 1.26x slower                                                  |
| json_dumps           | 10.4 ms                                                | 13.2 ms: 1.27x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.15x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 11.2 ms: 1.57x slower                                                  |
| python_startup         | 9.93 ms                                                | 16.0 ms: 1.61x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.59x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 45.1 ms: 1.30x slower                                                  |
| genshi_xml      | 50.2 ms                                                | 68.4 ms: 1.36x slower                                                  |
| genshi_text     | 22.8 ms                                                | 31.4 ms: 1.38x slower                                                  |
| mako            | 11.0 ms                                                | 16.5 ms: 1.50x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.38x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 567 ms: 1.96x faster                                                   |
| gc_traversal               | 3.46 ms                                                | 1.78 ms: 1.95x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 246 ms: 1.82x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 597 ms: 1.81x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 312 ms: 1.79x faster                                                   |
| async_tree_none            | 464 ms                                                 | 280 ms: 1.66x faster                                                   |
| mdp                        | 2.42 sec                                               | 1.47 sec: 1.65x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 339 ms: 1.64x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 498 ms: 1.45x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 525 ms: 1.36x faster                                                   |
| pathlib                    | 21.5 ms                                                | 19.9 ms: 1.08x faster                                                  |
| deepcopy                   | 352 us                                                 | 327 us: 1.08x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.96 ms: 1.07x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.06 us: 1.07x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.06x faster                                                   |
| float                      | 80.8 ms                                                | 77.6 ms: 1.04x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 93.1 ms: 1.04x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 78.3 ms: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 516 ms: 1.00x faster                                                   |
| async_generators           | 384 ms                                                 | 387 ms: 1.01x slower                                                   |
| json                       | 5.02 ms                                                | 5.11 ms: 1.02x slower                                                  |
| pidigits                   | 184 ms                                                 | 191 ms: 1.04x slower                                                   |
| pylint                     | 319 ms                                                 | 331 ms: 1.04x slower                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.94 sec: 1.04x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 21.7 ms: 1.05x slower                                                  |
| deepcopy_reduce            | 3.08 us                                                | 3.27 us: 1.06x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.25 sec: 1.07x slower                                                 |
| spectral_norm              | 110 ms                                                 | 118 ms: 1.07x slower                                                   |
| regex_dna                  | 168 ms                                                 | 180 ms: 1.07x slower                                                   |
| go                         | 139 ms                                                 | 153 ms: 1.10x slower                                                   |
| docutils                   | 2.64 sec                                               | 2.91 sec: 1.10x slower                                                 |
| scimark_fft                | 342 ms                                                 | 379 ms: 1.11x slower                                                   |
| comprehensions             | 19.8 us                                                | 22.0 us: 1.11x slower                                                  |
| coroutines                 | 23.9 ms                                                | 27.0 ms: 1.13x slower                                                  |
| raytrace                   | 299 ms                                                 | 341 ms: 1.14x slower                                                   |
| json_loads                 | 26.5 us                                                | 30.3 us: 1.14x slower                                                  |
| logging_silent             | 109 ns                                                 | 124 ns: 1.14x slower                                                   |
| chaos                      | 62.8 ms                                                | 71.8 ms: 1.14x slower                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 165 ms: 1.16x slower                                                   |
| sqlalchemy_imperative      | 21.8 ms                                                | 25.3 ms: 1.16x slower                                                  |
| scimark_sor                | 130 ms                                                 | 151 ms: 1.16x slower                                                   |
| 2to3                       | 264 ms                                                 | 310 ms: 1.18x slower                                                   |
| sympy_sum                  | 166 ms                                                 | 195 ms: 1.18x slower                                                   |
| pyflate                    | 448 ms                                                 | 529 ms: 1.18x slower                                                   |
| sympy_integrate            | 20.5 ms                                                | 24.2 ms: 1.18x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 90.9 ms: 1.19x slower                                                  |
| regex_compile              | 142 ms                                                 | 169 ms: 1.19x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 101 ms: 1.19x slower                                                   |
| html5lib                   | 63.6 ms                                                | 75.8 ms: 1.19x slower                                                  |
| tomli_loads                | 2.11 sec                                               | 2.51 sec: 1.19x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 890 ms: 1.20x slower                                                   |
| sympy_str                  | 292 ms                                                 | 352 ms: 1.21x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.85 sec: 1.22x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.33 ms: 1.22x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 270 us: 1.23x slower                                                   |
| pickle_pure_python         | 308 us                                                 | 381 us: 1.24x slower                                                   |
| scimark_lu                 | 114 ms                                                 | 142 ms: 1.25x slower                                                   |
| sympy_expand               | 468 ms                                                 | 584 ms: 1.25x slower                                                   |
| nqueens                    | 80.1 ms                                                | 100 ms: 1.25x slower                                                   |
| xml_etree_process          | 59.0 ms                                                | 74.2 ms: 1.26x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 86.4 ms: 1.26x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 206 us: 1.26x slower                                                   |
| logging_simple             | 6.63 us                                                | 8.42 us: 1.27x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.59 ms: 1.27x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 13.2 ms: 1.27x slower                                                  |
| deltablue                  | 3.45 ms                                                | 4.45 ms: 1.29x slower                                                  |
| django_template            | 34.7 ms                                                | 45.1 ms: 1.30x slower                                                  |
| logging_format             | 7.35 us                                                | 9.56 us: 1.30x slower                                                  |
| richards                   | 45.9 ms                                                | 59.8 ms: 1.30x slower                                                  |
| hexiom                     | 6.17 ms                                                | 8.08 ms: 1.31x slower                                                  |
| meteor_contest             | 104 ms                                                 | 136 ms: 1.31x slower                                                   |
| richards_super             | 51.9 ms                                                | 68.3 ms: 1.32x slower                                                  |
| telco                      | 6.53 ms                                                | 8.64 ms: 1.32x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 68.4 ms: 1.36x slower                                                  |
| genshi_text                | 22.8 ms                                                | 31.4 ms: 1.38x slower                                                  |
| generators                 | 32.2 ms                                                | 44.5 ms: 1.38x slower                                                  |
| fannkuch                   | 372 ms                                                 | 514 ms: 1.38x slower                                                   |
| mako                       | 11.0 ms                                                | 16.5 ms: 1.50x slower                                                  |
| coverage                   | 71.4 ms                                                | 111 ms: 1.55x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 11.2 ms: 1.57x slower                                                  |
| nbody                      | 89.3 ms                                                | 140 ms: 1.57x slower                                                   |
| python_startup             | 9.93 ms                                                | 16.0 ms: 1.61x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.18 ms: 3.38x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 97.4 ms: 9.02x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.13x slower                                                           |

Benchmark hidden because not significant (1): deepcopy_memo
Ignored benchmarks (20) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250407-3.14.0a6+-f0dcb29-NOGIL/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.076x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.37x