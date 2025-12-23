# Results vs. 3.12.6

- fork: diegorusso
- ref: executor_register
- machine: linux-x86_64
- commit hash: 92c1f91
- commit date: 2025-12-22
- overall geometric mean: 1.118x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251222-vultr-x86_64-diegorusso-executor_register-3.15.0a3+-92c1f91 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 247 ms: 1.06x faster                                                    |
| docutils       | 2.64 sec                                               | 2.69 sec: 1.02x slower                                                  |
| html5lib       | 63.6 ms                                                | 65.6 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                  | 1.00x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251222-vultr-x86_64-diegorusso-executor_register-3.15.0a3+-92c1f91 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 549 ms: 1.97x faster                                                    |
| async_tree_none            | 464 ms                                                 | 241 ms: 1.93x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 584 ms: 1.90x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 240 ms: 1.86x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 301 ms: 1.84x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 304 ms: 1.84x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 483 ms: 1.49x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 483 ms: 1.48x faster                                                    |
| async_generators           | 384 ms                                                 | 368 ms: 1.04x faster                                                    |
| asyncio_websockets         | 517 ms                                                 | 543 ms: 1.05x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.52x faster                                                            |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251222-vultr-x86_64-diegorusso-executor_register-3.15.0a3+-92c1f91 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 59.6 ms: 1.36x faster                                                   |
| nbody          | 89.3 ms                                                | 75.9 ms: 1.18x faster                                                   |
| pidigits       | 184 ms                                                 | 194 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                  | 1.15x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251222-vultr-x86_64-diegorusso-executor_register-3.15.0a3+-92c1f91 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.68 ms: 1.18x faster                                                   |
| regex_compile  | 142 ms                                                 | 122 ms: 1.17x faster                                                    |
| regex_dna      | 168 ms                                                 | 172 ms: 1.03x slower                                                    |
| regex_v8       | 20.6 ms                                                | 23.6 ms: 1.15x slower                                                   |
| Geometric mean | (ref)                                                  | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251222-vultr-x86_64-diegorusso-executor_register-3.15.0a3+-92c1f91 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| unpickle_pure_python | 221 us                                                 | 174 us: 1.27x faster                                                    |
| xml_etree_iterparse  | 96.7 ms                                                | 83.3 ms: 1.16x faster                                                   |
| pickle_pure_python   | 308 us                                                 | 277 us: 1.11x faster                                                    |
| xml_etree_generate   | 85.2 ms                                                | 77.2 ms: 1.10x faster                                                   |
| xml_etree_process    | 59.0 ms                                                | 53.7 ms: 1.10x faster                                                   |
| json_dumps           | 10.4 ms                                                | 9.44 ms: 1.10x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 1.94 sec: 1.09x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                    |
| json_loads           | 26.5 us                                                | 28.0 us: 1.05x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.10x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251222-vultr-x86_64-diegorusso-executor_register-3.15.0a3+-92c1f91 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.33 ms: 1.02x slower                                                   |
| python_startup         | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251222-vultr-x86_64-diegorusso-executor_register-3.15.0a3+-92c1f91 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.5 ms: 1.06x faster                                                   |
| mako            | 11.0 ms                                                | 10.5 ms: 1.04x faster                                                   |
| django_template | 34.7 ms                                                | 35.6 ms: 1.03x slower                                                   |
| genshi_xml      | 50.2 ms                                                | 53.6 ms: 1.07x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.00x faster                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251222-vultr-x86_64-diegorusso-executor_register-3.15.0a3+-92c1f91 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 45.9 ms                                                | 17.8 ms: 2.58x faster                                                   |
| richards_super             | 51.9 ms                                                | 21.6 ms: 2.41x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 549 ms: 1.97x faster                                                    |
| async_tree_none            | 464 ms                                                 | 241 ms: 1.93x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 584 ms: 1.90x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 240 ms: 1.86x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 301 ms: 1.84x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 304 ms: 1.84x faster                                                    |
| mdp                        | 2.42 sec                                               | 1.34 sec: 1.81x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 24.9 us: 1.62x faster                                                   |
| go                         | 139 ms                                                 | 91.7 ms: 1.52x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 483 ms: 1.49x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 483 ms: 1.48x faster                                                    |
| deepcopy                   | 352 us                                                 | 240 us: 1.46x faster                                                    |
| float                      | 80.8 ms                                                | 59.6 ms: 1.36x faster                                                   |
| logging_silent             | 109 ns                                                 | 82.1 ns: 1.33x faster                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 52.2 ms: 1.31x faster                                                   |
| scimark_fft                | 342 ms                                                 | 261 ms: 1.31x faster                                                    |
| deltablue                  | 3.45 ms                                                | 2.64 ms: 1.30x faster                                                   |
| unpickle_pure_python       | 221 us                                                 | 174 us: 1.27x faster                                                    |
| scimark_sor                | 130 ms                                                 | 103 ms: 1.26x faster                                                    |
| comprehensions             | 19.8 us                                                | 15.8 us: 1.26x faster                                                   |
| spectral_norm              | 110 ms                                                 | 87.6 ms: 1.26x faster                                                   |
| pyflate                    | 448 ms                                                 | 363 ms: 1.23x faster                                                    |
| pathlib                    | 21.5 ms                                                | 17.7 ms: 1.22x faster                                                   |
| chaos                      | 62.8 ms                                                | 52.2 ms: 1.20x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.57 us: 1.20x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.00 sec: 1.19x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.68 ms: 1.18x faster                                                   |
| nbody                      | 89.3 ms                                                | 75.9 ms: 1.18x faster                                                   |
| regex_compile              | 142 ms                                                 | 122 ms: 1.17x faster                                                    |
| crypto_pyaes               | 76.6 ms                                                | 65.8 ms: 1.16x faster                                                   |
| pprint_safe_repr           | 743 ms                                                 | 639 ms: 1.16x faster                                                    |
| pprint_pformat             | 1.52 sec                                               | 1.31 sec: 1.16x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 83.3 ms: 1.16x faster                                                   |
| raytrace                   | 299 ms                                                 | 263 ms: 1.14x faster                                                    |
| pickle_pure_python         | 308 us                                                 | 277 us: 1.11x faster                                                    |
| xml_etree_generate         | 85.2 ms                                                | 77.2 ms: 1.10x faster                                                   |
| logging_simple             | 6.63 us                                                | 6.02 us: 1.10x faster                                                   |
| xml_etree_process          | 59.0 ms                                                | 53.7 ms: 1.10x faster                                                   |
| json_dumps                 | 10.4 ms                                                | 9.44 ms: 1.10x faster                                                   |
| generators                 | 32.2 ms                                                | 29.4 ms: 1.10x faster                                                   |
| dulwich_log                | 78.9 ms                                                | 72.2 ms: 1.09x faster                                                   |
| tomli_loads                | 2.11 sec                                               | 1.94 sec: 1.09x faster                                                  |
| logging_format             | 7.35 us                                                | 6.77 us: 1.09x faster                                                   |
| thrift                     | 791 us                                                 | 731 us: 1.08x faster                                                    |
| scimark_lu                 | 114 ms                                                 | 106 ms: 1.08x faster                                                    |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                    |
| pycparser                  | 1.17 sec                                               | 1.09 sec: 1.07x faster                                                  |
| 2to3                       | 264 ms                                                 | 247 ms: 1.06x faster                                                    |
| genshi_text                | 22.8 ms                                                | 21.5 ms: 1.06x faster                                                   |
| fannkuch                   | 372 ms                                                 | 352 ms: 1.06x faster                                                    |
| meteor_contest             | 104 ms                                                 | 98.2 ms: 1.05x faster                                                   |
| async_generators           | 384 ms                                                 | 368 ms: 1.04x faster                                                    |
| mako                       | 11.0 ms                                                | 10.5 ms: 1.04x faster                                                   |
| typing_runtime_protocols   | 163 us                                                 | 157 us: 1.04x faster                                                    |
| pylint                     | 319 ms                                                 | 308 ms: 1.03x faster                                                    |
| hexiom                     | 6.17 ms                                                | 5.97 ms: 1.03x faster                                                   |
| json                       | 5.02 ms                                                | 4.91 ms: 1.02x faster                                                   |
| sympy_integrate            | 20.5 ms                                                | 20.3 ms: 1.01x faster                                                   |
| docutils                   | 2.64 sec                                               | 2.69 sec: 1.02x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.33 ms: 1.02x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.50 ms: 1.03x slower                                                   |
| sympy_sum                  | 166 ms                                                 | 171 ms: 1.03x slower                                                    |
| regex_dna                  | 168 ms                                                 | 172 ms: 1.03x slower                                                    |
| django_template            | 34.7 ms                                                | 35.6 ms: 1.03x slower                                                   |
| html5lib                   | 63.6 ms                                                | 65.6 ms: 1.03x slower                                                   |
| asyncio_websockets         | 517 ms                                                 | 543 ms: 1.05x slower                                                    |
| pidigits                   | 184 ms                                                 | 194 ms: 1.05x slower                                                    |
| json_loads                 | 26.5 us                                                | 28.0 us: 1.05x slower                                                   |
| sympy_str                  | 292 ms                                                 | 308 ms: 1.06x slower                                                    |
| genshi_xml                 | 50.2 ms                                                | 53.6 ms: 1.07x slower                                                   |
| nqueens                    | 80.1 ms                                                | 85.6 ms: 1.07x slower                                                   |
| sympy_expand               | 468 ms                                                 | 511 ms: 1.09x slower                                                    |
| regex_v8                   | 20.6 ms                                                | 23.6 ms: 1.15x slower                                                   |
| coverage                   | 71.4 ms                                                | 83.2 ms: 1.17x slower                                                   |
| gc_traversal               | 3.46 ms                                                | 4.24 ms: 1.23x slower                                                   |
| python_startup             | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                   |
| bench_thread_pool          | 941 us                                                 | 1.32 ms: 1.40x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.92 ms: 1.76x slower                                                   |
| bench_mp_pool              | 10.8 ms                                                | 214 ms: 19.80x slower                                                   |
| telco                      | 6.53 ms                                                | 161 ms: 24.73x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                            |

Benchmark hidden because not significant (2): sqlite_synth, coroutines
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251222-3.15.0a3+-92c1f91-JIT/bm-20251222-vultr-x86_64-diegorusso-executor_register-3.15.0a3+-92c1f91.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.118x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.19x