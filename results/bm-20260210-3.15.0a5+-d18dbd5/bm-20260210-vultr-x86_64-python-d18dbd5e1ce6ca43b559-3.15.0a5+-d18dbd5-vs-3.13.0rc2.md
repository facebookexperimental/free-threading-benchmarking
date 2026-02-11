# Results vs. 3.13.0rc2

- fork: python
- ref: d18dbd5e1ce6ca43b559
- machine: linux-x86_64
- commit hash: d18dbd5
- commit date: 2026-02-10
- overall geometric mean: 1.036x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 248 ms: 1.05x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.54 sec: 1.03x faster                                                 |
| html5lib       | 67.0 ms                                                      | 60.0 ms: 1.12x faster                                                  |
| Geometric mean | (ref)                                                        | 1.06x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 565 ms: 1.62x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 305 ms: 1.51x faster                                                   |
| async_tree_io              | 876 ms                                                       | 596 ms: 1.47x faster                                                   |
| async_tree_none            | 354 ms                                                       | 248 ms: 1.43x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 299 ms: 1.39x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 493 ms: 1.35x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 249 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 498 ms: 1.28x faster                                                   |
| async_generators           | 377 ms                                                       | 340 ms: 1.11x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 22.8 ms: 1.03x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.30x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 70.3 ms: 1.10x faster                                                  |
| pidigits       | 217 ms                                                       | 206 ms: 1.05x faster                                                   |
| nbody          | 85.1 ms                                                      | 90.9 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 132 ms                                                       | 124 ms: 1.07x faster                                                   |
| regex_effbot   | 3.08 ms                                                      | 3.06 ms: 1.01x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 22.8 ms: 1.01x slower                                                  |
| regex_dna      | 180 ms                                                       | 188 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                        | 1.01x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 84.7 ms: 1.12x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 1.82 sec: 1.10x faster                                                 |
| json_dumps           | 10.5 ms                                                      | 9.96 ms: 1.06x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 82.7 ms: 1.03x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 58.3 ms: 1.02x faster                                                  |
| unpickle_pure_python | 210 us                                                       | 213 us: 1.01x slower                                                   |
| json_loads           | 27.0 us                                                      | 28.2 us: 1.04x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 309 us: 1.05x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.29 ms: 1.01x faster                                                  |
| python_startup         | 11.0 ms                                                      | 12.5 ms: 1.13x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.06x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 20.9 ms: 1.03x faster                                                  |
| genshi_xml      | 48.8 ms                                                      | 49.5 ms: 1.02x slower                                                  |
| mako            | 11.3 ms                                                      | 11.9 ms: 1.05x slower                                                  |
| django_template | 34.1 ms                                                      | 36.3 ms: 1.06x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.14 sec: 2.07x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 565 ms: 1.62x faster                                                   |
| deepcopy                   | 355 us                                                       | 233 us: 1.52x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 305 ms: 1.51x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 26.0 us: 1.50x faster                                                  |
| async_tree_io              | 876 ms                                                       | 596 ms: 1.47x faster                                                   |
| async_tree_none            | 354 ms                                                       | 248 ms: 1.43x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 299 ms: 1.39x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 493 ms: 1.35x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 249 ms: 1.35x faster                                                   |
| go                         | 141 ms                                                       | 105 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 498 ms: 1.28x faster                                                   |
| scimark_sor                | 134 ms                                                       | 107 ms: 1.25x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.56 us: 1.22x faster                                                  |
| spectral_norm              | 111 ms                                                       | 95.5 ms: 1.16x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 84.7 ms: 1.12x faster                                                  |
| pylint                     | 317 ms                                                       | 283 ms: 1.12x faster                                                   |
| html5lib                   | 67.0 ms                                                      | 60.0 ms: 1.12x faster                                                  |
| scimark_fft                | 349 ms                                                       | 313 ms: 1.11x faster                                                   |
| async_generators           | 377 ms                                                       | 340 ms: 1.11x faster                                                   |
| pathlib                    | 19.2 ms                                                      | 17.4 ms: 1.11x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.82 sec: 1.10x faster                                                 |
| float                      | 77.5 ms                                                      | 70.3 ms: 1.10x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 67.9 ms: 1.10x faster                                                  |
| pyflate                    | 449 ms                                                       | 413 ms: 1.09x faster                                                   |
| regex_compile              | 132 ms                                                       | 124 ms: 1.07x faster                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.41 ms: 1.07x faster                                                  |
| richards                   | 45.2 ms                                                      | 42.4 ms: 1.07x faster                                                  |
| pprint_safe_repr           | 738 ms                                                       | 692 ms: 1.07x faster                                                   |
| richards_super             | 51.6 ms                                                      | 48.6 ms: 1.06x faster                                                  |
| hexiom                     | 5.99 ms                                                      | 5.64 ms: 1.06x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.20 sec: 1.06x faster                                                 |
| json_dumps                 | 10.5 ms                                                      | 9.96 ms: 1.06x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.42 sec: 1.06x faster                                                 |
| pidigits                   | 217 ms                                                       | 206 ms: 1.05x faster                                                   |
| 2to3                       | 260 ms                                                       | 248 ms: 1.05x faster                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 62.4 ms: 1.05x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| sympy_integrate            | 19.8 ms                                                      | 19.2 ms: 1.03x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 22.8 ms: 1.03x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 82.7 ms: 1.03x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 109 ms: 1.03x faster                                                   |
| genshi_text                | 21.5 ms                                                      | 20.9 ms: 1.03x faster                                                  |
| generators                 | 28.8 ms                                                      | 28.0 ms: 1.03x faster                                                  |
| coverage                   | 83.0 ms                                                      | 80.5 ms: 1.03x faster                                                  |
| logging_simple             | 6.16 us                                                      | 5.98 us: 1.03x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.54 sec: 1.03x faster                                                 |
| thrift                     | 778 us                                                       | 759 us: 1.03x faster                                                   |
| pycparser                  | 1.12 sec                                                     | 1.09 sec: 1.02x faster                                                 |
| xml_etree_process          | 59.3 ms                                                      | 58.3 ms: 1.02x faster                                                  |
| comprehensions             | 16.5 us                                                      | 16.2 us: 1.02x faster                                                  |
| chaos                      | 57.3 ms                                                      | 56.4 ms: 1.02x faster                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.29 ms: 1.01x faster                                                  |
| logging_silent             | 103 ns                                                       | 101 ns: 1.01x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 3.06 ms: 1.01x faster                                                  |
| nqueens                    | 78.6 ms                                                      | 78.0 ms: 1.01x faster                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 68.2 ms: 1.00x slower                                                  |
| regex_v8                   | 22.7 ms                                                      | 22.8 ms: 1.01x slower                                                  |
| sympy_str                  | 275 ms                                                       | 277 ms: 1.01x slower                                                   |
| sympy_sum                  | 156 ms                                                       | 157 ms: 1.01x slower                                                   |
| raytrace                   | 253 ms                                                       | 256 ms: 1.01x slower                                                   |
| unpickle_pure_python       | 210 us                                                       | 213 us: 1.01x slower                                                   |
| genshi_xml                 | 48.8 ms                                                      | 49.5 ms: 1.02x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 158 us: 1.02x slower                                                   |
| json                       | 4.93 ms                                                      | 5.07 ms: 1.03x slower                                                  |
| regex_dna                  | 180 ms                                                       | 188 ms: 1.04x slower                                                   |
| json_loads                 | 27.0 us                                                      | 28.2 us: 1.04x slower                                                  |
| fannkuch                   | 370 ms                                                       | 387 ms: 1.05x slower                                                   |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 309 us: 1.05x slower                                                   |
| mako                       | 11.3 ms                                                      | 11.9 ms: 1.05x slower                                                  |
| django_template            | 34.1 ms                                                      | 36.3 ms: 1.06x slower                                                  |
| nbody                      | 85.1 ms                                                      | 90.9 ms: 1.07x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.34 ms: 1.07x slower                                                  |
| sympy_expand               | 457 ms                                                       | 491 ms: 1.07x slower                                                   |
| python_startup             | 11.0 ms                                                      | 12.5 ms: 1.13x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.28 ms: 1.36x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.84 ms: 1.37x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.31 ms: 1.42x slower                                                  |
| telco                      | 7.82 ms                                                      | 157 ms: 20.05x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 267 ms: 24.27x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (3): meteor_contest, logging_format, sqlite_synth
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260210-3.15.0a5+-d18dbd5/bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.036x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.16x