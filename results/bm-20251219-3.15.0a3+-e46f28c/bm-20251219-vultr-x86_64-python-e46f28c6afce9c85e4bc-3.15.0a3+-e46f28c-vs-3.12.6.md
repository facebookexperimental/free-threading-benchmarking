# Results vs. 3.12.6

- fork: python
- ref: e46f28c6afce9c85e4bc
- machine: linux-x86_64
- commit hash: e46f28c
- commit date: 2025-12-19
- overall geometric mean: 1.068x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3+-e46f28c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 245 ms: 1.07x faster                                                   |
| docutils       | 2.64 sec                                               | 2.57 sec: 1.03x faster                                                 |
| html5lib       | 63.6 ms                                                | 60.3 ms: 1.06x faster                                                  |
| Geometric mean | (ref)                                                  | 1.05x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3+-e46f28c |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 554 ms: 1.95x faster                                                   |
| async_tree_none            | 464 ms                                                 | 243 ms: 1.91x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 584 ms: 1.90x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 243 ms: 1.84x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 308 ms: 1.82x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 307 ms: 1.81x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 533 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 533 ms: 1.34x faster                                                   |
| async_generators           | 384 ms                                                 | 345 ms: 1.12x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.50x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3+-e46f28c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.7 ms: 1.14x faster                                                  |
| nbody          | 89.3 ms                                                | 88.0 ms: 1.01x faster                                                  |
| pidigits       | 184 ms                                                 | 209 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3+-e46f28c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 123 ms: 1.16x faster                                                   |
| regex_effbot   | 3.17 ms                                                | 2.92 ms: 1.08x faster                                                  |
| regex_v8       | 20.6 ms                                                | 21.9 ms: 1.06x slower                                                  |
| regex_dna      | 168 ms                                                 | 188 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3+-e46f28c |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 84.8 ms: 1.14x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| unpickle_pure_python | 221 us                                                 | 213 us: 1.04x faster                                                   |
| json_dumps           | 10.4 ms                                                | 10.00 ms: 1.04x faster                                                 |
| xml_etree_generate   | 85.2 ms                                                | 83.1 ms: 1.03x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 58.0 ms: 1.02x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.12 sec: 1.01x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 311 us: 1.01x slower                                                   |
| json_loads           | 26.5 us                                                | 27.3 us: 1.03x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3+-e46f28c |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.28 ms: 1.02x slower                                                  |
| python_startup         | 9.93 ms                                                | 12.4 ms: 1.25x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3+-e46f28c |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.6 ms: 1.06x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 50.9 ms: 1.01x slower                                                  |
| django_template | 34.7 ms                                                | 35.5 ms: 1.02x slower                                                  |
| mako            | 11.0 ms                                                | 11.6 ms: 1.06x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3+-e46f28c |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.16 sec: 2.09x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 554 ms: 1.95x faster                                                   |
| async_tree_none            | 464 ms                                                 | 243 ms: 1.91x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 584 ms: 1.90x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 243 ms: 1.84x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 308 ms: 1.82x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 307 ms: 1.81x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 26.3 us: 1.53x faster                                                  |
| deepcopy                   | 352 us                                                 | 248 us: 1.42x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 533 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 533 ms: 1.34x faster                                                   |
| go                         | 139 ms                                                 | 105 ms: 1.33x faster                                                   |
| comprehensions             | 19.8 us                                                | 16.1 us: 1.23x faster                                                  |
| pathlib                    | 21.5 ms                                                | 17.8 ms: 1.21x faster                                                  |
| scimark_sor                | 130 ms                                                 | 108 ms: 1.20x faster                                                   |
| spectral_norm              | 110 ms                                                 | 93.5 ms: 1.18x faster                                                  |
| raytrace                   | 299 ms                                                 | 255 ms: 1.17x faster                                                   |
| dulwich_log                | 78.9 ms                                                | 68.2 ms: 1.16x faster                                                  |
| regex_compile              | 142 ms                                                 | 123 ms: 1.16x faster                                                   |
| logging_simple             | 6.63 us                                                | 5.74 us: 1.15x faster                                                  |
| generators                 | 32.2 ms                                                | 28.2 ms: 1.14x faster                                                  |
| float                      | 80.8 ms                                                | 70.7 ms: 1.14x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 84.8 ms: 1.14x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.18 sec: 1.13x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.73 us: 1.13x faster                                                  |
| chaos                      | 62.8 ms                                                | 55.7 ms: 1.13x faster                                                  |
| scimark_fft                | 342 ms                                                 | 304 ms: 1.12x faster                                                   |
| pylint                     | 319 ms                                                 | 284 ms: 1.12x faster                                                   |
| async_generators           | 384 ms                                                 | 345 ms: 1.12x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 69.0 ms: 1.11x faster                                                  |
| logging_format             | 7.35 us                                                | 6.63 us: 1.11x faster                                                  |
| pyflate                    | 448 ms                                                 | 404 ms: 1.11x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.07 sec: 1.09x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 18.9 ms: 1.09x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 63.0 ms: 1.09x faster                                                  |
| richards                   | 45.9 ms                                                | 42.3 ms: 1.09x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.92 ms: 1.08x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.70 ms: 1.08x faster                                                  |
| richards_super             | 51.9 ms                                                | 48.0 ms: 1.08x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.41 sec: 1.08x faster                                                 |
| pprint_safe_repr           | 743 ms                                                 | 692 ms: 1.07x faster                                                   |
| 2to3                       | 264 ms                                                 | 245 ms: 1.07x faster                                                   |
| sympy_sum                  | 166 ms                                                 | 155 ms: 1.07x faster                                                   |
| sympy_str                  | 292 ms                                                 | 273 ms: 1.07x faster                                                   |
| typing_runtime_protocols   | 163 us                                                 | 153 us: 1.07x faster                                                   |
| scimark_lu                 | 114 ms                                                 | 107 ms: 1.06x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| html5lib                   | 63.6 ms                                                | 60.3 ms: 1.06x faster                                                  |
| genshi_text                | 22.8 ms                                                | 21.6 ms: 1.06x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.28 ms: 1.05x faster                                                  |
| logging_silent             | 109 ns                                                 | 104 ns: 1.05x faster                                                   |
| meteor_contest             | 104 ms                                                 | 99.7 ms: 1.04x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 213 us: 1.04x faster                                                   |
| json_dumps                 | 10.4 ms                                                | 10.00 ms: 1.04x faster                                                 |
| thrift                     | 791 us                                                 | 766 us: 1.03x faster                                                   |
| docutils                   | 2.64 sec                                               | 2.57 sec: 1.03x faster                                                 |
| xml_etree_generate         | 85.2 ms                                                | 83.1 ms: 1.03x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                                  |
| xml_etree_process          | 59.0 ms                                                | 58.0 ms: 1.02x faster                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.32 ms: 1.02x faster                                                  |
| nbody                      | 89.3 ms                                                | 88.0 ms: 1.01x faster                                                  |
| nqueens                    | 80.1 ms                                                | 79.2 ms: 1.01x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 2.12 sec: 1.01x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 311 us: 1.01x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 50.9 ms: 1.01x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.28 ms: 1.02x slower                                                  |
| django_template            | 34.7 ms                                                | 35.5 ms: 1.02x slower                                                  |
| json_loads                 | 26.5 us                                                | 27.3 us: 1.03x slower                                                  |
| sqlite_synth               | 2.20 us                                                | 2.28 us: 1.03x slower                                                  |
| sympy_expand               | 468 ms                                                 | 484 ms: 1.03x slower                                                   |
| fannkuch                   | 372 ms                                                 | 385 ms: 1.04x slower                                                   |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                   |
| mako                       | 11.0 ms                                                | 11.6 ms: 1.06x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 21.9 ms: 1.06x slower                                                  |
| regex_dna                  | 168 ms                                                 | 188 ms: 1.12x slower                                                   |
| pidigits                   | 184 ms                                                 | 209 ms: 1.13x slower                                                   |
| coverage                   | 71.4 ms                                                | 81.7 ms: 1.14x slower                                                  |
| python_startup             | 9.93 ms                                                | 12.4 ms: 1.25x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.82 ms: 1.39x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.32 ms: 1.40x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.93 ms: 1.77x slower                                                  |
| telco                      | 6.53 ms                                                | 160 ms: 24.57x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 335 ms: 31.05x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (1): json
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251219-3.15.0a3+-e46f28c/bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3+-e46f28c.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.068x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.16x