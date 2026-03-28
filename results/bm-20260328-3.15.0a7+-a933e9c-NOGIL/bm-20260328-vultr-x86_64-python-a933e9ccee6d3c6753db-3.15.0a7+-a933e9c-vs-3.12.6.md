# Results vs. 3.12.6

- fork: python
- ref: a933e9ccee6d3c6753db
- machine: linux-x86_64
- commit hash: a933e9c
- commit date: 2026-03-28
- overall geometric mean: 1.026x slower
- HPT reliability: 73.04%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.44x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-vultr-x86_64-python-a933e9ccee6d3c6753db-3.15.0a7+-a933e9c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 281 ms: 1.07x slower                                                   |
| docutils       | 2.64 sec                                               | 2.66 sec: 1.01x slower                                                 |
| html5lib       | 63.6 ms                                                | 65.5 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-vultr-x86_64-python-a933e9ccee6d3c6753db-3.15.0a7+-a933e9c |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 614 ms: 1.81x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 623 ms: 1.74x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 326 ms: 1.71x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 261 ms: 1.71x faster                                                   |
| async_tree_none            | 464 ms                                                 | 288 ms: 1.61x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 352 ms: 1.58x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 521 ms: 1.39x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 546 ms: 1.31x faster                                                   |
| async_generators           | 384 ms                                                 | 375 ms: 1.03x faster                                                   |
| coroutines                 | 23.9 ms                                                | 24.4 ms: 1.02x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.41x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-vultr-x86_64-python-a933e9ccee6d3c6753db-3.15.0a7+-a933e9c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 74.1 ms: 1.09x faster                                                  |
| pidigits       | 184 ms                                                 | 187 ms: 1.02x slower                                                   |
| nbody          | 89.3 ms                                                | 121 ms: 1.35x slower                                                   |
| Geometric mean | (ref)                                                  | 1.08x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-vultr-x86_64-python-a933e9ccee6d3c6753db-3.15.0a7+-a933e9c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.95 ms: 1.07x faster                                                  |
| regex_v8       | 20.6 ms                                                | 21.5 ms: 1.05x slower                                                  |
| regex_dna      | 168 ms                                                 | 184 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                  | 1.02x slower                                                           |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-vultr-x86_64-python-a933e9ccee6d3c6753db-3.15.0a7+-a933e9c |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.89 sec: 1.11x faster                                                 |
| xml_etree_iterparse  | 96.7 ms                                                | 88.3 ms: 1.10x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 133 ms: 1.05x faster                                                   |
| json_dumps           | 10.4 ms                                                | 11.1 ms: 1.07x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 236 us: 1.07x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 338 us: 1.10x slower                                                   |
| json_loads           | 26.5 us                                                | 29.5 us: 1.11x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 96.1 ms: 1.13x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 68.9 ms: 1.17x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.04x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-vultr-x86_64-python-a933e9ccee6d3c6753db-3.15.0a7+-a933e9c |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.90 ms: 1.38x slower                                                  |
| python_startup         | 9.93 ms                                                | 16.1 ms: 1.63x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.50x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-vultr-x86_64-python-a933e9ccee6d3c6753db-3.15.0a7+-a933e9c |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 53.6 ms: 1.07x slower                                                  |
| genshi_text     | 22.8 ms                                                | 25.7 ms: 1.13x slower                                                  |
| django_template | 34.7 ms                                                | 40.0 ms: 1.15x slower                                                  |
| mako            | 11.0 ms                                                | 16.1 ms: 1.46x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.19x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-vultr-x86_64-python-a933e9ccee6d3c6753db-3.15.0a7+-a933e9c |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.31 sec: 1.85x faster                                                 |
| async_tree_io_tg           | 1.11 sec                                               | 614 ms: 1.81x faster                                                   |
| gc_traversal               | 3.46 ms                                                | 1.96 ms: 1.77x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 623 ms: 1.74x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 326 ms: 1.71x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 261 ms: 1.71x faster                                                   |
| async_tree_none            | 464 ms                                                 | 288 ms: 1.61x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 352 ms: 1.58x faster                                                   |
| bench_mp_pool              | 10.8 ms                                                | 7.00 ms: 1.54x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 521 ms: 1.39x faster                                                   |
| deepcopy                   | 352 us                                                 | 264 us: 1.33x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 546 ms: 1.31x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 31.4 us: 1.28x faster                                                  |
| pathlib                    | 21.5 ms                                                | 17.6 ms: 1.23x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 1.92 us: 1.15x faster                                                  |
| go                         | 139 ms                                                 | 122 ms: 1.14x faster                                                   |
| dulwich_log                | 78.9 ms                                                | 69.3 ms: 1.14x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.89 sec: 1.11x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.31 sec: 1.10x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 88.3 ms: 1.10x faster                                                  |
| float                      | 80.8 ms                                                | 74.1 ms: 1.09x faster                                                  |
| scimark_sor                | 130 ms                                                 | 120 ms: 1.08x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.95 ms: 1.07x faster                                                  |
| comprehensions             | 19.8 us                                                | 18.5 us: 1.07x faster                                                  |
| pylint                     | 319 ms                                                 | 298 ms: 1.07x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.90 us: 1.06x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.11 sec: 1.06x faster                                                 |
| logging_silent             | 109 ns                                                 | 103 ns: 1.05x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 133 ms: 1.05x faster                                                   |
| async_generators           | 384 ms                                                 | 375 ms: 1.03x faster                                                   |
| spectral_norm              | 110 ms                                                 | 108 ms: 1.02x faster                                                   |
| chaos                      | 62.8 ms                                                | 61.8 ms: 1.02x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.66 sec: 1.01x slower                                                 |
| pidigits                   | 184 ms                                                 | 187 ms: 1.02x slower                                                   |
| logging_simple             | 6.63 us                                                | 6.75 us: 1.02x slower                                                  |
| deltablue                  | 3.45 ms                                                | 3.51 ms: 1.02x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.4 ms: 1.02x slower                                                  |
| pyflate                    | 448 ms                                                 | 457 ms: 1.02x slower                                                   |
| json                       | 5.02 ms                                                | 5.15 ms: 1.02x slower                                                  |
| html5lib                   | 63.6 ms                                                | 65.5 ms: 1.03x slower                                                  |
| logging_format             | 7.35 us                                                | 7.63 us: 1.04x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 21.5 ms: 1.05x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 789 ms: 1.06x slower                                                   |
| 2to3                       | 264 ms                                                 | 281 ms: 1.07x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 53.6 ms: 1.07x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 11.1 ms: 1.07x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 236 us: 1.07x slower                                                   |
| hexiom                     | 6.17 ms                                                | 6.61 ms: 1.07x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 22.1 ms: 1.07x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.63 sec: 1.07x slower                                                 |
| sympy_str                  | 292 ms                                                 | 314 ms: 1.08x slower                                                   |
| nqueens                    | 80.1 ms                                                | 86.7 ms: 1.08x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 180 ms: 1.09x slower                                                   |
| regex_dna                  | 168 ms                                                 | 184 ms: 1.10x slower                                                   |
| pickle_pure_python         | 308 us                                                 | 338 us: 1.10x slower                                                   |
| scimark_lu                 | 114 ms                                                 | 127 ms: 1.11x slower                                                   |
| json_loads                 | 26.5 us                                                | 29.5 us: 1.11x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 96.1 ms: 1.13x slower                                                  |
| genshi_text                | 22.8 ms                                                | 25.7 ms: 1.13x slower                                                  |
| sympy_expand               | 468 ms                                                 | 528 ms: 1.13x slower                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 77.9 ms: 1.14x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 87.3 ms: 1.14x slower                                                  |
| richards                   | 45.9 ms                                                | 53.0 ms: 1.15x slower                                                  |
| django_template            | 34.7 ms                                                | 40.0 ms: 1.15x slower                                                  |
| richards_super             | 51.9 ms                                                | 59.9 ms: 1.15x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 68.9 ms: 1.17x slower                                                  |
| thrift                     | 791 us                                                 | 932 us: 1.18x slower                                                   |
| typing_runtime_protocols   | 163 us                                                 | 192 us: 1.18x slower                                                   |
| meteor_contest             | 104 ms                                                 | 123 ms: 1.19x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.32 ms: 1.21x slower                                                  |
| fannkuch                   | 372 ms                                                 | 454 ms: 1.22x slower                                                   |
| nbody                      | 89.3 ms                                                | 121 ms: 1.35x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 9.90 ms: 1.38x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.53 ms: 1.40x slower                                                  |
| mako                       | 11.0 ms                                                | 16.1 ms: 1.46x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.46 ms: 1.55x slower                                                  |
| coverage                   | 71.4 ms                                                | 111 ms: 1.55x slower                                                   |
| python_startup             | 9.93 ms                                                | 16.1 ms: 1.63x slower                                                  |
| telco                      | 6.53 ms                                                | 172 ms: 26.42x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.02x slower                                                           |

Benchmark hidden because not significant (5): generators, asyncio_websockets, regex_compile, raytrace, scimark_fft
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260328-3.15.0a7+-a933e9c-NOGIL/bm-20260328-vultr-x86_64-python-a933e9ccee6d3c6753db-3.15.0a7+-a933e9c.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.026x slower

# HPT report

- Reliability score: 73.04% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.44x