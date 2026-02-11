# Results vs. 3.12.6

- fork: python
- ref: d18dbd5e1ce6ca43b559
- machine: linux-x86_64
- commit hash: d18dbd5
- commit date: 2026-02-10
- overall geometric mean: 1.072x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 248 ms: 1.06x faster                                                   |
| docutils       | 2.64 sec                                               | 2.54 sec: 1.04x faster                                                 |
| html5lib       | 63.6 ms                                                | 60.0 ms: 1.06x faster                                                  |
| Geometric mean | (ref)                                                  | 1.05x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 565 ms: 1.97x faster                                                   |
| async_tree_none            | 464 ms                                                 | 248 ms: 1.87x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 299 ms: 1.87x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 305 ms: 1.82x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 596 ms: 1.82x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 249 ms: 1.79x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 498 ms: 1.45x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 493 ms: 1.45x faster                                                   |
| async_generators           | 384 ms                                                 | 340 ms: 1.13x faster                                                   |
| coroutines                 | 23.9 ms                                                | 22.8 ms: 1.05x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.52x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.3 ms: 1.15x faster                                                  |
| nbody          | 89.3 ms                                                | 90.9 ms: 1.02x slower                                                  |
| pidigits       | 184 ms                                                 | 206 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                  | 1.00x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 124 ms: 1.15x faster                                                   |
| regex_effbot   | 3.17 ms                                                | 3.06 ms: 1.04x faster                                                  |
| regex_v8       | 20.6 ms                                                | 22.8 ms: 1.11x slower                                                  |
| regex_dna      | 168 ms                                                 | 188 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                  | 1.01x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.82 sec: 1.16x faster                                                 |
| xml_etree_iterparse  | 96.7 ms                                                | 84.7 ms: 1.14x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| json_dumps           | 10.4 ms                                                | 9.96 ms: 1.04x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 213 us: 1.04x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 82.7 ms: 1.03x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 58.3 ms: 1.01x faster                                                  |
| pickle_pure_python   | 308 us                                                 | 309 us: 1.00x slower                                                   |
| json_loads           | 26.5 us                                                | 28.2 us: 1.06x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.29 ms: 1.02x slower                                                  |
| python_startup         | 9.93 ms                                                | 12.5 ms: 1.25x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.9 ms: 1.09x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 49.5 ms: 1.01x faster                                                  |
| django_template | 34.7 ms                                                | 36.3 ms: 1.05x slower                                                  |
| mako            | 11.0 ms                                                | 11.9 ms: 1.08x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.14 sec: 2.12x faster                                                 |
| async_tree_io_tg           | 1.11 sec                                               | 565 ms: 1.97x faster                                                   |
| async_tree_none            | 464 ms                                                 | 248 ms: 1.87x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 299 ms: 1.87x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 305 ms: 1.82x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 596 ms: 1.82x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 249 ms: 1.79x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 26.0 us: 1.55x faster                                                  |
| deepcopy                   | 352 us                                                 | 233 us: 1.51x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 498 ms: 1.45x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 493 ms: 1.45x faster                                                   |
| go                         | 139 ms                                                 | 105 ms: 1.33x faster                                                   |
| pathlib                    | 21.5 ms                                                | 17.4 ms: 1.24x faster                                                  |
| comprehensions             | 19.8 us                                                | 16.2 us: 1.22x faster                                                  |
| scimark_sor                | 130 ms                                                 | 107 ms: 1.21x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.56 us: 1.20x faster                                                  |
| raytrace                   | 299 ms                                                 | 256 ms: 1.17x faster                                                   |
| dulwich_log                | 78.9 ms                                                | 67.9 ms: 1.16x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.82 sec: 1.16x faster                                                 |
| spectral_norm              | 110 ms                                                 | 95.5 ms: 1.15x faster                                                  |
| generators                 | 32.2 ms                                                | 28.0 ms: 1.15x faster                                                  |
| regex_compile              | 142 ms                                                 | 124 ms: 1.15x faster                                                   |
| float                      | 80.8 ms                                                | 70.3 ms: 1.15x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 84.7 ms: 1.14x faster                                                  |
| async_generators           | 384 ms                                                 | 340 ms: 1.13x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.20 sec: 1.13x faster                                                 |
| pylint                     | 319 ms                                                 | 283 ms: 1.12x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 68.2 ms: 1.12x faster                                                  |
| chaos                      | 62.8 ms                                                | 56.4 ms: 1.11x faster                                                  |
| logging_simple             | 6.63 us                                                | 5.98 us: 1.11x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 62.4 ms: 1.10x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.64 ms: 1.09x faster                                                  |
| genshi_text                | 22.8 ms                                                | 20.9 ms: 1.09x faster                                                  |
| scimark_fft                | 342 ms                                                 | 313 ms: 1.09x faster                                                   |
| pyflate                    | 448 ms                                                 | 413 ms: 1.08x faster                                                   |
| richards                   | 45.9 ms                                                | 42.4 ms: 1.08x faster                                                  |
| logging_format             | 7.35 us                                                | 6.81 us: 1.08x faster                                                  |
| logging_silent             | 109 ns                                                 | 101 ns: 1.08x faster                                                   |
| pprint_safe_repr           | 743 ms                                                 | 692 ms: 1.07x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.42 sec: 1.07x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 19.2 ms: 1.07x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.09 sec: 1.07x faster                                                 |
| richards_super             | 51.9 ms                                                | 48.6 ms: 1.07x faster                                                  |
| 2to3                       | 264 ms                                                 | 248 ms: 1.06x faster                                                   |
| html5lib                   | 63.6 ms                                                | 60.0 ms: 1.06x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 157 ms: 1.06x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| sympy_str                  | 292 ms                                                 | 277 ms: 1.05x faster                                                   |
| coroutines                 | 23.9 ms                                                | 22.8 ms: 1.05x faster                                                  |
| scimark_lu                 | 114 ms                                                 | 109 ms: 1.05x faster                                                   |
| thrift                     | 791 us                                                 | 759 us: 1.04x faster                                                   |
| json_dumps                 | 10.4 ms                                                | 9.96 ms: 1.04x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.54 sec: 1.04x faster                                                 |
| typing_runtime_protocols   | 163 us                                                 | 158 us: 1.04x faster                                                   |
| unpickle_pure_python       | 221 us                                                 | 213 us: 1.04x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 3.06 ms: 1.04x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.34 ms: 1.03x faster                                                  |
| xml_etree_generate         | 85.2 ms                                                | 82.7 ms: 1.03x faster                                                  |
| nqueens                    | 80.1 ms                                                | 78.0 ms: 1.03x faster                                                  |
| meteor_contest             | 104 ms                                                 | 101 ms: 1.02x faster                                                   |
| genshi_xml                 | 50.2 ms                                                | 49.5 ms: 1.01x faster                                                  |
| xml_etree_process          | 59.0 ms                                                | 58.3 ms: 1.01x faster                                                  |
| pickle_pure_python         | 308 us                                                 | 309 us: 1.00x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.41 ms: 1.00x slower                                                  |
| json                       | 5.02 ms                                                | 5.07 ms: 1.01x slower                                                  |
| sqlite_synth               | 2.20 us                                                | 2.22 us: 1.01x slower                                                  |
| nbody                      | 89.3 ms                                                | 90.9 ms: 1.02x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.29 ms: 1.02x slower                                                  |
| fannkuch                   | 372 ms                                                 | 387 ms: 1.04x slower                                                   |
| django_template            | 34.7 ms                                                | 36.3 ms: 1.05x slower                                                  |
| sympy_expand               | 468 ms                                                 | 491 ms: 1.05x slower                                                   |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                   |
| json_loads                 | 26.5 us                                                | 28.2 us: 1.06x slower                                                  |
| mako                       | 11.0 ms                                                | 11.9 ms: 1.08x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 22.8 ms: 1.11x slower                                                  |
| pidigits                   | 184 ms                                                 | 206 ms: 1.12x slower                                                   |
| regex_dna                  | 168 ms                                                 | 188 ms: 1.12x slower                                                   |
| coverage                   | 71.4 ms                                                | 80.5 ms: 1.13x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.28 ms: 1.24x slower                                                  |
| python_startup             | 9.93 ms                                                | 12.5 ms: 1.25x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.31 ms: 1.39x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.84 ms: 1.68x slower                                                  |
| telco                      | 6.53 ms                                                | 157 ms: 24.03x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 267 ms: 24.71x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                           |
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260210-3.15.0a5+-d18dbd5/bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.072x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.17x