# Results vs. 3.12.6

- fork: python
- ref: d18dbd5e1ce6ca43b559
- machine: linux-x86_64
- commit hash: d18dbd5
- commit date: 2026-02-10
- overall geometric mean: 1.033x slower
- HPT reliability: 76.70%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.41x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 277 ms: 1.05x slower                                                   |
| docutils       | 2.64 sec                                               | 2.72 sec: 1.03x slower                                                 |
| html5lib       | 63.6 ms                                                | 66.5 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 600 ms: 1.85x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 614 ms: 1.76x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 327 ms: 1.71x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 266 ms: 1.68x faster                                                   |
| async_tree_none            | 464 ms                                                 | 286 ms: 1.62x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 353 ms: 1.57x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 604 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 627 ms: 1.14x faster                                                   |
| async_generators           | 384 ms                                                 | 370 ms: 1.04x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 510 ms: 1.01x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.8 ms: 1.01x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.38x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 72.4 ms: 1.12x faster                                                  |
| pidigits       | 184 ms                                                 | 219 ms: 1.19x slower                                                   |
| nbody          | 89.3 ms                                                | 121 ms: 1.35x slower                                                   |
| Geometric mean | (ref)                                                  | 1.13x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.68 ms: 1.18x faster                                                  |
| regex_compile  | 142 ms                                                 | 140 ms: 1.02x faster                                                   |
| regex_dna      | 168 ms                                                 | 172 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.4 ms: 1.09x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 1.97 sec: 1.07x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 132 ms: 1.05x faster                                                   |
| json_dumps           | 10.4 ms                                                | 11.0 ms: 1.07x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 236 us: 1.07x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 331 us: 1.07x slower                                                   |
| xml_etree_generate   | 85.2 ms                                                | 96.6 ms: 1.13x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 69.0 ms: 1.17x slower                                                  |
| json_loads           | 26.5 us                                                | 32.3 us: 1.22x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.72 ms: 1.36x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.9 ms: 1.60x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 54.7 ms: 1.09x slower                                                  |
| genshi_text     | 22.8 ms                                                | 25.9 ms: 1.14x slower                                                  |
| django_template | 34.7 ms                                                | 40.7 ms: 1.17x slower                                                  |
| mako            | 11.0 ms                                                | 15.7 ms: 1.43x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.20x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.31 sec: 1.85x faster                                                 |
| async_tree_io_tg           | 1.11 sec                                               | 600 ms: 1.85x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 614 ms: 1.76x faster                                                   |
| gc_traversal               | 3.46 ms                                                | 1.96 ms: 1.76x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 327 ms: 1.71x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 266 ms: 1.68x faster                                                   |
| async_tree_none            | 464 ms                                                 | 286 ms: 1.62x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 353 ms: 1.57x faster                                                   |
| bench_mp_pool              | 10.8 ms                                                | 7.07 ms: 1.53x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 30.5 us: 1.32x faster                                                  |
| deepcopy                   | 352 us                                                 | 268 us: 1.31x faster                                                   |
| pathlib                    | 21.5 ms                                                | 17.7 ms: 1.22x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 604 ms: 1.20x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.68 ms: 1.18x faster                                                  |
| go                         | 139 ms                                                 | 120 ms: 1.16x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 1.91 us: 1.15x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 627 ms: 1.14x faster                                                   |
| float                      | 80.8 ms                                                | 72.4 ms: 1.12x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 71.3 ms: 1.11x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 88.4 ms: 1.09x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.37 sec: 1.08x faster                                                 |
| scimark_sor                | 130 ms                                                 | 120 ms: 1.08x faster                                                   |
| tomli_loads                | 2.11 sec                                               | 1.97 sec: 1.07x faster                                                 |
| comprehensions             | 19.8 us                                                | 18.6 us: 1.07x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.89 us: 1.06x faster                                                  |
| pylint                     | 319 ms                                                 | 300 ms: 1.06x faster                                                   |
| logging_silent             | 109 ns                                                 | 104 ns: 1.05x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 132 ms: 1.05x faster                                                   |
| async_generators           | 384 ms                                                 | 370 ms: 1.04x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.03x faster                                                 |
| generators                 | 32.2 ms                                                | 31.6 ms: 1.02x faster                                                  |
| regex_compile              | 142 ms                                                 | 140 ms: 1.02x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 510 ms: 1.01x faster                                                   |
| raytrace                   | 299 ms                                                 | 297 ms: 1.01x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.8 ms: 1.01x faster                                                  |
| chaos                      | 62.8 ms                                                | 63.4 ms: 1.01x slower                                                  |
| scimark_fft                | 342 ms                                                 | 346 ms: 1.01x slower                                                   |
| regex_dna                  | 168 ms                                                 | 172 ms: 1.03x slower                                                   |
| pyflate                    | 448 ms                                                 | 460 ms: 1.03x slower                                                   |
| docutils                   | 2.64 sec                                               | 2.72 sec: 1.03x slower                                                 |
| deltablue                  | 3.45 ms                                                | 3.60 ms: 1.04x slower                                                  |
| html5lib                   | 63.6 ms                                                | 66.5 ms: 1.05x slower                                                  |
| 2to3                       | 264 ms                                                 | 277 ms: 1.05x slower                                                   |
| logging_simple             | 6.63 us                                                | 6.96 us: 1.05x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 785 ms: 1.06x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 11.0 ms: 1.07x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.62 sec: 1.07x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 236 us: 1.07x slower                                                   |
| sympy_integrate            | 20.5 ms                                                | 22.0 ms: 1.07x slower                                                  |
| sympy_str                  | 292 ms                                                 | 312 ms: 1.07x slower                                                   |
| pickle_pure_python         | 308 us                                                 | 331 us: 1.07x slower                                                   |
| sympy_sum                  | 166 ms                                                 | 179 ms: 1.08x slower                                                   |
| hexiom                     | 6.17 ms                                                | 6.64 ms: 1.08x slower                                                  |
| logging_format             | 7.35 us                                                | 7.93 us: 1.08x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 54.7 ms: 1.09x slower                                                  |
| json                       | 5.02 ms                                                | 5.48 ms: 1.09x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 126 ms: 1.10x slower                                                   |
| nqueens                    | 80.1 ms                                                | 88.8 ms: 1.11x slower                                                  |
| sympy_expand               | 468 ms                                                 | 521 ms: 1.11x slower                                                   |
| crypto_pyaes               | 76.6 ms                                                | 86.1 ms: 1.12x slower                                                  |
| thrift                     | 791 us                                                 | 895 us: 1.13x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 96.6 ms: 1.13x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 77.6 ms: 1.13x slower                                                  |
| genshi_text                | 22.8 ms                                                | 25.9 ms: 1.14x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 69.0 ms: 1.17x slower                                                  |
| django_template            | 34.7 ms                                                | 40.7 ms: 1.17x slower                                                  |
| pidigits                   | 184 ms                                                 | 219 ms: 1.19x slower                                                   |
| richards                   | 45.9 ms                                                | 54.7 ms: 1.19x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 194 us: 1.19x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.26 ms: 1.20x slower                                                  |
| richards_super             | 51.9 ms                                                | 62.3 ms: 1.20x slower                                                  |
| meteor_contest             | 104 ms                                                 | 125 ms: 1.21x slower                                                   |
| json_loads                 | 26.5 us                                                | 32.3 us: 1.22x slower                                                  |
| fannkuch                   | 372 ms                                                 | 455 ms: 1.22x slower                                                   |
| nbody                      | 89.3 ms                                                | 121 ms: 1.35x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 9.72 ms: 1.36x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.55 ms: 1.42x slower                                                  |
| mako                       | 11.0 ms                                                | 15.7 ms: 1.43x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.46 ms: 1.55x slower                                                  |
| coverage                   | 71.4 ms                                                | 112 ms: 1.57x slower                                                   |
| python_startup             | 9.93 ms                                                | 15.9 ms: 1.60x slower                                                  |
| telco                      | 6.53 ms                                                | 173 ms: 26.44x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.03x slower                                                           |

Benchmark hidden because not significant (2): spectral_norm, regex_v8
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260210-3.15.0a5+-d18dbd5-NOGIL/bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.033x slower

# HPT report

- Reliability score: 76.70% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.41x