# Results vs. 3.12.6

- fork: python
- ref: bdd23c0bb95faa37130f
- machine: linux-x86_64
- commit hash: bdd23c0
- commit date: 2025-04-28
- overall geometric mean: 1.036x faster
- HPT reliability: 57.93%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 281 ms: 1.07x slower                                                   |
| docutils       | 2.64 sec                                               | 2.70 sec: 1.02x slower                                                 |
| html5lib       | 63.6 ms                                                | 65.4 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 515 ms: 2.16x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 223 ms: 2.00x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 543 ms: 1.99x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 281 ms: 1.99x faster                                                   |
| async_tree_none            | 464 ms                                                 | 255 ms: 1.82x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 308 ms: 1.80x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 465 ms: 1.55x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 493 ms: 1.45x faster                                                   |
| async_generators           | 384 ms                                                 | 356 ms: 1.08x faster                                                   |
| coroutines                 | 23.9 ms                                                | 22.9 ms: 1.04x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.57x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 67.3 ms: 1.20x faster                                                  |
| pidigits       | 184 ms                                                 | 185 ms: 1.01x slower                                                   |
| nbody          | 89.3 ms                                                | 111 ms: 1.24x slower                                                   |
| Geometric mean | (ref)                                                  | 1.01x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.87 ms: 1.10x faster                                                  |
| regex_compile  | 142 ms                                                 | 143 ms: 1.01x slower                                                   |
| regex_v8       | 20.6 ms                                                | 21.2 ms: 1.03x slower                                                  |
| regex_dna      | 168 ms                                                 | 184 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                  | 1.01x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 86.4 ms: 1.12x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.07x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 2.09 sec: 1.01x faster                                                 |
| unpickle_pure_python | 221 us                                                 | 225 us: 1.02x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 328 us: 1.07x slower                                                   |
| xml_etree_generate   | 85.2 ms                                                | 91.8 ms: 1.08x slower                                                  |
| json_loads           | 26.5 us                                                | 29.6 us: 1.12x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 66.2 ms: 1.12x slower                                                  |
| json_dumps           | 10.4 ms                                                | 12.7 ms: 1.22x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.04x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.27 ms: 1.29x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.6 ms: 1.57x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.43x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 55.4 ms: 1.10x slower                                                  |
| genshi_text     | 22.8 ms                                                | 26.2 ms: 1.15x slower                                                  |
| django_template | 34.7 ms                                                | 40.1 ms: 1.16x slower                                                  |
| mako            | 11.0 ms                                                | 15.4 ms: 1.40x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.20x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 515 ms: 2.16x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 223 ms: 2.00x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 543 ms: 1.99x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 281 ms: 1.99x faster                                                   |
| gc_traversal               | 3.46 ms                                                | 1.78 ms: 1.94x faster                                                  |
| mdp                        | 2.42 sec                                               | 1.30 sec: 1.85x faster                                                 |
| async_tree_none            | 464 ms                                                 | 255 ms: 1.82x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 308 ms: 1.80x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 465 ms: 1.55x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 493 ms: 1.45x faster                                                   |
| deepcopy                   | 352 us                                                 | 288 us: 1.22x faster                                                   |
| float                      | 80.8 ms                                                | 67.3 ms: 1.20x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 34.5 us: 1.17x faster                                                  |
| go                         | 139 ms                                                 | 123 ms: 1.13x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 86.4 ms: 1.12x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 70.6 ms: 1.12x faster                                                  |
| scimark_sor                | 130 ms                                                 | 117 ms: 1.11x faster                                                   |
| pathlib                    | 21.5 ms                                                | 19.4 ms: 1.11x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.87 ms: 1.10x faster                                                  |
| spectral_norm              | 110 ms                                                 | 100 ms: 1.10x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 2.01 us: 1.10x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.33 sec: 1.09x faster                                                 |
| async_generators           | 384 ms                                                 | 356 ms: 1.08x faster                                                   |
| logging_silent             | 109 ns                                                 | 101 ns: 1.08x faster                                                   |
| generators                 | 32.2 ms                                                | 30.0 ms: 1.07x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.07x faster                                                   |
| pylint                     | 319 ms                                                 | 304 ms: 1.05x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.94 us: 1.05x faster                                                  |
| raytrace                   | 299 ms                                                 | 286 ms: 1.04x faster                                                   |
| coroutines                 | 23.9 ms                                                | 22.9 ms: 1.04x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.03x faster                                                 |
| chaos                      | 62.8 ms                                                | 60.8 ms: 1.03x faster                                                  |
| comprehensions             | 19.8 us                                                | 19.3 us: 1.03x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 2.09 sec: 1.01x faster                                                 |
| scimark_fft                | 342 ms                                                 | 338 ms: 1.01x faster                                                   |
| regex_compile              | 142 ms                                                 | 143 ms: 1.01x slower                                                   |
| pidigits                   | 184 ms                                                 | 185 ms: 1.01x slower                                                   |
| deltablue                  | 3.45 ms                                                | 3.50 ms: 1.01x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 225 us: 1.02x slower                                                   |
| pyflate                    | 448 ms                                                 | 457 ms: 1.02x slower                                                   |
| docutils                   | 2.64 sec                                               | 2.70 sec: 1.02x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 762 ms: 1.03x slower                                                   |
| html5lib                   | 63.6 ms                                                | 65.4 ms: 1.03x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 21.2 ms: 1.03x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.57 sec: 1.03x slower                                                 |
| logging_simple             | 6.63 us                                                | 6.89 us: 1.04x slower                                                  |
| logging_format             | 7.35 us                                                | 7.74 us: 1.05x slower                                                  |
| 2to3                       | 264 ms                                                 | 281 ms: 1.07x slower                                                   |
| sympy_sum                  | 166 ms                                                 | 177 ms: 1.07x slower                                                   |
| pickle_pure_python         | 308 us                                                 | 328 us: 1.07x slower                                                   |
| sympy_integrate            | 20.5 ms                                                | 21.9 ms: 1.07x slower                                                  |
| hexiom                     | 6.17 ms                                                | 6.59 ms: 1.07x slower                                                  |
| nqueens                    | 80.1 ms                                                | 85.6 ms: 1.07x slower                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 153 ms: 1.07x slower                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 73.7 ms: 1.08x slower                                                  |
| sympy_str                  | 292 ms                                                 | 314 ms: 1.08x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 91.8 ms: 1.08x slower                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.5 ms: 1.08x slower                                                  |
| richards                   | 45.9 ms                                                | 49.7 ms: 1.08x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 83.3 ms: 1.09x slower                                                  |
| regex_dna                  | 168 ms                                                 | 184 ms: 1.10x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 55.4 ms: 1.10x slower                                                  |
| richards_super             | 51.9 ms                                                | 57.4 ms: 1.11x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 127 ms: 1.11x slower                                                   |
| json_loads                 | 26.5 us                                                | 29.6 us: 1.12x slower                                                  |
| sympy_expand               | 468 ms                                                 | 523 ms: 1.12x slower                                                   |
| xml_etree_process          | 59.0 ms                                                | 66.2 ms: 1.12x slower                                                  |
| genshi_text                | 22.8 ms                                                | 26.2 ms: 1.15x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.05 ms: 1.15x slower                                                  |
| django_template            | 34.7 ms                                                | 40.1 ms: 1.16x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 190 us: 1.16x slower                                                   |
| fannkuch                   | 372 ms                                                 | 447 ms: 1.20x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 12.7 ms: 1.22x slower                                                  |
| meteor_contest             | 104 ms                                                 | 127 ms: 1.23x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.35 ms: 1.24x slower                                                  |
| nbody                      | 89.3 ms                                                | 111 ms: 1.24x slower                                                   |
| telco                      | 6.53 ms                                                | 8.25 ms: 1.26x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 9.27 ms: 1.29x slower                                                  |
| mako                       | 11.0 ms                                                | 15.4 ms: 1.40x slower                                                  |
| coverage                   | 71.4 ms                                                | 109 ms: 1.53x slower                                                   |
| python_startup             | 9.93 ms                                                | 15.6 ms: 1.57x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.13 ms: 3.32x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 95.4 ms: 8.84x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (2): json, asyncio_websockets
Ignored benchmarks (20) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250428-3.14.0a7+-bdd23c0-NOGIL/bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.036x faster

# HPT report

- Reliability score: 57.93% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.37x