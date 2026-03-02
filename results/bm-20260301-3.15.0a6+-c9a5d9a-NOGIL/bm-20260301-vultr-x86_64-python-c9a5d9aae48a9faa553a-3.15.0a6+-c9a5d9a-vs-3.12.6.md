# Results vs. 3.12.6

- fork: python
- ref: c9a5d9aae48a9faa553a
- machine: linux-x86_64
- commit hash: c9a5d9a
- commit date: 2026-03-01
- overall geometric mean: 1.032x slower
- HPT reliability: 84.31%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.44x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 285 ms: 1.08x slower                                                   |
| docutils       | 2.64 sec                                               | 2.72 sec: 1.03x slower                                                 |
| html5lib       | 63.6 ms                                                | 65.9 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 603 ms: 1.84x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 630 ms: 1.72x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 326 ms: 1.71x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 261 ms: 1.71x faster                                                   |
| async_tree_none            | 464 ms                                                 | 283 ms: 1.64x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 349 ms: 1.59x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 518 ms: 1.40x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 538 ms: 1.33x faster                                                   |
| async_generators           | 384 ms                                                 | 379 ms: 1.01x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 514 ms: 1.01x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.8 ms: 1.00x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.42x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 72.6 ms: 1.11x faster                                                  |
| pidigits       | 184 ms                                                 | 207 ms: 1.12x slower                                                   |
| nbody          | 89.3 ms                                                | 126 ms: 1.41x slower                                                   |
| Geometric mean | (ref)                                                  | 1.12x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.87 ms: 1.10x faster                                                  |
| regex_compile  | 142 ms                                                 | 142 ms: 1.00x faster                                                   |
| regex_v8       | 20.6 ms                                                | 20.9 ms: 1.02x slower                                                  |
| regex_dna      | 168 ms                                                 | 180 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                  | 1.00x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 89.1 ms: 1.09x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.00 sec: 1.05x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 134 ms: 1.04x faster                                                   |
| json_dumps           | 10.4 ms                                                | 11.0 ms: 1.06x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 237 us: 1.07x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 332 us: 1.08x slower                                                   |
| xml_etree_generate   | 85.2 ms                                                | 100 ms: 1.17x slower                                                   |
| json_loads           | 26.5 us                                                | 31.6 us: 1.19x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 71.0 ms: 1.20x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.06x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.83 ms: 1.37x slower                                                  |
| python_startup         | 9.93 ms                                                | 16.0 ms: 1.62x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.49x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 55.3 ms: 1.10x slower                                                  |
| genshi_text     | 22.8 ms                                                | 26.1 ms: 1.14x slower                                                  |
| django_template | 34.7 ms                                                | 40.4 ms: 1.16x slower                                                  |
| mako            | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.20x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.31 sec: 1.85x faster                                                 |
| async_tree_io_tg           | 1.11 sec                                               | 603 ms: 1.84x faster                                                   |
| gc_traversal               | 3.46 ms                                                | 1.96 ms: 1.76x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 630 ms: 1.72x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 326 ms: 1.71x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 261 ms: 1.71x faster                                                   |
| async_tree_none            | 464 ms                                                 | 283 ms: 1.64x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 349 ms: 1.59x faster                                                   |
| bench_mp_pool              | 10.8 ms                                                | 7.08 ms: 1.52x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 518 ms: 1.40x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 538 ms: 1.33x faster                                                   |
| deepcopy                   | 352 us                                                 | 269 us: 1.31x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 31.0 us: 1.30x faster                                                  |
| pathlib                    | 21.5 ms                                                | 17.4 ms: 1.24x faster                                                  |
| go                         | 139 ms                                                 | 120 ms: 1.16x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 1.92 us: 1.15x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 70.4 ms: 1.12x faster                                                  |
| float                      | 80.8 ms                                                | 72.6 ms: 1.11x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.87 ms: 1.10x faster                                                  |
| comprehensions             | 19.8 us                                                | 18.1 us: 1.10x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 89.1 ms: 1.09x faster                                                  |
| pylint                     | 319 ms                                                 | 295 ms: 1.08x faster                                                   |
| scimark_sor                | 130 ms                                                 | 121 ms: 1.07x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.44 sec: 1.07x faster                                                 |
| logging_silent             | 109 ns                                                 | 102 ns: 1.07x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.92 us: 1.05x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 2.00 sec: 1.05x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 134 ms: 1.04x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.04x faster                                                 |
| chaos                      | 62.8 ms                                                | 61.7 ms: 1.02x faster                                                  |
| async_generators           | 384 ms                                                 | 379 ms: 1.01x faster                                                   |
| raytrace                   | 299 ms                                                 | 296 ms: 1.01x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 514 ms: 1.01x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.8 ms: 1.00x faster                                                  |
| regex_compile              | 142 ms                                                 | 142 ms: 1.00x faster                                                   |
| regex_v8                   | 20.6 ms                                                | 20.9 ms: 1.02x slower                                                  |
| scimark_fft                | 342 ms                                                 | 351 ms: 1.03x slower                                                   |
| docutils                   | 2.64 sec                                               | 2.72 sec: 1.03x slower                                                 |
| spectral_norm              | 110 ms                                                 | 114 ms: 1.03x slower                                                   |
| logging_simple             | 6.63 us                                                | 6.87 us: 1.04x slower                                                  |
| html5lib                   | 63.6 ms                                                | 65.9 ms: 1.04x slower                                                  |
| pyflate                    | 448 ms                                                 | 470 ms: 1.05x slower                                                   |
| logging_format             | 7.35 us                                                | 7.76 us: 1.06x slower                                                  |
| hexiom                     | 6.17 ms                                                | 6.52 ms: 1.06x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 11.0 ms: 1.06x slower                                                  |
| deltablue                  | 3.45 ms                                                | 3.68 ms: 1.07x slower                                                  |
| json                       | 5.02 ms                                                | 5.37 ms: 1.07x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 795 ms: 1.07x slower                                                   |
| regex_dna                  | 168 ms                                                 | 180 ms: 1.07x slower                                                   |
| unpickle_pure_python       | 221 us                                                 | 237 us: 1.07x slower                                                   |
| sympy_str                  | 292 ms                                                 | 314 ms: 1.08x slower                                                   |
| sympy_integrate            | 20.5 ms                                                | 22.2 ms: 1.08x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 179 ms: 1.08x slower                                                   |
| pickle_pure_python         | 308 us                                                 | 332 us: 1.08x slower                                                   |
| 2to3                       | 264 ms                                                 | 285 ms: 1.08x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.65 sec: 1.09x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 55.3 ms: 1.10x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 127 ms: 1.11x slower                                                   |
| richards                   | 45.9 ms                                                | 51.5 ms: 1.12x slower                                                  |
| pidigits                   | 184 ms                                                 | 207 ms: 1.12x slower                                                   |
| sympy_expand               | 468 ms                                                 | 526 ms: 1.12x slower                                                   |
| nqueens                    | 80.1 ms                                                | 90.2 ms: 1.13x slower                                                  |
| thrift                     | 791 us                                                 | 902 us: 1.14x slower                                                   |
| crypto_pyaes               | 76.6 ms                                                | 87.3 ms: 1.14x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 78.0 ms: 1.14x slower                                                  |
| genshi_text                | 22.8 ms                                                | 26.1 ms: 1.14x slower                                                  |
| richards_super             | 51.9 ms                                                | 59.3 ms: 1.14x slower                                                  |
| django_template            | 34.7 ms                                                | 40.4 ms: 1.16x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 100 ms: 1.17x slower                                                   |
| meteor_contest             | 104 ms                                                 | 122 ms: 1.18x slower                                                   |
| json_loads                 | 26.5 us                                                | 31.6 us: 1.19x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 195 us: 1.19x slower                                                   |
| xml_etree_process          | 59.0 ms                                                | 71.0 ms: 1.20x slower                                                  |
| fannkuch                   | 372 ms                                                 | 459 ms: 1.23x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.49 ms: 1.25x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 9.83 ms: 1.37x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.50 ms: 1.37x slower                                                  |
| nbody                      | 89.3 ms                                                | 126 ms: 1.41x slower                                                   |
| mako                       | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                  |
| coverage                   | 71.4 ms                                                | 114 ms: 1.60x slower                                                   |
| python_startup             | 9.93 ms                                                | 16.0 ms: 1.62x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.62 ms: 1.72x slower                                                  |
| telco                      | 6.53 ms                                                | 174 ms: 26.58x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.03x slower                                                           |

Benchmark hidden because not significant (1): generators
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260301-3.15.0a6+-c9a5d9a-NOGIL/bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.032x slower

# HPT report

- Reliability score: 84.31% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.44x