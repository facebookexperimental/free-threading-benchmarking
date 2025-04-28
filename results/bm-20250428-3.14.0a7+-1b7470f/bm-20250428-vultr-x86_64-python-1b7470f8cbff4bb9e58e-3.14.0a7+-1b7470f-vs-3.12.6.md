# Results vs. 3.12.6

- fork: python
- ref: 1b7470f8cbff4bb9e58e
- machine: linux-x86_64
- commit hash: 1b7470f
- commit date: 2025-04-28
- overall geometric mean: 1.116x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-vultr-x86_64-python-1b7470f8cbff4bb9e58e-3.14.0a7+-1b7470f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 247 ms: 1.07x faster                                                   |
| docutils       | 2.64 sec                                               | 2.51 sec: 1.05x faster                                                 |
| Geometric mean | (ref)                                                  | 1.06x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-vultr-x86_64-python-1b7470f8cbff4bb9e58e-3.14.0a7+-1b7470f |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 603 ms: 1.84x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 307 ms: 1.81x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 311 ms: 1.80x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 604 ms: 1.79x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 255 ms: 1.75x faster                                                   |
| async_tree_none            | 464 ms                                                 | 268 ms: 1.73x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 508 ms: 1.42x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 514 ms: 1.39x faster                                                   |
| async_generators           | 384 ms                                                 | 327 ms: 1.17x faster                                                   |
| coroutines                 | 23.9 ms                                                | 22.8 ms: 1.05x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.49x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-vultr-x86_64-python-1b7470f8cbff4bb9e58e-3.14.0a7+-1b7470f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 69.8 ms: 1.16x faster                                                  |
| nbody          | 89.3 ms                                                | 87.6 ms: 1.02x faster                                                  |
| pidigits       | 184 ms                                                 | 200 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-vultr-x86_64-python-1b7470f8cbff4bb9e58e-3.14.0a7+-1b7470f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.68 ms: 1.18x faster                                                  |
| regex_compile  | 142 ms                                                 | 122 ms: 1.17x faster                                                   |
| regex_dna      | 168 ms                                                 | 171 ms: 1.02x slower                                                   |
| regex_v8       | 20.6 ms                                                | 21.4 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                  | 1.07x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-vultr-x86_64-python-1b7470f8cbff4bb9e58e-3.14.0a7+-1b7470f |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.85 sec: 1.14x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 91.6 ms: 1.06x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 211 us: 1.05x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 81.8 ms: 1.04x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 57.1 ms: 1.03x faster                                                  |
| pickle_pure_python   | 308 us                                                 | 304 us: 1.01x faster                                                   |
| json_loads           | 26.5 us                                                | 27.2 us: 1.02x slower                                                  |
| json_dumps           | 10.4 ms                                                | 11.4 ms: 1.10x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-vultr-x86_64-python-1b7470f8cbff4bb9e58e-3.14.0a7+-1b7470f |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 8.67 ms: 1.21x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.1 ms: 1.52x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.36x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-vultr-x86_64-python-1b7470f8cbff4bb9e58e-3.14.0a7+-1b7470f |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.6 ms: 1.11x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 47.6 ms: 1.05x faster                                                  |
| django_template | 34.7 ms                                                | 34.3 ms: 1.01x faster                                                  |
| mako            | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.02x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-vultr-x86_64-python-1b7470f8cbff4bb9e58e-3.14.0a7+-1b7470f |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.13 sec: 2.15x faster                                                 |
| async_tree_io_tg           | 1.11 sec                                               | 603 ms: 1.84x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 307 ms: 1.81x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 311 ms: 1.80x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 604 ms: 1.79x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 255 ms: 1.75x faster                                                   |
| async_tree_none            | 464 ms                                                 | 268 ms: 1.73x faster                                                   |
| deepcopy                   | 352 us                                                 | 247 us: 1.43x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 508 ms: 1.42x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 28.9 us: 1.39x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 514 ms: 1.39x faster                                                   |
| go                         | 139 ms                                                 | 109 ms: 1.28x faster                                                   |
| raytrace                   | 299 ms                                                 | 249 ms: 1.20x faster                                                   |
| scimark_sor                | 130 ms                                                 | 108 ms: 1.20x faster                                                   |
| comprehensions             | 19.8 us                                                | 16.7 us: 1.19x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.59 us: 1.19x faster                                                  |
| spectral_norm              | 110 ms                                                 | 93.0 ms: 1.19x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.68 ms: 1.18x faster                                                  |
| chaos                      | 62.8 ms                                                | 53.2 ms: 1.18x faster                                                  |
| async_generators           | 384 ms                                                 | 327 ms: 1.17x faster                                                   |
| regex_compile              | 142 ms                                                 | 122 ms: 1.17x faster                                                   |
| dulwich_log                | 78.9 ms                                                | 67.8 ms: 1.16x faster                                                  |
| float                      | 80.8 ms                                                | 69.8 ms: 1.16x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.10 sec: 1.16x faster                                                 |
| generators                 | 32.2 ms                                                | 27.9 ms: 1.15x faster                                                  |
| pylint                     | 319 ms                                                 | 278 ms: 1.15x faster                                                   |
| logging_silent             | 109 ns                                                 | 95.0 ns: 1.15x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.85 sec: 1.14x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.0 ms: 1.13x faster                                                  |
| crypto_pyaes               | 76.6 ms                                                | 68.0 ms: 1.13x faster                                                  |
| logging_simple             | 6.63 us                                                | 5.90 us: 1.12x faster                                                  |
| pyflate                    | 448 ms                                                 | 401 ms: 1.12x faster                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 61.6 ms: 1.11x faster                                                  |
| genshi_text                | 22.8 ms                                                | 20.6 ms: 1.11x faster                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.7 ms: 1.11x faster                                                  |
| logging_format             | 7.35 us                                                | 6.64 us: 1.11x faster                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 129 ms: 1.11x faster                                                   |
| scimark_fft                | 342 ms                                                 | 309 ms: 1.10x faster                                                   |
| richards                   | 45.9 ms                                                | 41.8 ms: 1.10x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 18.7 ms: 1.10x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 151 ms: 1.10x faster                                                   |
| sympy_str                  | 292 ms                                                 | 265 ms: 1.10x faster                                                   |
| richards_super             | 51.9 ms                                                | 47.4 ms: 1.09x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.40 sec: 1.08x faster                                                 |
| hexiom                     | 6.17 ms                                                | 5.70 ms: 1.08x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 687 ms: 1.08x faster                                                   |
| 2to3                       | 264 ms                                                 | 247 ms: 1.07x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.10 sec: 1.06x faster                                                 |
| nqueens                    | 80.1 ms                                                | 75.4 ms: 1.06x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| typing_runtime_protocols   | 163 us                                                 | 155 us: 1.06x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 91.6 ms: 1.06x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.26 ms: 1.06x faster                                                  |
| genshi_xml                 | 50.2 ms                                                | 47.6 ms: 1.05x faster                                                  |
| coroutines                 | 23.9 ms                                                | 22.8 ms: 1.05x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.51 sec: 1.05x faster                                                 |
| sympy_expand               | 468 ms                                                 | 447 ms: 1.05x faster                                                   |
| unpickle_pure_python       | 221 us                                                 | 211 us: 1.05x faster                                                   |
| xml_etree_generate         | 85.2 ms                                                | 81.8 ms: 1.04x faster                                                  |
| xml_etree_process          | 59.0 ms                                                | 57.1 ms: 1.03x faster                                                  |
| meteor_contest             | 104 ms                                                 | 100 ms: 1.03x faster                                                   |
| scimark_lu                 | 114 ms                                                 | 111 ms: 1.03x faster                                                   |
| json                       | 5.02 ms                                                | 4.88 ms: 1.03x faster                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.28 ms: 1.03x faster                                                  |
| nbody                      | 89.3 ms                                                | 87.6 ms: 1.02x faster                                                  |
| pickle_pure_python         | 308 us                                                 | 304 us: 1.01x faster                                                   |
| django_template            | 34.7 ms                                                | 34.3 ms: 1.01x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.18 us: 1.01x faster                                                  |
| fannkuch                   | 372 ms                                                 | 377 ms: 1.01x slower                                                   |
| regex_dna                  | 168 ms                                                 | 171 ms: 1.02x slower                                                   |
| json_loads                 | 26.5 us                                                | 27.2 us: 1.02x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 21.4 ms: 1.04x slower                                                  |
| mako                       | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                  |
| pidigits                   | 184 ms                                                 | 200 ms: 1.09x slower                                                   |
| telco                      | 6.53 ms                                                | 7.18 ms: 1.10x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 11.4 ms: 1.10x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.05 ms: 1.11x slower                                                  |
| coverage                   | 71.4 ms                                                | 80.9 ms: 1.13x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 8.67 ms: 1.21x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.63 ms: 1.34x slower                                                  |
| python_startup             | 9.93 ms                                                | 15.1 ms: 1.52x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.86 ms: 1.70x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 88.6 ms: 8.20x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.08x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250428-3.14.0a7+-1b7470f/bm-20250428-vultr-x86_64-python-1b7470f8cbff4bb9e58e-3.14.0a7+-1b7470f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.116x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.13x