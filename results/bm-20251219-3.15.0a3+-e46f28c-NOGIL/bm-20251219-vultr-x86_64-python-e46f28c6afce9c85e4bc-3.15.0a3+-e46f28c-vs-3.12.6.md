# Results vs. 3.12.6

- fork: python
- ref: e46f28c6afce9c85e4bc
- machine: linux-x86_64
- commit hash: e46f28c
- commit date: 2025-12-19
- overall geometric mean: 1.031x slower
- HPT reliability: 86.71%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3+-e46f28c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 276 ms: 1.05x slower                                                   |
| docutils       | 2.64 sec                                               | 2.73 sec: 1.03x slower                                                 |
| html5lib       | 63.6 ms                                                | 66.6 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3+-e46f28c |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 607 ms: 1.83x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 604 ms: 1.79x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 321 ms: 1.74x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 262 ms: 1.70x faster                                                   |
| async_tree_none            | 464 ms                                                 | 285 ms: 1.63x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 350 ms: 1.58x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 597 ms: 1.21x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 623 ms: 1.15x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 510 ms: 1.01x faster                                                   |
| async_generators           | 384 ms                                                 | 380 ms: 1.01x faster                                                   |
| coroutines                 | 23.9 ms                                                | 24.3 ms: 1.02x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.38x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3+-e46f28c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 72.9 ms: 1.11x faster                                                  |
| pidigits       | 184 ms                                                 | 226 ms: 1.23x slower                                                   |
| nbody          | 89.3 ms                                                | 120 ms: 1.35x slower                                                   |
| Geometric mean | (ref)                                                  | 1.14x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3+-e46f28c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.83 ms: 1.12x faster                                                  |
| regex_compile  | 142 ms                                                 | 141 ms: 1.01x faster                                                   |
| regex_v8       | 20.6 ms                                                | 21.3 ms: 1.03x slower                                                  |
| regex_dna      | 168 ms                                                 | 175 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3+-e46f28c |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 89.1 ms: 1.09x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 132 ms: 1.05x faster                                                   |
| unpickle_pure_python | 221 us                                                 | 233 us: 1.06x slower                                                   |
| tomli_loads          | 2.11 sec                                               | 2.24 sec: 1.06x slower                                                 |
| json_dumps           | 10.4 ms                                                | 11.1 ms: 1.07x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 331 us: 1.07x slower                                                   |
| xml_etree_generate   | 85.2 ms                                                | 96.7 ms: 1.13x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 69.5 ms: 1.18x slower                                                  |
| json_loads           | 26.5 us                                                | 32.2 us: 1.21x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.07x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3+-e46f28c |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.64 ms: 1.35x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3+-e46f28c |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 57.4 ms: 1.14x slower                                                  |
| django_template | 34.7 ms                                                | 40.0 ms: 1.15x slower                                                  |
| genshi_text     | 22.8 ms                                                | 26.7 ms: 1.17x slower                                                  |
| mako            | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.22x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3+-e46f28c |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.30 sec: 1.86x faster                                                 |
| async_tree_io_tg           | 1.11 sec                                               | 607 ms: 1.83x faster                                                   |
| gc_traversal               | 3.46 ms                                                | 1.91 ms: 1.81x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 604 ms: 1.79x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 321 ms: 1.74x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 262 ms: 1.70x faster                                                   |
| async_tree_none            | 464 ms                                                 | 285 ms: 1.63x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 350 ms: 1.58x faster                                                   |
| bench_mp_pool              | 10.8 ms                                                | 7.15 ms: 1.51x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 29.9 us: 1.35x faster                                                  |
| deepcopy                   | 352 us                                                 | 271 us: 1.30x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 597 ms: 1.21x faster                                                   |
| pathlib                    | 21.5 ms                                                | 17.9 ms: 1.21x faster                                                  |
| go                         | 139 ms                                                 | 120 ms: 1.16x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 623 ms: 1.15x faster                                                   |
| dulwich_log                | 78.9 ms                                                | 69.5 ms: 1.13x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.83 ms: 1.12x faster                                                  |
| comprehensions             | 19.8 us                                                | 17.7 us: 1.12x faster                                                  |
| float                      | 80.8 ms                                                | 72.9 ms: 1.11x faster                                                  |
| scimark_sor                | 130 ms                                                 | 119 ms: 1.09x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.35 sec: 1.09x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 89.1 ms: 1.09x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.06 us: 1.07x faster                                                  |
| logging_silent             | 109 ns                                                 | 102 ns: 1.07x faster                                                   |
| pylint                     | 319 ms                                                 | 299 ms: 1.06x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 132 ms: 1.05x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.94 us: 1.05x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.12 sec: 1.04x faster                                                 |
| raytrace                   | 299 ms                                                 | 292 ms: 1.02x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 510 ms: 1.01x faster                                                   |
| regex_compile              | 142 ms                                                 | 141 ms: 1.01x faster                                                   |
| async_generators           | 384 ms                                                 | 380 ms: 1.01x faster                                                   |
| chaos                      | 62.8 ms                                                | 62.5 ms: 1.01x faster                                                  |
| scimark_fft                | 342 ms                                                 | 343 ms: 1.01x slower                                                   |
| spectral_norm              | 110 ms                                                 | 111 ms: 1.01x slower                                                   |
| logging_simple             | 6.63 us                                                | 6.70 us: 1.01x slower                                                  |
| generators                 | 32.2 ms                                                | 32.6 ms: 1.01x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.3 ms: 1.02x slower                                                  |
| pyflate                    | 448 ms                                                 | 459 ms: 1.03x slower                                                   |
| pprint_safe_repr           | 743 ms                                                 | 763 ms: 1.03x slower                                                   |
| hexiom                     | 6.17 ms                                                | 6.35 ms: 1.03x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 21.3 ms: 1.03x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.73 sec: 1.03x slower                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.57 sec: 1.03x slower                                                 |
| logging_format             | 7.35 us                                                | 7.65 us: 1.04x slower                                                  |
| regex_dna                  | 168 ms                                                 | 175 ms: 1.04x slower                                                   |
| html5lib                   | 63.6 ms                                                | 66.6 ms: 1.05x slower                                                  |
| 2to3                       | 264 ms                                                 | 276 ms: 1.05x slower                                                   |
| sympy_integrate            | 20.5 ms                                                | 21.6 ms: 1.05x slower                                                  |
| sympy_str                  | 292 ms                                                 | 308 ms: 1.05x slower                                                   |
| sympy_sum                  | 166 ms                                                 | 175 ms: 1.06x slower                                                   |
| unpickle_pure_python       | 221 us                                                 | 233 us: 1.06x slower                                                   |
| tomli_loads                | 2.11 sec                                               | 2.24 sec: 1.06x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 11.1 ms: 1.07x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 331 us: 1.07x slower                                                   |
| json                       | 5.02 ms                                                | 5.47 ms: 1.09x slower                                                  |
| sympy_expand               | 468 ms                                                 | 513 ms: 1.10x slower                                                   |
| deltablue                  | 3.45 ms                                                | 3.81 ms: 1.10x slower                                                  |
| nqueens                    | 80.1 ms                                                | 89.8 ms: 1.12x slower                                                  |
| richards                   | 45.9 ms                                                | 51.5 ms: 1.12x slower                                                  |
| thrift                     | 791 us                                                 | 889 us: 1.12x slower                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 77.2 ms: 1.13x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 86.5 ms: 1.13x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 129 ms: 1.13x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 96.7 ms: 1.13x slower                                                  |
| richards_super             | 51.9 ms                                                | 59.2 ms: 1.14x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 57.4 ms: 1.14x slower                                                  |
| django_template            | 34.7 ms                                                | 40.0 ms: 1.15x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 189 us: 1.16x slower                                                   |
| genshi_text                | 22.8 ms                                                | 26.7 ms: 1.17x slower                                                  |
| meteor_contest             | 104 ms                                                 | 121 ms: 1.17x slower                                                   |
| xml_etree_process          | 59.0 ms                                                | 69.5 ms: 1.18x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.23 ms: 1.19x slower                                                  |
| json_loads                 | 26.5 us                                                | 32.2 us: 1.21x slower                                                  |
| fannkuch                   | 372 ms                                                 | 455 ms: 1.22x slower                                                   |
| pidigits                   | 184 ms                                                 | 226 ms: 1.23x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 9.64 ms: 1.35x slower                                                  |
| nbody                      | 89.3 ms                                                | 120 ms: 1.35x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.51 ms: 1.38x slower                                                  |
| mako                       | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                  |
| coverage                   | 71.4 ms                                                | 111 ms: 1.56x slower                                                   |
| bench_thread_pool          | 941 us                                                 | 1.48 ms: 1.57x slower                                                  |
| python_startup             | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                  |
| telco                      | 6.53 ms                                                | 173 ms: 26.51x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.03x slower                                                           |
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251219-3.15.0a3+-e46f28c-NOGIL/bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3+-e46f28c.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.031x slower

# HPT report

- Reliability score: 86.71% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.40x