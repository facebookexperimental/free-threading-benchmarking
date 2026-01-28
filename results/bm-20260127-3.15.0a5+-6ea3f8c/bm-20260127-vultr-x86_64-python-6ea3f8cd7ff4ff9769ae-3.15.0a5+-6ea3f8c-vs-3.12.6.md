# Results vs. 3.12.6

- fork: python
- ref: 6ea3f8cd7ff4ff9769ae
- machine: linux-x86_64
- commit hash: 6ea3f8c
- commit date: 2026-01-27
- overall geometric mean: 1.077x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 248 ms: 1.06x faster                                                   |
| docutils       | 2.64 sec                                               | 2.56 sec: 1.03x faster                                                 |
| html5lib       | 63.6 ms                                                | 59.7 ms: 1.06x faster                                                  |
| Geometric mean | (ref)                                                  | 1.05x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 564 ms: 1.97x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 552 ms: 1.96x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 293 ms: 1.91x faster                                                   |
| async_tree_none            | 464 ms                                                 | 244 ms: 1.90x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 302 ms: 1.84x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 246 ms: 1.81x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 492 ms: 1.47x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 490 ms: 1.46x faster                                                   |
| async_generators           | 384 ms                                                 | 341 ms: 1.13x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.53x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.9 ms: 1.14x faster                                                  |
| nbody          | 89.3 ms                                                | 90.8 ms: 1.02x slower                                                  |
| pidigits       | 184 ms                                                 | 202 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 123 ms: 1.16x faster                                                   |
| regex_effbot   | 3.17 ms                                                | 2.75 ms: 1.15x faster                                                  |
| regex_dna      | 168 ms                                                 | 173 ms: 1.03x slower                                                   |
| regex_v8       | 20.6 ms                                                | 22.4 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.82 sec: 1.16x faster                                                 |
| xml_etree_iterparse  | 96.7 ms                                                | 84.4 ms: 1.15x faster                                                  |
| json_dumps           | 10.4 ms                                                | 9.73 ms: 1.06x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 82.1 ms: 1.04x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 213 us: 1.04x faster                                                   |
| xml_etree_process    | 59.0 ms                                                | 57.9 ms: 1.02x faster                                                  |
| pickle_pure_python   | 308 us                                                 | 309 us: 1.01x slower                                                   |
| json_loads           | 26.5 us                                                | 28.1 us: 1.06x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.05x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.28 ms: 1.02x slower                                                  |
| python_startup         | 9.93 ms                                                | 12.5 ms: 1.25x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.8 ms: 1.04x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 49.9 ms: 1.01x faster                                                  |
| django_template | 34.7 ms                                                | 35.7 ms: 1.03x slower                                                  |
| mako            | 11.0 ms                                                | 11.7 ms: 1.06x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.16 sec: 2.09x faster                                                 |
| async_tree_io_tg           | 1.11 sec                                               | 564 ms: 1.97x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 552 ms: 1.96x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 293 ms: 1.91x faster                                                   |
| async_tree_none            | 464 ms                                                 | 244 ms: 1.90x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 302 ms: 1.84x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 246 ms: 1.81x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 26.5 us: 1.52x faster                                                  |
| deepcopy                   | 352 us                                                 | 238 us: 1.48x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 492 ms: 1.47x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 490 ms: 1.46x faster                                                   |
| go                         | 139 ms                                                 | 105 ms: 1.33x faster                                                   |
| comprehensions             | 19.8 us                                                | 16.1 us: 1.23x faster                                                  |
| pathlib                    | 21.5 ms                                                | 17.5 ms: 1.23x faster                                                  |
| scimark_sor                | 130 ms                                                 | 108 ms: 1.20x faster                                                   |
| raytrace                   | 299 ms                                                 | 250 ms: 1.20x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.63 us: 1.17x faster                                                  |
| generators                 | 32.2 ms                                                | 27.6 ms: 1.17x faster                                                  |
| regex_compile              | 142 ms                                                 | 123 ms: 1.16x faster                                                   |
| tomli_loads                | 2.11 sec                                               | 1.82 sec: 1.16x faster                                                 |
| spectral_norm              | 110 ms                                                 | 95.5 ms: 1.15x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.75 ms: 1.15x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 84.4 ms: 1.15x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 69.0 ms: 1.14x faster                                                  |
| float                      | 80.8 ms                                                | 70.9 ms: 1.14x faster                                                  |
| async_generators           | 384 ms                                                 | 341 ms: 1.13x faster                                                   |
| chaos                      | 62.8 ms                                                | 55.8 ms: 1.13x faster                                                  |
| logging_simple             | 6.63 us                                                | 5.89 us: 1.13x faster                                                  |
| pylint                     | 319 ms                                                 | 283 ms: 1.12x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.22 sec: 1.12x faster                                                 |
| logging_format             | 7.35 us                                                | 6.56 us: 1.12x faster                                                  |
| scimark_fft                | 342 ms                                                 | 306 ms: 1.12x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 69.4 ms: 1.10x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 62.5 ms: 1.09x faster                                                  |
| richards                   | 45.9 ms                                                | 42.0 ms: 1.09x faster                                                  |
| pyflate                    | 448 ms                                                 | 413 ms: 1.09x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.08 sec: 1.08x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 19.0 ms: 1.08x faster                                                  |
| richards_super             | 51.9 ms                                                | 48.4 ms: 1.07x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.76 ms: 1.07x faster                                                  |
| logging_silent             | 109 ns                                                 | 102 ns: 1.07x faster                                                   |
| json_dumps                 | 10.4 ms                                                | 9.73 ms: 1.06x faster                                                  |
| html5lib                   | 63.6 ms                                                | 59.7 ms: 1.06x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.43 sec: 1.06x faster                                                 |
| 2to3                       | 264 ms                                                 | 248 ms: 1.06x faster                                                   |
| pprint_safe_repr           | 743 ms                                                 | 700 ms: 1.06x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| sympy_sum                  | 166 ms                                                 | 157 ms: 1.06x faster                                                   |
| sympy_str                  | 292 ms                                                 | 277 ms: 1.05x faster                                                   |
| typing_runtime_protocols   | 163 us                                                 | 156 us: 1.05x faster                                                   |
| deltablue                  | 3.45 ms                                                | 3.29 ms: 1.05x faster                                                  |
| scimark_lu                 | 114 ms                                                 | 109 ms: 1.05x faster                                                   |
| genshi_text                | 22.8 ms                                                | 21.8 ms: 1.04x faster                                                  |
| thrift                     | 791 us                                                 | 760 us: 1.04x faster                                                   |
| xml_etree_generate         | 85.2 ms                                                | 82.1 ms: 1.04x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 213 us: 1.04x faster                                                   |
| docutils                   | 2.64 sec                                               | 2.56 sec: 1.03x faster                                                 |
| meteor_contest             | 104 ms                                                 | 101 ms: 1.03x faster                                                   |
| xml_etree_process          | 59.0 ms                                                | 57.9 ms: 1.02x faster                                                  |
| nqueens                    | 80.1 ms                                                | 79.3 ms: 1.01x faster                                                  |
| genshi_xml                 | 50.2 ms                                                | 49.9 ms: 1.01x faster                                                  |
| pickle_pure_python         | 308 us                                                 | 309 us: 1.01x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.44 ms: 1.01x slower                                                  |
| nbody                      | 89.3 ms                                                | 90.8 ms: 1.02x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.28 ms: 1.02x slower                                                  |
| sqlite_synth               | 2.20 us                                                | 2.25 us: 1.02x slower                                                  |
| django_template            | 34.7 ms                                                | 35.7 ms: 1.03x slower                                                  |
| fannkuch                   | 372 ms                                                 | 383 ms: 1.03x slower                                                   |
| regex_dna                  | 168 ms                                                 | 173 ms: 1.03x slower                                                   |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                   |
| json_loads                 | 26.5 us                                                | 28.1 us: 1.06x slower                                                  |
| mako                       | 11.0 ms                                                | 11.7 ms: 1.06x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 22.4 ms: 1.09x slower                                                  |
| pidigits                   | 184 ms                                                 | 202 ms: 1.10x slower                                                   |
| coverage                   | 71.4 ms                                                | 81.1 ms: 1.14x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.31 ms: 1.25x slower                                                  |
| python_startup             | 9.93 ms                                                | 12.5 ms: 1.25x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.32 ms: 1.41x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.88 ms: 1.72x slower                                                  |
| telco                      | 6.53 ms                                                | 158 ms: 24.27x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 279 ms: 25.82x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (3): coroutines, sympy_expand, json
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260127-3.15.0a5+-6ea3f8c/bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.077x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.16x